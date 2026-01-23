# Dart Hello World on Docker & Azure VM 🚀

This repository contains a simple **Hello World** application written in [Dart](https://dart.dev), containerized using Docker, and practiced entirely on a **Linux Virtual Machine (VM) hosted on Microsoft Azure**.  
The project demonstrates directory and file creation, editing with Linux text editors (`vim`), Docker image building, container execution, and pushing code to GitHub — all through Linux commands on Azure.

---

## 📂 Project Structure

.
├── Dockerfile
└── hello.dart
└── README.md


---

## 🛠️ Prerequisites
- An Azure Linux VM (or any Linux environment)
- Installed [Docker](https://docs.docker.com/get-docker/)
- Installed [Git](https://git-scm.com/)

---

## 📄 Source Code

**hello.dart**
void main() {
  print("Hello world! from dart app ");
}

**Dockerfile**
FROM dart:stable
WORKDIR /app
COPY hello.dart /app/hello.dart
CMD ["dart","run","hello.dart"]


📌 Steps Practiced
1. Directory & File Creation

linux commands:
mkdir dart-app
cd dart-app
touch hello.dart Dockerfile

2. Editing Files with vim
linux commands:
vim hello.dart
vim Dockerfile

write Dart code and Dockerfile content respectively

-> press Esc and then write to Save and exit (:wq)

3. Build Docker Image
Docker command : 
docker build -t dart-hello-world .

4. Run Container

command :
docker run --rm dart-hello-world


Expected output:
Hello world! from dart app

5. Initialize Git Repository
git commands:
git init
git add .
git commit -m "Initial commit: Dart Hello World with Docker"


6. Push to GitHub

commands :
git branch -M main
git remote add origin https://github.com/<your-username>/<repo-name>.git
git push -u origin main


🎯 Purpose
This project was created to practice:

Writing a Dart "Hello World" program

Using Linux commands for directory and file management

Editing files with vim

Containerizing apps with Docker

Running containers on an Azure VM

Setting up Git and pushing code to GitHub from Linux
