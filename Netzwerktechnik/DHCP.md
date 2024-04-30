Dieses Protokoll ermöglicht die Zuweisung der Netzwerkkonfiguration an einen
Client durch einen Server. Dadurch ist es möglich die IP-Adressen an die Clients
zu vergeben und die freien und vergebenen IP-Adressen innerhalb eines Netzes
zu verwalten. Die Phasen von DHCP sind:
1. DHCP-Discover → Netzwerkbroadcast an alle verfügbaren DHCP-Server
2. DHCP-Offer → Antwort vom DHCP-Server und ein Vorschlag einer IP-
Adresse. Das Angebot ist an die MAC-Adresse des anfragenden Geräts
adressiert.
3. DHCP-Request → DHCP-Client hat sich entschieden, Broadcast mit Server-
Identifier im Paket.
4. DHCPACK oder DHCPNAK → Der vom Client ausgewählter Server bestätigt
mit DHCP-Acknowledged die IP-Adresse oder zieht sein Angebot zurück
Die Vorteile von DHCP sind:
- Die Verwaltung und Vergabe von IP-Adressen wird automatisiert
- IP-Adresskonflikte werden vermieden
- Verringerter Konfigurationsaufwand bei Endgeräten
 
Um es zu ermöglichen die Vergabe von IP-Adressen an Geräte zu kontrollieren
besteht auf DHCP-Servern die Möglichkeit eine Liste mit MAC-Adressen zu hin-
terlegen. Nur MAC-Adressen, die in der hinterlegten Liste abgelegt sind, bekom-
men vom DHCP-Server eine IP-Adresse zugewiesen. Eine weitere Möglichkeit
ist die Verwendung von IEEE 802.1X.