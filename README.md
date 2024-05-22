# Portfolio Webseite
Dieses Repository enthält den Code für meine persönliche Portfolio Webseite. Die Webseite wurde mit HTML, CSS und JavaScript erstellt und dient dazu, meine Projekte, Fähigkeiten und Erfahrungen zu präsentieren.

## Inhaltsverzeichnis:
1. [Installation](#1)
2. [Tech Stack](#2)
    1. [EC2-Instanz](#3)
    2. [ECR (Elastic Container Registry)](#4)
    3. [ECS (Elastic Container Service)](#5)
    4. [API Gateway](#6)
    5. [Lambda für DynamoDB und SES](#7)
    6. [DynamoDB Tabelle](#8)
    7. [SES Verbindung](#9)
    8. [Amplify](#10)
9. [Licence](#11)

## Installation

Um dieses Projekt lokal auszuführen, führen Sie die folgenden Schritte aus:

Projekt klonen:

~~~bash  
  git clone https://github.com/Ashkan-pahlavan/AAM.git
~~~

Anschließend index.html-Datei mit linker Maustaste ausführen und Webseite aufrufen.


## Tech Stack

### EC2-Instanz
Für die Entwicklung und Bereitstellung dieser Webseite nutzen wir eine EC2-Instanz auf AWS. Die EC2-Instanz wurde konfiguriert, um die Webseite zu hosten und bietet eine skalierbare und zuverlässige Umgebung für den Betrieb der Anwendung.

Um auf die EC2-Instanz zuzugreifen, können Sie eine Verbindung über SSH herstellen und die erforderlichen Dateien für die Webseite auf die Instanz übertragen. Stellen Sie sicher, dass Sie die erforderlichen Sicherheitsgruppen und Berechtigungen konfiguriert haben, um einen sicheren Zugriff auf die Instanz zu gewährleisten.

**Erforderliche Konfigurationen:**
- **VPC (Virtual Private Cloud):** Erstellen Sie eine VPC, um ein isoliertes Netzwerk für Ihre Ressourcen zu haben.
- **Öffentliches Subnetz:** Stellen Sie sicher, dass die EC2-Instanz in einem öffentlichen Subnetz platziert wird, damit sie über das Internet erreichbar ist.
- **Sicherheitsgruppe:** Konfigurieren Sie eine Sicherheitsgruppe, um den eingehenden und ausgehenden Datenverkehr zu steuern. Erlauben Sie mindestens den HTTP/HTTPS-Zugriff (Port 80/443) und SSH-Zugriff (Port 22) für die Verwaltung.
- **Elastic IP:** Weisen Sie der EC2-Instanz eine Elastic IP zu, um eine statische IP-Adresse zu erhalten, die Sie für den Zugriff auf Ihre Webseite verwenden können.

### ECR (Elastic Container Registry)
Um Container-Images für diese Anwendung zu hosten und zu verwalten, nutzen wir die Elastic Container Registry (ECR) von AWS. Die ECR ermöglicht es uns, Docker-Images zu speichern und zu versionieren, um eine zuverlässige Bereitstellung unserer Anwendung zu gewährleisten.

Stellen Sie sicher, dass Sie Docker-Images für Ihre Anwendung erstellen und diese Images in der ECR hochladen, um sie für die Bereitstellung auf der EC2-Instanz verfügbar zu machen.


### ECS (Elastic Container Service)
Für die Bereitstellung und Verwaltung von Container-Anwendungen nutzen wir den Elastic Container Service (ECS) von AWS. ECS ermöglicht es uns, Docker-Container in einer skalierbaren und zuverlässigen Umgebung auszuführen, wodurch wir unsere Anwendung einfach und effizient skalieren können.

Stellen Sie sicher, dass Sie Ihre Anwendung mit ECS konfigurieren und bereitstellen, um von den Vorteilen einer containerisierten Umgebung zu profitieren.

### API Gateway
Um eine API für unsere Anwendung zu erstellen, nutzen wir das API Gateway von AWS. Das API Gateway ermöglicht es uns, RESTful APIs zu erstellen und zu verwalten, die als Einstiegspunkt für unsere Backend-Services dienen.

Konfigurieren Sie das API Gateway, um Anfragen an Ihre Lambda-Funktionen weiterzuleiten, die mit DynamoDB und SES interagieren.

### Lambda für DynamoDB und SES
Für die serverlose Verarbeitung unserer Backend-Logik nutzen wir AWS Lambda. Lambda-Funktionen können auf Ereignisse reagieren und ermöglichen uns, eine skalierbare und kosteneffiziente Architektur zu implementieren.

Erstellen Sie eine Lambda-Funktion, die mit DynamoDB für das Speichern und Abrufen von Daten sowie mit Amazon SES für den E-Mail-Versand interagiert.

### DynamoDB Tabelle
Um die Daten unserer Anwendung zu speichern, nutzen wir Amazon DynamoDB. DynamoDB ist ein NoSQL-Datenbankservice, der eine schnelle und flexible Datenverarbeitung ermöglicht.

Erstellen Sie eine DynamoDB-Tabelle, um die erforderlichen Daten für Ihre Anwendung zu speichern. Stellen Sie sicher, dass die Tabelle korrekt konfiguriert ist, um die benötigten Lese- und Schreibkapazitäten zu erfüllen.

### SES Verbindung
Für den E-Mail-Versand in unserer Anwendung nutzen wir Amazon Simple Email Service (SES). SES ermöglicht es uns, Transaktions- und Marketing-E-Mails in einer skalierbaren und zuverlässigen Weise zu versenden.

Konfigurieren Sie die Verbindung zu Amazon SES, um E-Mails aus Ihrer Anwendung zu senden. Stellen Sie sicher, dass die erforderlichen Berechtigungen und Einstellungen für den E-Mail-Versand konfiguriert sind.

### Amplify
Um deine Portfolio-Webseite mit Git, AWS Amplify und Visual Studio Code (VS Code) zu hosten, gehe wie folgt vor: Erstelle zunächst ein neues Git-Repository und pushe deinen Code zu einem Git-Hosting-Dienst wie GitHub. Melde dich dann bei AWS Amplify an, wähle "Get Started" unter "Deploy" und verbinde Amplify mit deinem Repository. Konfiguriere die Build-Einstellungen und starte den Deployment-Prozess. Mit der Git-Erweiterung in VS Code kannst du Änderungen committen und pushen, damit Amplify deine Webseite automatisch neu baut und deployt.


## Licence
[MIT](https://choosealicense.com/licenses/mit/)  

[![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](https://choosealicense.com/licenses/mit/)  