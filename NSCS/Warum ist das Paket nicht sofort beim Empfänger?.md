![[metrics-delaycomps.png]]
## Zeitliche Komponenten
- Bei der eigentlichen Übertragung wird das Paket typischerweise Bit für Bit hintereinander übertragen - es wird serialisiert. Die Dauer ist abhängig von der Paketgröße und der Datenrate der Verbindung. 
- Die Übertragungsverzögerung wird auch *transmission delay* oder *serialization delay* genannt.
$$
Übertragungsverzögerung [s] = \frac{Datenmenge[bit]}{Übertrangungsrate[bit/s]}
$$
- Die Übertragung eines einzelnen Bits/Symbole über das Medium wie Kabel, Funk etc. vom Sender zum Empfänger dauert eine gewisse Zeit. Diese wird als Ausbreitungsverzögerung oder auch *propagation delay* bezeichnet.
$$
Ausbreitungsverzögerung[s] = \frac{Distanz[m]}{Ausbreitungsgeschwindigkeit[m/s]}
$$
### HÜ: Ausbreitungsverzögerung
$$
\frac{300}{300 * 10^6} = \frac{1}{10^6} Sekunden
$$
$$
\frac{1000 * 10^3}{200 * 10^6} = \frac{5}{10^3} = \frac{1}{200} Sekunden
$$
$$
\frac{36000 * 10^3}{300 * 10^6} = \frac{120}{10^3} = \frac{12}{100} Sekunden
$$
$$
\frac{371 * 10^9}{300 * 10^6} = 71 * 10^3 Sekunden
$$
### Bsp.
$$
\frac{100}{2\times10^8} = \frac{1}{2\times10^6} = \frac{1}{2}\times10^{-6} s
$$
$$
\frac{1500 \times 8}{10^9} = \frac{1,5\times8}{10^6} = \frac{12}{10^6}s
$$
