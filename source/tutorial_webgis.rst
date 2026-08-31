.. _tutorial-1:

Tutorial: Almacenamiento, gestión y publicación de tus datos espaciales
=======================================================================

.. admonition:: **Disponibilidad**

   **Cloud SaaS** (todas las ediciones), **On premise** (todas las ediciones), **Open Source**

NextGIS Web es un servidor GIS que funciona como centro de datos, te permitirá almacenar, administrar y publicar información espacial de manera flexible y eficiente. En este tutorial paso a paso, aprenderás a convertir tus archivos GIS en mapas web interactivos, así como en servicios OGC, teselas, y también a crear y gestionar datos directamente desde el servidor. ¡Regístrate para obtener una cuenta gratuita en la nube y pruébalo ahora mismo!

Descarga los `datos <https://nextgis.com/tutorials/store_manage_publish_geospatial_data.zip>`_ 
del tutorial (Fuente: Sistema de Información Espacial de `Wroclaw <https://geoportal.wroclaw.pl/>`_) 

Basico

1. `Crear cuenta y SIG Web <tutorial_webgis.rst#paso-16-crear-una-cuenta-gratuita-y-sig-web>`_
2. `Crear grupo de recursos <tutorial_webgis.rst#paso-26-accede-a-tu-sig-web-y-crea-un-grupo-de-recursos>`_
3. `Cargar capa vectorial <tutorial_webgis.rst#paso-36-cargar-y-publicar-una-capa-vectorial>`_
4. `Cargar estilo <tutorial_webgis.rst#paso-46-cargar-estilo>`_
5. `Cargar capa ráster <tutorial_webgis.rst#paso-56-cargar-capa-ráster>`_
6. `Publicar Mapa Web <tutorial_webgis.rst#paso-66-publicar-mapa-web>`_

Advanzado

7. `Agregar capa WMS externa al Mapa Web <tutorial_webgis.rst#Agregar-capa-WMS-externa-al-Mapa-Web>`_
8. `Agregar Mapa Base al Mapa Web <tutorial_webgis.rst#Agregar-Mapa-Base-al-Mapa-Web>`_
9. `Crear capa vectorial dentro del SIG Web <tutorial_webgis.rst#Crear-capa-vectorial-dentro-del-SIG-Web>`_
10. `Editar capa vectorial en el Mapa Web y adjuntar archivos <tutorial_webgis.rst#Editar-capa-vectorial-en-el-Mapa-Web-y-adjuntar-archivos>`_
11. `Publicar servicio OGC API - Features <tutorial_webgis.rst#Publicar-servicio-OGC-API---Features>`_
12. `Qué sigue? <tutorial_webgis.rst#qué-sigue>`_

.. _account:

Paso 1/6: Crear una cuenta gratuita y SIG Web
---------------------------------------------

Ve a `my.nextgis.com <https://my.nextgis.com/>`_, haz clic en el botón **Crear una cuenta** y regístrate con tu dirección de correo electrónico.

Una vez completado el registro, se mostrará la página de tu cuenta. Selecciona el menú **SIG Web** en el panel izquierdo, elige un nombre (en este ejemplo se usa *ngw-inicio.nextgis.com*) y selecciona la ubicación del centro de datos más cercana (en este ejemplo, *Falkenstein*). Luego, haz clic en **Crear un SIG Web**.

.. figure:: _static/tutorial1-paso1-1_es.webp
   :name: tutorial_create_wg_pic
   :align: center
   :width: 20cm

Cuando finalice el proceso de creación, el contenido de la página cambiará, y podrás ver un enlace directo a tu nuevo SIG Web.

.. figure:: _static/tutorial1-paso1-2_es.webp
   :name: tutorial_my_wg_pic
   :align: center
   :width: 20cm

.. _webgis:

Paso 2/6: Accede a tu SIG Web y crea un grupo de recursos
---------------------------------------------------------

Haz clic en el enlace (para este ejemplo *ngw-inicio.nextgis.com*) o escríbelo directamente en la barra de direcciones de tu navegador.

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



