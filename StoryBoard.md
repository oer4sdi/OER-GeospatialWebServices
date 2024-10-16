# OER zu Geospatial Web Services      
         	           	
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
5. Zusammenfassung 

**Generelle Informationen**

Dieses Tutorial richtet sich hauptsächlich an Teilnehmer, die in etwa ... Minuten ihre Fähigkeiten zur Integration von Daten aus Geospatial Web Services verbessern wollen. Du solltest bestenfalls einige Grundkenntnisse im Umgang mit GIS-Software besitzen.

Dieses Tutorial wurde am Institut für Geodäsie der Fachhochschule Bochum in enger Zusammenarbeit mit der Universität Münster und der Universität Bochum entwickelt. Hauptautor ist Fabian Przybylak unter der Leitung von Prof. Dr. Carsten Keßler und in Zusammenarbeit mit Lucas Rudnik.

Du darfst das OER (H5P-Inhalte) unter den Bedingungen der CC-BY-SA 4.0-Lizenz frei verwenden, verändern und vervielfältigen. Jeglicher Code, der mit dem OER zur Verfügung gestellt wird, kann unter den Bedingungen der MIT-Lizenz verwendet werden. Bitte lesen Sie die [vollständigen Lizenzbedingungen](/LICENSE.md). 

Das Projekt OER4SDI wurde von der Digitalen Hochschule NRW empfohlen und wird durch das Ministerium für Kultur und Wissenschaft NRW gefördert. 

## 2. Thematischer Hintergrund

**Gliederung des thematischen Hintergrunds** 
* Kurze Einleitung mit allgemeinem Kontext und Hintergrund (in wenigen Sätzen) 
* Inhaltliche Vertiefung (Videoformat + Textakkordion welches die gegebenen Informationen zusammenfasst)


### 2.1 Kurze Einführung

**Worum geht es eigentlich?**
Die rasche Entwicklung von Methoden und Techniken zur Erfassung von Geodaten bietet die Möglichkeit, riesige Mengen von Geodaten zu sammeln. Sie stellt jedoch auch verschiedene Datenorganisationen und Datennutzer vor die Herausforderung, große Mengen von Geodaten zu verwalten, gemeinsam zu nutzen, zu verarbeiten und zu analysieren. Datenorganisationen stehen vor der Herausforderung, neue Lösungen für die Verwaltung, Speicherung und gemeinsame Archivierung dieser riesigen Datenmengen zu finden.

Ein Online-Dienst um geografische Informationen und räumliche Daten über das Internet bereit zu stellen sind Geospatial Web Services. Diese Dienste ermöglichen es Benutzern, geografische Daten effizient zu teilen, zu suchen, zu visualisieren, abzurufen und zu analysieren.

**Welches Problem besteht dabei?**
Datenverbreitungssysteme müssen sich immer mit einem Heterogenitätsproblem auseinandersetzen. Verschiedene Quellen können die Effektivität des Austauschs und der Verwaltung von Geodaten behindern. Verschiedene Betriebssysteme, Hardware, Software, Datenformate und Schnittstellen sind mit dem Problem der syntaktischen Heterogenität verbunden. Wenn zwei Webdienste die Schnittstellen des jeweils anderen nicht kennen, können sie keine Nachrichten und Daten austauschen.

**Welche Lösung gibt es dafür?**
Aus diesem Grund sind Geospatial Web Services in der Regel nach den vom Open Geospatial Consortium entwickelten OGC-Standards organisiert. Diese Standards ermöglichen, dass die Services interoperabel sind und von verschiedenen Anwendungen und Plattformen übergreifend verwendet werden können.

### 2.2 Inhaltliche Vertiefung (Video)

**Was sind Geospatial Webdienste?**
Geospatial Web Services sind eine Art von Webdiensten, die es ermöglichen, Geodaten und -dienste im Internet bereitzustellen, abzurufen und zu verarbeiten. Diese Dienste werden in der Regel von Geodaten- oder GIS-Organisationen, Regierungsbehörden, Unternehmen und anderen Einrichtungen bereitgestellt, die Geodaten verwalten.
![](Single_Learning_Element/Img/Slide1.png) 
**Wofür braucht man Geospatial Web Services?**
Durch die Verwendung von Geospatial Web Services können Benutzer auf Geodaten von verschiedenen Quellen zugreifen, umfassende Analysen durchführen und maßgeschneiderte Anwendungen und Visualisierungen erstellen.

