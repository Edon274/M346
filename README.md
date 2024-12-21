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

## **1) Installation 🛠️**

### **Installation der AWS CLI**
Um die AWS CLI zu installieren, führe folgende Befehle aus:


**sudo apt update
- sudo apt install curl unzip
- curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
- unzip awscliv2.zip
- sudo ./aws/install**

Überprüfe, ob die Installation erfolgreich war:

**aws --version**

Du solltest eine Ausgabe wie aws-cli/2.x.x erhalten.

![image](https://github.com/user-attachments/assets/11ee9f2f-3f45-49b0-90a8-0244f670bcbd)

### **2) Konfiguration der AWS CLI**
Jetzt konfigurieren wir die AWS CLI mit deinem AWS-Account:

**aws configure**

Du wirst nach folgenden Angaben gefragt:

- AWS Access Key ID: x (wird später noch überschrieben)
- AWS Secret Access Key x (wird später noch überschrieben)
- Default region name: us-east-1
- Default output format: json

### **3) Credentials aktualisieren**
Melde dich bei deinem AWS Lab oder deinem AWS-Account an.
Gehe zu den AWS Details und kopiere die dort angezeigten Zugangsdaten (AWS CLI).

![image](https://github.com/user-attachments/assets/b274df54-cd11-4ee5-a92e-b425f8663654)

![image](https://github.com/user-attachments/assets/bee4a4de-7fb2-483d-b924-980ecdefea74)
**Auf Show klicken.**

![image](https://github.com/user-attachments/assets/6f7b429b-a2b0-4025-b40c-aaf76382ef8c)

**Inhalt kopieren**

Öffne die Datei ~/.aws/credentials:

**nano ~/.aws/credentials**

Füge den Inhalt, den du kopiert hast ein:

![image](https://github.com/user-attachments/assets/a9876bde-686c-40b4-b812-c8cef49798a8)

Speichere und beende die Datei mit **CTRL+O, Enter** und **CTRL+X**.

### **4) Verbindung testen**
Teste die Verbindung, indem du den folgenden Befehl ausführst:

**aws s3 ls**

![image](https://github.com/user-attachments/assets/a8194f15-7dcf-418d-8b03-c2b02898ee3c)

Wenn keine Fehler auftreten, ist die Verbindung korrekt eingerichtet.

### **5) Skript hinzufügen und ausführen**
Navigiere zum Ordner, in dem du das Skript speichern möchtest:

**cd ~/Ordner**

Erstelle eine neue Datei für das Skript:

Beispiel: **nano wp.sh**

Kopiere das Installationsskript ([Hier geht's zum Skript](Skript)) und füge es in die Datei ein.
Speichere und schliesse die Datei mit **CTRL+O, Enter** und **CTRL+X**.

![image](https://github.com/user-attachments/assets/eb871404-e838-488b-849c-7ce915d804e3)

### **6)Rechte vergeben**
Mache das Skript ausführbar:

**chmod +x wp.sh**

### **6) Skript ausführen**
Starte die Installation, indem du das Skript ausführst:

**./wp.sh**

### **7) Browser öffnen**
Sobald das Skript abgeschlossen ist, rufe die IP-Adresse deines AWS-Servers auf:

![image](https://github.com/user-attachments/assets/628e2278-12fe-47dd-8297-370996d24ca0)

http://deine-IP/

![image](https://github.com/user-attachments/assets/75356a1e-d603-413b-bdee-5e3bdc247f15)

Du solltest jetzt die Installationsseite von Wordpress sehen. 🥳

![image](https://github.com/user-attachments/assets/99773fcf-32ba-4a1e-a8de-0c6ccd1ae7e2)

---

## **Testfälle 🔍**



---

## **Fazit 🏁**

