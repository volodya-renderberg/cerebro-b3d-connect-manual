.. _work-panel-page:

Working Panel
=============

Панель отображаемая когда файл активной задачи находится в работе.

.. image:: ../_static/images/working_panel.png

`Work panel (видео) <https://youtu.be/43lPkwNfywU>`_

.. _work_panel_from_cerebro:

From Cerebro:
--------------

Группа кнопок получения данных с *Cerebro* полностью аналогична :ref:`selected_panel_from_cerebro`

.. _work_panel_download_version:

Download version
~~~~~~~~~~~~~~~~

:guilabel:`Download version` - Загрузка версии активной задачи с *Cerebro* на локальный компьютер пользователя, полностью аналогична :ref:`selected_panel_download_version`

.. _work_panel_update_incoming:

Update incoming
~~~~~~~~~~~~~~~

:guilabel:`Update incoming` - Загрузка с *Cerebro* недостающих входящих компонентов для активной задачи, полностью аналогична :ref:`selected_panel_update_incoming`

.. _work_panel_source_panel:

Sources panel
~~~~~~~~~~~~~

:guilabel:`Sources panel` - Открытие панели с перечнем исходников активной задачи, с возможностью загрузки ``collections`` по выбору из исходников в текущий рабочий файл.

.. _work_panel_fix_scene:

Fix scene:
----------

Панель переходного периода из *Ftrack*

Recover paths
~~~~~~~~~~~~~

Замена путей библиотек после переезда из *Ftrack*.

:guilabel:`Recover paths` - откроет проводник где надо выбрать файл *recover.json* созданный при бекапе проекта.

Save position of linked objects
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

:guilabel:`Save position of linked objects` - Сохраняет в текстовый файл положения линкованных объектов и соответствующие им анимационные экшены.

Set position
~~~~~~~~~~~~

:guilabel:`Set position` - применяет из текстового файла положения линкованных объектов и соответствующие им анимационные экшены, анимационные экшены должны присутствовать в сцене.

.. _work_panel_local:

Local:
------

Группа кнопок взаимодействия с локальными весриями активной задачи.

.. _work_panel_open_version:

Open version
~~~~~~~~~~~~

:guilabel:`Open version` - Открытие локальной версии активной задачи по выбору.

.. attention:: **top** версия рабочего файла будет перезаписана, если не был сделан :ref:`work_panel_commit` данные не сохранятся.

.. _work_panel_open_task_folder:

Open task folder
~~~~~~~~~~~~~~~~

:guilabel:`Open task folder` - Запуск проводника в папке данной задачи.

.. _work_panel_textures:


.. _work_panel_notes:

Notes:
------

Чат по задаче.

`(видео) <https://disk.yandex.ru/i/yRKNPQEyOGHjIw>`_


.. _work_panel_open_last_commit_by_web:

Open by web
~~~~~~~~~~~

:guilabel:`Open by web` - Открывает страницу задачи в вёб браузере.


Textures:
---------

.. _work_panel_collect_textures:

Collect textures
~~~~~~~~~~~~~~~~

:guilabel:`Collect textures` - Сборка текстур с перезаписью путей, в директорию **textures** активной задачи. 

`Collect textures (видео) <https://youtu.be/iTCtTxtwsns>`_

.. note:: Собираются только текстуры находящиеся за пределами :ref:`projects_folder_settings`.

.. _work_panel_edit_textures:

Edit textures
~~~~~~~~~~~~~

:guilabel:`Edit textures` - Открытие графического редактора для редактирования текстур из директории **textures** активной задачи.

`Edit textures (видео) <https://youtu.be/pwS9yW_cA9s>`_


Специфичные для типов задач панели:
-----------------------------------

.. toctree::
   :maxdepth: 1

   work_panel/animation_tools
   work_panel/animatic_tools


.. _work_panel_to_cerebro:

To Cerebro:
------------

.. _work_panel_check:

Check
~~~~~

:guilabel:`Check` - Проверка текущей сцены на соответствие с требованиями для данного типа задачи.

* При обнаружении несоответствий, будет запущено информационное окно.

   .. image:: ../_static/images/check_window.png

* :guilabel:`select` - кнопка на против каждого неисправного объекта в информационном окне:

      * Выделит объект, если он выделяем.

      * Создаст запись в ``Info`` панели или терминале, где можно скопировать имя объекта для поиска в ``Outliner`` или ``Image Editor`` если это текстура.

      .. image:: ../_static/images/check_wrong_info_panel.png

.. _work_panel_commit:

Commit
~~~~~~

:guilabel:`Commit` - Фиксация изменений **top** версии, создание новой локальной версии, запуск фоновой загрузки версии на *Cerebro*.

* Если поставить галочку ``To Review`` то статус задачи изменится на *на утверждение* при этом будет выполнена процедура :ref:`work_panel_check`.

.. image:: ../_static/images/commit_to_review.png

.. _work_panel_change_status_to_pending_review:

Change status to "на утверждение"
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

:guilabel:`Change status to "на утверждение"` - Изменение статуса на *на утверждение* без создания версии.


.. _work_panel_playblast:

Playblast:
----------

Создание и отправка версий плейбластов на *Cerebro* с настройками проекта и шота.

.. image:: ../_static/images/working_panel_playblast.png

.. _work_panel_playblast_local_playblast:

Local playblast
~~~~~~~~~~~~~~~

:guilabel:`Local playblast` - Создание плейбласта без отправки версии, но с сохранением по настройкам.

Playblast to version
~~~~~~~~~~~~~~~~~~~~

:guilabel:`Playblast to version` - Создание версии с плейбластом.

.. image:: ../_static/images/playblast_to_version.png

Параметры всплывающего диалога:

* **Status to "на утверждение"** - назначение статуса задачи, по умолчанию ``True``, если снять галочку то статус задачи не изменится.

* **Use latest playblast** - создаст версию с последним сохранённым плейбластом созданным в :ref:`work_panel_playblast_local_playblast`.

* **Description** - обязательное для заполнения поле с кратким комментарием для данной версии.

* **Make commit** - если ``True`` то будет так же сделан и :ref:`work_panel_commit`, по умолчанию ``True``.


Close
-----

:guilabel:`Close` - вернёт на :ref:`tasks-list-page`