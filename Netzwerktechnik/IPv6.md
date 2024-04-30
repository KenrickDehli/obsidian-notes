# IPv6
Der Nachfolger von IPv4. 
- 128 Bit lang
- Darstellung in Hexadezimalzahlen
- Netzteil 64 Bit lang
- Interface Identifier 64 Bit lang
- Ein Interface kann nun mehrere IP-Adressen haben
	- link-local-address: nicht im Internet geroutet und nur im lokalen Netzwerk gültig -> fe:80::/10 + MAC-Adresse vom Interface
	- global-unique-address: wie der Name sagt, Adresse die ins Internet geroutet wird
	- temporary-global-address: Routing im Internet, nützlich für privacy extensions, um temporär gültige, aber im Internet routbare IP-Adressen zu erzeigen
- Konfiguration kann stateless (ohne DHCP, Interface weist sich selber zu) oder stateful (mit DHCP) erfolgen
