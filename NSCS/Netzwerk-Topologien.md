Unter einer Netzwerktopologie versteht man die Anordnung, wie die einzelnen Knoten (*nodes*) miteinander durch Leitungen (*links*) verbunden sind.
- Unter den Knoten versteht man die Kommunikationsteilnehmer im Netzwerk. Dies können z.B. Computer, Notebooks, Sensoren, Netzwerkelemente, etc. sein.
- Die Wahl der Topologie beeinflusst
	- Verkabelungsaufwand
	- Robustheit (Redundanz vs. single-point of failure)
	- Komplexität
	- Echtzeitfähigkeit

## Punkt-zu-Punkt (Point-to-Point)
![[Pasted image 20230926140250.png]]
- Einfache, direkte Kommunikation zwischen Gesprächspartner
- Vorhersagbare, nutzbare Übertragungsrate
- Übertragungsrate muss nicht zwischen Teilnehmern geteilt werden
- Bei Ausfall des Links keine Übertragung möglich
- Beispiele
	- Internetzugänge über Telefonleitungen: Digital Subscriber Line (*DSL*), *last mile*
	- Richtfunkstrecken zur Anbindung entfernter Gebiete
## Bus
![[Pasted image 20230926140727.png]]
- Alle Knoten sind an ein gemeinsames Buskabel angeschlossen
- Geringerer Verkabelungsaufwand
- Es kann immer nur ein Knoten senden
	- Aufwändige Verfahren für den Zugriff auf den Bus, z.B. **Carrier Sense** / Multiple Access / **Collision Detection**
	- Bei hohem Nachrichtenaufkommen sinkt Gesamt-Übertragungsrate
- Beispiele
	- Frühe Varianten des Ethernet Standards Link
	- CAN-Bus in Fahrzeugen
	- Installationsbusse für Gebäude wie KNX, "Bticino"
- **Carrier Sense:** warten bis niemand überträgt
- **Collision Detection** --> Stoppen der Übertragung bei Datenkollision
	- Zufällige Wartezeiten dann
	- Neuer Übertragungsversuch
## Ring
![[Pasted image 20231003133557.png]]
- Weiterentwicklung des Bussystems
	- Jeder Knoten ist mit zwei Nachbarknoten verbunden
	- Ausfall einer Verbindung kann kompensiert werden
	- Nicht mehr häufig in Verwendung
- Zugriff über Token (Staffelholz) realisiert
	- Jener Knoten, der an der Reihe ist, darf senden
	- Token wird im Kreis weitergereicht
- Beispiele: IBM Token Ring
## Stern (Star)
![[Pasted image 20231003134833.png]]
- Kommunikation über zentralen Knoten
	- Ausfall eines Links beeinträchtigt nur einen Knoten
	- zentraler Knoten als *Single Point of Failure*
	- Erlaubt konzeptionell paarweise Kommunikation, dadurch höhere Gesamt-Datenrate
	- höherer Verkabelungsaufwand
- Sonderform bei drahtlosen Netzwerken - Zelle (*cell*)
	- Teilnehmer kommunizieren über Basisstation, *access point* etc.
## Vermaschtes Netz (Mesh)
![[Pasted image 20231003135228.png]]
- Entfall einer zentralen Komponente
	- Knoten sind über Links mit mehreren anderen Knoten verbunden
	- Erhöhte Ausfallsicherheit
	- Knoten leiten Daten für andere Knoten weiter
	- Größere Komplexität