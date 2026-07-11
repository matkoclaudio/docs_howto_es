.. _tutorial-1:

Tutorial: Almacenamiento, gestión y publicación de tus datos espaciales
=======================================================================

.. admonition:: **Disponibilidad**

   **Cloud SaaS** (todas las ediciones), **On premise** (todas las ediciones), **Open Source**

NextGIS Web es un servidor GIS que funciona como centro de datos, te permitirá almacenar, administrar y publicar información espacial de manera flexible y eficiente. En este tutorial paso a paso, aprenderás a convertir tus archivos GIS en mapas web interactivos, así como en servicios OGC, teselas, y también a crear y gestionar datos directamente desde el servidor. ¡Regístrate para obtener una cuenta gratuita en la nube y pruébalo ahora mismo!

Descarga los `datos <https://nextgis.com/tutorials/store_manage_publish_geospatial_data.zip>`_ 
del tutorial (fuente: Sistema de Información Espacial de `Wroclaw <https://geoportal.wroclaw.pl/>`_) 

Basico

1. `Crear cuenta y SIG Web <tutorial_webgis.rst#paso-16-crear-una-cuenta-gratuita-y-sig-web>`_
2. `Crear grupo de recursos <tutorial_webgis.rst#paso-26-accede-a-tu-sig-web-y-crea-un-grupo-de-recursos>`_
3. `Cargar capa vectorial <tutorial_webgis.rst#paso-36-cargar-y-publicar-una-capa-vectorial>`_
4. `Cargar estilo <tutorial_webgis.rst#paso-46>`_
5. `Cargar capa ráster <tutorial_webgis.rst#paso-56>`_
6. `Publicar Mapa Web <tutorial_webgis.rst#paso-66>`_

Advanzado

7. `Agregar capa WMS externa al Mapa Web <https://docs.nextgis.com/docs_howto/source/tutorial_webgis.html#add-external-wms-layer-to-web-map>`_
8. `Agregar Mapa Base <https://docs.nextgis.com/docs_howto/source/tutorial_webgis.html#add-basemaps-to-web-map>`_
9. `Crear capa vectorial dentro del SIG Web <https://docs.nextgis.com/docs_howto/source/tutorial_webgis.html#create-vector-layer-inside-web-gis>`_
10. `Editar capa vectorial en el Mapa Web y adjuntar archivos <https://docs.nextgis.com/docs_howto/source/tutorial_webgis.html#edit-vector-layer-on-a-web-map-add-file-attachments>`_
11. `Publicar servicio OGC API — Features <https://docs.nextgis.com/docs_howto/source/tutorial_webgis.html#ogc-api>`_
12. `Qué sigue? <https://docs.nextgis.com/docs_howto/source/tutorial_webgis.html#what-next>`_

.. _account:

Paso 1/6: Crear una cuenta gratuita y SIG Web
---------------------------------------------

Ve a `my.nextgis.com <https://my.nextgis.com/>`_, haz clic en el botón **Crear una cuenta** y regístrate con tu dirección de correo electrónico.

Una vez completado el registro, se mostrará la página de tu cuenta. Selecciona el menú **SIG Web** en el panel izquierdo, elige un nombre (en este ejemplo se usa *ngw-inicio.nextgis.com*) y selecciona la ubicación del centro de datos más cercana (en este ejemplo, *Falkenstein*). Luego, haz clic en **Crear un SIG Web**.

.. figure:: _static/tutorial1-paso1-1_es.webp

Cuando finalice el proceso de creación, el contenido de la página cambiará, y podrás ver un enlace directo a tu nuevo SIG Web.

.. figure:: _static/tutorial1-paso1-2_es.webp

.. _webgis:

Paso 2/6: Accede a tu SIG Web y crea un grupo de recursos
---------------------------------------------------------

Haz clic en el enlace de (para este ejemplo *ngw-inicio.nextgis.com*) o escríbelo directamente en la barra de direcciones de tu navegador.

Aparecerá la interfaz principal de tu SIG Web.

.. figure:: _static/tutorial1-paso2-1_es.webp

