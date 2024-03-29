.. _faq-page:

FAQ
====

.. _all_shots_by_100_frames:

Все шоты по 100 кадров
-----------------------

Это означает, что у шотов не прописаны оба или один из двух тегов ``fstart``, ``fend``

.. image:: ./../_static/images/faq_fstart_fend_tags.png

Возможно эти теги не назначены на проект, тогда сначала их надо добавить в проект и потом сделать :ref:`animatic_tools_re_create_selected_animatic` в задаче аниматика.

.. _no_projects_list_after_login:

Не загружается список проектов после авторизации в плагине
------------------------------------------------------------

Скорее всего в этот момент одновременно с блендером запущен деск-топ приложение серебры.

К сожалению при обычной авторизации это приложение конфликтует с плагином по запросам на сервер, есть два варианта решения:

* надо или выполнить :ref:`auth_from_password_from_desktop_cerebro`

* или просто закрыть деск-топ приложение серебры и перезапустить блендер.


.. _no_rules_of_user:

Есть список проектов, но нет списка задач или пустая соурс панель в задаче, но связи точно должны быть
--------------------------------------------------------------------------------------------------------

Возможно данный пользователь не добавлен в проект на уровне прав. Надо обратится к менеджерам.


.. _no_opened_shot:

Не открывается анимационный шот, блендер виснет или падает при открытии
------------------------------------------------------------------------

При постоянно изменяющемся контенте, оверайд объекты сцены часто ломаются и это один из симптомов таких поломок.

Иногда причиной может быть отсутствующий или устаревший контент данного шота на данном компьютере. 

Поэтому вначале надо убедится, в свежести контена, для этого сделать:

* :ref:`selected_panel_update_incoming` (долго, но однозначно) 

* или через :ref:`work_panel_source_panel` (для всего кроме локаций, если сомневаетесь в свежести контента локации - то только упдейт).

Если обновление контента не помогает то :ref:`build-scene-page` - делает свежую сборку сцены, при которой будет использована вся анимация из поломанной сцены.

* Вместо **Open version** или **Open from incoming**, в зависимости от того что вы делали, надо выполнить **Build from version** или **Build from incoming** соответственно


.. _geometry_in_zero_of_world:

Геометрия прсонажей или пропсов после открытия шота находится в центре комнаты, хотя риги на своих местах
----------------------------------------------------------------------------------------------------------

Это ещё один из симптомов когда ломается оверрайд объекты рецепт в предыдущем пункте :ref:`no_opened_shot`


.. _no_exists_object_in_shot:

Не отображается какой-либо объект или локация в шоте
-----------------------------------------------------

Если объект находится в аутлайнере, но его нет в сцене, то данный ассет скорее всего просто отсутствует на локальной компьютере.

Лечение:

* если это пропс из локации то надо сделать :ref:`selected_panel_update_incoming`

* если это объект не из локации - то загрузить на комп через :ref:`work_panel_source_panel`

.. note:: все эти загрузки загружают ассеты только на данный компьютер, но ничего не меняют в самой сцене, поэтому после загрузок сцену надо переоткрыть.


Если этих объектов нет даже в аутлайнере, то это недостаток сборки шота, надо обращаться к менеджеру.


.. _no_loaded_objects_in_build:

При билде не загружаются некоторые объекты в сцену
---------------------------------------------------

Для начала надо убедится что данные объекты присутствуют в :ref:`work_panel_source_panel` и они в последних версиях и при случае сделать загрузку.

Если отсутсвует локация или что-то из её контента то надо сделать :ref:`selected_panel_update_incoming`.

.. note:: все эти загрузки загружают ассеты только на данный компьютер, но ничего не меняют в самой сцене, поэтому после загрузок сцену надо переоткрыть.

Если загрузка конетнта не помогла значит дело скорее всего в самих ассетах и надо обратится к менеджеру или в тех поддержку студии.


.. _no_making_animations_in_build:

Билд не восстанавливает всю анимацию или положение объектов
------------------------------------------------------------

Означает что при анимации нарушено одно или несколько их этих правил: :ref:`animation_tech_rules`, 

если самостоятельно восстановить анимацию не удалось - то в тех поддержку студии.


.. _no_exists_object_in_source_panel:

Объект отсутствует в соурс панели
---------------------------------

надо обратится к менеджеру, чтобы установили необходимые связи.


.. _no_can_activate_pose_mode_of_character:

Не получается активировать режим POSE рига
-----------------------------------------------

Это один из полуполоманных состояний оверрайд объектов, как правило иконка рига в этом случае более тусклая, лечение:

Правый клик в аутлайнере по самому объекту рига(арматуре) и выбираем в контекстном меню **Library Override / Make / Selected**

Возможно надо будет сделать эту же процедуру и для коллекции.

.. _link_action:

Не сохраняются ключи на персонаже.
-----------------------------------

Значит на риге присутствует линкованный экшн из локации. Возникает это при позицонировании :ref:`location_position_propses` (п.2)

Лечение - сделать экшн локальным. Клик по "цепочке" в экшен эдиторе.

.. image:: ./../_static/images/unlock_anim_action.png


.. _connection_error:

Ошибка ``Exception: Connection error:`` 
-----------------------------------------

.. note:: Не получается сделать коммит или любую другую операцию, связанную с доступом на сервер. Тип ошибки указан в последней строке сообщения.

.. image:: ./../_static/images/connection_error_message.png


Есть два способа решения:

* надо или выполнить :ref:`auth_from_password_from_desktop_cerebro`

* или просто закрыть деск-топ приложение серебры и перезапустить блендер.