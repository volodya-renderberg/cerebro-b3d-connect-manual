.. _render-tools-page:

Render Tools
===============

Доп функционал для задач c видоим деятельности ``render``.

.. image:: ../../_static/images/render_tools.png


Clear folder
-------------

:guilabel:`Clear folder` - удаляет содержимое из папки ``render_output`` в директории задачи.


Settings
---------

:guilabel:`Settings` - выставляет основные настройки и прописывает пути.

* Выставляет высоту, ширину кадра и fps из параметров проекта.

* Выставляет тайминг по параметрам шота.

* Прописывает пути во всех нодах **file_output** по шаблонам:
    
    * для **OPEN_EXR_MULTILAYER**: 

        * в параметре ``base_path`` : //render_output/ v ``N`` / ``AssetName`` _ v ``N`` _ ``ThisNodeLabel`` _#####

        .. image:: ../../_static/images/exr_multilayer_node_path.png    

    * для остальных типов:

        * в параметре ``base_path`` : //render_output/ v ``N`` /

        * в ``file_slots[0].path`` : ``AssetName`` _ v ``N`` _ ``ThisNodeLabel`` _#####

        .. image:: ../../_static/images/png_node_path.png

    .. note:: где ``N`` - номер будущего коммита.