Es importante destacar que, en NextGIS Web, todo es un recurso: capas, mapas web, carpetas (grupos), conexiones a servicios y bases de datos. Estos recursos se organizan en forma de árbol, al igual que los archivos en tu ordenador.

Vamos a crear nuestro primer recurso: una carpeta o grupo de recursos llamado *Wroclaw*. Para ello, haz clic en el botón azul **Crear recurso**, situado en la parte superior de la página.

.. tip:: Si no visualizas el botón **Crear recurso**, primero debes iniciar sesión. Haz clic en el botón **Conectarse** (ubicado en la esquina superior derecha), a continuación, selecciona **Iniciar sesión con NextGIS ID**.

.. figure:: _static/tutorial1-paso2-2_es.webp

Cuando haces clic en **Crear recurso**, aparece una ventana que muestra todas las opciones de recursos disponibles que puedes crear en el contexto actual. Selecciona **Grupo de recursos**.

.. figure:: _static/tutorial1-paso2-3_es.webp

La ventana de creación de recursos consta de varias pestañas, en este caso solo necesitamos establecer el nombre *Wroclaw* en la pestaña **Recurso**.

.. figure:: _static/tutorial1-paso2-4_es.webp

Clic en **Crear** y te redirigirá a la página del nuevo recurso.

.. figure:: _static/tutorial1-paso2-5_es.webp

La URL en tu navegador es la ruta al recurso, y el número al final de la URL corresponde al ID del recurso.

*Wroclaw* es un elemento hijo dentro de la carpeta *Grupo de recursos principal* donde lo creamos. El recurso padre se muestra arriba del nombre del recurso.

Ahora puedes cargar datos en esta carpeta.

.. _vector:

Paso 3/6: Cargar y publicar una capa vectorial 
----------------------------------------------

Descarga los `datos <https://nextgis.com/tutorials/store_manage_publish_geospatial_data.zip>`_ del tutorial y descomprime el archivo en tu ordenador.

En tu SIG Web, dentro de la carpeta *Wroclaw*, haz clic en **Crear recurso** y selecciona el tipo de recurso **Capa vectorial**.

.. figure:: _static/tutorial1-paso3-1_es.webp

Verás la interfaz para la creación de recursos con varias pestañas. 

.. figure:: _static/tutorial1-paso3-2_es.webp

En la pestaña predeterminada llamada **Capa vectorial**, agrega el archivo llamado ``bicycle_roads.gpkg`` del conjunto de datos del tutorial. Puedes hacerlo mediante *arrastrar y soltar* el archivo, o bien un clic en **Seleccione un set de datos** y luego seleccionar el archivo.

Una vez finalizada la carga, se muestra el tamaño del archivo.

Ahora ve a la pestaña **Recurso** e ingresa el nombre para visualizar la nueva capa, por ejemplo *Bicisendas*. Luego haz clic en el botón **Crear**.

.. figure:: _static/tutorial1-paso3-3_es.webp

Creada la capa vectorial serás redirigido a su URL. Al igual que antes, el número al final de esta URL representa el ID de tu recurso capa.

Esta página contiene la información de la capa:

* Su ubicación en el árbol de recursos (*Grupo de recursos principal / Wroclaw*);
* Metadatos básicos (SRC, tipo de geometría, recuento de objetos geográficos, etc.);
* Listado de **Campos**, también conocido como estructura de atributos.

.. figure:: _static/tutorial1-paso3-4_es.webp

En la sección de **Acceso externo** encontrarás una URL generada automáticamente que permite acceder a la capa como MVT Teselas Vectoriales. Puedes, ahora mismo, conectar estos datos a una aplicación web o agregarlos a QGIS mediante este enlace. Más información sobre `MVT Teselas Vectoriales <https://docs.nextgis.com/docs_ngweb/source/services.html#mvt-vector-tiles>`_.



Para ver los datos, abre la tabla de características haciendo clic en **Tabla** en el menú de la derecha

.. |button_open_feature_table| image:: _static/button_open_feature_table.png
   :width: 6mm


