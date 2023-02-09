.. _copy-location-page:

Создание копии ассета Локации
===============================

`Видео <https://disk.yandex.ru/i/m36XgFy9SX3wfw>`_

Команды в терминале для этой задачи
-----------------------------------

Получение ``ID`` текущего ассета
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block::

    import os; os.environ["CEREBRO_B3D_CURRENT_ASSET_ID"]

Запуск панели копирования входящих связей
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block::

   bpy.ops.cerebro.copy_incoming_links("INVOKE_DEFAULT")


Переименовывание ``root`` колекции локации
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block::

    import os; bpy.context.collection.name=f"{os.environ['CEREBRO_B3D_CURRENT_ASSET_NAME']}_rig"

