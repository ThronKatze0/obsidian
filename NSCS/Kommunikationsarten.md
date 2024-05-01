---
id: Kommunikationsarten
aliases: []
tags: []
---

- Simplex - Kommunikation nur in eine Richtung
- Duplex (Halb-Duplex) - Kommunikation in beide Richtungen - aber nicht gleichzeitig
- Voll-Duplex - Kommunikation in beiden Richtungen gleichzeitig möglich

## Standardisierung

- Alle Teilnehmer in einem Netzwerk müssen dieselbe Sprache sprechen und sich auch an die Kommunikationsregeln halten.
- Standardisierung findet auf unterschiedlichsten Ebenen statt und umfasst u.a.
  - Kabel und Steckerverbindungen
  - Physikalische Größen wie Spannungen, Frequenzen
  - Adressierungsschema
    - MAC-Adresse: 00:00:00:00:00:00 => 48 Bit
      - HW-Spezifisch
      - Erste drei Bits geben den Hersteller an
  - Vergabe von Adressen und eindeutigen Namen
  - Aufbau von ausgetauschten Nachrichten
  - Darstellung von einzelnen Zeichen (Emojis, Umlaute), Sprache, Video

### ISO - Internationale Organisation für Normung

- International Organization for Standardization
- Beispiele
  - Strukturierte Verkabelung - ISO/IEC 11801
  - Standard-Reihe zur Informationssicherheit ISO/IEC 27000

### ITU- International Telecommunication Union (ITU)

- Internationale Fernmeldeunion
- Codecs = Coder + Decoder
- Beispiele
  - Audio-Codecs wie ITU-T G.711 (z.B. MP3, AAC)
  - xDSL Technologien wie ITU-T G.993.2
  - Video-Codecs wie H.264, H.265

### IEEE - Institute of Electrical and Electronics Engineers

- Fokus auf elektronische Standards
- Beispiele
  - WLAN - IEEE 802.11
  - Bluetooth - IEEE 802.15.1
  - Ethernet - IEEE 802.3

### IETF - Internet Engineering Task Force

- Internet-Protokolle
- Beispiele
  - IPv4 - RFC 791
  - HTTP - RFC 1945

### World-Wide-Web Consortium

- Organisation, die sich mit der Entwicklung im WWW befasst
- Beispiele
  - HTML
  - XML
  - PNG, SVG

## Leitungs- vs. Paketvermittlung

- Netzwerke können Kommunikation über zwei Grundlegende Arten anbieten
  - Leitungsvermittlung
    - Vor der eigentlichen Kommunikation wird von den Kommunikationspartnern eine Verbindung aufgebaut
    - Diese Verbindung (Leitung) wird exklusiv genutzt
    - Netzwerk reserviert entsprechende Ressourcen (Anteile der Übertragungskapazität einer Leitung)
  - Paketvermittlung
    - Die Daten der Kommunikationspartner werden in Pakete aufgeteilt
    - Die Pakete enthalten Informationen über Absender und Empfänger
    - Die Knoten im Netzwerk beschränken sich auf das Weiterleiten von Paketen zum Empfänger
    - Das Netzwerk kann meist nicht garantieren, dass die Pakete zugestellt werden (_best effort_)
    - Pakete können in unterschiedlicher Reihenfolge am Empfänger ankommen
    - Sender und Empfänger werden oft auch als Quelle (_source_) und Ziel (_destination_) bezeichnet
    - Netzwerk kann mehr Teilnehmer unterstützen, da statistisch gesehen nicht immer alle gleichzeitig senden

#### Addressierung von Paketen

- **Unicast:** Paket an **einen Empfänger**
- **Multicast**: Paket an **mehrere Empfänger**
- **Broadcast:** Paket an **alle Empfänger**
- **Anycast**: Paket an **einen beliebigen Empfänger** einer Gruppe