Para ver los datos, abre la tabla de características haciendo clic en |button_open_feature_table| **Tabla** en el menú de la derecha

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

Desde la URL de la capa, haz clic en el botón **Crear recurso**. Verás un conjunto diferente de recursos disponibles, ya que una capa vectorial solo puede ser el elemento padre de estilos y formularios. Empleamos los estilos QGIS como la vía principal para definir la apariencia de los datos. Selecciona **Estilo vectorial QGIS**.

.. figure:: _static/tutorial1-paso4-1_es.webp

Desde la pestaña **Estilo QGIS** carga el archivo llamado ``bicycle_roads.qml`` del conjunto de datos del tutorial. Luego, haz clic en el botón **Crear**.

.. figure:: _static/tutorial1-paso4-2_es.webp

Una vez creado el estilo vectorial, serás redirigido a la URL del estilo. Pulsa **Previsualizar** en el menú lateral derecho para comprobar su aspecto final.

En la sección **Acceso externo** encontrarás una URL autogenerada que te permitirá acceder a estos datos con el estilo aplicado como un *Servicio de Mapas Teselados (TMS)*, el cual podrás importar, por ejemplo, directamente en QGIS. Para más información, consulta la sección dedicada a `TMS <https://docs.nextgis.com/docs_ngweb/source/services.html#tms-service>`_.

A continuación, puedes cargar otro tipo de capa o pasar directamente a `Publicar Mapa Web <tutorial_webgis.rst#paso-66-publicar-mapa-web>`_.

.. _raster:

Paso 5/6: Cargar capa ráster
----------------------------

Vuelve al grupo de recursos *Wroclaw* haciendo clic en su nombre en la ruta de navegación.

.. figure:: _static/tutorial1-paso5-1_es.webp
   :name: 
   :align: center
   :width: 20cm


Haz clic en el botón **Crear recurso** y selecciona **Capa ráster**.

.. figure:: _static/tutorial1-paso5-2_es.webp
   :name: 
   :align: center
   :width: 20cm



En la pestaña **Capa ráster**, arrastra y suelta el archivo denominado ``plan.tif`` del conjunto de datos del tutorial, o haz clic en **Seleccione un set de datos** y selecciona el archivo. Luego, haz clic en el botón **Crear**.

.. figure:: _static/tutorial1-paso5-3_es.webp
   :name: 
   :align: center
   :width: 20cm


Creada la capa ráster se te redireccionará a su URL. Aquí puedes ver:

* Su ubicación en el árbol de recursos (*Grupo de recursos principal / Wroclaw*).
* Metadatos básicos (bandas, dimensiones, etc.).

.. figure:: _static/tutorial1-paso5-4_es.webp
   :name: 
   :align: center
   :width: 20cm


En la sección **Acceso externo** encontrarás una URL de acceso **Cloud Optimized GeoTIFF** generada automáticamente para estos datos. Con este enlace puedes conectar estos datos a recursos externos al instante.

Puedes aplicar estilos de QGIS a los recursos ráster creando subrecursos. Sin embargo, para archivos ráster RGB(A), basta con hacer clic en **Crear estilo QGIS predeterminado**, hagámoslo!. Creado el estilo ráster predeterminado serás redirigido a su URL.

.. figure:: _static/tutorial1-paso5-5_es.webp
   :name: 
   :align: center
   :width: 20cm


La URL de acceso a **Teselas ráster (TMS)** para estos datos también se genera de forma automática. Puedes utilizar este enlace para conectar estos datos a recursos externos como teselas ráster con el estilo ya aplicado.

También puedes hacer clic en **Previsualizar** en el menú derecho y explorar el ráster que acabas de cargar.

.. figure:: _static/tutorial1-paso5-6_es.webp
   :name: 
   :align: center
   :width: 20cm

Ahora crearemos un mapa web con los datos que acabamos de cargar.

.. _webmap:

Paso 6/6: Publicar Mapa Web
---------------------------

