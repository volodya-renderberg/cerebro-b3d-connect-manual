.. _common-page:

Общее
========

.. _common_all_videos:

Все видео
----------

* `Самое начало (видео) <https://disk.yandex.ru/i/lZMF2WP23D8M-w>`_
* `Взятие задачи в работу от нуля (видео) <https://disk.yandex.ru/i/zuYEATMGdzNsrw>`_
* `Взять задачу из входящей (видео) <https://disk.yandex.ru/i/X6x8qTIpGkBitg>`_
* `Взять в работу из глобальной версии (видео) <https://disk.yandex.ru/i/JYaW1WCQeMDc6g>`_
* `Открыть локальную версию (видео) <https://disk.yandex.ru/i/9oVC42fhqFfmiw>`_
* `Открыть топ версию (видео) <https://disk.yandex.ru/i/1ajRtiMWME_8Kw>`_
* `Создание версии рабочего файла (видео) <https://disk.yandex.ru/i/395pcfgLT97vCg>`_

.. _common_start:

Самое начало работы
--------------------

`Видео <https://disk.yandex.ru/i/lZMF2WP23D8M-w>`_

* устанавливать от серебры ничего не нужно.

* требуется только установить студийный плагин :ref:`install-page`.

* определить место на диске где будут хранится файлы :ref:`projects_folder_settings`.

* авторизация в плагине по нику и паролю из серебры :ref:`authentication-page`.

.. _common_responsibility_area:

Зона отвественности плагина
----------------------------

* Формирование локальной файловой структуры.

   .. note:: всё деалет плагин сам

* Версионный контроль

   .. note:: не требуются наколеночные сохранения файлов с выдумыванием номеров и имён

   функции:

   * :ref:`work_panel_commit`
   * :ref:`work_panel_download_version`
   * :ref:`work_panel_open_version`

* Взаимодействие с сереброй

   .. note:: скачать-закачать версию, открыть чат по задаче в серебре, или собрать на локальный комп всё необходимое для текущей задачи по входящим связям

   функции:

   * :ref:`work_panel_commit`
   * :ref:`work_panel_download_version`
   * :ref:`work_panel_open_last_commit_by_web`
   * :ref:`selected_panel_update_incoming`
   * :ref:`work_panel_source_panel`

* Обеспечение взаимосвязей между задач

   .. note:: можно брать в работу файлы или компоненты файлов из входящих задач, то-есть если что-то надо забрать из одной задачи в другую - ничего искать и качать не нужно, достаточно просто попросить менеджера установить связь.

   функции:

   * :ref:`work_panel_source_panel`
   * :ref:`selected_panel_open_from_incoming`

* Доп функционал по видам деятельности

   .. note:: всякие фишечки

   * :ref:`work_panel_tech_functions`

.. _common_pull_task:

Взятие задачи в работу
------------------------

Общее для всех способов взятия в работу это найти и выбрать задачу в :ref:`tasks-list-page`, после чего кликнуть по кнопке :guilabel:`select` напртив имени задачи (:ref:`tasks_list_select_button`).

.. _common_pull_task_from_null:

От нуля
~~~~~~~~

`Видео <https://disk.yandex.ru/i/zuYEATMGdzNsrw>`_

.. note:: нет ни глобальных, ни локальных версий, нет ни каких данных из входящих задач, только тз.

* взять в работу текущую сцену :ref:`selected_panel_current_scene_to_work`.


.. _common_pull_task_from_incoming:

Открыть из входящей
~~~~~~~~~~~~~~~~~~~~~

`Видео <https://disk.yandex.ru/i/X6x8qTIpGkBitg>`_

.. note:: нет версий данной задачи, но существуют версии входящей задачи этого же ассета, например есть модель, а мы в задаче рига.

* взять в работу сцену из входящей задачи :ref:`selected_panel_open_from_incoming`

.. _common_pull_task_from_global:

Взять из глобальной версии
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

`Видео <https://disk.yandex.ru/i/JYaW1WCQeMDc6g>`_

.. note:: отсутствие локальных версий, или надобность взять какую-либо глобальную версию.

* скачать глобальную версию в локальную :ref:`selected_panel_download_version`

* открыть скаченную версию :ref:`selected_panel_open_version`

.. _common_pull_task_from_local:

Открыть локальную версию
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

`Видео <https://disk.yandex.ru/i/9oVC42fhqFfmiw>`_

.. note:: наличие локальной версии

.. attention:: при открытии локальной версии топ версия будет ею перетёрта.

* открыть локальную версию :ref:`selected_panel_open_version`

.. _common_pull_task_from_top:

Открыть топ версию
~~~~~~~~~~~~~~~~~~~~

`Видео <https://disk.yandex.ru/i/1ajRtiMWME_8Kw>`_

.. note:: наличие топ версии.

* открыть локальную версию :ref:`selected_panel_open`


.. _common_push_task:

Создание версии рабочего файла
-------------------------------

`Видео <https://disk.yandex.ru/i/395pcfgLT97vCg>`_

Сохранение рабочего файла ``Ctrl+S`` просто сохраняет топ версию, но этот файл легко может быть перетёрт при открытии локальной версии :ref:`selected_panel_open_version`.

Для надёжной фиксации изменений, или отправки отчёта используется :ref:`work_panel_commit`

.. note::

   * Сохранение промежуточной версии для себя.

   * Отправка отчёта.

   * Учёт потраченного времени.