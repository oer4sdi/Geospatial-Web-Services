## Skript Videoguide 1 Modul 1


### Aufgabe: 


Stöbere einige Zeit auf den Webseiten der angehängten Linksammlung und prüfe welche Services auf den Webseiten angeboten werden. Achte zusätzlich darauf in welcher Form die Services bereitstehen (WMS, WFS, etc.).

* Geodatenkatalog Deutschland: https://gdk.gdi-de.org/gdi-de/srv/ger/catalog.search#/home
* Geoportal Deutschland: https://www.geoportal.de/ 
* Geodatenkatalog Schweiz: https://www.geocat.ch/geonetwork/srv/ger/catalog.search#/home

Du hast nun einige Quellen kennengelernt über die du Geospatial Web Services finden kannst. Wähle im folgenden einen WMS- und einen dazu passenden WFS-Service aus und implementiere diese in ein simples QGIS Projekt. Folge dazu gerne auch dem angehängten Videoguide. 
Falls ein Service mal nicht funktionieren sollte dann probiere zunächst einen anderen aus. Es kann vorkommen, dass Services vom Provider nicht mehr unterstützt werden oder Links nicht mehr aktuell sind. 

### Skript

Hallo und herzlich willkommen. In diesem Screencast beschäftigen wir uns mit dem Thema "Geospatial Web Services". Wir werden uns einige Beispiele für WMS- und WFS-Services ansehen und diese in einem einfachen QGIS-Projekt integrieren.

Bevor wir jedoch mit der Integration in QGIS beginnen, wollen wir uns zunächst Webseiten ansehen, auf denen wir potenzielle Services finden können. 

Eine gute Quelle für Geospatial Web Services ist der Geodatenkatalog Deutschland (https://gdk.gdi-de.org/gdi-de/srv/ger/catalog.search#/home). Hier kannst du über die Such-funktion oder die vorgeschlagenen Kategoriensehr einfach verschiedene Services finden. Vie-le der Datensätze können direkt in einer Webkarte aufgerufen werden, um einen ersten Ein-druck von den enthaltenen Daten zu bekommen. Wenn wir in die Datenbeschreibung gehen dann bekommen wir außerdem eine kurze Zusammenfassung der Inhalte und die für die verknüpfung notwendigen URLs zu unseren Services geliefert. 

Dem ähnlich ist das Geoportal Deutschland (https://www.geoportal.de/), hier werden eben-falls viele Services für Datensätze in Deutschland angeboten. Die Angebotenen Datensätze umfassen allerdings weniger kleine Einzelprodukte, sondern stellen in der Regel großflächige bereits verarbeitete Produkte dar, die häufig das gesamte Bundesgebiet abdecken. Es gibt ebenfalls die Möglichkeit die Angebotenen Produkte über eine Webkarte zu sichten. Über das Ausrufezeichen gelangen wir zu einer Informationsseite, die entweder direkt eine URL zu den angebotenen Services bereithält, oder aber auf die richtige Seite verweist. 

Auch im Ausland gibt es einige gut organisierte Geodatenkataloge ein Beispiel hierfür ist der Geodatenkatalog der Schweiz	 (https://www.geocat.ch/geonetwork/srv/ger/catalog.search#/home), sucht man also auslän-dische Services, kommt man häufig nicht draum herum auch auf internationalen Webseiten danach zu suchen.

Für unser Beispiel möchten wir einen WMS-Service von Basemap.de nutzen, der verschiede-ne topographische Karten für Deutschland bereitstellt. Der Service hat die folgende Adresse: https://basemap.de/dienste/wms_capabilities_web_raster.xml 

Sowie einen "Web Feature Service (WFS)" des Bundesamts für Kartographie und Geodäsie, der verschiedene geographische Informationen wie Verwaltungsgrenzen, Flächennutzung und Geodätische Referenzsysteme bereitstellt. Als konkreten Service wählen wir den "WFS VG2500", der Verwaltungsgrenzen für Deutschland bereitstellt. Dieser Service hat die Adres-se: https://sgx.geodatenzentrum.de/wfs_vg2500

Bevor wir nun mit der Integration der Services beginnen, möchte ich noch kurz den Unter-schied zwischen WMS und WFS erläutern. Ein WMS (Web Map Service) ist ein Service, der Kartenbilder in Echtzeit generiert und diese als Rasterbilder (z.B. PNG oder JPEG) zurücklie-fert. Diese Bilder können dann in verschiedenen Anwendungen wie z.B. QGIS oder Google Maps angezeigt werden. Ein WFS (Web Feature Service) hingegen liefert vektorbasierte geo-graphische Informationen, wie z.B. Punkte, Linien oder Polygone, zurück. Diese können dann ebenfalls in verschiedenen Anwendungen wie z.B. QGIS angezeigt werden, können darüber hinaus aber auch weiterverarbeitet werden. Web Feature Services sind für also sehr mäch-tig, zeitgleich aber auch sehr rechenintensiv. 

Nun können wir aber mit der Integration der Services in QGIS beginnen. Dazu öffnen wir zunächst QGIS und erstellen ein neues Projekt. Anschließend fügen wir über den Menüpunkt "Layer" -> "Add Layer" -> "Add WMS/WMTS Layer" den WMS-Service hinzu. Hierbei müssen wir lediglich einen Namen festlegen und die URL des Services eingeben. anschließend kön-nen wir aus einer Liste von verfügbaren Layern auswählen. Wir wählen hier beispielsweise den Layer "" aus.

Als nächstes fügen wir über den Menüpunkt "Layer" -> "Add Layer" -> "Add WFS Layer" den WFS-Service hinzu. Hierbei müssen wir ebenfalls einen Namen vergeben und die URL des Services eingeben. Danach können wir wieder aus einer Liste von verfügbaren Layern aus-wählen. Wir wählen hier den Layer "" aus, der die Verwaltungsgrenzen der deutschen Bun-desländer enthält.

Mit einem WFS-Service können wir verschiedene Aktionen durchführen, die mit einem WMS-Service nicht möglich sind. Zum Beispiel können wir die Daten aus dem WFS-Service in QGIS bearbeiten, analysieren und modifizieren, um neue Erkenntnisse zu gewinnen oder neue Karten zu erstellen. Wir können auch komplexe Abfragen durchführen, um nur be-stimmte Daten auszuwählen und zu visualisieren.

Ein weiterer Vorteil von WFS-Service ist, dass er in der Lage ist, aktualisierte Daten bereitzu-stellen, während WMS-Service lediglich statische Kartenbilder liefert. Wenn die Daten in der WFS-Datenbank aktualisiert werden, können wir die Änderungen sofort im QGIS-Projekt se-hen und darauf reagieren.

Zusammenfassend bietet der Einsatz von WMS- und WFS-Services in QGIS eine leistungs-starke Möglichkeit, um geospatiale Daten anzuzeigen, zu analysieren und zu modifizieren. Mit einem WMS-Service können wir schnell und einfach Kartenbilder darstellen, während ein WFS-Service uns detaillierte Informationen über geographische Daten liefert, die wir bearbeiten und analysieren können, um neue Erkenntnisse zu gewinnen.

Das war unser Screencast zum Thema "Integration von Geospatial Web Services in QGIS". Ich hoffe, dass ich euch einen guten Einblick in die Verwendung von WMS- und WFS-Services in QGIS geben konnten. Vielen Dank fürs Zuschauen!