**Wie sind GWS aufgebaut und gibt es vorherrschende Standards?**
Geospatial Web Services sind strukturiert, um geografische Daten und Funktionalitäten über das Web bereitzustellen. Sie basieren in der Regel auf einer Client-Server-Architektur, bei der der Client (in der Regel ein Webbrowser) eine Anfrage an den Server stellt und dieser daraufhin geografische Daten und Funktionalitäten zurückliefert.

Geospatial Web Services verwenden in der Regel eine oder mehrere standardisierte Schnittstellen, die von dem Open Geospatial Consortium (OGC) spezifiziert wurden. Die OGC-Schnittstellen definieren das Format und die Struktur der Daten, die vom Server zurückgegeben werden, sowie die Methoden und Parameter, mit denen die Daten abgefragt werden können.
![](Single_Learning_Element/Img/Slide2.png) 
**Was ist das OGC?**
Das OGC oder auch Open Geospatial Consortium ist eine gemeinnützige Organisation, die sich auf die Entwicklung von Standards für Geodaten und Geodienste konzentriert. Die Organisation wurde im Jahr 1994 gegründet und hat ihren Hauptsitz in den USA.

Das Ziel des OGC ist es, offene Standards für Geodaten und -dienste zu entwickeln und zu fördern, um die Interoperabilität und den Austausch von Geodaten und -diensten zwischen verschiedenen Systemen, Anwendungen und Organisationen zu erleichtern. Die OGC-Standards umfassen Protokolle für den Zugriff auf Geodaten (z.B. WMS, WFS, WCS), Datenmodellierung, Geoprocessing, Metadaten, Katalogisierung und vieles mehr.

Das OGC Consortium arbeitet eng mit anderen Standardisierungsorganisationen und Regierungsbehörden weltweit zusammen, um sicherzustellen, dass die Standards für Geodaten und -dienste in verschiedenen Anwendungsbereichen und in verschiedenen Ländern harmonisiert sind.

Die Mitgliedschaft im OGC steht Organisationen und Einzelpersonen aus der Geodaten- und Geodienstbranche offen und bietet ihnen die Möglichkeit, an der Entwicklung von Standards teilzunehmen und von der Zusammenarbeit mit anderen Fachleuten zu profitieren.
![](Single_Learning_Element/Img/Slide3.png) 
**Wie sehen die OGC-Architekturelemente und die wichtigsten OGC-Standards aus?**
Die OGC Web Services-Architektur besteht aus einer Reihe von Komponenten, die zusammenarbeiten, um die verschiedenen Arten von Geodaten-Webdiensten bereitzustellen. Die wichtigsten Komponenten sind:

* **Service Provider:** Dies ist der Server, der den Webdienst bereitstellt und auf Anfragen von Clients antwortet.
* **Service Requester:** Dies ist der Client, der den Webdienst anfordert und auf die Antwort vom Service Provider wartet.
* **Service Registry:** Dies ist ein Verzeichnis, das Informationen über verfügbare Geodaten-Webdienste enthält, damit Service Requester diese finden und verwenden können.
* **Service Broker:** Dies ist ein Vermittler, der die Interoperabilität zwischen verschiedenen Geodaten-Webdiensten ermöglicht, indem er Daten und Anfragen zwischen ihnen übersetzt.
![](Single_Learning_Element/Img/Slide4.png) 
Geospatial Web Services verwenden offene Standards und Protokolle, um den Austausch von Geodaten zwischen verschiedenen Systemen und Plattformen zu erleichtern. Zu den wichtigsten Standards gehören: 

* Web Map Service (**WMS**) 
* Web Feature Service (**WFS**)
* Web Coverage Service (**WCS**)
* Catalog Service (**CSW**)
* Sensor Observation Service (**SOS**)

