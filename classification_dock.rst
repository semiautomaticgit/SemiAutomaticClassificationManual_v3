.. _classification_dock:

*******************
Classification dock
*******************

.. |br| raw:: html

 <br />

.. figure:: _static/classification_dock.jpg
	:align: right
	
	:guilabel:`Classification`
	
The dock ``Classification`` is designed to manage the **spectral signatures**, and **classify** remote sensing image (or ``band set``).

The classification process requires the spectral signatures that define the land cover classes (for instance calculated from the ROIs of a ``Training shapefile`` in the :ref:`roi_dock`). In addition, it is possible to import spectral signatures from other projects or from the :ref:`USGS_spec_library_tab`.

The classification can be performed for the entire image, or for a portion of it, creating a :ref:`classification_preview`. Similarly to the :ref:`ROI_creation`, classification previews are created with a click on any image pixel; preview classifications are temporarily placed inside a layer group named ``Class_temp_group``, and they are deleted when the QGIS session is closed. It is possible to choose between the Macroclass ID or Class ID as reference for the :ref:`classification_alg`.

A :ref:`classification_style` (i.e. a .qml file) can be defined for classifications and previews, allowing for the custom definition of class colors (which overrides the color defined in the :ref:`signature_list`).

A .tif file is created as output classification. Also, the :ref:`classification_output` allows for the automatic conversion of the classification from raster to vector (a shapefile), the calculation of the classification accuracy, and the definition of a mask for the land cover classification (using a polygon shapefile). Other options are defined in the :ref:`classification_process`.
		
.. _signature_list_file:
 
Signature list file
-------------------

* ``Open`` : open a signature list file (a .xml file);
* ``Save`` : save the signature list to file; if no signature list file is already defined, a window will open for the selection of where to save the signature file.

.. _signature_list:
 
Signature list
--------------

The ``Signature list`` displays the collected signatures. Double click on any table item to check/uncheck all the item checkboxes; only the spectral signatures checked in this list are used for the classification, therefore, it is possible to quickly assess the effect of each signature in the classification result.
A single click on any item allows for editing the signature IDs and Infos directly.

* Table fields:
	* ``S`` : checkbox field;
	* ``MC ID`` : Macroclass ID;
	* ``MC Info`` : Macroclass Information;
	* ``C ID`` : Class ID;
	* ``C Info`` : Class Information;
	* ``Color`` : color field; double click to select a color for the class.
* |delete_sign|: delete highlighted spectral signatures;
* |spectral_library|: import a spectral library from ASTER spectral libraries (i.e. files .txt downloaded from http://speclib.jpl.nasa.gov), USGS spectral libraries (i.e. files .asc downloaded from http://speclab.cr.usgs.gov/spectral-lib.html), or generic .csv files;
* |USGS_spectral_library|: open the :ref:`USGS_spec_library_tab`;
* |export_csv| : open a window for the directory selection where signatures are exported as single .csv files;
* |sign_plot|: add highlighted signatures to the :ref:`spectral_signature_plot`;
* ``Export list``: export the signature list to a signature file (i.e. a .xml file);
* ``Import list``: import a .xml file, adding the spectral signatures to the ones in the ``Signature list``.

	**Tip**: the signature list is automatically saved every time the QGIS project is saved, or manually saved by clicking the button ``Save`` in the :ref:`signature_list_file`.
	
.. |delete_sign| image:: _static/semiautomaticclassificationplugin_delete_signature.png
	:width: 20pt
	
.. |spectral_library| image:: _static/semiautomaticclassificationplugin_import_spectral_library.png
	:width: 20pt
	
.. |USGS_spectral_library| image:: _static/semiautomaticclassificationplugin_import_USGS_spectral_library.png
	:width: 20pt
		
.. |export_csv| image:: _static/semiautomaticclassificationplugin_export_sign_to_csv.png
	:width: 20pt
	
.. |sign_plot| image:: _static/semiautomaticclassificationplugin_sign_tool.png
	:width: 20pt
	
.. _classification_alg:

Classification algorithm
------------------------

*  ``Select a classification algorithm`` : available classification algorithms are: Maximum Likelihood; Minimum Distance; Spectral Angle Mapping;
* ``Threshold`` : if threshold is equal to 0, then all image pixels are classified; otherwise: 
	* for Maximum Likelihood, pixels are unclassified if probability is less than threshold  value (max 100);
	* for Minimum Distance, pixels are unclassified if distance is greater than threshold value;
	* for Spectral Angle Mapping, pixels are unclassified if spectral angle distance is greater than threshold value (max 90).
* ``Use Macroclass ID`` : if checked the classification is performed using the Macroclass ID; if unchecked, then the classification is performed using the ID class only.

.. _classification_preview:

Classification preview
----------------------

* [+]: recall the pointer for the creation of a classification preview ;
* ``Size`` : size in pixel unit of a classification preview (i.e. the side lenght of a square, centered at the clicked pixel);
* [ ``Redo`` ]: create a new classification preview centered at the same pixel of the previous one.

.. _classification_style:

Classification style
--------------------

* [ ``Select qml`` ]: select a previously saved .qml file; this configuration is stored in the QGIS project;
* [ ``Reset`` ]: reset classification and preview styles to default (i.e. colors are automatically assigned to classes).

.. _classification_output:

Classification output
---------------------

* ``Apply mask`` : if checked, it allows the users to select a shapefile for the purpose of masking the classification (i.e. image pixels outside this shapefile will be unclassified);
* [ ``Reset`` ]: reset the shapefile mask.
* ``Create vector`` : if checked, a shapefile classification is saved into the same folder and with the same name defined for the classification output;
* ``Classification report`` : if checked, a report about the land cover classification is calculated, providing the pixel count, the percentage and area for each class; the report is saved as a .csv file in the same folder and with the same name defined for the classification output and the suffix ``_report``; in addition, the results are shown in the :ref:`classification_report_tab`;
* [ ``Perform classification`` ]: open a window for the selection of output destination, and perform the image classification that is saved as a .tif file, along with the optional outputs.

Following a brief video of this tool.

.. raw:: html

	<iframe allowfullscreen="" frameborder="0" height="360" src="http://www.youtube.com/embed/GFySyhlVnYw?rel=0" width="640"></iframe>

http://www.youtube.com/watch?v=GFySyhlVnYw
