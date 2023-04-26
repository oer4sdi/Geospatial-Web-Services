## Skript Videoguide 2 Modul 1


### Aufgabe: 


Lade dir die zur Verfügung gestellten Geodaten herunter und schaue dir das Folgende Video an. Deine Aufgabe besteht darin dem Screencast zu Folgen und selbst einen WMS- und einen WFS-Service Local auf deinem System zu hosten. Prüfe anschließend in QGIS ob du erfolgreich warst,  indem du die Services in ein neues QGIS-Projekt einbindest. 
Falls du dich noch tiefer mit dem Thema beschäftigen willst, dann findest du weitere Tutorials in der offiziellen Dokumentation von GeoServer unter: 
https://docs.geoserver.org/

### Skript

[Einleitung]
Hallo und herzlich willkommen. In diesem Screencast werden wir die freie Software GeoSer-ver über Docker installieren, ausführen und selbst einen WMS- Service einrichten. Ich werde dich durch den Prozess führen, wie du GeoServer über Docker installierst, Workspaces und Stores erstellst, Layer veröffentlichst, Styles hinzufügst und die Services in QGIS überprüfst. Lass uns loslegen!


[Schritt 1: GeoServer von Docker ausführen]
Der erste Schritt ist, GeoServer über Docker auszuführen. Um dies zu tun, öffnen wir die Kommandozeile oder unser Terminal und stellen sicher, dass Docker installiert und ausge-führt wird. Gib den folgenden Befehl ein, um GeoServer von Docker zu pullen, also herunter-zuladen:

```shell
docker pull docker.osgeo.org/geoserver:2.22.0
```

Dieser Vorgang kann einige Minuten in Anspruch nehmen.
 
Wenn der Vorgang abgeschlossen ist, dann gib den folgenden Befehl ein, um GeoServer auszuführen:

```shell
docker run -it -p 80:8080 docker.osgeo.org/geoserver:2.22.0
```

Dieser Befehl startet GeoServer auf Port 8080.


[Schritt 2: GeoServer Web Interface]
Nachdem wir GeoServer von Docker gestartet haben, können wir auf das Web-Interface zugreifen, indem wir in unserem Webbrowser "http://localhost:8080/geoserver" in die Such-leiste eingeben. Wir landen auf der Startseite unseres Geoservers. Diese ist zunächst recht unaussagekräftig und wir haben sehr eingeschränkte Auswahlmöglichkeiten. Das ändert sich, wenn wir uns im oberen Teil der Seite anmelden. Verwende hier die Standardanmeldeinfor-mationen ("admin" als Benutzername und "geoserver" als Passwort).

Sobald wir angemeldet sind, sehen wir die Startseite des GeoServer Web Interface. Hier können wir auf verschiedene Funktionen und Einstellungen zugreifen, wie z.B. die Verwaltung von Workspaces, Stores, Layern und Styles.

Workspaces dienen in GeoServer als eine Art Container für Ressourcen wie Layer, Stile, Da-tenquellen und Einstellungen. Ein Workspace kann als eine Art Namensraum für Ressourcen betrachtet werden, die innerhalb dieses Namensraums eindeutig identifiziert werden kön-nen. Ein Workspace wird verwendet, um verschiedene Projekte oder Arbeitsbereiche inner-halb einer einzigen GeoServer-Installation zu organisieren.

Ein Store ist eine Schnittstelle zu einer bestimmten Art von Geodatenquelle. Ein Store kann beispielsweise eine Verbindung zu einem PostGIS-Datenbankserver, einem Shapefile-Ordner oder einem WMS-Server sein. Es gibt verschiedene Arten von Stores in GeoServer, je nach Art der Datenquelle, die man verwenden möchte. Hier werden also die Bezüge zu den Da-tenquellen hergestellt. 

Ein Layer repräsentiert einen bestimmten Geodatensatz, der über WebServices abgerufen werden kann und in einer bestimmten Art und Weise dargestellt wird und Styles beschreiben die Symbolisierungen der einzelnen Layer. 

[Schritt 3: Workspace und Store erstellen]
Als nächstes werden wir einen neuen Workspace und Store erstellen. Klicke auf "Work-spaces" und dann auf "Neuen Workspace hinzufügen". Gib einen Namen für den Workspace ein und lege eine URI fest. Die URI kannst du dir ausdenken, wichtig ist nur das du die äußere Form einer Webadresse einhälst. Wenn du einen Service nicht nur lokal hosten möchtest, sondern im Web anbietest, sollte die URI natürlich eine gültige, von dir verwaltete We-badresse beinhalten. Danach kannst du "Speichern".