**Was ist der Unterschied zwischen den verschiedenen Services?**
* Ein Web Map Service (**WMS**) ermöglicht es einem Client, statische Kartenbilder von einem Server abzurufen und anzuzeigen.
* Ein Web Feature Service (**WFS**) ermöglicht den Zugriff auf und die Abfrage von vektorbasierten Geodaten.
* Ein Web Coverage Service (**WCS**) ermöglicht den Zugriff auf und die Abfrage von räumlichen Rasterdaten wie Satellitenbildern oder Höhenmodellen.
* Ein Catalog Service (**CSW**) ermöglicht es einem Client, Metadaten über verfügbare Geodaten und -dienste zu suchen und abzurufen.
* Ein Sensor Observation Service (**SOS**) ermöglicht den Zugriff auf Echtzeitdaten von Sensoren, z.B. Umweltsensoren.
![](Single_Learning_Element/Img/Slide5.png) 
**Wie sieht eine typische Web-Anfrage für einen Web map Service aus?**
Das Web Map Service (WMS) Protokoll ist eine von dem Open Geospatial Consortium (OGC) definierte Schnittstelle, die es ermöglicht, Karten und geografische Daten über das Web abzufragen und zu visualisieren. Das WMS-Protokoll definiert das Format und die Struktur der Daten, die vom Server zurückgegeben werden, sowie die Methoden und Parameter, mit denen die Daten abgefragt werden können.

Das WMS-Protokoll verwendet HTTP oder HTTPS als Transportprotokoll. Eine typische WMS-Anfrage besteht aus einer URL, die verschiedene Parameter enthält, die den Inhalt der Karte bestimmen. Hier ist ein Beispiel einer WMS-Anfrage und der zugehörigen Parameter:
![](Single_Learning_Element/Img/Slide6.png) 
Der Server verarbeitet die Anfrage und sendet die Karte als Antwort im angeforderten Format zurück. Die Karte kann dann im Browser oder in einer Anwendung angezeigt werden.

**Welche weiteren Anfragen können an einen WMS-Server gestellt werden?**
Ein WMS-Protokoll definiert noch weitere Anfragen, die von einem Client an einen WMS-Server gesendet werden können.

* **GetCapabilities:** Mit dieser Anfrage kann der Client Informationen über die verfügbaren Layer und Funktionen des WMS-Servers abrufen. Die Antwort enthält eine XML-Datei, die die verfügbaren Layer, ihre Eigenschaften und Metadaten sowie die unterstützten Operationen und Formate enthält.
* **GetMap:** Mit dieser Anfrage kann der Client eine Karte vom Server abrufen. Die Parameter dieser Anfrage umfassen den gewünschten Ausschnitt der Karte, die Größe und das Format der Karte sowie die gewünschten Layer und Stile.
* **GetFeatureInfo:** Mit dieser Anfrage kann der Client Informationen über die Eigenschaften von Objekten in einem bestimmten Punkt auf der Karte abrufen. Die Antwort enthält eine XML-Datei oder ein anderes Format, das die Attribute und Werte der Objekte enthält.
* **DescribeLayer:** Mit dieser Anfrage kann der Client Informationen über die Eigenschaften und Metadaten eines bestimmten Layers abrufen. Die Antwort enthält eine XML-Datei oder ein anderes Format, das die Eigenschaften und Metadaten des Layers enthält.

Es gibt auch andere Anfragen wie **GetLegendGraphic** und **GetStyles**, die für bestimmte Anwendungsfälle nützlich sein können.
![](Single_Learning_Element/Img/Slide7.png) 
**Welche weiteren Anfragen können an einen WFS-Server gestellt werden?**
Ein Web Feature Service (WFS) Server verwendet andere Anfragen als ein Web Map Service (WMS) Server, da der WFS-Standard sich auf den Zugriff und die Abfrage von vektorbasierten Geodaten konzentriert, während der WMS-Standard die Visualisierung von Karten im Fokus hat.

* **GetCapabilities:** Mit dieser Anfrage kann der Client Informationen über die verfügbaren Layer und Funktionen des WFS-Servers abrufen. Die Antwort enthält eine XML-Datei, die die verfügbaren Layer, ihre Eigenschaften und Metadaten sowie die unterstützten Operationen und Formate enthält.
* **DescribeFeatureType:** Mit dieser Anfrage kann der Client die Struktur eines bestimmten Layers abrufen. Die Antwort enthält eine XML-Datei, die die Eigenschaften und Attribute des Layers definiert.
* **GetFeature:** Mit dieser Anfrage kann der Client vektorbasierte Geodaten aus einem oder mehreren Layern abrufen. Die Parameter dieser Anfrage umfassen den gewünschten Ausschnitt der Daten, die Attribute und Eigenschaften, die zurückgegeben werden sollen, und die Filterbedingungen, die auf die Daten angewendet werden sollen.
* **Transaction:** Mit dieser Anfrage kann der Client Änderungen an den Daten auf dem WFS-Server vornehmen. Die Operationen können Insert, Update oder Delete sein, und sie werden in einer XML-Datei definiert, die an den Server gesendet wird.

