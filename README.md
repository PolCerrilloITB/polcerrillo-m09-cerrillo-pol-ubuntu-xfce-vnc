# polcerrillo-m09-cerrillo-pol-ubuntu-xfce-vnc

## 📌 Project Overview:
This project provides a Dockerized Ubuntu 24.04 environment with XFCE desktop, VNC server, SSH, VS Code, and Python. The goal is to enable remote graphical access and development in a lightweight containerized setup.
## 🚀 Getting Started
### 1️⃣ Clone the Repository
```bash
git clone https://github.com/PolCerrilloITB/polcerrillo-m09-cerrillo-pol-ubuntu-xfce-vnc.git
cd polcerrillo-m09-cerrillo-pol-ubuntu-xfce-vnc
```
### 2️⃣ Build the Docker Image
```bash
docker build -t polcerrillo/m09-cerrillo-pol:ubuntu-xfce-vnc .
```
### 3️⃣ Run the Container
```bash
docker run -dit -p 5901:5901 -p 5431:22 --name my-ubuntu-xfce polcerrillo/m09-cerrillo-pol:ubuntu-xfce-vnc bash
```
### 4️⃣ Access the Running Container
```bash
docker exec -it polcerrillo/m09-cerrillo-pol:ubuntu-xfce-vnc bash
```
### 5️⃣ Set Up and Start VNC Server
```bash
export USER=ROOT
chmod +x ~/.vnc/xstartup
vncserver -kill :1
vncserver :1 -geometry 1920x1080 -depth 24
```
## 🖥️ Connecting via VNC
1. Using Remmina (or any VNC client)
2. Connect to 127.0.0.1:5901 (if running locally)
3. Default password: developerpassword
    · You can change this in the Dockerfile, but it's not recommended.

## 🔧 Additional Information
· SSH is accessible via port 5431
· XFCE is the chosen desktop environment for its lightweight nature
· The image includes Visual Studio Code and Python for development

## 📝 Notes
· If VNC does not start, ensure that the xstartup script has execution permissions.
· Modify ports in the docker run command if needed.
· Use docker stop my-ubuntu-xfce to stop the container.

## [![Docker Hub](https://img.shields.io/badge/Docker%20Hub-0db7ed?style=for-the-badge&logo=docker&logoColor=white)](https://hub.docker.com/r/polcerrillo/m09-cerrillo-pol)DockerHub Public URL
https://hub.docker.com/repository/docker/polcerrillo/m09-cerrillo-pol/tags/ubuntu-xfce-vnc/sha256-afec394f4bf88e91452d314976d9c2cc9c683d8ad23aec1adcae44ad8e253f43

 ## License

This project is open-source and maintained by Pol Cerrillo. Feel free to modify and improve it!
