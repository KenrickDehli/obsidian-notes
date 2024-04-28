Netzwerktechnik beschreibt den Themenbereich der sich mit Netzwerken und deren Konfiguration, Aufbau und Erstellung beschäftigt. Ein Netzwerk kann dabei vieles beschreiben, von einem kleinen Heim-Netzwerk um seine smarten Geräte miteinander zu verbinden oder das klassische Beispiel, das Internet. Das Internet ist dabei ein dezentrales Netzwerk von unzähligen Rechnern, das (natürlich erstmal Physisch) über bestimmte Protokolle miteinander verbunden sind und sich Pakete gegenseitig schicken. Dafür werden sogenannte IP-Adressen verwendet um einen bestimmten Rechner adressieren zu können. Sogenannte ISP (wie Vodafone, Telekom etc.) fragen bei Organisationen wie der RIPE NCC für Europa nach IP-Adressbereichen nach und dürfen diese an den Endverbraucher zuteilen. Die Kommunikation zwischen ISPs passiert dabei über Knotenpunkte. Vorteile eines so riesigen Netzes ist es, das es an sich nicht einfach 'down' gehen kann, da nicht ein einziger Rechner das Internet aufrecht erhält, sondern jeder Rechner ein Teil davon ist. 
	
Bei IP-Adressen gibt es verschiedene Versionen, die gängigsten sind IPv4 und IPv6. IPv4 ist eine Adresse aus 32-Bit bzw. 4 Byte. IPv6 ...
IPv6 hat gegenüber IPv4 den Vorteil, das es keine Knappheit an Adressen gibt. IPv4 hat fast seine gesamten Adressen -> 2^32 aufgebraucht, bei IPv6 gibt es allerdings mehr Adressen als Sandkörner auf dieser Welt. 

Man kann sich nun vorstellen, dass es ein kompliziertes Unterfangen sein kann Pakete von einem Ort an den anderen zu bringen. Man stellt sich dabei die Frage: Wohin damit? Wem soll ich es schicken? Wie soll ich es schicken?
Dafür gibt es einen Teilbereich der Netzwerktechnik der sich Routing nennt. Beim Routing geht es darum Pakete über bestimmte Strecken an andere Router und Rechner weiterzuleiten.
Dafür hat jeder Router (wie er bei uns allen zuhause steht) Routingtabellen konfiguriert, bei denen er nachfragen kann wo sich eine bestimmte Adresse befindet. Wenn ein Router eine IP-Adresse nicht kennt, so fragt er quasi einfach drauf los und fragt den nächst vorhandenen Router, ob er diese Adresse kennt. Dieses Spiel geht solange weiter bis ein Router diese Frage beantworten kann. Dann geht diese Kette rückwärts wieder zurück an den ursprünglichen Router und dieser schickt dann also sein Packet los. Im Internet gibt es dabei das sogenannte DNS-Protokoll, was grundsätzlich ein Übersetzer von IP-Adressen in URL bzw. Domänen ist, den eine IP-Adresse ist für uns Menschen schwerer zu merken als www.google.de. Ein Router ist innerhalb eines Netzwerks stets der Eintrittspunkt bzw. 'das Standardgateway' um in ein Netz reinzukommen. 

Will man sich die manuelle Konfiguration von IP-Adressen innerhalb eines Netzes ersparen, so kann man DHCP verwenden, was ein Dienst beschreibt, der automatisch IP-Adressen an Hosts zuweist. 