Durch DNS wird die Namensauflösung realisiert. Um die Namensauflösung
zu realisieren muss ein Hostname in eine für den Computer verständliche IP-
Adresse umgewandelt werden. Die acht Schritte eines DNS-Lookups:
1. User gibt eine Adresse ein
2. Der Resolver fragt einen DNS-Stamm-Namensserver ab
3. Der Stammserver antwortet dem Resolver mit der Adresse eines Top Level
Domain Servers, der die Informationen zu den Domains enthält.
4. Der Resolver sendet dann eine Anfrage an die TLD .com
5. Der TLD Server antortet dann mit der IP Adresse des Namesservers der
Domain, die der User in Schritt 1 angegeben hat.
6. Der rekursive Resolver sendet eine Anfrage an den Namensserver der Do-
main.
7. Die IP-Adresse wird dann von Namensserver an den Resolver zurück-
gegeben
8. Der DNS Resolver beantwortet die Anfrage des Webbrowsers mit der IP-
Adresse er Domain, die ursprünglich angefragt wurde.
Anschließend kann der Browser die Anfrage für die Webseite erstellen:
1. Der Browser sendet eine HTTP-Anfrage an die IP-Adresse
2. Der Server liefert die Webseite, die anschließend im Browser dargestellt
wird.
Für DNS wird oft der TCP/UDP Port 53 angewendet.