Ahora que ya tenemos un par de capas con estilos aplicados, estamos listos para publicar nuestro primer mapa web. Para ello vuelve al grupo de recursos *Wroclaw* y crea un nuevo recurso, **Mapa Web**.

.. figure:: _static/tutorial1-paso6-1_es.webp
   :name: 
   :align: center
   :width: 20cm


Hay muchos parámetros que se pueden configurar para un mapa web. En la pestaña **Recurso**, introduce el nombre del mapa, por ejemplo, *Wroclaw*.

.. figure:: _static/tutorial1-paso6-2_es.webp
   :name: 
   :align: center
   :width: 20cm


En la pestaña **Capas** se define el contenido del mapa web. Haz clic en el botón |button_plus_layer| **Capa**. Hay que tener en cuenta que, lo que se añade al mapa es la representación visual de los datos, por lo que **debes seleccionar estilos y no capas**. Las casillas de verificación, junto a los nombres de las capas, no están activas. Puedes hacer clic en una capa y seleccionar su *estilo secundario*, o simplemente hacer clic en el botón **Seleccionar el primer recurso hijo elegible** |button_pick_first| que aparece a la derecha de la capa. Selecciona tanto la capa *Bicisendas* como la capa *plan*.

.. |button_pick_first| image:: _static/button_pick_first.png
   :width: 6mm

.. |button_plus_layer| image:: _static/button_plus_layer.png
   :width: 6mm


.. figure:: _static/tutorial1-paso6-3_es.webp
   :name: 
   :align: center
   :width: 20cm


Después de eso, puedes hacer clic en la capa para editar sus propiedades.

.. figure:: _static/tutorial1-paso6-4_es.webp
   :name: 
   :align: center
   :width: 20cm


Cambia a la pestaña **Configuración**. Busca la fila *Extensión inicial* y haz clic en el botón **From layers**. Luego selecciona la capa *Bicisendas* y haz clic en el botón **Seleccionar elegido**. Ahora el mapa se abrirá mostrando el área de esta capa.

.. figure:: _static/tutorial1-paso6-5_es.webp
   :name: 
   :align: center
   :width: 20cm


Haz clic en el botón **Crear** para finalizar la creación del mapa web.

Los recursos de tipo mapa web tienen un modo especial de visualización. Se puede acceder a él desde el panel derecho de la interfaz del recurso.

.. figure:: _static/tutorial1-paso6-6_es.webp
   :name: 
   :align: center
   :width: 16cm


O, si vuelves al grupo de recursos *Wroclaw*, haz clic en el ícono de mapa |button_open_web_map| que se encuentra a la derecha del nombre del recurso Mapa Web.

.. |button_open_web_map| image:: _static/button_open_web_map.png
   :width: 6mm

Al hacer clic en |button_open_web_map| **Mostrar**, se abrirá un mapa web interactivo. Cada mapa tiene su propia URL de visualización y cuenta con numerosas herramientas para explorar y administrar los datos.

.. figure:: _static/tutorial1-paso6-7_es.webp
   :name: 
   :align: center
   :width: 20cm


Las pestañas de la izquierda permiten administrar capas, identificar, buscar y editar elementos geográficos, así como compartir o imprimir el mapa. Consulta la `documentación <https://docs.nextgis.com/docs_ngweb/source/webmaps_client.html>`_ para obtener más información sobre las herramientas y paneles del mapa web.  

Puedes crear tantos mapas web como necesites, combinando las capas disponibles y sus estilos.

Exploremos qué más puedes hacer con NextGIS Web:

* `Agregar capa WMS externa al Mapa Web <tutorial_webgis.rst#Agregar-capa-WMS-externa-al-Mapa-Web>`_
* `Agregar Mapa Base al Mapa Web <tutorial_webgis.rst#Agregar-Mapa-Base-al-Mapa-Web>`_.
* `Crear capa vectorial dentro del SIG Web <tutorial_webgis.rst#Crear-capa-vectorial-dentro-del-SIG-Web>`_.
* `Editar capa vectorial en el Mapa Web y adjuntar archivos <tutorial_webgis.rst#Editar-capa-vectorial-en-el-Mapa-Web-y-adjuntar-archivos>`_.
* `Publicar servicio OGC API - Features <tutorial_webgis.rst#Publicar-servicio-OGC-API---Features>`_.

