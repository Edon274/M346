# **Testfall: SSH-Verbindung**

## **Ziel**

Überprüfen, ob eine SSH-Verbindung zum Webserver erfolgreich hergestellt werden kann.

## **Schritte**

- Öffne ein Terminal oder eine Kommandozeile.
- Führe den folgenden Befehl aus, um die Verbindung herzustellen:

**ssh -i ~/.ssh/aws/<Schlüsselname>.pem ubuntu@<IP-Adresse>(IP vom Webserver)**

- Ersetze **Schlüsselname** durch den Namen des generierten SSH-Schlüssels.

## **Erwartete Ergebnise**

Du siehst die Willkommensnachricht oder den Prompt des Servers.

![image](https://github.com/user-attachments/assets/2e83178b-7b2f-4bd1-9e04-8f462e2bcc4f)

---

## **Fehlerbehebung**

Falls die Verbindung nicht hergestellt werden kann:

- Stelle sicher, dass die öffentliche IP-Adresse korrekt ist.
- Überprüfe, ob der SSH-Dienst auf dem Server läuft:

**sudo systemctl status ssh**

- Prüfe, ob die Sicherheitsgruppen in AWS den Port 22 für SSH geöffnet haben.

[Zurück zu README.md](README.md)


