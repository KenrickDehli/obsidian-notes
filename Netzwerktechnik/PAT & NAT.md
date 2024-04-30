Port Address Translation ersetzt IP-Adressen eines privaten Netzwerks in eine
einzige öffentlichen IP-Adresse. Die Zuordnung zu den Engeräten erfolgt über
neu vergebene Portnummern. PAT wird häufig für den Internetzugang genutzt
und hilft, [[IPv4]]-Adressen einzusparen. PAT ist also eine Erweiterung von NAT.

Network Address Translation wird in IP-Routern eingesetzt, der lokale Netzwerke mit dem Internet
verbinden. Damit alle Endgeräte innerhalb eines Netzes Internet-Zugang bekom-
men (durch die öffentliche Adresse), speichert der Router alle Portnummern der
TCP-Verbindungen in einer NAT-Tabelle. NAT übersetzt also die Adressen der
lokalen IP-Adresse in die Öffentliche IP-Adresse und umgekehrt.

Wird bei [[IPv6]] theoretisch nicht mehr benötigt, ist aber aufgrund von Parallelbetrieb bspw. noch im Einstatz.