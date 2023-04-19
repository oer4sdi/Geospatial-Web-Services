# OER zu Geospatial Web Services (in Arbeit!)       
         	           	
## 1. Überblick

In dieser Open Educational Resource (OER) lernst du, welche Formen von **Geospatial Web Services** existieren, wie sie strukturiert sind, wie sie in ein Open Source GIS (QGIS) integriert und über GeoServer veröffentlicht werden können. 

**Nachdem du die folgende OER abgeschlossen hast, wirst du wissen:**
* was Geospatial Web Services und OGC-Standards sind
* wo Sie nützliche Geospatial Web Services finden und identifizieren können und wie sie strukturiert sind
* wie man Web Services in QGIS integriert und mit Daten daraus arbeitet 
* wie man seine eigenen Web Services mit GeoServer veröffentlicht 

**Das OER ist wie folgt aufgebaut**

1. Überblick
2. Thematischer Hintergrund 
3. Übungen und Leitfäden
4. Quiz 
5. Nachbereitung 

**Generelle Informationen**

Dieses Tutorial richtet sich hauptsächlich an Teilnehmer, die in etwa ... Minuten ihre Fähigkeiten zur Integration von Daten aus Geospatial Web Services verbessern wollen. Du solltest bestenfalls einige Grundkenntnisse im Umgang mit GIS-Software besitzen.

Dieses Tutorial wurde am Institut für Geodäsie der Fachhochschule Bochum in enger Zusammenarbeit mit der Universität Münster und der Universität Bochum entwickelt. Hauptautor ist Fabian Przybylak unter der Leitung von Prof. Dr. Carsten Keßler.