.. _wms:

Agregar capa WMS externa al Mapa Web
------------------------------------

Puedes conectar datos externos `WMS <https://docs.nextgis.com/glossary.html#term-WMS>`_, `WFS <https://docs.nextgis.com/glossary.html#term-WFS>`_, `TMS <https://docs.nextgis.com/glossary.html#term-TMS>`_ y `PostGIS <https://docs.nextgis.com/glossary.html#term-PostGIS>`_ a NextGIS Web. Vamos a explorarlo con el ejemplo de la ortofoto de *Wroclaw* que se ofrece como un servicio público WMS.

Vuelve al grupo de recursos de *Wroclaw* y crea un nuevo recurso: **Conexión WMS**.

.. figure:: _static/tutorial1-paso7-1_es.webp
   :name: 
   :align: center
   :width: 20cm


En la pestaña **Recurso**, establece el nombre: *Servicio ortofoto de Wroclaw*

.. figure:: _static/tutorial1-paso7-2_es.webp
   :name: 
   :align: center
   :width: 20cm


En la pestaña **Conexión WMS**, establece la siguiente URL: ``https://gis1.um.wroc.pl/arcgis/services/ogc/OGC_ortofoto_2024/MapServer/WMSServer``

.. figure:: _static/tutorial1-paso7-3_es.webp
   :name: 
   :align: center
   :width: 20cm


Luego, haz clic en el botón **Crear**.

Vuelve al grupo de *Wroclaw* y crea otro recurso: **Capa WMS**.

.. figure:: _static/tutorial1-paso7-4_es.webp
   :name: 
   :align: center
   :width: 20cm


En la pestaña **Recurso**, establece el nombre: *Capa ortofoto de Wroclaw*.

.. figure:: _static/tutorial1-paso7-5_es.webp
   :name: 
   :align: center
   :width: 20cm


En la pestaña **Capa WMS**, haz clic en el campo **Conexión WMS** y selecciona el recurso *Servicio de ortofoto de Wroclaw*, luego haz clic en **Seleccionar elegido**.

.. figure:: _static/tutorial1-paso7-6_es.webp
   :name: 
   :align: center
   :width: 20cm


En la lista desplegable **Formato de imagen**, selecciona *image/png*, en la lista desplegable de **Capas WMS**, selecciona *Ortofotomapa 2024 - GUGiK*, y por último en **Remote SRS** selecciona *WGS84/Lon-lat(EPSG:4326)*

.. figure:: _static/tutorial1-paso7-7_es.webp
   :name: 
   :align: center
   :width: 20cm


Luego, haz clic en el botón **Crear**. La conexión WMS y la capa fueron creadas.

En la sección **Acceso externo**, encontrarás una URL generada automáticamente que se puede usar para conectar los datos como teselas ráster. Ahora mismo puedes agregar estos datos a una aplicación web o a una aplicación de escritorio como QGIS. Tu SIG Web actúa como un *proxy* para el servicio WMS.

.. figure:: _static/tutorial1-paso7-8_es.webp
   :name: 
   :align: center
   :width: 20cm


Para **Agregar la capa WMS al Mapa Web**, vuelve al grupo de recursos de *Wroclaw* y haz clic en el ícono |button_edit| del lápiz de editar junto al Mapa Web.

.. |button_edit| image:: _static/button_edit.png
   :width: 6mm

.. figure:: _static/tutorial1-paso7-9_es.webp
   :name: 
   :align: center
   :width: 20cm


En la pestaña **Capas**, haz clic en el botón |button_plus_layer| **Layer**, selecciona *Capa ortofoto de Wroclaw* y haz clic en el botón **Seleccionar elegido**. La capa WMS ahora se agrega al Mapa Web.

.. figure:: _static/tutorial1-paso7-10_es.webp
   :name: 
   :align: center
   :width: 20cm