Klicke anschließend erneut auf den neu erstellten Workspace und nun erscheint zusätzlich eine Auswahl von Services. Aktiviere hier das Kontrollkästchen für WMS und WFS. Damit legst du fest, dass alle in dem Workspace enthaltenen Daten als WMS und als WFS von dei-nem GeoServer zur Verfügung gestellt werden. 

Wechsle jetzt auf den Menüpunkt „Stores“ und gehe auf "Neuen Store hinzufügen". Wähle den entsprechenden Datentyp aus (z. B. "Shapefile") und gib die erforderlichen Informatio-nen ein. Vergebe einen Namen, suche den richtigen Dateipfad Klicke auf "Speichern", wenn du fertig bist.


[Schritt 4: Layer veröffentlichen]
Jetzt können wir unsere Layer veröffentlichen. Klicke auf den Reiter „Layer“, und dann auf "Neuen Layer hinzufügen". Ordne den Layer dem gewünschten Workspace und Store zu, füge einen Namen, einen Titel und eine Beschreibung hinzu, damit der Layer leicht identifiziert werden kann. Lasse das verwendete Koordinatensystem aus den Daten auslesen. Lege au-ßerdem die Bounding Box für den Layer fest, indem du entweder die Werte manuell eingibst oder auf "Compute from data" und „compute from native Boarder“ klickst, um sie automa-tisch aus den Daten auslesen zu lassen und.
Klicke auf "Speichern", wenn du fertig bist.

[Schritt 5: Styles hinzufügen]
Nachdem wir unseren Layer erfolgreich veröffentlicht haben, können wir nun Styles zu die-sen hinzufügen. Klicke auf den "Styles" Reiter. Hier könntest du nun Styles speziell für die 
Neuen Layer erstellen. Styles kannst du entweder händisch über eine Konsole in css schrei-ben oder du kannst eine Stildatei, beispielsweise eine sld Datei aus QGIS einladen. 

Wir nutzen in diesem Tutorial einen bereits angelegten Stil der zu den Daten in unserem Store passt. Wir wählen also den Stil „“ und navigieren über den "Publishing" -Reiter, um den neuen Style dem richtigen Layer zuzuordnen und klicken anschließend auf "Speichern“. 


Diese Schritte können wir nun beliebig oft wiederholen. Ich lege noch einen weiteren Layer im erstellten Workspace an. 

[Schritt 7: Service testen in QGIS]
Jetzt können wir überprüfen, ob unsere Services funktionieren. Öffne QGIS und füge den WMS-Service hinzu, indem du auf "Layer" -> "Neuer WMS-Layer" klickst. Oder in deinem Brows Fenster einen Rechtsklick auf WMS und dann Neue verbindung hinzufügen drückst. Gib die URL des WMS-Services ein, wähle den Layer aus, den du veröffentlicht hast, und füge den Layer hinzu. 

Die URL deines eigenen Geoservers findest du am einfachsten heraus, indem du über das Logo zurück auf die Startseite der Weboberfläche gehst und dort auf den gewünschten Ser-vice klickst. In diesem Fall möchten wir die URL für unseren WMS Service erfahren. Wir wählen diesen also an und es öffnet sich eine neue XML Seite. Die URL die wir zum Verknüp-fen benötigen finden wir in der Suchleiste unseres Browsers. Also einfach kopieren und bei QGIS einfügen. 

Füge nun ebenfalls den WFS-Service hinzu, indem du auf "Layer" -> "Neuer WFS-Layer" klickst. Gib die URL des WFS-Services ein, wähle den Layer aus, den du veröffentlicht hast, und füge den Layer hinzu.

Überprüfe nun, ob die Services ordnungsgemäß funktionieren, indem du auf die verschiede-nen Layer klickst und sicherstellst, dass die Daten richtig angezeigt werden.

[Schritt 9: Fazit]
Herzlichen Glückwunsch! Du hast erfolgreich GeoServer über Docker ausgeführt, Work-spaces und Stores erstellt, Layer veröffentlicht, Styles hinzugefügt und WMS- und WFS

 in QGIS getestet. 

Insgesamt ist GeoServer eine leistungsstarke und vielseitige Software, mit der du Geodaten schnell und einfach veröffentlichen und freigeben kannst. Mit ein wenig Übung und Erfah-rung kannst du GeoServer verwenden, um ansprechende und informative Karten und Geoda-tenanwendungen zu erstellen.