Du darfst das OER (H5P-Inhalte) unter den Bedingungen der CC-BY-SA 4.0-Lizenz frei verwenden, verändern und vervielfältigen. Jeglicher Code, der mit dem OER zur Verfügung gestellt wird, kann unter den Bedingungen der MIT-Lizenz verwendet werden. Bitte lesen Sie die [vollständigen Lizenzbedingungen] (https://github.com/oer4sdi/Geospatial-Web-Services/blob/main/LICENSE.md). 

Das Projekt OER4SDI wurde von der Digitalen Hochschule NRW empfohlen und wird durch das Ministerium für Kultur und Wissenschaft NRW gefördert. 

## 2. Thematischer Hintergrund

**Gliederung des thematischen Hintergrunds** 
* Kurze Einleitung mit allgemeinem Kontext und Hintergrund (in wenigen Sätzen) 
* Thematisches Video (Hauptinformationen über den Inhalt; Textakkordion welches die gegebenen Informationen zusammenfasst)


### 2.1 Kurze Einführung

**Worum geht es eigentlich?**
Die rasche Entwicklung von Methoden und Techniken zur Erfassung von Geodaten bietet die Möglichkeit, riesige Mengen von Geodaten zu sammeln. Sie stellt jedoch auch verschiedene Datenorganisationen und Datennutzer vor die Herausforderung, große Mengen von Geodaten zu verwalten, gemeinsam zu nutzen, zu verarbeiten und zu analysieren. Datenorganisationen stehen vor der Herausforderung, neue Lösungen für die Verwaltung, Speicherung und gemeinsame Archivierung dieser riesigen Datenmengen zu finden.

Ein Online-Dienst um geografische Informationen und räumliche Daten über das Internet bereit zu stellen sind Geospatial Web Services. Diese Dienste ermöglichen es Benutzern, geografische Daten effizient zu teilen, zu suchen, zu visualisieren, abzurufen und zu analysieren.

**Welches Problem besteht dabei?**
Datenverbreitungssysteme müssen sich immer mit einem Heterogenitätsproblem auseinandersetzen. Verschiedene Quellen können die Effektivität des Austauschs und der Verwaltung von Geodaten behindern. Verschiedene Betriebssysteme, Hardware, Software, Datenformate und Schnittstellen sind mit dem Problem der syntaktischen Heterogenität verbunden. Wenn zwei Webdienste die Schnittstellen des jeweils anderen nicht kennen, können sie keine Nachrichten und Daten austauschen.

**Welche Lösung gibt es dafür?**
Aus diesem Grund sind Geospatial Web Services in der Regel nach den vom Open Geospatial Consortium entwickelten OGC-Standards organisiert. Diese Standards ermöglichen, dass die Services interoperabel sind und von verschiedenen Anwendungen und Plattformen übergreifend verwendet werden können.

### 2.2 Thematisches Video (Hauptinformationen)

...

## 3. Übungen und Leitfäden

**Aufbau der Übungen und Leitfäden** 
* Übung 
* Videoguide (Screencast)

### 3.1 Übung 1

**Benötigte Softwarekomponenten, die in dieser Übung verwendet werden:** 

**QGIS** ist eine freie und quelloffene, plattformübergreifende Desktop-Anwendung für geografische Informationssysteme (GIS), die das Anzeigen, Bearbeiten, Drucken und Analysieren von Geodaten unterstützt. 
(Sie können **QGIS** über die offizielle Website https://qgis.org/de/site/forusers/download.html installieren und der dortigen Anleitung folgen)

**Übung**



### 3.2 Übung 2
**Benötigte Softwarekomponenten, die in dieser Übung verwendet werden:** 

**QGIS** ist eine freie und quelloffene, plattformübergreifende Desktop-Anwendung für geografische Informationssysteme (GIS), die das Anzeigen, Bearbeiten, Drucken und Analysieren von Geodaten unterstützt.

**GeoServer** ist ein in Java geschriebener Open-Source-Server, der es Benutzern ermöglicht, Geodaten gemeinsam zu nutzen, zu verarbeiten und zu bearbeiten.

**Übung**


## 5. Quiz


## 5. Auspacken

Hey! Das hast du gut gemacht! Wir hoffen, dass Sie nun eine Vorstellung davon haben, wie Sie mit Geospatial Web Services wie WMS und WMF Services in Ihrem GIS arbeiten und wie Sie Ihre eigenen Web Services über Geoserver einrichten können.  


**Interessiert daran, mehr zu lernen?**

Im Internet finden Sie eine Fülle von Ressourcen zu Geospatial Web Services. Hier sind einige Empfehlungen: 

* Zhao, P., & Di, L. (Eds.). (2010). Geospatial Web Services: Advances in information interoperability: Fortschritte bei der Interoperabilität von Informationen. IGI Global. https://www.igi-global.com/book/geospatial-web-services/46010 
* Kralidis, A. T. (2007). Geospatial Web Services (Geodaten-Webdienste): The evolution of geospatial data infrastructure. In The Geospatial Web (S. 223-228). Springer, London. https://link.springer.com/chapter/10.1007/978-1-84628-827-2_22 
* van den Brink, L., Barnaghi, P., Tandy, J., Atemezing, G., Atkinson, R., Cochrane, B., ... & Janowicz, K. (2019). Best Practices für die Veröffentlichung, Abfrage und Nutzung von Geodaten im Web. Semantic Web, 10(1), 95-114. https://content.iospress.com/articles/semantic-web/sw305
* Clabby, J. (2003). Webdienste erklärt: Lösungen und Anwendungen für die reale Welt. Prentice Hall Professional. https://books.google.be/books?hl=nl&lr=&id=AKkFqV9-_9AC&oi=fnd&pg=PR13&dq=%22fundamentals+of+web+services%22&ots=PL1iLMeHGW&sig=H9XAty66RX8LFIKAo9-VmOOEZDA#v=onepage&q=%22fundamentals%20of%20web%20services%22&f=false
* Link zu einer Seite oder einer Vorlesung, die OGC WMS in einer einfachen Sprache beschreibt: https://www.ogc.org/standards/wms/introduction 
* Link zu einer Seite oder einer Vorlesung, die OGC WFS in einfacher Sprache beschreibt: http://opengeospatial.github.io/e-learning/wfs/text/basic-main.html
* Link zu Geospatial Web Services: https://gis4schools.readthedocs.io/en/latest/part2/2_1.html


**Ihr Feedback ist willkommen!**

Wenn Sie Defizite in diesem OER-Modul festgestellt haben oder Ideen zur Verbesserung des OER-Materials haben, sind Sie herzlich eingeladen, Einträge in die Issue-Liste im [Github repository dieses OERs]( https://github.com/oer4sdi/...).