Guarda el mapa y ábrelo en modo de visualización. Verás que un ortofotomapa detallado de una fuente externa ahora sirve como base para los datos cargados anteriormente.

.. figure:: _static/tutorial1-paso7-11_es.webp
   :name: 
   :align: center
   :width: 20cm


.. _basemap:

Agregar Mapa Base al Mapa Web
-----------------------------

Los Mapas Web, por defecto, usan el mapa base estándar de *OpenStreetMap (OSM)*. También puedes conectar otros mapas base y usarlos con tus Mapas Web.

Vuelve al grupo de recursos de *Wroclaw* y crea un nuevo recurso: **Mapa base**.

.. figure:: _static/tutorial1-paso8-1_es.webp
   :name: 
   :align: center
   :width: 20cm


Aquí puedes usar nuestra colección pública y colaborativa de geoservicios, `qms.nextgis.com <https://qms.nextgis.com/>`_. Comienza a escribir el nombre del mapa base en el campo **Elegir de QMS** y selecciona el que necesites de los resultados de la búsqueda.

.. figure:: _static/tutorial1-paso8-2_es.webp
   :name: 
   :align: center
   :width: 20cm

Todos los demás campos se completarán automáticamente, y también habrá una vista previa disponible para explorar el mapa base seleccionado.

Una forma alternativa de crear un mapa base es introducir manualmente la URL de una **Tesela XYZ**.

Usa el control deslizante en la esquina superior derecha para comparar este mapa base con el predeterminado de *OSM*.

.. figure:: _static/tutorial1-paso8-3_es.webp
   :name: 
   :align: center
   :width: 20cm



En la pestaña **Recurso**, establece el nombre del mapa base.


.. figure:: _static/tutorial1-paso8-4_es.webp
   :name: 
   :align: center
   :width: 20cm

Haz clic en el botón **Crear**.

Para agregar el mapa base recién creado al Mapa Web, vuelve al grupo de recursos de *Wroclaw* y edita con |button_edit| el recurso **Mapa Web**.

.. figure:: _static/tutorial1-paso8-5_es.webp
   :name: 
   :align: center
   :width: 20cm

En la pestaña **Mapas base**, haz clic en el botón |button_plus_layer| **Agregar** y selecciona el recurso **Mapa base** creado. Luego, haz clic en **Seleccionar elegido** y guarda el Mapa Web.

.. figure:: _static/tutorial1-paso8-6_es.webp
   :name: 
   :align: center
   :width: 20cm

Abre el Mapa Web en modo de visualización |button_open_web_map|. Ahora puedes usar el nuevo mapa base.

.. figure:: _static/tutorial1-paso8-7_es.webp
   :name: 
   :align: center
   :width: 20cm

.. _empty_layer:

Crear capa vectorial dentro del SIG Web
---------------------------------------

No solo es posible cargar datos desde archivos, sino que también puedes crear conjuntos de datos directamente dentro del SIG Web.

Vuelve al grupo de recursos *Wroclaw* y crea un nuevo recurso **Capa vectorial**.

.. figure:: _static/tutorial1-paso9-1_es.webp
   :name: 
   :align: center
   :width: 20cm

A continuación, en la pestaña **Capa vectorial**, selecciona la opción **Crear capa vacía**, y luego selecciona el tipo de geometría **Punto**.

.. figure:: _static/tutorial1-paso9-2_es.webp
   :name: 
   :align: center
   :width: 20cm


En la pestaña **Recurso**, asigna un nombre a la nueva capa, por ejemplo, *Aparcabicis*, y haz clic en el botón **Crear**.

.. figure:: _static/tutorial1-paso9-3_es.webp
   :name: 
   :align: center
   :width: 20cm


Una vez que la capa vectorial es creada, serás redirigido a su URL. Ahora podrás añadirle atributos, para ello haz clic en el botón |button_edit| **Actualizar** en el menú de la derecha.

.. figure:: _static/tutorial1-paso9-4_es.webp
   :name: 
   :align: center
   :width: 20cm


