# **Projekt M346** 

### Projekt von:

- Rilind Rama
- Savvas Ioannidis
- Edon Thaqi

## Inhaltsverzeichnis 📜
- [Einleitung](#einleitung)
- [Anforderung](#anforderung)
- [Installation](#installation)
- [Testfälle](#testfälle)
- [Fazit](#fazit)

---

## **Einleitung 🚀**

In diesem Projekt haben wir ein Skript entwickelt, das die Installation eines Apache-Webservers und einer WordPress-Instanz auf AWS automatisiert. Das Skript richtet alle notwendigen Komponenten ein, einschliesslich Sicherheitsgruppen, einer Datenbank und der Verbindung von WordPress zur Datenbank. Ziel war es, eine einfache und schnelle Installation zu ermöglichen.

---

## **Anforderungen 📋**

Damit das Skript funktioniert, braucht man:

- Einen AWS-Account
- Die AWS-CLI, um Befehle auszuführen
- Git, um das Projekt herunterzuladen
- Einen Browser, um später die WordPress-Seite zu öffnen

---

## **Installation 🛠️**

### **Installation der AWS CLI**
Um die AWS CLI zu installieren, führe folgende Befehle aus:


**sudo apt update
sudo apt install curl unzip
curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
unzip awscliv2.zip
sudo ./aws/install**

Überprüfe, ob die Installation erfolgreich war:

**aws --version**

Du solltest eine Ausgabe wie aws-cli/2.x.x erhalten.

### **1) Konfiguration der AWS CLI**
Jetzt konfigurieren wir die AWS CLI mit deinem AWS-Account:

**aws configure**

Du wirst nach folgenden Angaben gefragt:

AWS Access Key ID: x (wird später noch überschrieben)
AWS Secret Access Key x (wird später noch überschrieben)
Default region name: us-east-1
Default output format: json

### **2) Credentials aktualisieren**
Melde dich bei deinem AWS Lab oder deinem AWS-Account an.
Gehe zu den AWS Details und kopiere die dort angezeigten Zugangsdaten (AWS CLI).

Öffne die Datei ~/.aws/credentials:

**nano ~/.aws/credentials**

Füge den Inhalt, den du kopiert hast ein:
[default]
aws_access_key_id=DeinAccessKey
aws_secret_access_key=DeinSecretKey
aws_session_token=DeinSessionToken

Speichere und beende die Datei mit CTRL+O, Enter und CTRL+X.

### **3) Verbindung testen
Teste die Verbindung, indem du den folgenden Befehl ausführst:

**aws s3 ls**

Wenn keine Fehler auftreten, ist die Verbindung korrekt eingerichtet.

### **4) Skript hinzufügen und ausführen**
Navigiere zum Ordner, in dem du das Skript speichern möchtest:

**cd ~/Ordner**

Erstelle eine neue Datei für das Skript:

**nano install_wordpress.sh**

Kopiere das Installationsskript ([Hier geht's zum Skript](Skript.md)) und füge es in die Datei ein.
Speichere und schliesse die Datei.

### **5)Rechte vergeben**
Mache das Skript ausführbar:

**chmod +x install_wordpress.sh**

### **6) Skript ausführen**
Starte die Installation, indem du das Skript ausführst:

**./install_wordpress.sh**

### **6) Browser öffnen**
Sobald das Skript abgeschlossen ist, rufe die IP-Adresse deines AWS-Servers auf:

http://<deine-IP>/

Du solltest jetzt die Installationsseite von Wordpress sehen.
---

## **Testfälle 🔍**



---

## **Fazit 🏁**