Es gibt ebenfalls noch andere Anfragen wie **LockFeature**, **GetPropertyValue** und **GetFeatureWithLock**.
![](Single_Learning_Element/Img/Slide8.png) 
**Was ist GeoServer?**
GeoServer wurde erstmals im Jahr 2001 von der Open Source Geospatial Foundation (OSGeo) ins Leben gerufen. Die Idee hinter GeoServer war, eine Open-Source-Software zu schaffen, die es Benutzern ermöglicht, Geodaten im Web zu verwalten und bereitzustellen.

Die ursprüngliche Version von GeoServer wurde von der australischen Regierungsbehörde Geoscience Australia entwickelt und als Open-Source-Software veröffentlicht. Im Laufe der Jahre wurde GeoServer von einer breiten Community von Entwicklern weiterentwickelt und verbessert, die neue Funktionen hinzufügten und die Leistung und Stabilität der Software verbesserten.

GeoServer hat seit seiner Gründung eine starke Unterstützung von der OSGeo-Community erfahren. Die OSGeo ist eine gemeinnützige Organisation, die sich der Förderung von Open-Source-Geodaten-Software widmet und GeoServer ist eines ihrer wichtigsten Projekte. GeoServer hat auch eine aktive Benutzer-Community und wird von vielen Regierungsbehörden, Unternehmen und gemeinnützigen Organisationen auf der ganzen Welt eingesetzt.

Heute ist GeoServer eine der beliebtesten Open-Source-Softwarelösungen für Geodatenmanagement und -bereitstellung im Web. Es ist bekannt für seine Flexibilität, Skalierbarkeit und Leistung und wird von einer wachsenden Anzahl von Entwicklern und Benutzern weltweit genutzt.
![](Single_Learning_Element/Img/Slide9.png) 
**Welche Funktionen hat GeoServer?**
GeoServer bietet eine Plattform für die Verwaltung und Veröffentlichung von Geodaten im Web, indem es Daten in verschiedenen Geodatenformaten (wie zum Beispiel Shapefiles, Geotiffs, PostGIS-Datenbanken) verarbeitet und sie als Webdienste (wie zum Beispiel WMS, WFS, WCS) bereitstellt.

Die Funktionen von GeoServer umfassen:

* **Datenmanagement:** GeoServer ermöglicht es Benutzern, Geodaten aus verschiedenen Quellen zu importieren und zu verwalten. Es unterstützt verschiedene Datenformate, einschließlich Vektor- und Rasterdaten, sowie Datenbanken wie PostGIS, Oracle und MySQL.
* **Datenverarbeitung:** GeoServer kann Daten transformieren und filtern, um sie in verschiedenen Formaten und Projektionen bereitzustellen. Es kann auch Daten aggregieren und Gruppierungen erstellen, um benutzerdefinierte Ansichten bereitzustellen.
* **Bereitstellung von Webdiensten:** GeoServer bietet eine breite Palette von Webdiensten, einschließlich Web Map Service (WMS), Web Feature Service (WFS) und Web Coverage Service (WCS). Diese Webdienste ermöglichen es Benutzern, Geodaten auf einfache Weise über das Internet zu visualisieren, zu analysieren und herunterzuladen.
* **Sicherheit:** GeoServer bietet eine robuste Sicherheitsinfrastruktur, die es Benutzern ermöglicht, den Zugriff auf Geodaten zu steuern. Es unterstützt Authentifizierung und Autorisierung, sowie HTTPS-Verschlüsselung für sichere Datenübertragung.
* **Skalierbarkeit:** GeoServer kann auf einer Vielzahl von Plattformen ausgeführt werden, einschließlich Desktop-Computern, Servern und Cloud-Infrastrukturen. Es ist auch in der Lage, hohe Lasten zu bewältigen und bietet eine hohe Verfügbarkeit und Leistung.

Insgesamt ist GeoServer eine leistungsstarke und vielseitige Plattform für die Verwaltung und Bereitstellung von Geodaten im Web. Die es Benutzern ermöglicht, Geodaten auf einfache Weise zu verwalten und zu teilen, was es zu einem wichtigen Werkzeug für Geodateninfrastrukturen macht.
![](Single_Learning_Element/Img/Slide10.png) 
## 3. Übungen und Leitfäden