.. figure:: _static/tutorial1-paso3-5_es.webp 

Selecciona cualquier característica y haz clic en **Abrir** para verla.

Se abrirá una ventana, en la que verás todas las propiedades del elemento seleccionado, incluidos los atributos, geometría y una representación cartográfica superpuesta al mapa base predeterminado.

.. figure:: _static/tutorial1-paso3-6_es.webp

La tabla de entidades permite inspeccionar, editar y gestionar las entidades de la capa vectorial como registros de base de datos independientes, sin necesidad de usar mapas u otras aplicaciones. (`Más información <https://docs.nextgis.com/docs_ngweb/source/feature_table.html#ngw-feature-table-blank>`_ )

.. _style:

Paso 4/6: Cargar estilo
-----------------------

Si deseas generar **teselas TMS** o **añadir una capa a un Mapa Web**, es necesario definir su apariencia, es decir, su *estilo*. Puedes hacer clic en **Crear un estilo QGIS por defecto**. Para esta capa disponemos de un archivo especial que determina los colores y la estructura de las líneas en función de los valores de los atributos.

En la página de la capa, haz clic en el botón **Crear recurso**. Verás un conjunto diferente de recursos disponibles, ya que una capa vectorial solo puede ser el elemento padre de estilos y formularios. Empleamos los estilos QGIS como la vía principal para definir la apariencia de los datos. Selecciona **Estilo vectorial de QGIS**.

.. figure:: _static/tutorial_select_qstyle_en.png

Upload the file called ``bicycle_roads.qml`` from the tutorial dataset. Then click the **Create** button.

.. figure:: _static/tutorial_create_qstyle_en.png

The vector style is created and you are redirected to its page. Click **Preview** in the menu on the right to see how the style looks.

In the **External access** section you'll find an auto-generated URL you can use to connect this styled data as a Tiled Map Service, for example, add it to QGIS. `More on TMS <https://docs.nextgis.com/docs_ngweb/source/services.html#tms-service>`_

Now you can upload another type of layer or skip to the `Web Map creation <https://docs.nextgis.com/docs_howto/source/tutorial_webgis.html#step-6-6-publish-web-map>`_.

.. _raster:

Paso 5/6: Cargar capa ráster
----------------------------

Return to the *Wroclaw* resource group by clicking its name at the current path.

.. figure:: _static/tutorial_return_folder_en.png
   :name: 
   :align: center
   :width: 20cm


Click the **Create resource** button and select **Raster layer**.

.. figure:: _static/tutorial_select_raster_layer_en.png
   :name: 
   :align: center
   :width: 20cm


On the **Raster layer** tab drag and drop the file called ``plan.tif``  from the tutorial dataset or click **Select the dataset** and select the file. Then click the **Create** button.

.. figure:: _static/tutorial_raster_upload_en.png
   :name: 
   :align: center
   :width: 20cm


The raster layer is created and you are redirected to its page. Here you can see:

* Its place in the resource tree (Main resource group / Wroclaw);
* Basic metadata (bands, dimensions etc.);



.. figure:: _static/tutorial_raster_result_en.png
   :name: 
   :align: center
   :width: 20cm

In the **External access** section you'll find an auto-generated **Cloud Optimized GeoTIFF** access URL to this data. Right away you can connect this data to external resources using this link.

You can style rasters with QGIS styles by creating child resources. To style RGB(A) rasters, however, you can simply click **Create default QGIS style**. Let’s do it. The default raster style is created and you are redirected to its page. 

.. figure:: _static/tutorial_def_raster_style_result_en.png
   :name: 
   :align: center
   :width: 20cm


**Raster tiles (TMS)** access URL to this data is automatically generated. Right away you can use this link to connect this data as styled raster tiles to external resources.

You could also click **Preview** in the right menu and explore the uploaded raster.

.. figure:: _static/tutorial_raster_preview_en.png
   :name: 
   :align: center
   :width: 20cm

Now let's create a Web Map with the data we've just uploaded.

.. _webmap:

