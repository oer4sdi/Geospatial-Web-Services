# OER on Geospatial Web Services (work in progress!)       


         	           	
## 1. Overview

In this Open Educational Resource (OER) you will learn which forms of **geospatial web services** exist, how they are structured, how they can be integrated into an open source GIS (QGIS) and connect with a self published GeoServer. After you have completed this tutorial, you will know how:

* (Module 1) Geospatial Web Services are structured 
* (Module 1) to find and identify usefull Geospatial Web Services
* (Module 2) to integrate Web Map Services (WMS) in QGIS and visualize Data from it 
* (Module 2) to integrate Web Feature Services (WFS) in QGIS and get Data from it
* (Module 3) to publish your own Data as Web Map Service (WMS) through GeoServer 


The module is structured as follows

1. Overview
2. Thematic Background 
3. Excercices and Guides
4. Wrap up 

If you are mainly interested in the technical aspects, you can jump directly to chapter 3 where we guide you through the technical exercise. With the help of self-tests you can check if you have understood the essential concepts and technologies.

This tutorial is mainly designed for students who want to spend about ... minutes on improving their skills in integrating Data from Geosaptial Web Services. You should have some basic knowledge of GIS Software and it wouldn't be bad if you already have some experience in using the free open source Software Geoserver.

This tutorial was developed at the Institute of Geodesy at Bochum University of Applied Sciences in close cooperation with the University of Münster and the University of Bochum. Main author is Fabian Przybylak under the direction of Prof. Dr. Carsten Keßler.

You are free to use, alter and reproduce the tutorial (H5P content) under the terms of the CC-BY-SA 4.0 license. Any code provided with the tutorial can be used under the terms of the MIT license. Please see the [full license terms](https://github.com/...../blob/main/LICENSE.md).

The OER4SDI project has been recommended by the Digital University NRW and is funded by the Ministry of Culture and Science NRW. 


## 2. Thematic Background

**Module 1:** 
With the following slides we provide you with some general context and background on Geospatial Web Services. 

**Module 2:** 

**Module 3:**

### 2.1 Read and learn...

**Module 1:** 

Hier wird erklärt was Geospatial web Services sind (Aufbau, Funktion). Hier werden außerdem Abkürzungen wie OGC etc. erklärt. (Standards) und auf standard Befehle eingegangen wie getCapabilities und getMap

In the most simplistic way a Web service may be defined as "a Web accesable program code which performs a task of either processing or serving some data. Although there are many other definitions in the related literature, the one in W3C (2004) seems to be quite complete and refering to also lately popular REST style Web services. It states that " We can identify two major classes of Web services: REST-compliant Web services, in which the primary purpose of the service is to manipulate XML representations of Web resources using a uniform set of "stateless" operations; and arbitrary Web services, in which the service may expose an arbitrary set of operations. (Definition EO4Geo)

**Module 2:** 
Es wird auf die verschiedenen Angebote eingegangen (WMS, WMTS, WFS, etc.) und wie diese sich voneinander unterscheiden

**Module 3:**
Hier wird darauf eingegangen wie Serversysteme aufgebaut sind und es wird Geoserver als OpenSource Produkt vorgestellt 

### 2.2 Test your knowledge

**Module 1:** 
Quizfragen Modul 1

**Module 2:** 
Quizfragen Modul 2

**Module 3:**
Quizfragen Modul 3


**Quiz Fragen des Spider MOOCS:** 

* Question 1: What operations does WMS include? (!GetMap!, !GetFeatureInfo!, GetFeature, !GetCapabilities!)
* Question 2: Which data formates are generally produced by WMS? (KML, !JPEG, PNG, SVG, GIF!, GML)
* Question 3: Given the following GetMap() request which attribute should be modified so that the map is zoomed in on the city of Dortmund? (Layers, Service, !Bbox!, Request)



## 3. Excercices and Guides


**A) Software components used in this Module:** 

