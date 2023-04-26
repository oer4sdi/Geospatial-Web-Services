##Skript Videoguide 1 Modul 1


###Aufgabe: 


Stöbere einige Zeit auf den Webseiten der angehängten Linksammlung und prüfe welche Services auf den Webseiten angeboten werden. Achte zusätzlich darauf in welcher Form die Services bereitstehen (WMS, WFS, etc.).
o	Geodatenkatalog Deutschland: https://gdk.gdi-de.org/gdi-de/srv/ger/catalog.search#/home
o	Geoportal Deutschland: https://www.geoportal.de/ 
o	Geodatenkatalog Schweiz: https://www.geocat.ch/geonetwork/srv/ger/catalog.search#/home
Du hast nun einige Quellen kennengelernt über die du Geospatial Web Services finden kannst. Wähle im folgenden einen WMS- und einen dazu passenden WFS-Service aus und implementiere diese in ein simples QGIS Projekt. Folge dazu gerne auch dem angehängten Videoguide. 
Falls ein Service mal nicht funktionieren sollte dann probiere zunächst einen anderen aus. Es kann vorkommen, dass Services vom Provider nicht mehr unterstützt werden oder Links nicht mehr aktuell sind. 

###Skript

Hallo und herzlich willkommen zu einem neuen Screencast zum Thema "Geospatial Web Services". In diesem Screencast möchten wir uns einige Beispiele für WMS- und WFS-Services ansehen und diese in einem einfachen QGIS-Projekt integrieren.

Bevor wir jedoch mit der Integration der Services beginnen, wollen wir uns zunächst die Webseiten ansehen, auf denen wir die Services finden können. Eine gute Quelle für geospa-tiale Services ist der Geodatenkatalog Deutschland (https://gdk.gdi-de.org/gdi-de/srv/ger/catalog.search#/home). Hier kann man über die Suchfunktion verschiedene Ser-vices finden und diese direkt in QGIS einbinden. Eine ähnliche Seite ist das Geoportal Deutschland (https://www.geoportal.de/), auf der ebenfalls viele Services angeboten wer-den.

Ein weiterer Geodatenkatalog ist der Geodatenkatalog Schweiz (https://www.geocat.ch/geonetwork/srv/ger/catalog.search#/home), auf dem man eine Vielzahl von Geodaten und Services finden kann.

Für unser Beispiel möchten wir den WMS-Service von Basemap.de nutzen, der verschiedene topographische Karten für Deutschland bereitstellt. Der Service hat die folgende Adresse: https://basemap.de/dienste/wms_capabilities_web_raster.xml.



Für unser Beispiel möchten wir den "Web Feature Service (WFS)" des Bundesamts für Karto-graphie und Geodäsie nutzen, der verschiedene geographische Informationen wie Verwal-tungsgrenzen, Flächennutzung und Geodätische Referenzsysteme bereitstellt. Als konkreten Service wählen wir den "WFS VG2500", der Verwaltungsgrenzen für Deutschland bereitstellt. Der Service hat die folgende Adresse: https://sgx.geodatenzentrum.de/wfs_vg2500

Bevor wir nun mit der Integration der Services beginnen, möchten wir noch kurz den Unter-schied zwischen WMS und WFS erläutern. WMS (Web Map Service) ist ein geospatialer Ser-vice, der Kartenbilder in Echtzeit generiert und diese als Rasterbilder (z.B. PNG oder JPEG) zurückliefert. Diese Bilder können dann in verschiedenen Anwendungen wie z.B. QGIS oder Google Maps angezeigt werden. WFS (Web Feature Service) hingegen liefert vektorbasierte geographische Informationen, wie z.B. Punkte, Linien oder Polygone, zurück. Diese können dann ebenfalls in verschiedenen Anwendungen wie z.B. QGIS angezeigt und weiterverarbei-tet werden.

Nun können wir mit der Integration der Services in QGIS beginnen. Dazu öffnen wir zunächst QGIS und erstellen ein neues Projekt. Anschließend fügen wir über den Menüpunkt "Layer" -> "Add Layer" -> "Add WMS/WMTS Layer" den WMS-Service hinzu. Hierbei müssen wir ledig-lich die URL des Services eingeben und können anschließend aus einer Liste von verfügbaren Layern auswählen. Wir wählen hier beispielsweise den Layer "" aus.

Als nächstes fügen wir über den Menüpunkt "Layer" -> "Add Layer" -> "Add WFS Layer" den WFS-Service hinzu. Hierbei müssen wir ebenfalls die URL des Services eingeben und können anschließend aus einer Liste von verfügbaren Layern auswählen. Wir wählen hier beispiels-weise den Layer "" aus, der die Verwaltungsgrenzen der deutschen Bundesländer enthält.

Mit einem WFS-Service können wir verschiedene Aktionen durchführen, die mit einem WMS-Service nicht möglich sind. Zum Beispiel können wir die Daten aus dem WFS-Service in QGIS bearbeiten, analysieren und modifizieren, um neue Erkenntnisse zu gewinnen oder neue Karten zu erstellen. Wir können auch komplexe Abfragen durchführen, um nur be-stimmte Daten auszuwählen und zu visualisieren.

Ein weiterer Vorteil von WFS-Service ist, dass er in der Lage ist, aktualisierte Daten bereitzu-stellen, während WMS-Service lediglich statische Kartenbilder liefert. Wenn die Daten in der WFS-Datenbank aktualisiert werden, können wir die Änderungen sofort im QGIS-Projekt se-hen und darauf reagieren.

Zusammenfassend bietet der Einsatz von WMS- und WFS-Services in QGIS eine leistungs-starke Möglichkeit, um geospatiale Daten anzuzeigen, zu analysieren und zu modifizieren. Mit einem WMS-Service können wir schnell und einfach Kartenbilder darstellen, während ein WFS-Service uns detaillierte Informationen über geographische Daten liefert, die wir bearbeiten und analysieren können, um neue Erkenntnisse zu gewinnen.

Das war unser Screencast zum Thema "Integration von Geospatial Web Services in QGIS". Wir hoffen, dass wir Ihnen einen guten Einblick in die Verwendung von WMS- und WFS-Services in QGIS geben konnten. Vielen Dank fürs Zuschauen!
