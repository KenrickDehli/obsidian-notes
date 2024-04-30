Bei einem VPN handelt es sich um ein virutelles Netzwerk. Die Verbindung er-
folgt mithilfe eines VPN-Servers, der dem Endgerät intern eine neue IP-Adresse
zuweist. Die Verschlüsselten Datenleitungen werden VPN Tunnel genannt, denn
die Verschlüsselung "gräbt" einen abhörsicheren Tunnel durch das ungeschützte
Internet. Die Informationen zwischen Endgerät und Server werden also ver-
schlüsselt, durch den Tunnel transportiert und am Ende des Tunnels wieder
ausgepackt.

Virtual LAN, bezeichnet ein von der physikalischen LAN-Infrastruktur unabhängiges,
logisch getrenntes LAN. Also die Aufteilung eines Switch bzw. Netz, aus bspw.
Sicherheitsgründen, in mehrere logische Bereiche. Dabei sind die Geräte alle an
einem Switch angeschlossen, allerdings in unterschiedlichen logischen Netzen.
Die Benötigten Schritte um ein VLAN zu konfigurieren:
1. Anzahl der VLANS und deren Größe überlegen. Danach benötigt jedes
VLAN solche Informationen, als ob es ein echtes Netz wäre. Dabei die
Frage stellen ”Sollen die Netze alle gleich groß sein oder sind auch ver-
schieden große Netze möglich?”
2. VLANS für das jeweilge Interface konfigurieren und dabei die Ports auf
dem Switch den gewünschten VLANS zuweisen.
3. Auf dem Router die Subinterfaces anlegen
4. Auf dem Router die Subinterfaces auf Trunk schalten
5. Jedes Subinterface so konfigurieren, als ob es ein echtes Interface wäre,
also IP-Adresse + Subnetmaske eintragen.
6. Trunk auf dem Switch schalten.