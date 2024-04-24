- komplette Funktionalität einer Netzwerkanwendung in Schichten (*layer*) aufgeteilt
- Jede Schicht hat ihre spezielle Aufgabe und bietet ihre Dienste der darüberliegenden bzw. darunterliegenden Schicht an.
- Schichten erlauben Austauschbarkeit von Funktionalität/Technologien
## Netzwerkprotokolle
- Ein Protokoll ist eine Art Vereinbarung zwischen Kommunikationspartnern und definiert
	- wie die ausgetauschten Nachrichten aufgebaut sind
	- das (zeitliche) Verhalten der Kommunikationspartner
### Internet Protocol Suite
- im Deutschen auch Internetprotokollfamilie bzw. TCP/IP Modell
- definiert von der IETF im RFC 1122 aus dem Jahr **1989**
- besteht aus vier Schichten
	- **Application Layer**
	- **Transport Layer**
	- **Internet Layer**
	- **Link Layer**
#### Application Layer
- Dienste und Applikationen wie Webbrowsing, Mail, Voice over IP
- Werden durch Prozesse / Applikationen auf einzelnen Rechnern implementiert
- Bekannte Vertreter
	- Hypertext Transfer Protocol (HTTP)
	- Simple Mail Transfer Protocol (SMTP)
	- Domain Name Service (DNS)
#### Transport Layer
- Sorgt für die Kommunikation zwischen den Prozessen / Applikationen
- Bieten Funktionalität wie zuverlässige Übertragung, Flow Control
- Bekannte Vertreter
	- TCP (Transmission Control Protocol)
	- UDP (User Datagram Protocol)
#### Internet Layer
- Ermöglicht globale Konnektivität mittels Paketvermittlung
- Adressierungsschema für Rechner im weltweiten Netz
- Internet Protocol (IP) Version 4 bzw. 6 (IPv4/IPv6)
#### Link Layer
- Eigentliche, physische Übertragung von Daten
- Übertrangungsmedien
- Signaldarstellung
- Codierung
- Medienzugriff
- Fehlererkennung / Fehlerkorrektur
### ISO / OSI Modell
- Open Systems Interconnection Referenzmodell
- standardisiert von der ISO im Jahr 1984
- Please Do Not Throw Salami Pizza Away
- sieben Schichten (*layer*)
	- **Application**
	- **Presentation**
	- **Session**
	- **Transport**
	- **Network**
	- **Data Link**
	- **Physical**

| Internet Protocol Suite | ISO / OSI Modell |
| ----------------------- | ---------------- |
|                         | Application      |
| Application             | Presentation     |
|                         | Session          |
| Transport               | Transport        |
| Internet                | Network          |
| Link-                   | Data Link        |
| Layer                   | Physical         |
### Bitübertragungsschicht
- Definiert wie einzelne Bits mit Hilfe von physikalischen Größen ausgetauscht werden.
- Typische Festlegungen
	- Wahl des physischen Übertragungsmedium
	- Aufbau von Steckern, Kabeln, Buchsen
	- Antennen und Frequenzen
	- Darstellung der Bits durch physikalische Größen
- Beispiel UART - Serielle Schnittstelle des Raspberry Pi
- Fragestellungen:
	- Welche Pins werden benötigt und wie werden diese verbunden?
	- Wie viel Volt ist eine logische 1 bzw. eine logisch 0?
	- Wie lange dauert ein einzelnes Bit?
	- Wie wird der Beginn der Übertragung signalisiert?
- Übertragungsmöglichkeiten:
	- elektrische Signale
		- POTS (pretty old telephone system)
			- Modems ca. 56 kbps Ende der 90er
			- DSL -> 1-100 Mbps
				- ADSL
				- VDSL
	- optische Signale
		- Lichtwellenleiter (aka Glasfaser)
		- Infrarot
	- elektromagnetische Wellen
		- Funk
		- Schall
- Übertragungsmedien
	- Drahtweg / Kabel
		- Vorteile
			- Einfache Technik
			- Günstig in Herstellung
		- Nachteile
			- Eingeschränkte Reichweite
			- Empfindlich auf äußere Störeinflüsse
	- Funkweg
		- Vorteile
			- Überbrückung hoher Distanzen
			- Erreichbarkeit entfernter Gebiete
			- Komfort
		- Nachteile
			- Empfindlich hinsichtlich Störung
			- Abhörsicherheit
			- Geringe Datenraten
	- Lichtwellenleiter
		- Vorteile
			- Hohe Distanzen und Datenraten möglich
			- Unempfindlich hinsichtlich äußeren Störungen
			- Weniger Platzbedarf und Gewicht
		- Nachteile
			- Teure Gerätetechnik
			- Aufwändigere Anschlusstechnik
			- Mechanisch empfindlich