Paso 6/6: Publicar Mapa Web
---------------------------

Now that we have a couple of styled layers we are ready to publish our first Web Map. Return to the *Wroclaw* resource group and create a new resource — **Web Map**.

.. figure:: _static/tutorial_select_webmap_en.png
   :name: 
   :align: center
   :width: 20cm


There are a lot of things that could be set for a Web Map. On the “Resource” tab enter the name for the map, e.g. ``Wroclaw``.

.. figure:: _static/tutorial_webmap_name_en.png
   :name: 
   :align: center
   :width: 20cm


On the **Layers** tab you define the content of this Web Map. Click the |button_plus_layer| **Layer** button. What is added to the map is the visual representation of the data, so you need to select styles, not layers. That is why checkboxes near layer names are not active. You could enter the layer and select its child style, or simply click |button_pick_first| **Select first eligible child resource** on the right side of the layer to select it. Select both *“Bicycle roads”* and *“plan”* layers.

.. |button_pick_first| image:: _static/button_pick_first.png
   :width: 6mm

.. |button_plus_layer| image:: _static/button_plus_layer.png
   :width: 6mm


.. figure:: _static/tutorial_webmap_add_layers_en.png
   :name: 
   :align: center
   :width: 20cm


After that you can click on the layer to edit its properties.

.. figure:: _static/tutorial_webmap_layer_settings_en.png
   :name: 
   :align: center
   :width: 20cm


Switch to the **Settings** tab. Find the “Initial extent” row and click the **From layer** button. Then select *Bicycle roads* layer and click the **Pick selected** button. Now the map will open viewing the area of this layer.

.. figure:: _static/tutorial_webmap_extent_en.png
   :name: 
   :align: center
   :width: 20cm


Click the **Create** button to finalize Web Map creation. 

Web Map resources have a special **Display** mode. It could be accessed from the right panel of the resource interface.

.. figure:: _static/tutorial_webmap_display_en.png
   :name: 
   :align: center
   :width: 16cm


Or, if you return to the *Wroclaw* resource group, click the |button_open_web_map| map icon to the right of the Web Map resource name.

.. |button_open_web_map| image:: _static/button_open_web_map.png
   :width: 6mm

When you click |button_open_web_map| **Display**, an interactive Web Map opens. Each map has its own display URL and a lot of tools to explore and manage the data. 

.. figure:: _static/tutorial_webmap_displayed_en.png
   :name: 
   :align: center
   :width: 20cm

Tabs on the left allow to manage layers, identify, find and edit features, share or print the map. See documentation for more information about Web Map tools and panels: https://docs.nextgis.com/docs_ngweb/source/webmaps_client.html

You can create as many Web Maps as you need, combining available layers and their styles.

Let's explore what else you can do:

* `Add data published on external servers <https://docs.nextgis.com/docs_howto/source/tutorial_webgis.html#add-external-wms-layer-to-web-map>`_;
* `Change basemap <https://docs.nextgis.com/docs_howto/source/tutorial_webgis.html#add-basemaps-to-web-map>`_;
* `Create a vector layer from skratch <https://docs.nextgis.com/docs_howto/source/tutorial_webgis.html#create-vector-layer-inside-web-gis>`_;
* `Edit vector features on a Web Map and attach files <https://docs.nextgis.com/docs_howto/source/tutorial_webgis.html#edit-vector-layer-on-a-web-map-add-file-attachments>`_;
* `Publish OGC API — Features service <https://docs.nextgis.com/docs_howto/source/tutorial_webgis.html#publish-ogc-api-features-service>`_.

.. _wms:

Add external WMS layer to Web Map
---------------------------------

You can connect external :term:`WMS`, :term:`WFS`, :term:`TMS` and :term:`PostGIS` data to NextGIS Web. Let’s explore it with the example of Wroclaw orthophoto serving as a public WMS service.

Return to the *Wroclaw* resource group and create a new resource — **WMS connection**.

.. figure:: _static/tutorial_select_wms_con_en.png
   :name: 
   :align: center
   :width: 20cm