Aquí, en la pestaña **Campos**, haz clic en el botón |button_plus_layer| **Agregar**.

Configura las propiedades del nuevo campo en el panel lateral:

* Nombre para mostrar: ``Número de plazas de aparcamiento``, 
* Nombre clave: ``numero_plazas_aparcamiento``, 
* Tipo: INTEGER. 



.. figure:: _static/tutorial1-paso9-5_es.webp
   :name: 
   :align: center
   :width: 16cm

Luego, haz clic en el botón **Guardar**.

Ahora es momento de crear un *estilo* para la nueva capa. En la página del recurso de la capa vectorial, haz clic en **Crear recurso** y selecciona **Estilo vectorial QGIS**.

En la pestaña **Estilo QGIS**, selecciona **Estilo definido por el usuario**. Aquí tienes disponible un constructor de estilos simple, (Recomendamos usar QGIS para crear estilos, pero para tareas rápidas, este constructor integrado puede ser útil), configura un círculo azul de tamaño 12 y un borde blanco de ancho 1. Luego, haz clic en el botón **Crear**.

.. figure:: _static/tutorial1-paso9-6_es.webp
   :name: 
   :align: center
   :width: 20cm


Se ha creado una nueva capa vectorial dentro del SIG Web.

Ahora puedes añadirla a los Mapas Web y publicarla a través de `Servicios OGC <https://docs.nextgis.com/docs_howto/source/tutorial_webgis.html#publish-ogc-api-features-service>`_

Aunque primero, añadiremos algunas entidades a la capa, recién creada, usando la interfaz web.

.. _edit:

Editar capa vectorial en el Mapa Web y adjuntar archivos
--------------------------------------------------------

Vuelve al grupo de recursos *Wroclaw* y entra en el modo |button_edit| **Actualizar** del Mapa Web.

.. figure:: _static/tutorial1-paso10-1_es.webp
   :name: 
   :align: center
   :width: 20cm


Primero, ve a la pestaña **Capas**, haz clic en el botón |button_plus_layer| **Layer** y agrega la capa *Aparcabicis* haciendo clic en |button_pick_first| **Seleccionar el primer elegible** en el lado derecho de la capa. Luego, haz clic en **Seleccionar elegido** y arrastra la capa *Aparcabicis* a la parte superior de la lista de capas.

.. figure:: _static/tutorial1-paso10-2_es.webp
   :name: 
   :align: center
   :width: 20cm

A continuación, ve a la pestaña **Configuración**, busca el menú desplegable **Edición de capas** y selecciona **Habilitar**. Guarda los cambios.

.. figure:: _static/tutorial1-paso10-3_es.webp
   :name: 
   :align: center
   :width: 20cm

Acabas de añadir la nueva capa vectorial al mapa y has activado la edición de capas. Ahora ve al modo |button_open_web_map| **Mostrar** del mapa.

.. figure:: _static/tutorial1-paso10-4_es.webp
   :name: 
   :align: center
   :width: 16cm

Haz zoom a un lugar en el mapa donde te gustaría colocar un nuevo estacionamiento de bicicletas. Luego, abre el menú contextual de la capa haciendo clic en los tres puntos a la derecha de su nombre y selecciona |button_edit| **Editar**.

.. figure:: _static/tutorial1-paso10-5_es.webp
   :name: 
   :align: center
   :width: 16cm

Han aparecido nuevas herramientas en el mapa. 

Selecciona la herramienta |button_maptool_plus| y haz clic en el lugar deseado.

.. |button_maptool_plus| image:: _static/button_maptool_plus_nw.png
   :width: 6mm
   :alt: +

.. figure:: _static/tutorial1-paso10-6_es.webp
   :name: 
   :align: center
   :width: 20cm

A continuación, aparecerá una ventana emergente donde puedes establecer los valores de los atributos, por ejemplo, **10** para el número de plazas de estacionamiento.

.. figure:: _static/tutorial1-paso10-7_es.webp
   :name: 
   :align: center
   :width: 20cm

