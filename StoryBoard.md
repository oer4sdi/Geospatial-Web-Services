# OER on Geospatial Web Services (work in progress!)       


         	           	
## 1. Overview

In this Open Educational Resource (OER) you will learn which forms of **Geospatial Web Services** exist, how they are structured, how they can be integrated into an open source GIS (QGIS) and connect with a self published GeoServer. 

After you have completed the following Modules, you will know:
* (Module 1) what Geospatial Web Services and OGC standards are
* (Module 1) where to find and identify usefull Geospatial Web Services and learn how they are structured
* (Module 1) how to integrate Web Map Services (WMS) in QGIS and visualize Data from it 
* (Module 1) how to integrate Web Feature Services (WFS) in QGIS and get Data from it
* (Module 3) how to publish your own Data as Web Map Service (WMS) through GeoServer 


The modules are structured as follows

1. Overview
2. Thematic Background 
3. Excercises, Guides and Quiz 
4. Wrap up 

This tutorial is mainly designed for participants who want to spend about ... minutes on improving their skills in integrating Data from Geospatial Web Services. You should have some basic knowledge of GIS Software and it wouldn't be bad if you already have some experience in using the free open source Software Geoserver.

This tutorial was developed at the Institute of Geodesy at Bochum University of Applied Sciences in close cooperation with the University of Münster and the University of Bochum. Main author is Fabian Przybylak under the direction of Prof. Dr. Carsten Keßler.

