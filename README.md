# 🐳 Install Docker & MicroK8s on Ubuntu

This guide will walk you through installing **Docker Engine** and **MicroK8s** on an Ubuntu system.
#[banner](![image](https://github.com/user-attachments/assets/21320235-ee42-4ab0-89be-acd8c66f2087)


---

## 🚀 Install Docker Engine

### 🔹 Step 1: Update System Packages
Before installing Docker, update your package list:
```sh
sudo apt-get update && sudo apt-get upgrade -y
```

### 🔹 Step 2: Install Docker Engine
Run the following command to install Docker:
```sh
sudo apt-get install docker.io -y
```

### 🔹 Step 3: Add User to Docker Group (Run Docker Without sudo)
1. **Create the Docker group** (if it doesn’t exist):
    ```sh
    sudo groupadd docker
    ```
2. **Add your current user to the Docker group**:
    ```sh
    sudo usermod -aG docker $USER
    ```
3. **Apply group changes** (logout and log back in, or run):
    ```sh
    newgrp docker
    ```

---

## 🚢 Install MicroK8s

### 🔹 Step 1: Install MicroK8s Using Snap
Run the following command to install **MicroK8s**:
```sh
sudo snap install microk8s --classic
```

### 🔹 Step 2: Add User to MicroK8s Group
Allow your user to run MicroK8s commands without `sudo`:
```sh
sudo usermod -aG microk8s $USER
```

### 🔹 Step 3: Apply Group Changes
Logout and log back in, or apply changes immediately:
```sh
newgrp microk8s
```

### 🔹 Step 4: Verify MicroK8s Installation
Check if MicroK8s is running properly:
```sh
microk8s status --wait-ready
```

---

## 🎯 Next Steps
- ✅ Deploy your first Kubernetes application in MicroK8s.
- ✅ Explore Kubernetes commands using `microk8s kubectl`.
- ✅ Enable additional MicroK8s addons with `microk8s enable dns ingress`.

---

### 📌 Author  
🚀 **T S Sundar Raj**  
🔗


