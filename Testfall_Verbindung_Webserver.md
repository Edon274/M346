# **Testfall: Verbindung zum Webserver**

## **Ziel**

Überprüfen, ob der Webserver korrekt installiert wurde und die WordPress-Seite erreichbar ist.

## **Schritte**

- Öffne einen Webbrowser deiner Wahl (z. B. Chrome oder Firefox).
- Gib die öffentliche IP-Adresse des Servers ein, die beim Ausführen des Skripts angezeigt wurde. Beispiel: http://Webserver Ip.
- Drücke Enter, um die Seite zu laden.

## **Erwartete Ergebnis:**

Die WordPress-Installationsseite wird im Browser angezeigt.

![image](https://github.com/user-attachments/assets/c2e2a8a9-9e2c-4218-bf8a-4f20ea3f0cd6)


---

## **Fehlerbehebung**

- Überprüfe, ob der Webserver läuft: sudo systemctl status apache2.
- Prüfe, ob die Sicherheitsgruppen in AWS den Port 80 geöffnet haben.

[Zurück zu README.md](README.md)