Hay dos pestañas adicionales disponibles. En la pestaña **Descripción** puedes ingresar cualquier texto enriquecido con imágenes para describir la entidad. En la pestaña **Adjuntos**, puedes adjuntar un número ilimitado de fotos o cualquier tipo de archivo a la entidad. Cambia a la pestaña **Adjuntos**, haz clic en el botón |button_upload| **Subir** y selecciona los archivos ``Bicycle_parking.jpg`` y ``WRM_Regulations.pdf`` del conjunto de datos del tutorial.

.. |button_upload| image:: _static/button_upload.png
   :width: 6mm

.. figure:: _static/tutorial1-paso10-8_es.webp
   :name: 
   :align: center
   :width: 20cm

Haz clic en el botón **Ok** para guardar la entidad. 

Luego, vuelve al menú contextual de la capa **Aparcabicis** y haz clic en **Dejar de editar**.

.. figure:: _static/tutorial1-paso10-9_es.webp
   :name: 
   :align: center
   :width: 14cm

Confirma las ediciones haciendo clic en el botón **Guardar** en el cuadro de diálogo emergente.

.. figure:: _static/tutorial1-paso10-10_es.webp
   :name: 
   :align: center
   :width: 12cm

Se ha creado una nueva entidad.

Haz clic en el símbolo del punto en el mapa. Aparecerá un panel de identificación donde podrás explorar los atributos y archivos adjuntos de la entidad.

.. figure:: _static/tutorial1-paso10-11_es.webp
   :name: 
   :align: center
   :width: 20cm

Haz clic en las fotos y panoramas adjuntos para verlos.

Ahora que tenemos datos en esta capa, publiquémosla a través de OGC API Features.

.. _ogc_api:

Publicar servicio OGC API - Features
------------------------------------

Publicaremos una capa con el protocolo *OGC API — Features*, para que pueda ser editada en software externo. Vuelve al grupo de recursos **Wroclaw** y crea un nuevo recurso, **Servicio OGC API Features**.

.. figure:: _static/tutorial1-paso11-1_es.webp
   :name: 
   :align: center
   :width: 20cm

La creación del servicio es un proceso sencillo. Todo lo que necesitas es seleccionar una capa.

En la pestaña del **Servicio OGC API Features**, haz clic en el botón |button_plus_layer| **Agregar** y selecciona la capa **Aparcabicis**, luego haz clic en el botón **Seleccionar elegido**.

.. figure:: _static/tutorial1-paso11-2_es.webp
   :name: 
   :align: center
   :width: 20cm

Por defecto, el recurso se llamará simplemente *Servicio OGC API Features*, para establecer un nombre personalizado, ve a la pestaña **Recurso** e ingresa *Aparcabicis (servicio de entidades)*. Luego haz clic en el botón **Crear**.

.. note:: El nombre *Aparcabicis* ya está siendo usado para el recurso de capa vectorial, por lo que debes agregar *servicio de entidades* al final.

.. figure:: _static/tutorial1-paso11-3_es.webp
   :name: 
   :align: center
   :width: 20cm

Al crear el servicio serás redirigido a su URL. En la sección **Acceso externo** puedes ver el *enlace* del servicio publicado. Copia la URL para usarla en aplicaciones externas.

.. figure:: _static/tutorial1-paso11-4_es.webp
   :name: 
   :align: center
   :width: 20cm

.. _next:

Qué sigue?
----------

Felicitaciones! completaste el tutorial y aprendiste los conceptos básicos de la gestión de datos geoespaciales en NextGIS Web.

Todavía hay muchas cosas por explorar, puedes aprender a:

* Administrar usuarios y permisos, para configurar combinaciones de acceso únicas para cada capa, servicio y mapa;
* Administrar sistemas de referencia de coordenadas;
* Administrar datos directamente desde QGIS, incluyendo la publicación de proyectos, la gestión de estilos y la edición colaborativa;
* y mucho más.

Prueba otros tutoriales o profundiza en la documentación para aprender más.