On the resource tab set the name — ``Wroclaw orthophoto service``:

.. figure:: _static/tutorial_wms_con_name_en.png
   :name: 
   :align: center
   :width: 20cm


On the WMS Connection tab set the URL: https://gis1.um.wroc.pl/arcgis/services/ogc/OGC_ortofoto_2024/MapServer/WMSServer

.. figure:: _static/tutorial_wms_con_link_en.png
   :name: 
   :align: center
   :width: 20cm


Then click the **Create** button.

Return to the *Wroclaw* group again and create another resource — **WMS layer**.

.. figure:: _static/tutorial_select_wms_layer_en.png
   :name: 
   :align: center
   :width: 20cm


On the Resource tab set the name — ``Wroclaw orthophoto layer``:

.. figure:: _static/tutorial_wms_layer_name_en.png
   :name: 
   :align: center
   :width: 20cm


On the **WMS Layer** tab click the *“WMS Connection”* field and select **Wroclaw orthophoto service** resource, then click **Pick selected**.

.. figure:: _static/tutorial_wms_layer_pick_con_en.png
   :name: 
   :align: center
   :width: 20cm


In the *“Image format”* dropdown list select **image/png**, and in the *WMS layers* dropdown list select **Ortofotomapa 2024 - GUGiK**.

.. figure:: _static/tutorial_wms_layer_settings_en.png
   :name: 
   :align: center
   :width: 20cm


Then click the **Create** button. WMS connection and layer are created. 

In the **External access** section you'll find an auto-generated URL that can be used to connect the data as **raster tiles**. Right away you can add this data to a Web app or a desktop app such as QGIS. Your Web GIS serves as a proxy for the WMS service.

.. figure:: _static/tutorial_wms_layer_result_en.png
   :name: 
   :align: center
   :width: 20cm


To **add the WMS layer to the Web Map** return to the *Wroclaw* resource group and click the |button_edit| pencil icon next to the Web Map.

.. |button_edit| image:: _static/button_edit.png
   :width: 6mm

.. figure:: _static/tutorial_webmap_edit_select_en.png
   :name: 
   :align: center
   :width: 20cm


On the **Layers** tab click |button_plus_layer| **Layer** button, select *“Wroclaw orthophoto layer”* and click **Pick selected** button. WMS layer is now added to the Web Map.

.. figure:: _static/tutorial_webmap_add_wms_en.png
   :name: 
   :align: center
   :width: 20cm


Save the map and open it in display mode. You’ll see that a detailed orthophotomap from external source is now underlaying the previously uploaded data.

.. figure:: _static/tutorial_webmap_with_wms_en.png
   :name: 
   :align: center
   :width: 20cm


.. _basemap:

Add basemaps to Web Map
---------------------------

By default Web Maps use the standard OpenStreetMap basemap. But you can connect other basemaps and use them with your Web Maps.

Return to the *Wroclaw* resource group and create a new resource — **Basemap**.

.. figure:: _static/tutorial_select_basemap_en.png
   :name: 
   :align: center
   :width: 20cm


Here you can use our public crowdsourced collection of map services, qms.nextgis.com. Start entering the name of the basemap in the **Pick from QMS** field and select what you need from search results.

.. figure:: _static/tutorial_qms_pick_poistron_en.png
   :name: 
   :align: center
   :width: 20cm

All other fields will be filled automatically, also a preview will be available to explore the selected basemap.

An alternative way to create a basemap is to enter the URL for the **XYZ tiles** manually. 

Use the slider in the top right corner to compare this basemap to the default OSM.

.. figure:: _static/tutorial_basemap_preview_en.png
   :name: 
   :align: center
   :width: 20cm



On the **Resource** tab set the name of the basemap.


.. figure:: _static/tutorial_basemap_name_en.png
   :name: 
   :align: center
   :width: 20cm

Click the **Create** button.

To add the newly created basemap to the Web Map return to the *Wroclaw* resource group and |button_edit| edit the Web Map resource.

.. figure:: _static/tutorial_webmap_enter_update_en.png
   :name: 
   :align: center
   :width: 20cm

