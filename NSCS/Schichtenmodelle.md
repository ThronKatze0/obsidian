---
id: Schichtenmodelle
aliases: []
tags: []
---

- komplette Funktionalität einer Netzwerkanwendung in Schichten (_layer_) aufgeteilt
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
- sieben Schichten (_layer_)
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

### Ethernet

- De-facto Standard für LAN Anwendungen
- Entwicklung reicht bis in die 1970er Jahre zurück
- Standards aus der 802.3 IEEE Arbeitsgruppe
- Ethernet ist eine Link Layer Technologie im TCP/IP Modell
- Data link layer (L2) und Physical layer (1)

#### Ethernet - Data link layer

- Übertragung der Daten erfolgt in Framse
  ![[ethernet-frame.jpg]]
- Ankündigung der Übertragung mit Bitfolge 1010101...
- Empfänger (Destination) und Absender (Source) werden über Adressen identifiziert (MAC Adresse, phys. Adresse)
- Adressen werden vom Hersteller vergeben
- Nutzdaten typischerweise bis zu 1500 Bytes
- Interpretation der Nutzdaten abhängig von Type Feld
- Fehlererkennung über Frame Check Squence (FCS) - 32-Bit Prüfsumme (fehlerhafte Frames werden verworfen)

#### Ethernet - MAC-Adressen

- Identifizieren Absender und Empfänger
- 48-Bit Adressen, hexadezimale Schreibweise
- DC:A6:32:85:E6:FE bzw. DC-A6-32-85-E6-FE
- Vordere Bits identifizieren Hersteller (Registry)
- Ab Werk vom Hersteller gesetzt, keinse Konfiguration erforderlich
- Spezielle Adresse FF:FF:FF:FF:FF:FF für Broadcast im Netzwerks

#### Ethernet - Physical Layer

- Verwendete Topologien
  - Ursprünglich Bus
  - Mittlerweile Stern bzw. Point to Point
- Ethernet unterstützt unterschiedliche Kabel/Technologien
  - Koaxialkabel (z.B. 1000BASE-T), 10 Base -> 10Mbps
  - Twisted-Pair-Kabel (z.B. 1000Base-t)
  - Single-Mode Glasfaser (eine Wellenlänge, 1000BASE-LS)
  - Multi-Mode Glasfaser (mehrere Wellenlängen, 1000BASE-SX)
- Basis bildet meist eine strukturierte Verkabelung

#### Strukturierte Verkabelung

- Konzept für die Verkabelung mit anwendungsneutralen Kommunikationskabeln in und zwischen Gebäuden
- Anwendungsneutral bedeutet, die Verkabelung kann für unterschiedliche Zwecke wie Rechnernetze, Telefonie etc. verwendet werden
- Europäische Norm CENELEC - EN 50173 und EN 50174
- International ISO/IEC 11801
- Definieren unter anderem Kabeltypen - Category 5, 5e, 6, 7, etc.

#### Ethernet - Horizontale Verkabelung

- Sternförmige Verkabelung mit Switch als zentralen Punkt
- Geräte werden mittels Patchkabel an Anschlussdose angeschlossen
- Fixes Verlegekabel zwischen Anschlussdose und Patchpanel

#### Patch Kabel Aufdruck Informationen

- Kabeltyp
- Länge
- Hersteller
- Zertifizierung

### Switches

- Verteilt Ethernet Frames im lokalen Netzwerk
- Wertet Ethernet Header aus - insbesondere Destination Address
- Arbeitet auf ISO/OSI Layer 2
- Unterschiedliche Bauformen
  - Anzahl von RJ-45 (Registered Jack) Ports
  - Small Form-Factor Pluggable (SFP) Ports für Glasfaserverbindungen
  - Desktop oder 19" Rack Montage

#### Funktionsweise von Switches

- Switch verwaltet eine interne Tabelle mit Mappings von MAC Adresse auf bestimmten Ports
- Switch lernt laufend die Einträge der Tabelle
  - Ausgenommen Switch empfängt Frame auf Port 3
  - Switch entnimmt die Quell-Adresse 00:15:5d:45:f7:2d aus dem Ethernet Header
  - Speichert neuen Eintrag 00:15:5d:45:f7:2d -> Port 3
- Weiterleitung basierend auf Ziel-Adresse
  - Gibt es einen Eintrag für die MAC Adresse
  - Wenn ja, dann Weiterleitung über Ports aus Tabelle
- Verhinderung von Schleifen mit Hilfe des Spanning Tree Protokolls

  13.5.2.7 -> Dotted Decimal notation

  143.205.0.0/16
  Netz-Id Host-Id
  16 (Bedeutung) -> 16 Bit für Netz-Id, 16 Bit für Host-Id
