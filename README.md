<div align="center">

<img src="https://kubernetes.io/images/kubernetes-horizontal-color.png" width="400" alt="Kubernetes Logo"/>

<br/>
<br/>

# ⛵ KubeStarter — Your Kubernetes Journey Starts Here!

### 🚀 From Zero to Kubernetes Hero — One YAML at a Time!

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=22&pause=1000&color=326CE5&center=true&vCenter=true&random=false&width=650&lines=Welcome+to+KubeStarter!+%E2%9B%B5;Learn+Kubernetes+the+Fun+Way+%F0%9F%8E%89;From+KIND+Install+to+Production+Deployments+%F0%9F%9A%80;Open+Source+%7C+Beginner+Friendly+%7C+Hands+On+%F0%9F%94%A5;Star+%E2%AD%90+This+Repo+and+Start+Your+Journey!" alt="Typing SVG" />

<br/>

![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![KIND](https://img.shields.io/badge/KIND-Cluster-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white)
![YAML](https://img.shields.io/badge/YAML-Configs-CB171E?style=for-the-badge&logo=yaml&logoColor=white)
![Shell](https://img.shields.io/badge/Shell-Scripts-4EAA25?style=for-the-badge&logo=gnu-bash&logoColor=white)
![Open Source](https://img.shields.io/badge/Open_Source-%E2%9D%A4-red?style=for-the-badge)

<br/>

![GitHub stars](https://img.shields.io/github/stars/bharijaSaatvik/kubestarter?style=social)
![GitHub forks](https://img.shields.io/github/forks/bharijaSaatvik/kubestarter?style=social)
![GitHub watchers](https://img.shields.io/github/watchers/bharijaSaatvik/kubestarter?style=social)
![GitHub issues](https://img.shields.io/github/issues/bharijaSaatvik/kubestarter)
![GitHub license](https://img.shields.io/github/license/bharijaSaatvik/kubestarter)

<br/>

**🌍 Welcome, Kubernetes explorers from every corner of the globe!**

Whether you are in 🇮🇳 India, 🇺🇸 USA, 🇬🇧 UK, 🇩🇪 Germany, 🇯🇵 Japan, 🇧🇷 Brazil, 🇦🇺 Australia, or anywhere on Earth — this repo is YOUR launchpad into the world of Kubernetes!

</div>

---

## 📖 What is KubeStarter?

> **KubeStarter** is your **all-in-one** Kubernetes learning playground — a complete hands-on guide that takes you from **installing your first cluster** to **deploying production-grade applications!**

### 🎯 This Repository Includes:

| # | Topic | Status |
|---|-------|--------|
| 1 | 🏗️ **KIND Cluster Installation** — Install Kubernetes locally in minutes | ✅ |
| 2 | 📦 **Core Kubernetes Concepts** — Pods, Services, Deployments, and more | ✅ |
| 3 | 🏛️ **Kubernetes Architecture** — Master and Worker node deep dive | ✅ |
| 4 | 📝 **YAML Configurations** — Ready-to-use config files for every resource | ✅ |
| 5 | 🚀 **Deployments and Scaling** — Deploy apps and scale like a pro | ✅ |
| 6 | 🌐 **Services and Networking** — Expose your apps to the world | ✅ |
| 7 | 💾 **Storage and Volumes** — Persistent data in Kubernetes | ✅ |
| 8 | 🔐 **ConfigMaps and Secrets** — Manage configuration securely | ✅ |
| 9 | 📊 **Namespaces and Resource Quotas** — Organize and limit resources | ✅ |
| 10 | 🎯 **Real-World Projects** — Hands-on projects to practice | ✅ |

---

## 🤔 Who Is This For?

| 👤 You Are | 🎯 What You Will Get |
|-----------|---------------------|
| 🌱 **Complete Beginner** | Step-by-step installation and first deployment |
| 💻 **Developer** | Learn to containerize and deploy your apps on K8s |
| 🔧 **DevOps Engineer** | Production-ready configs and best practices |
| 🎓 **Student** | Perfect study material for CKA/CKAD prep |
| 🤓 **Curious Explorer** | Fun hands-on way to understand cloud-native tech |

---


## 🗺️ Table of Contents

- [🏗️ KIND Installation Guide](#%EF%B8%8F-kind-installation-guide)
- [🏛️ Kubernetes Architecture](#%EF%B8%8F-kubernetes-architecture)
- [🧱 Core Concepts](#-core-concepts)
- [📝 YAML Crash Course](#-yaml-crash-course)
- [🚀 Hands-On Labs](#-hands-on-labs)
- [📂 Repository Structure](#-repository-structure)
- [🤝 Contributing](#-contributing)
- [⭐ Star This Repo](#-star-this-repo)

---

## 🏗️ KIND Installation Guide

> **KIND** = **K**ubernetes **IN** **D**ocker — It runs a full Kubernetes cluster inside Docker containers on your local machine! Perfect for learning and testing!

### 📋 Prerequisites

Before installing KIND, make sure you have these installed:

| Tool | Purpose | Check Command |
|------|---------|---------------|
| 🐳 **Docker** | Container runtime | `docker --version` |
| 🔧 **kubectl** | Kubernetes CLI | `kubectl version --client` |
| 🐧 **Linux/WSL/Mac** | Operating System | `uname -a` |

---

### 🐳 Step 1 — Install Docker (If Not Installed)

**For Ubuntu/Debian (WSL included):**

| Step | Command |
|------|---------|
| Update packages | `sudo apt-get update` |
| Install dependencies | `sudo apt-get install -y ca-certificates curl gnupg lsb-release` |
| Add Docker GPG key | `sudo mkdir -p /etc/apt/keyrings && curl -fsSL https://download.docker.com/linux/ubuntu/gpg \| sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg` |
| Add Docker repo | `echo "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" \| sudo tee /etc/apt/sources.list.d/docker.list` |
| Install Docker | `sudo apt-get update && sudo apt-get install -y docker-ce docker-ce-cli containerd.io` |
| Add user to docker group | `sudo usermod -aG docker $USER` |
| Apply group changes | `newgrp docker` |
| Verify | `docker --version` |

**For macOS:**

| Step | Command |
|------|---------|
| Install via Homebrew | `brew install --cask docker` |
| Open Docker Desktop | Launch Docker Desktop from Applications |
| Verify | `docker --version` |

---

### 🔧 Step 2 — Install kubectl

**For Linux/WSL:**

| Step | Command |
|------|---------|
| Download kubectl | `curl -LO "https://dl.k8s.io/release/$(curl -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"` |
| Make executable | `chmod +x kubectl` |
| Move to PATH | `sudo mv kubectl /usr/local/bin/` |
| Verify | `kubectl version --client` |

**For macOS:**

| Step | Command |
|------|---------|
| Install via Homebrew | `brew install kubectl` |
| Verify | `kubectl version --client` |

---

### ⛵ Step 3 — Install KIND

**For Linux/WSL:**

| Step | Command |
|------|---------|
| Download KIND | `curl -Lo ./kind https://kind.sigs.k8s.io/dl/v0.20.0/kind-linux-amd64` |
| Make executable | `chmod +x ./kind` |
| Move to PATH | `sudo mv ./kind /usr/local/bin/kind` |
| Verify | `kind version` |

**For macOS:**

| Step | Command |
|------|---------|
| Install via Homebrew | `brew install kind` |
| Verify | `kind version` |

**For Windows (PowerShell):**

| Step | Command |
|------|---------|
| Download KIND | `curl.exe -Lo kind-windows-amd64.exe https://kind.sigs.k8s.io/dl/v0.20.0/kind-windows-amd64` |
| Move to PATH | `Move-Item .\kind-windows-amd64.exe C:\kind\kind.exe` |
| Verify | `kind version` |

---

### 🚀 Step 4 — Create Your First Cluster!

**Quick Single Node Cluster:**

| Step | Command |
|------|---------|
| Create cluster | `kind create cluster --name my-first-cluster` |
| Verify cluster | `kubectl cluster-info --context kind-my-first-cluster` |
| See nodes | `kubectl get nodes` |
| See all pods | `kubectl get pods -A` |

---

### 🏗️ Step 5 — Create a Multi-Node Cluster (Recommended)

First create a config file. Open your editor:

| Step | Command |
|------|---------|
| Create config file | `nano kind-config.yml` |
| Paste config below | See YAML below |
| Save and exit | `Ctrl+O → Enter → Ctrl+X` |
| Create cluster | `kind create cluster --config kind-config.yml --name kubestarter` |
| Verify | `kubectl get nodes` |

---


**KIND Multi-Node Cluster Configuration:**

```yaml
kind: Cluster
apiVersion: kind.x-k8s.io/v1alpha4
nodes:
  - role: control-plane
    kubeadmConfigPatches:
      - |
        kind: InitConfiguration
        nodeRegistration:
          kubeletExtraArgs:
            node-labels: "ingress-ready=true"
    extraPortMappings:
      - containerPort: 80
        hostPort: 80
        protocol: TCP
      - containerPort: 443
        hostPort: 443
        protocol: TCP
  - role: worker
  - role: worker
  - role: worker
```


**KIND Management Commands:**

| What You Want | Command |
|--------------|---------|
| ✅ Create cluster | `kind create cluster --name my-cluster` |
| ✅ Create with config | `kind create cluster --config kind-config.yml --name my-cluster` |
| 📋 List clusters | `kind get clusters` |
| 🗑️ Delete cluster | `kind delete cluster --name my-cluster` |
| 🗑️ Delete ALL clusters | `kind delete clusters --all` |
| 🐳 Load Docker image into KIND | `kind load docker-image my-app:latest --name my-cluster` |
| 📋 List nodes | `kubectl get nodes -o wide` |
| 🔍 Cluster info | `kubectl cluster-info --context kind-my-cluster` |

---



## 🏛️ Kubernetes Architecture

> Understanding the architecture is the **foundation** of your Kubernetes journey. Let us break it down piece by piece!

### 🗺️ The Big Picture