On the **Basemaps** tab click |button_plus_layer| **Add** button and select the created Basemap resource. Then click **Pick selected** and save the Web Map.

.. figure:: _static/tutorial_webmap_add_basemap_en.png
   :name: 
   :align: center
   :width: 20cm

Open the Web Map in |button_open_web_map| display mode. Now the new basemap is used.

.. figure:: _static/tutorial_webmap_positron_en.png
   :name: 
   :align: center
   :width: 20cm

.. _empty_layer:

Create vector layer inside Web GIS
------------------------------------

It is possible not only to upload data from files, but also to create datasets right inside the Web GIS. 

Return to the *Wroclaw* resource group and create a new resource — **Vector layer**.

.. figure:: _static/tutorial_select_empty_layer_en.png
   :name: 
   :align: center
   :width: 20cm

Then open the dropdown menu on the “Vector layer” tab and select **Create empty layer**.

.. figure:: _static/tutorial_create_empty_layer_en.png
   :name: 
   :align: center
   :width: 20cm

In the changed interface select the **Point** geometry type.

.. figure:: _static/tutorial_empty_layer_geom_en.png
   :name: 
   :align: center
   :width: 20cm


On the **Resource** tab set the name for the new layer, e.g. ``Bicycle parkings``, and click the **Create** button.

.. figure:: _static/tutorial_empty_layer_name_en.png
   :name: 
   :align: center
   :width: 20cm

The vector layer is created and you are redirected to its page. Now you need to add attributes to it. Click |button_edit| **Update** in the right menu.

.. figure:: _static/tutorial_empty_layer_result_en.png
   :name: 
   :align: center
   :width: 20cm


Here, on the **Fields** tab, click the |button_plus_layer| **Add** button.

Set up the properties of the new field in the side panel: 

* Display name: ``Number of parking spaces``, 
* Keyname: ``parking_spaces``, 
* Type: INTEGER. 



.. figure:: _static/tutorial_add_field_en.png
   :name: 
   :align: center
   :width: 16cm

Then click the **Save** button.

Now it’s time to create a style for the new layer. On the vector layer resource page click **Create resource** and select **QGIS vector style**. 

On the **QGIS Style** tab open the dropdown menu and select **User-defined style**.

.. figure:: _static/tutorial_style_custom_select_en.png
   :name: 
   :align: center
   :width: 20cm

Simple style constructor is available here. We recommend using QGIS to create styles, but for quick tasks this built-in constructor could be useful. Set up a blue circle with size 12 and white stroke with 1 width. Then click the **Create** button.

.. figure:: _static/tutorial_style_custom_set_en.png
   :name: 
   :align: center
   :width: 20cm


A new vector layer is created inside Web GIS. 

You can now add it to Web Maps and `publish it via OGC services <https://docs.nextgis.com/docs_howto/source/tutorial_webgis.html#publish-ogc-api-features-service>`_.

But first we'll add some features to the newly created layer using Web interface.

.. _edit:

Edit vector layer on a Web Map, add file attachments
-----------------------------------------------------

Return to the *Wroclaw* resource group and enter the |button_edit| Update mode of the Web Map.

.. figure:: _static/tutorial_webmap_edit_select_en.png
   :name: 
   :align: center
   :width: 20cm


First, go to the **Layers** tab, click the |button_plus_layer| **Layer** button and add *Bicycle parkings* layer by clicking |button_pick_first| **Select first eligible child resource** on the right side of the layer. Then click **Pick selected**, and drag *Bicycle parkings* layers to the top of the layers list.

.. figure:: _static/tutorial_webmap_add_empty_en.png
   :name: 
   :align: center
   :width: 20cm

Next, go to the  **Settings** tab, find the **Layers editing** dropdown menu and select **Enable**. Save the changes.

.. figure:: _static/tutorial_webmap_enable_editing_en.png
   :name: 
   :align: center
   :width: 20cm

You have just added the new vector layer to the map and activated layer editing. Now go to the |button_open_web_map| “Display” mode of the map.

