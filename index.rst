.. Semi-Automatic Classification Plugin documentation master file

Semi-Automatic Classification Plugin's User Manual
================================================================

.. |br| raw:: html

  <br />

Written by Luca Congedo, the **Semi-Automatic Classification Plugin** is a free plugin for `QGIS <http://www.qgis.org>`_ (open source) that allows for the **semi-automatic supervised classification** of remote sensing images, providing tools to expedite the creation of ROIs (training areas) through region growing or multiple ROI creation. The spectral signatures of training areas can be automatically calculated and displayed in a spectral signature plot. It is possible to import spectral signatures from external sources. Also, a tool allows for the selection and download of spectral signatures from the `USGS Spectral Library <http://speclab.cr.usgs.gov/spectral-lib.html>`_ . Several tools are available for the pre processing phase (image clipping, Landsat conversion to reflectance), the classification process (Minimum Distance, Maximum Likelihood, Spectral Angle Mapping algorithms, and classification previews), and the post processing phase (conversion to vector, accuracy assessment, land cover change, classification report).
The first version of the Semi-Automatic Classification Plugin was written by Luca Congedo for the `Adapting to Climate Change in Coastal Dar es Salaam Project <http://www.planning4adaptation.eu/>`_.

For more information and tutorials visit the official site `From GIS to Remote Sensing <http://fromgistors.blogspot.com/>`_.

|br| 

**How to cite:**

*Congedo Luca, Munafo' Michele, Macchi Silvia (2013). "Investigating the Relationship between Land Cover and Vulnerability to Climate Change in Dar es Salaam". Working Paper, Rome: Sapienza University.* Available at:
http://www.planning4adaptation.eu/Docs/papers/08_NWP-DoM_for_LCC_in_Dar_using_Landsat_Imagery.pdf

|br|

**License:**

Except where otherwise noted, content of this work is licensed under a `Creative Commons
Attribution-ShareAlike 4.0 International License <http://creativecommons.org/licenses/by-sa/4.0/>`_.

|br|

``Semi-Automatic Classification Plugin is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, version 3 of the License.
Semi-Automatic Classification Plugin is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.
See the GNU General Public License for more details. You should have received a copy of the GNU General Public License along with Semi-Automatic Classification Plugin. If not, see http://www.gnu.org/licenses/.``

|br|

.. toctree::
	:maxdepth: 3
	:numbered:
  
	Installation.rst
	semi-automatic_OS.rst
	Interface.rst
	remote_sensing.rst
	Tutorials.rst