* **QGIS** is a free and open-source cross-platform desktop geographic information system (GIS) application that supports viewing, editing, printing, and analysis of geospatial data. QGIS functions as geographic information system (GIS) software, allowing users to analyze and edit spatial information, in addition to composing and exporting graphical maps. QGIS supports raster, vector and mesh layers. Vector data is stored as either point, line, or polygon features. Multiple formats of raster images are supported, and the software can georeference images.QGIS supports shapefiles, personal geodatabases, dxf, MapInfo, PostGIS, and other industry-standard formats. Web services, including Web Map Service and Web Feature Service, are also supported to allow use of data from external sources. QGIS integrates with other open-source GIS packages, including PostGIS, GRASS GIS, and MapServer. Plugins written in Python or C++ extend QGIS's capabilities. Plugins can geocode using the Google Geocoding API, perform geoprocessing functions similar to those of the standard tools found in ArcGIS, and interface with PostgreSQL/PostGIS, SpatiaLite and MySQL databases. (**Module 2**)
* **GeoServer** is an open-source server written in Java that allows users to share, process and edit geospatial data. Designed for interoperability, it publishes data from any major spatial data source using open standards. GeoServer has evolved to become an easy method of connecting existing information to virtual globes such as Google Earth and NASA World Wind as well as to web-based maps such as OpenLayers, Leaflet, Google Maps and Bing Maps. GeoServer functions as the reference implementation of the Open Geospatial Consortium Web Feature Service standard, and also implements the Web Map Service, Web Coverage Service and Web Processing Service specifications. (**Module 3**)
* **Docker** allows us to package all needed software components as Docker Images and execute those images as Docker Containers in the Docker Environment, e.g. on Linux, Windows or Mac. With the docker-compose tool we can define multiple docker images and configure how they communicate with each other. (**Module 3**)

**B) Guide for the Software installation and regestration**

You can install **QGIS** via the official website https://qgis.org/de/site/forusers/download.html and follow the guidance which is provided. Please note that QGIS provides not only the latest version, but also a stable version, which is preferable. A Registration is not necessary. (**Module 2**)

To install **Geoserver** you also have to go to the official website https://geoserver.org/ and follow the provided guidance. Again you can choose between the latest and a stable Version. We recommend the stable Version. (**Module 3**)  

To Install **Docker** please go to the official web site [https://docs.docker.com/get-docker/](https://docs.docker.com/get-docker/) and follow the guidance which is provided there to install docker on your local computer (Linux, Windows or Mac). It is recommended to have at least 8GB RAM to support smooth functioning of Docker. (**Module 3**)


### 3.1 Identify Web Services needed for the use Case (Module 1)

Aufzählung und kurzer Guide auf welchen Ebenen Daten zu finden sind. Hier könnten Anbieter wie Copernicus oder auch GDI.de vorgestellt werden 

* Link zum Geodatenkatalog https://gdk.gdi-de.org/gdi-de/srv/ger/catalog.search#/home Hier sind einige Services aus Deutschland und der INSPIRE Umgebung zu finden und nach Themen filterbar. 
* WMS Deutscher Wetterdienst, GetCapabilities: https://maps.dwd.de/geoserver/ows?service=wms&version=1.3.0&request=GetCapabilities Umfangreicher Dienst des DWD (gut um zu zeigen wie mächtig WMS Services sein können

### 3.2 Integrate Web Map Services (WMS, WMTS) in QGIS and visualize Data from it (Module 2)

Hier wird in Qgis gewechselt und es wird grundsätzlich vorgestellt wie Web Services integriert werden können. Anhand der in Kapitel 3.1 identifizierten Services wird ein WMS Service genutzt um einige Datensätze zu visualisieren.  

Abschließend wird die Aufgabe gestellt einen weiteren Service eines anderen Anbieters einzubinden (WMS, WMTS)

### 3.3 integrate Web Feature Services (WFS) in QGIS and get Data from it (Module 2)

In diesem Abschnitt wird ein WFS Service in QGIS eingeladen. Es wird gezeigt, dass die Daten nun nicht nur visualisiert werden sondern physisch als bearbeitbare Temporärlyer vorliegen. 

### 3.4 Publish a Web Service with the open source Software GeoServer (Module 3)



## 4. Wrap up

Hey! You did a great job! You ... 
We hope that you now have an idea of how to work with ... 


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
