# **Testfall: Verbindung zum Webserver**

## **Ziel**

Überprüfen, ob der Webserver korrekt installiert wurde und die WordPress-Seite erreichbar ist.

## **Schritte**

- Öffne einen Webbrowser deiner Wahl (z. B. Chrome oder Firefox).
- Gib die öffentliche IP-Adresse des Servers ein, die beim Ausführen des Skripts angezeigt wurde. Beispiel: http://Webserver Ip.
- Drücke Enter, um die Seite zu laden.

## **Erwartete Ergebnis:**

Die WordPress-Installationsseite wird im Browser angezeigt.



---

## **Fehlerbehebung**

- Überprüfe, ob der Webserver läuft: sudo systemctl status apache2.
- Prüfe, ob die Sicherheitsgruppen in AWS den Port 80 geöffnet haben.

[Zurück zu README.md](README.md)