.. figure:: _static/tutorial_webmap_display_en.png
   :name: 
   :align: center
   :width: 16cm

Zoom in to a place on the map where you would like to place a new bicycle parking. Next, open the layer's context menu by clicking the three dots to the right of its name, and select |button_edit| **Edit**.

.. figure:: _static/tutorial_layer_start_edit_en.png
   :name: 
   :align: center
   :width: 16cm

New tools have appeared on the map. 

Select |button_maptool_plus| tool and click on the desired place.

.. |button_maptool_plus| image:: _static/button_maptool_plus.png
   :width: 6mm
   :alt: +

.. figure:: _static/tutorial_add_point_en.png
   :name: 
   :align: center
   :width: 20cm

Pop-up modal window appears, where you can set attribute values, e.g. ``15`` as the number of parking spaces.

.. figure:: _static/tutorial_add_point_attr_en.png
   :name: 
   :align: center
   :width: 20cm

There are also two additional tabs available. On the **Description** tab you could enter any rich-text with images to describe the feature. On the **Attachments** tab you could attach an unlimited number of photos or any sort of files to the feature. Change tab to the “Attachments”, click the |button_upload| **Upload** button and select ``Bicycle_parking.jpg`` and ``WRM_Regulations.pdf`` files from the tutorial dataset.

.. |button_upload| image:: _static/button_upload.png
   :width: 6mm

.. figure:: _static/tutorial_add_attachments_en.png
   :name: 
   :align: center
   :width: 20cm

Click the **OK** button to save the feature. 

Then go to the context menu of *Bicycle parkings* layer again and click **Stop editing**.

.. figure:: _static/tutorial_stop_edit_en.png
   :name: 
   :align: center
   :width: 14cm

Confirm the edits by clicking the **Save** button in the pop-up dialog.

.. figure:: _static/tutorial_edit_confirm_en.png
   :name: 
   :align: center
   :width: 12cm

A new feature is created. 

Click on the point symbol on the map. An identification panel will appear, where you can explore the attributes and attachments of the feature.

.. figure:: _static/tutorial_feature_identify_en.png
   :name: 
   :align: center
   :width: 20cm

Click on the attached photos and panoramas to view them.

Now that we have data in this layer, let's publish it via OGC API Features.

.. _ogc_api:

Publish OGC API — Features service 
--------------------------------------

We'll publish this layer with OGC API — Features protocol so that it can be edited in external software. Go back to the *Wroclaw* resource group and create a new resource, **OGC API Features service**.

.. figure:: _static/tutorial_select_ogcapif_en.png
   :name: 
   :align: center
   :width: 20cm

Service creation is a simple process. All you need is to select a layer. 

On the **OGC API Features service** tab click the |button_plus_layer| **Add** button and select the *Bicycle parkings* layer, then click the **Pick selected** button.

.. figure:: _static/tutorial_ogcapif_select_layer_en.png
   :name: 
   :align: center
   :width: 20cm

By default the resource would be called just "OGC API Features service". To set a custom display name go to the **Resource** tab and enter ``Bicycle parkings (features service)``. Then click the **Create** button.

.. note:: The name "Bicycle parkings" is already used for the vector layer resource, so you need to add "features service" at the end. 

.. figure:: _static/tutorial_ogcapif_name_en.png
   :name: 
   :align: center
   :width: 20cm

The service is created and you are redirected to its page. In the **External access** section you can see the endpoint of the published service. Copy the URL to use it in external applications.

.. figure:: _static/tutorial_ogcapif_result_en.png
   :name: 
   :align: center
   :width: 20cm

.. _next:

What next
-----------

Congratulations! You’ve completed the tutorial and learned the basics of geospatial data management in NextGIS Web.

There are still a lot of things to explore. You can learn to:

* manage users and permissions, allowing to set up unique access combinations for each layer, service and map;
* manage coordinate reference systems;
* manage data directly from QGIS, including project publishing, style management and collaborative editing;
* and many more.

Try other tutorials or dive into documentation to learn more.















