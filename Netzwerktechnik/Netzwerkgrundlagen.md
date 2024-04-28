
Ein Netzwerk ist eine Verbindung mehrerer Computer zum Zweck des Datenaustauschs, für verteilte Anwendungen oder auch für die Kommunikation zwischen ihren Benutzer*innen. Grundlagen der Vernetzung sind dabei: 
- Computer muss nicht direkt mit demjenigen Verbunden sein, mit dem er Daten austauschen soll. 
- Ausfall oder Überlastung eines bestimmten Verbindungswegs kann durch Alternativen kompensiert werden. 
## Funktionsebenen
Für alle Schichtenmodelle gilt folgendes: 

Die Daten, die über einen Kommunikationskanal übertragen werden sollen, werden auf der Seite des Senders zunächts Schicht für Schicht nach unten weitergeleitet und jeweils mit den spezifischen Zusatzinformationen für diese Schicht versehen. Schließlich werden si über die unterste Schicht, die eigentliche physikalische Verbindung, übertragen. Auf der Empfängerseite werden sie dann wieder schichtweise nach oben weitergeleitet. Jede Schicht ermittelt die für sie bestimmten Informationen und regelt die Weiterleitung an die nächsthöhere Schicht. 

### OSI-Referenzmodell
Um die Ebenen eines Netzwerks auseinanderhalten zu können, bedient man sich sogenannter Schichtenmodelle. Das bekannteste ist dabei das OSI(Open Systems Interconnect)-Referenzmodell von der ISO. Es besteht aus 7 Schichten:

1. Bit-Übertragungsschicht → Physical Layer
2. Sicherungsschicht → Data Layer
3. Vermittlungsschicht → Network Layer
4. Transportschicht → Transport Layer
5. Sitzungsschicht → Session Layer
6. Darstellungsschicht → Presentation Layer
7. Anwendungsschicht → Application Layer

#### 1. Bit-Übertragungsschicht
 - beschreibt wie die Übertragung von Daten elektrisch bzw. physikalisch erfolgt. OSI-basierte Netzwerkstandards beschreiben hier die Struktur der Signale. 
 - Kabel, Lichtwellenleiter, Funk oder Ähnliches
#### 2. Sicherungsschicht
 - beschreibt Vorkehrungen, die dafür sorgen, dass aus den einzelnen zu übertragenden Bits, ein verlässlicher Datenfluss wird. 
 - dazu gehört die Media Access Control MAC, wenn mehrere Geräte denselben Kanal verwenden, sowie Logical Link Control LLC, bei der es um die Herstellung und Aufrechterhaltung von Verbindungen zwischen den Geräten geht. 
 - Viele Protokolle implementieren auf dieser Schicht eine Fehlerkontrolle
 - Protokolle: Ethernet, Token Ring
#### 3. Netzwerkschicht
 - definiert diejenigen Komponenten und Protokolle des Netzwerks, die an der indirekten Verbindung von Computern beteiligt sind. 
 -  hier ist Routing erforderlich
 - IP-Protokoll 
#### 4. Transportschicht
 - Multiplexmechanismen, die die Anbindung der Datenpakete an konkrete Prozesse auf den kommunizierenden Rechnern ermöglicht (Ports)
 - Verbindungslose Protokolle wie UDP
 - Verbindungsorientierte Protokolle wie TCP (Gewährleistung das Pakete vollständig am Ziel ankommen)
#### 5. Sicherungsschicht
 - stellt kontinuierliche Kommunikation zwischen kooperierenden Anwendungen oder Prozessen zwischen verschiedenen Rechnern sicher
- Tokens und Protokolle
#### 6. Darstellungsschicht
- Konvertierung und Übertragung von Datenformaten, Zeichensätzen, grafischen Anweisungen und Dateidiensten → ASCII, Unicode etc. 
#### 7. Anwendungsschicht
- unmittelbare Kommunikation zwischen den Benutzeroberflächen der Anwendungsprogramme
### Schichtenmodell der Internetprotokolle
Im Bereich der TCP/IP Netzwerkprotokolle, wir häufig ein Modell aus nur vier Schichten verwendet (nach DDN):
1. Netzzugangsschicht → Network Access Layer oder Link Layer 
2. Internetschicht → Internet Layer
3. Host-zu-Host-Transportschicht → Transport Layer
4. Anwendungsschicht → Application Layer
#### Netzzugangsschicht
- beschreibt die physikalische Datenübertragung. 
- viele unterschiedliche Protokolle
#### Internetschicht
- logische Adressierung der Rechner im Netz, durch die die grundsätzliche Identifizierbarkeit des jeweiligen Rechners sichergestellt wird. 
- Routing, Weiterleitung von Daten über verschiedene physikalisch und/oder logisch getrennte Netze hinweg
- IP-Protokoll, welches die IP-Adressen definiert. Außerdem weißt es jedem Datenpaket einen Header zu, mit Quell- und Zieladresse. 
- ein Datenpaket dieser Ebene wird als Datagramm bezeichnet. 
#### Host-zu-Host-Transportschicht
- Host bezeichnet jeden Computer, der an das Netzwerk angeschlossen ist. 
- zuverlässigen Datenaustausch zwischen den kommunizierenden Rechnern. 
- zwei wesentliche Protokolle, welche immer einzeln und nie gleichzeitig verwendet werden → UDP (User Datagramm Protocol) und TCP (Transmission Control Protocol)
- UDP → erlaubt direkte Nutzung der IP-Datagramme, keine virtuelle Verbindung zwischen den beiden Rechnern → keine Kontrolle
- TCP → größeren Overhead als UDP, dafür aber zuverlässiger Transportdienst. Über Länge und Byte-Offset wird über jedes Datenpaket Buch geführt, sowie eine Übertragungskontrolle mit Neuübertragung. Sorgt dafür, dass alle Daten vollständig und in der richtigen Reihenfolge übertragen werden. 
#### Anwendungsschicht
- definiert die Kommunikation zwischen den Anwendungsprogrammen auf den einzelnen Rechnern. 
- Protokolle: HTTP für Webserver, FTP zur Dateiübertragung, SMPT für E-Mail Versand
### Klassifizierung von Netzwerken
#### Reichweite des Netzwerks
Die Unterteilung der Netzwer