**Aufbau der Übungen und Leitfäden** 
* Aufgabenstellung 
* Videoguide (Screencast)

### 3.1 Übung 1

**Benötigte Softwarekomponenten, die in dieser Übung verwendet werden:** 

**QGIS** ist eine freie und quelloffene, plattformübergreifende Desktop-Anwendung für geografische Informationssysteme (GIS), die das Anzeigen, Bearbeiten, Drucken und Analysieren von Geodaten unterstützt.

**Aufgabenstellung**

Stöbere einige Zeit auf den Webseiten der angehängten Linksammlung und prüfe welche Services auf den Webseiten angeboten werden. Achte zusätzlich darauf in welcher Form die Services bereitstehen (WMS, WFS, etc.).

* [Geodatenkatalog Deutschland](https://gdk.gdi-de.org/gdi-de/srv/ger/catalog.search#/home)
* [Geoportal Deutschland](https://www.geoportal.de/) 
* [Geodatenkatalog Schweiz](https://www.geocat.ch/geonetwork/srv/ger/catalog.search#/home)

Du hast nun einige Quellen kennengelernt über die du Geospatial Web Services finden kannst. Wähle im folgenden die nachfolgenden Services aus und implementiere diese in ein simples QGIS Projekt. Folge dazu gerne auch dem angehängten Videoguide. 

* [Farbige Basiskarte](https://basemap.de/dienste/wms_capabilities_web_raster.xml)
* [Deutsche Verwaltungsgrenze](https://sgx.geodatenzentrum.de/wfs_vg2500) 

Es kann vorkommen, dass Services vom Provider nicht mehr unterstützt werden oder Links nicht mehr aktuell sind. Falls ein Service mal nicht funktionieren sollte dann such dir auf den angegebenen Webseiten gerne andere Services für die Übung heraus und nutze diese nach dem gleichen Schema.

**Skript zum Videoguide**

**Webseiten mit potentiellen Services**

**Geodatenkatalog Deutschland**

Der Geodatenkatalog Deutschland präsentiert Geodaten des Bundesgebietes. Die Daten werden von verschiedenen Behörden und Organisationen bereitgestellt und von der Arbeitsgemeinschaft der Vermessungsverwaltungen der Länder der Bundesrepublik Deutschland (AdV) betreut. Grundsätzliches Ziel des Geodatenkatalogs ist es, den Zugang zu und die Verbreitung von Geodaten in Deutschland zu erleichtern und zu fördern.

Über die Suche oder die angebotenen Themenbereiche können viele verschiedene Dienste ausgewählt werden. Zentrale Themenbereiche sind Geobasisdaten mit topographischen Karten, digitalen Geländemodellen, Luft- und Satellitenbildern, Daten der Verwaltung, Daten zu Umwelt und Natur, Verkehr und Infrastruktur sowie baurelevante Geodaten.

Die Hauptfunktion der Website ist die Suche nach Geodaten, die Anzeige von Metadaten zu einzelnen Datensätzen und die Möglichkeit, Daten herunterzuladen. Der Katalog enthält auch Informationen über die Organisationen, die die Daten zur Verfügung stellen.

Die Daten jeder Karte können direkt im Browser geöffnet werden, um einen Überblick über die Karte zu erhalten. Die Datenbeschreibung einer Karte enthält eine kurze Zusammenfassung des Inhalts und die für die Verlinkung notwendigen URLs.

![](Single_Learning_Element/Img/Geodatenkatalog_Deutschland.png)



**Geoportal Deutschland**

Das Geoportal Deutschland bietet ebenfalls Geodaten von Deutschland an, allerdings sind diese Karten großflächiger und bereits aufbereitet und decken meist das gesamte Bundesgebiet ab.
Es wird vom Bundesamt für Kartographie und Geodäsie (BKG) betrieben und dient als Zugangspunkt zu Geodaten verschiedener Behörden und Organisationen.
Nutzerinnen und Nutzer können nach bestimmten Geodaten suchen, z.B. nach Orten, Themen, Datentypen und vielem mehr.

![](Single_Learning_Element/Img/Geoportal.png)

Das Geoportal ermöglicht die direkte Anzeige der Geodaten sowie die Interaktion und Bearbeitung der Karten. Über das Ausrufezeichensymbol ist es möglich, Informationen zu den Karten zu erhalten und die URL der Karte abzurufen.

![](Single_Learning_Element/Img/Geoportal_2.png)

Das Geoportal unterstützt somit den Zugriff auf Geodaten über verschiedene Standards und Protokolle wie WMS und WFS.



**Einbindung von einem WMS und WFS-Server in QGIS**

WMS von basemap.de ist eine [Farbige Basiskarte](https://basemap.de/dienste/wms_capabilities_web_raster.xml)

WFS vom Geodatenzentrum mit den [Deutschen Verwaltungsgrenzen](https://sgx.geodatenzentrum.de/wfs_vg2500)

**Anleitung zum Einbinden der Services in QGIS**

* Neues Projekt erstellen
* Open Street MAps installieren (falls nicht vorhanden)
* WMS- und WFS-Layer hinzufügen
	--> Linksklick auf "Layer" --> "Layer hinzufügen" --> "WMS/WMTS-Layer hinzufügen" oder "WFS-Layer hinzufügen" 
	--> den Button "Neu" anklicken und einen Namen für den Layer festlegen und die URL des Layers einfügen --> "OK" drücken und mit "Schließen" den Vorgang abschließen
Diesen Vorgang einmal für den WMS-Layer und einmal für den WFS-Layer durchführen.
* Im Browser zuerst bei "WMS Test" die Pfeile zum aufklappen drücken und "basemap.de Web Raster Farbe" in die Karte ziehen
  Danach bei "WFS Test" den Layer "Bundesland" in die Karte ziehen
* In das Fenster Layer wechseln und mit einem Rechtsklick auf den Layer "Bundesland" und einem weiteren auf "Attributtabelle" lassen sich Eigenschaften des WFS-Layers anzeigen --> über einen Klick auf "Eigenschaften" können Veränderungen in dem Layer vorgenommen werden, wie zum Beispiel an der Symbolisierung des Layers

![](Single_Learning_Element/Img/QGIS/QGIS_Anleitung.png)

**Unterschiede zwischen WMS- und WFS-Layern**

* WMS-Layer sind nur für die Darstellung von statischen Kartenbildern da
* WFS-Layer sind in der Lage aktualisierte Daten bereit- und darzustellen, zudem ist es möglich Veränderungen in der Darstellung des Layers vorzunehmen


Zusammenfassend lässt sich sagen, dass die Verwendung von WMS- und WFS-Services in QGIS eine leistungsstarke Möglichkeit bietet, Geodaten anzuzeigen, zu analysieren und zu modifizieren. Ein WMS-Service ermöglicht eine schnelle und einfache Darstellung von Karten, während ein WFS-Service detaillierte Informationen über Geodaten liefert, die bearbeitet und analysiert werden können, um neue Erkenntnisse zu gewinnen.



### 3.2 Übung 2
**Benötigte Softwarekomponenten, die in dieser Übung verwendet werden:** 

**Docker** ist eine Open-Source-Plattform, die es Entwicklern ermöglicht, Anwendungen in Containern zu erstellen, zu verteilen und auszuführen, indem sie die Isolation und Portabilität von Containern nutzt.

**GeoServer** ist ein in Java geschriebener Open-Source-Server, der es Benutzern ermöglicht, Geodaten gemeinsam zu nutzen, zu verarbeiten und zu bearbeiten.

**QGIS** ist eine freie und quelloffene, plattformübergreifende Desktop-Anwendung für geografische Informationssysteme (GIS), die das Anzeigen, Bearbeiten, Drucken und Analysieren von Geodaten unterstützt.

**Aufgabenstellung**

Folge dem Screencast und erstelle selbst einen WMS- und einen WFS-Service, den du Local auf deinem System hosten kannst. Prüfe anschließend in QGIS ob du erfolgreich warst,  indem du die Services in ein neues QGIS-Projekt einbindest. 

Stelle sicher, dass du Docker Desktop bereits auf deinem System installiert hast und dich mit dem Programm etwas vertraut gemacht hast. Folge anschließend den ersten Schritten im Video um GeoServer über Docker zu installieren und zu starten. 

Falls du dich noch tiefer mit dem Thema beschäftigen willst, dann findest du weitere Tutorials in der [offiziellen Dokumentation](https://docs.geoserver.org/) von GeoServer. 

**Skript zum Videoguide**
**Erstellen von WMS- und WFS-Services in Docker**

Zuerst muss die Docker Desktop Anwendung installiert werden. Sobald die Software von docker.com erfolgreich installiert wurde und die Desktop-Version gestartet werden kann, kann mit der Erstellung des GeoServers begonnen werden.

Zuerst muss GeoServer über Docker gestartet werden, indem der Befehl

```shell
docker pull docker.osgeo.org/geoserver:2.22.0
```

in die Kommandozeile des Computers eingegeben wird, z.B. cmd für Windows-Systeme. Wenn dieser Vorgang abgeschlossen ist, kann der Befehl 


```shell
docker run -it -p 8080:8080 docker.osgeo.org/geoserver:2.22.0
```

eingegeben werden, um GeoServer auszuführen. Dieser Befehl startet GeoServer innerhalb eines Docker-Containers, in diesem Fall auf dem Port „8080“. Sollte dieser Port bereits belegt sein, kann die Nummer einfach geändert werden.

Als nächstes wird die Seite http://localhost:8080/geoserver im Webbrowser geöffnet, um auf die Startseite des GeoServers zu gelangen. Um vollen Zugriff auf die Seite des GeoServers zu erhalten, muss man sich auf der Seite mit den Zugangsdaten „admin“ und dem Passwort „geoserver“ anmelden. Nun siehst du die Startseite des GeoServer Web Interface.

Einen Überblick über das Interface erhalten

* Arbeitsbereiche --> Container für Ressourcen, wie Layer, Stile und Datenspeicher --> wird benutzt um verschiedene Projekte innerhalb einer Geoserverinstallation zu organisieren

* Datenspeicher --> Schnittstelle zu einer bestimmten Art von Geodatenquelle

* Layer --> Repräsentiert einen bestimmten Geodatensatz der über Webservices abgerufen werden kann

* Stile --> beschreiben die Darstellung in dem die passenden Symbolisierungen den einzelnen Layern zugeordnet werden

Die von GeoServer voreingestellten Arbeitsbereiche sind für diese Übung nicht von Interesse, da es sich um Beispielsätze handelt. Diese können zur besseren Übersicht gelöscht werden. Das Löschen eines Arbeitsbereiches löscht direkt alle damit verbundenen Layer und Datenspeicher, nur die Stile bleiben erhalten.

Nach erfolgreichem Löschen kann ein neuer Arbeitsbereich angelegt werden. Dazu klickt man auf „Neuen Arbeitsbereich anlegen“ und gibt diesem einen Namen und eine URI. In diesem Fall „New York“ Undals URI http://www.NewYork.com. Diese URI kann fiktiv sein, muss aber der Schreibweise einer Webadresse entsprechen.

Wenn dieser Arbeitsbereich gespeichert ist, wird er angeklickt und anschließend müssen im Bereich Services die Kontrollkästchen „WFS“ und „WMS“ aktiviert werden.

Danach wird ein neuer Datenspeicher im Bereich Datenspeicher hinzugefügt. Hier werden Verknüpfungen für die Datentypen erstellt, damit GeoServer auf die Quellen zugreifen kann. In diesem Beispiel arbeiten wir nur mit Shapefiles und klicken auf „Directory of spatial files (shapefiles)“, um alle Shapefiles in einem Ordner zu verknüpfen. Der Arbeitsbereich New York wird ausgewählt und der Name der Datenquelle auf „Citydata“ gesetzt. Bei den Verknüpfungsparametern wird über „Durchsuchen“ --> data/ --> nyc/ der Ordner mit den bereitgestellten Datensätzen verknüpft. Mit „Speichern“ werden die neuen Layer angezeigt.

In diesem Fenster können verschiedene Datensätze eingesehen und publiziert werden. In unserem Fall wird der Layer „poly_Landworks“ publiziert. Im neuen Fenster geben wir dem Layer den Namen „Manhattan_Landmarks“. Danach muss das Koordinatenreferenzsystem korrekt eingestellt werden und das Begrenzungsrechteck berechnet werden, indem auf „Aus den Daten berechnen“ und „Aus den nativen Grenzen berechnen“ geklickt wird. Anschließend muss gespeichert werden.

In der Layer-Vorschau kann über „Open Layers“ der veröffentlichte Layer angezeigt werden. Da dieser noch einfarbig ist und keine Unterschiede erkennen lässt, können dem Layer entsprechende Stile hinzugefügt werden.

Im Bereich Stile kann entweder ein eigener Stil erstellt oder ein bereits erstellter Stil verwendet werden. Wir verwenden den bereits angelegten Stil „polylandmarks“ und navigieren auf den Reiter Publishing und klicken das Kästchen „Default“ an und speichern. Nun hat sich in der Layer-Vorschau schon einiges getan. Um den Layer zu vervollständigen, müssen noch der Punktdatensatz „poi“ und der Liniendatensatz „tiger_roads“ wie zuvor der Stil publiziert werden. Die entsprechenden Symbolisierungen in den Stilen sind „poi“ und „simple_roads“.

Nachdem diese Schritte durchgeführt wurden, sind eigene Dienste erfolgreich erstellt worden. Diese können nun in QGIS integriert werden. Dazu sind die gleichen Schritte wie in Übung 1 notwendig. Die URL findet man, indem man auf das GeoServer-Logo klickt, wodurch man wieder auf die Startseite gelangt. Über „WMS 1.3.0“ gelangt man zu den WMS-Layern und über „WFS 2.0.0“ zu den WFS-Layern.

Nach der Integration der Layer in QGIS ist die Übung erfolgreich abgeschlossen.

## 4. Quiz

**Fragen**

* Welche Anfragen können an einen WMS-Server gestellt werden?

* Wofür steht die Abkürzung "OGC"?

* Was sind Geospatial Web Services?

* Welcher Service ermöglicht den Zugriff, sowie die Abfrage von vektorbasierten Geodaten?

* Welche vier Komponenten in der OGC Web Service-Architektur sind die wichtigsten?

* Wann und wo wurde das Open Geospacial Consortium (OGC) gegründet?

* Von wem wurde GeoServer über die Jahre weiterentwickelt?

* Welche Funktionen hat Geoserver?

* Zwei Zuordnungsfragen zu WMS-Server Anfragen und WFS-Server Anfragen


## 5. Zusammenfassung

Hey! Das hast du gut gemacht! Wir hoffen, dass du nun eine Vorstellung davon hast, wie du mit Geospatial Web Services wie WMS und WMF Services in deinem GIS arbeiten und wie du deine eigenen Web Services über Geoserver einrichten kannst.  


**Interessiert daran, mehr zu lernen?**

Im Internet findest du eine Fülle von Ressourcen zu Geospatial Web Services. Hier sind einige Empfehlungen: 

* [Zhao, P., & Di, L. (Eds.). (2010). Geospatial Web Services: Advances in information interoperability: Fortschritte bei der Interoperabilität von Informationen. IGI Global.](https://www.igi-global.com/book/geospatial-web-services/46010) 
* [Kralidis, A. T. (2007). Geospatial Web Services (Geodaten-Webdienste): The evolution of geospatial data infrastructure. In The Geospatial Web (S. 223-228). Springer, London.](https://link.springer.com/chapter/10.1007/978-1-84628-827-2_22) 
* [van den Brink, L., Barnaghi, P., Tandy, J., Atemezing, G., Atkinson, R., Cochrane, B., ... & Janowicz, K. (2019). Best Practices für die Veröffentlichung, Abfrage und Nutzung von Geodaten im Web. Semantic Web, 10(1), 95-114.](https://content.iospress.com/articles/semantic-web/sw305)
* [Clabby, J. (2003). Webdienste erklärt: Lösungen und Anwendungen für die reale Welt. Prentice Hall Professional.](https://books.google.be/books?hl=nl&lr=&id=AKkFqV9-_9AC&oi=fnd&pg=PR13&dq=%22fundamentals+of+web+services%22&ots=PL1iLMeHGW&sig=H9XAty66RX8LFIKAo9-VmOOEZDA#v=onepage&q=%22fundamentals%20of%20web%20services%22&f=false)
* [Link zu einer Seite oder einer Vorlesung, die OGC WMS in einer einfachen Sprache beschreibt](https://www.ogc.org/standards/wms/introduction) 
* [Link zu einer Seite oder einer Vorlesung, die OGC WFS in einfacher Sprache beschreibt](http://opengeospatial.github.io/e-learning/wfs/text/basic-main.html)
* [Link zu Geospatial Web Services](https://gis4schools.readthedocs.io/en/latest/part2/2_1.html)


**Dein Feedback ist willkommen!**

Wenn du Defizite in diesem OER-Modul festgestellt hast oder Ideen zur Verbesserung des OER-Materials hast, bist du herzlich eingeladen, Einträge in die Issue-Liste im [Github repository dieses OERs](https://github.com/oer4sdi/Geospatial-Web-Services).
