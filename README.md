# Portfolio Webseite
Dieses Repository enthält den Code für meine persönliche Portfolio Webseite. Die Webseite wurde mit HTML, CSS und JavaScript erstellt und dient dazu, meine Projekte, Fähigkeiten und Erfahrungen zu präsentieren.

## Inhaltsverzeichnis:
1. [Installation](#1)
2. [Tech Stack](#2)
    1. [EC2-Instanz](#3)
    2. [ECR (Elastic Container Registry)](#4)
    3. [ECS (Elastic Container Service)](#5)
6. [Licence](#6)

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


## Licence
[MIT](https://choosealicense.com/licenses/mit/)  

[![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](https://choosealicense.com/licenses/mit/)  
 
 