You are free to use, alter and reproduce the tutorial (H5P content) under the terms of the CC-BY-SA 4.0 license. Any code provided with the tutorial can be used under the terms of the MIT license. Please see the [full license terms](https://github.com/oer4sdi/Geospatial-Web-Services/blob/main/LICENSE.md). 

The OER4SDI project has been recommended by the Digital University NRW and is funded by the Ministry of Culture and Science NRW. 

### 1.1 Metadata 


## 2. Thematic Background and Guides

**classical sructure of the thematic background** 
* Short Introduction with some general context and background (In a few Sentences) 
* Video (Main Information about the content)
* Video Guide (in the context of the given content)
* Text Accordeon (Summarizes the given information)


### 2.1 Short Introduction

**Module 1:** 
Here is explained what Geospatial web Services are (structure, function). Abbreviations like OGC etc. are also explained here. (standards) 

Es wird auf die verschiedenen Angebote eingegangen (WMS, WMTS, WFS, etc.) und wie diese sich voneinander unterscheiden

**Module 3:**
Hier wird darauf eingegangen wie Serversysteme aufgebaut sind und es wird Geoserver als OpenSource Produkt vorgestellt 

## 2.2 Video/Main Informations

**Module 1:** 
* M1V1: Introduction to the topic: Structure, function and standards of Geospatial Web Services 
* M1V2: Screencast on data acquisition (where to find good geospatial web services) + explain requests (get...)

**Module 2:** 
* M2V1: Present the functional framework of the different Geospatial Web Services (WMS, WFS, etc.). 
* M2V2: Screencast on how to integrate Geospatial Web Services into QGIS

**Module 3:**
* M3V1: Introduction to the functions of server structures around Geospatial Web Services (Geoserver as an example).
* M3V2: Screencast on publishing a Geospatial Web Service (WMS) via Geoserver

## 3. Excercices and Quiz

**classical sructure of the Excercices and Quizzes** 
* Excercise (Mostly oriented to the videoguide)
* Quiz (checks the understanding of the given information)

### 3.1 Module 1: Identify Web Services needed for the use Case 

**Required software components used in this Module:** 
* No special software is required 

**Excercice**
Aufzählung und kurzer Video Guide auf welchen Ebenen Daten zu finden sind. Hier könnten Anbieter wie Copernicus oder auch GDI.de vorgestellt werden 

* Link zum Geodatenkatalog https://gdk.gdi-de.org/gdi-de/srv/ger/catalog.search#/home Hier sind einige Services aus Deutschland und der INSPIRE Umgebung zu finden und nach Themen filterbar. 
* WMS Deutscher Wetterdienst, GetCapabilities: https://maps.dwd.de/geoserver/ows?service=wms&version=1.3.0&request=GetCapabilities Umfangreicher Dienst des DWD (gut um zu zeigen wie mächtig WMS Services sein können
* 

**Quiz**
Quizfragen des Spider MOOCS:
* Question 1: What operations does WMS include? (!GetMap!, !GetFeatureInfo!, GetFeature, !GetCapabilities!)
* Question 2: Which data formates are generally produced by WMS? (KML, !JPEG, PNG, SVG, GIF!, GML)
* Question 3: Given the following GetMap() request which attribute should be modified so that the map is zoomed in on the city of Dortmund? (Layers, Service, !Bbox!, Request)

Quizfragen zu OGC Standards:
* http://learningzone.rspsoc.org.uk/index.php/Learning-Materials/Introduction-to-OGC-Standards/10.1-Final-Quiz



### 3.2 Module 2: Integrate Web Map Services (WMS) in QGIS and visualize Data from it

**Required software components used in this Module:** 
* **QGIS** is a free and open-source cross-platform desktop geographic information system (GIS) application that supports viewing, editing, printing, and analysis of geospatial data. QGIS functions as geographic information system (GIS) software, allowing users to analyze and edit spatial information, in addition to composing and exporting graphical maps. QGIS supports raster, vector and mesh layers. Vector data is stored as either point, line, or polygon features. Multiple formats of raster images are supported, and the software can georeference images.QGIS supports shapefiles, personal geodatabases, dxf, MapInfo, PostGIS, and other industry-standard formats. Web services, including Web Map Service and Web Feature Service, are also supported to allow use of data from external sources. QGIS integrates with other open-source GIS packages, including PostGIS, GRASS GIS, and MapServer. Plugins written in Python or C++ extend QGIS's capabilities. Plugins can geocode using the Google Geocoding API, perform geoprocessing functions similar to those of the standard tools found in ArcGIS, and interface with PostgreSQL/PostGIS, SpatiaLite and MySQL databases.

**Guide for the Software installation and regestration**
* You can install **QGIS** via the official website https://qgis.org/de/site/forusers/download.html and follow the guidance which is provided. Please note that QGIS provides not only the latest version, but also a stable version, which is preferable. A Registration is not necessary.

**Excercice/Guide**
* Hier wird im Video Guide in Qgis gewechselt und es wird grundsätzlich vorgestellt wie Web Services integriert werden können. Anhand der in Kapitel 3.1 identifizierten Services wird ein WMS Service genutzt um einige Datensätze zu visualisieren.
* Außerdem wird ein WFS Service in QGIS eingeladen. Es wird gezeigt, dass die Daten nun nicht nur visualisiert werden sondern physisch als bearbeitbare Temporärlyer vorliegen. 
* Abschließend wird die Aufgabe gestellt einen weiteren Service eines anderen Anbieters einzubinden (WMS, WFS)

**Quiz**
* ?

### 3.3 Modul 3: Publish a Web Service with the open source Software GeoServer

**Required software components used in this Module:** 
* **QGIS** is a free and open-source cross-platform desktop geographic information system (GIS) application that supports viewing, editing, printing, and analysis of geospatial data. QGIS functions as geographic information system (GIS) software, allowing users to analyze and edit spatial information, in addition to composing and exporting graphical maps. QGIS supports raster, vector and mesh layers. Vector data is stored as either point, line, or polygon features. Multiple formats of raster images are supported, and the software can georeference images.QGIS supports shapefiles, personal geodatabases, dxf, MapInfo, PostGIS, and other industry-standard formats. Web services, including Web Map Service and Web Feature Service, are also supported to allow use of data from external sources. QGIS integrates with other open-source GIS packages, including PostGIS, GRASS GIS, and MapServer. Plugins written in Python or C++ extend QGIS's capabilities. Plugins can geocode using the Google Geocoding API, perform geoprocessing functions similar to those of the standard tools found in ArcGIS, and interface with PostgreSQL/PostGIS, SpatiaLite and MySQL databases.
* **GeoServer** is an open-source server written in Java that allows users to share, process and edit geospatial data. Designed for interoperability, it publishes data from any major spatial data source using open standards. GeoServer has evolved to become an easy method of connecting existing information to virtual globes such as Google Earth and NASA World Wind as well as to web-based maps such as OpenLayers, Leaflet, Google Maps and Bing Maps. GeoServer functions as the reference implementation of the Open Geospatial Consortium Web Feature Service standard, and also implements the Web Map Service, Web Coverage Service and Web Processing Service specifications. 

**Guide for the Software installation and regestration**
* You can install **QGIS** via the official website https://qgis.org/de/site/forusers/download.html and follow the guidance which is provided. Please note that QGIS provides not only the latest version, but also a stable version, which is preferable. A Registration is not necessary. 
* To install **Geoserver** you also have to go to the official website https://geoserver.org/ and follow the provided guidance. Again you can choose between the latest and a stable Version. We recommend the stable Version.   

**Excercice/Guide**
* ?

**Quiz**
* ?


## 4. Wrap up

Hey! You did a great job! We hope that you now have an idea of how to work with Geospatial Web Services like WMS and WMF Services in your GIS and how to setup your own Web Services through Geoserver.  


**Interested In Learning More?**

On the Internet you will find a wealth of resources on Geospatial Web Services. Here are some recommendations: 

* Zhao, P., & Di, L. (Eds.). (2010). Geospatial web services: Advances in information interoperability: Advances in information interoperability. IGI Global. https://www.igi-global.com/book/geospatial-web-services/46010 
* Kralidis, A. T. (2007). Geospatial web services: The evolution of geospatial data infrastructure. In The Geospatial Web (pp. 223-228). Springer, London. https://link.springer.com/chapter/10.1007/978-1-84628-827-2_22 
* van den Brink, L., Barnaghi, P., Tandy, J., Atemezing, G., Atkinson, R., Cochrane, B., ... & Janowicz, K. (2019). Best practices for publishing, retrieving, and using spatial data on the web. Semantic Web, 10(1), 95-114. https://content.iospress.com/articles/semantic-web/sw305
* Clabby, J. (2003). Web services explained: Solutions and applications for the real world. Prentice Hall Professional. https://books.google.be/books?hl=nl&lr=&id=AKkFqV9-_9AC&oi=fnd&pg=PR13&dq=%22fundamentals+of+web+services%22&ots=PL1iLMeHGW&sig=H9XAty66RX8LFIKAo9-VmOOEZDA#v=onepage&q=%22fundamentals%20of%20web%20services%22&f=false
* Link to a page or lecture describing OGC WMS with an easy language: https://www.ogc.org/standards/wms/introduction 
* Link to a page or lecture describing OGC WFS with an easy language: http://opengeospatial.github.io/e-learning/wfs/text/basic-main.html
* Link to geospatial web services: https://gis4schools.readthedocs.io/en/latest/part2/2_1.html


**Your feedback is welcome!**

If you have identified shortcomings in this OER module or have ideas for improving the OER material, you are invited to add entries to the issue list in the [Github repository of this OER]( https://github.com/oer4sdi/...).
