<div align="center">


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


```
╔══════════════════════════════════════════════════════════════════════╗
║                      KUBERNETES CLUSTER                             ║
╠══════════════════════════════════════════════════════════════════════╣
║                                                                     ║
║  ┌──────────────────────────────────────────────────────────────┐  ║
║  │                   CONTROL PLANE (Master Node)                 │  ║
║  │                                                              │  ║
║  │  ┌─────────────┐  ┌─────────────┐  ┌────────────────────┐  │  ║
║  │  │  API Server  │  │  Scheduler  │  │ Controller Manager │  │  ║
║  │  │  (kube-      │  │  (kube-     │  │ (kube-controller   │  │  ║
║  │  │  apiserver)  │  │  scheduler) │  │  -manager)         │  │  ║
║  │  │              │  │             │  │                    │  │  ║
║  │  │  Front door  │  │  Assigns    │  │  Keeps desired     │  │  ║
║  │  │  of cluster  │  │  pods to    │  │  state = actual    │  │  ║
║  │  │  All traffic │  │  nodes      │  │  state always      │  │  ║
║  │  │  goes here   │  │             │  │                    │  │  ║
║  │  └─────────────┘  └─────────────┘  └────────────────────┘  │  ║
║  │                                                              │  ║
║  │  ┌────────────────────────────────────────────────────────┐ │  ║
║  │  │                        etcd                            │ │  ║
║  │  │         Key-Value Store — Brain of the Cluster         │ │  ║
║  │  │         Stores ALL cluster state and data              │ │  ║
║  │  └────────────────────────────────────────────────────────┘ │  ║
║  └──────────────────────────────────────────────────────────────┘  ║
║                              │                                      ║
║                 communicates │ via API                              ║
║                              │                                      ║
║  ┌──────────────────────────────────────────────────────────────┐  ║
║  │                      WORKER NODE 1                            │  ║
║  │                                                              │  ║
║  │   ┌──────────┐    ┌─────────────┐    ┌──────────────────┐  │  ║
║  │   │ kubelet  │    │ kube-proxy  │    │Container Runtime │  │  ║
║  │   │          │    │             │    │(containerd/Docker│  │  ║
║  │   │ Node     │    │ Network     │    │ Runs containers  │  │  ║
║  │   │ Agent    │    │ rules/proxy │    │ inside pods      │  │  ║
║  │   └──────────┘    └─────────────┘    └──────────────────┘  │  ║
║  │                                                              │  ║
║  │   ┌──────────┐  ┌──────────┐  ┌──────────┐  ┌──────────┐  │  ║
║  │   │  Pod 1   │  │  Pod 2   │  │  Pod 3   │  │  Pod 4   │  │  ║
║  │   │  nginx   │  │   app    │  │  redis   │  │   api    │  │  ║
║  │   └──────────┘  └──────────┘  └──────────┘  └──────────┘  │  ║
║  └──────────────────────────────────────────────────────────────┘  ║
║                                                                     ║
║  ┌──────────────────────────────────────────────────────────────┐  ║
║  │                      WORKER NODE 2                            │  ║
║  │                                                              │  ║
║  │   ┌──────────┐    ┌─────────────┐    ┌──────────────────┐  │  ║
║  │   │ kubelet  │    │ kube-proxy  │    │Container Runtime │  │  ║
║  │   └──────────┘    └─────────────┘    └──────────────────┘  │  ║
║  │                                                              │  ║
║  │   ┌──────────┐  ┌──────────┐  ┌──────────┐                 │  ║
║  │   │  Pod 5   │  │  Pod 6   │  │  Pod 7   │                 │  ║
║  │   │  mysql   │  │  worker  │  │  queue   │                 │  ║
║  │   └──────────┘  └──────────┘  └──────────┘                 │  ║
║  └──────────────────────────────────────────────────────────────┘  ║
║                                                                     ║
╚══════════════════════════════════════════════════════════════════════╝
```

---

### 🧠 Control Plane Components — The Brain of Kubernetes

| Component | Emoji | What It Does | Simple Analogy |
|-----------|-------|--------------|----------------|
| **API Server** | 🚪 | Front door to the cluster. ALL communication passes through it | Reception desk at a hotel |
| **etcd** | 🧠 | Stores all cluster data as key-value pairs | Hotel database with all reservations |
| **Scheduler** | 📋 | Decides which node should run a new pod | Hotel manager assigning rooms to guests |
| **Controller Manager** | 🔄 | Makes sure desired state always matches actual state | Housekeeping ensuring rooms are always clean |
| **Cloud Controller** | ☁️ | Talks to cloud provider APIs like AWS, GCP, Azure | Hotel travel desk booking external trips |

---

### 💪 Worker Node Components — The Muscle of Kubernetes

| Component | Emoji | What It Does | Simple Analogy |
|-----------|-------|--------------|----------------|
| **kubelet** | 🤖 | Agent on each node ensuring pods are running correctly | Room service staff on each floor |
| **kube-proxy** | 🌐 | Manages network rules and routes traffic to correct pods | Hotel telephone operator connecting calls |
| **Container Runtime** | 🐳 | Actually runs the containers (containerd or Docker) | The actual hotel room where guests stay |

---

### 🚀 How a Pod Gets Scheduled — Step by Step Journey


```
YOU type: kubectl apply -f pod.yml
          │
          ▼
┌─────────────────────┐
│  1. kubectl CLI      │  Sends HTTP request to API Server
└─────────────────────┘
          │
          ▼
┌─────────────────────┐
│  2. API Server       │  Validates request + Authenticates user
│  (kube-apiserver)    │  Stores pod definition in etcd
└─────────────────────┘
          │
          ▼
┌─────────────────────┐
│  3. etcd             │  Saves: "Pod requested but NOT yet assigned"
│  (cluster database)  │
└─────────────────────┘
          │
          ▼
┌─────────────────────┐
│  4. Scheduler        │  Watches for unassigned pods
│  (kube-scheduler)    │  Picks the best node based on resources
│                      │  Updates API Server: "Run this on Node 2"
└─────────────────────┘
          │
          ▼
┌─────────────────────┐
│  5. API Server       │  Notifies kubelet on Worker Node 2
│                      │
└─────────────────────┘
          │
          ▼
┌─────────────────────┐
│  6. kubelet          │  Receives instruction from API Server
│  (on Worker Node 2)  │  Tells Container Runtime to start container
└─────────────────────┘
          │
          ▼
┌─────────────────────┐
│  7. Container        │  Pulls image from registry (Docker Hub etc)
│  Runtime             │  Starts the container inside the Pod
└─────────────────────┘
          │
          ▼
┌─────────────────────┐
│  8. kubelet reports  │  "Pod is Running!" sent back to API Server
│  back                │  API Server updates etcd with running status
└─────────────────────┘
          │
          ▼

     Pod is LIVE! 🎉
```


---

## 🧱 Core Concepts of Kubernetes

> Master these building blocks and you will understand 90 percent of Kubernetes!

---

### 📦 1. Pods — The Smallest Deployable Unit

| Feature | Details |
|---------|---------|
| What is a Pod | The smallest and simplest deployable unit in Kubernetes |
| What it contains | One or more containers that share network and storage |
| IP Address | Every pod gets its own unique IP address inside the cluster |
| Lifecycle | Created → Running → Succeeded or Failed → Terminated |
| Key Rule | Pods are ephemeral — they can die and be replaced at any time |
| Analogy | A pod is like an apartment — containers are roommates sharing it |

---

### 🚀 2. Deployments — The App Manager

| Feature | Details |
|---------|---------|
| What it does | Manages pods and ensures the desired number are always running |
| Self-healing | If a pod dies, Deployment automatically creates a new one |
| Rolling Updates | Update your app version with ZERO downtime |
| Rollback | Instantly go back to the previous working version |
| Scaling | Change replica count to scale up or down within seconds |
| Analogy | A restaurant manager ensuring enough waiters are always working |

---

### 🌐 3. Services — The Networking Layer

| Type | What It Does | When To Use |
|------|-------------|-------------|
| **ClusterIP** | Internal cluster access only | App to app communication inside the cluster |
| **NodePort** | Exposes app on every node on a port 30000 to 32767 | Development and testing |
| **LoadBalancer** | Creates external cloud load balancer | Production apps needing external access |
| **ExternalName** | Maps to an external DNS name | Connecting to external databases or APIs |

---

### 🔐 4. ConfigMaps and Secrets

| Resource | Purpose | Use For |
|----------|---------|---------|
| **ConfigMap** | Store non-sensitive configuration data | Database hosts, feature flags, URLs |
| **Secret** | Store sensitive data encoded in base64 | Passwords, API keys, TLS certificates |

---

### 📊 5. Namespaces — Virtual Clusters

| Feature | Details |
|---------|---------|
| What it is | A virtual sub-cluster inside a physical cluster |
| Purpose | Organize resources and isolate teams and environments |
| Default ones | default, kube-system, kube-public, kube-node-lease |
| Analogy | Floors in an office building — each team gets their own floor |

---

### 💾 6. Volumes and Storage

| Type | Lifetime | Best Use Case |
|------|----------|---------------|
| **emptyDir** | Lives as long as the pod | Temporary scratch space and cache |
| **hostPath** | Lives as long as the node | Access node filesystem for testing only |
| **PersistentVolume** | Independent of pod and node | Database storage and file uploads |
| **PersistentVolumeClaim** | Independent of pod and node | Request and use storage from PersistentVolume |

---


## 📝 YAML Crash Course

> YAML is the language of Kubernetes — every resource is defined in YAML!

### 📖 YAML Golden Rules

| Rule | Correct Example | Wrong Example |
|------|----------------|---------------|
| Use spaces NOT tabs | 2 spaces for indent | Never use tab key |
| Colon then space | `name: nginx` | `name:nginx` |
| Dash then space for lists | `- item` | `-item` |
| Consistent indentation | Always 2 spaces | Mixing 2 and 4 spaces |
| Case sensitive | `apiVersion` | `apiversion` will fail |

---

### 📄 Template 1 of 5 — Pod YAML



```yaml
apiVersion: v1
kind: Pod
metadata:
  name: my-first-pod
  labels:
    app: nginx
    env: learning
spec:
  containers:
    - name: nginx-container
      image: nginx:latest
      ports:
        - containerPort: 80
      resources:
        requests:
          memory: "64Mi"
          cpu: "250m"
        limits:
          memory: "128Mi"
          cpu: "500m"
```


---

### 📄 Template 2 of 5 — Deployment YAML

```yaml
apiVersion: apps/v1
kind: Deployment
metadata:
  name: nginx-deployment
  labels:
    app: nginx
spec:
  replicas: 3
  selector:
    matchLabels:
      app: nginx
  template:
    metadata:
      labels:
        app: nginx
    spec:
      containers:
        - name: nginx
          image: nginx:1.25
          ports:
            - containerPort: 80
          resources:
            requests:
              memory: "64Mi"
              cpu: "250m"
            limits:
              memory: "128Mi"
              cpu: "500m"
```

---

### 📄 Template 3 of 5 — Service YAML

```yaml
apiVersion: v1
kind: Service
metadata:
  name: nginx-service
  labels:
    app: nginx
spec:
  type: NodePort
  selector:
    app: nginx
  ports:
    - protocol: TCP
      port: 80
      targetPort: 80
      nodePort: 30080
```

---

### 📄 Template 4 of 5 — Namespace with Resource Quota

```yaml
apiVersion: v1
kind: Namespace
metadata:
  name: dev-environment
  labels:
    env: development
    team: backend
```

---

### 📄 Template 5 of 5 — Resource Quota YAML

```yaml
apiVersion: v1
kind: ResourceQuota
metadata:
  name: dev-quota
  namespace: dev-environment
spec:
  hard:
    requests.cpu: "4"
    requests.memory: "8Gi"
    limits.cpu: "8"
    limits.memory: "16Gi"
    pods: "20"
    services: "10"
    secrets: "20"
    configmaps: "20"
```

---

## 🚀 Hands-On Labs

### 🧪 Lab 1 — Deploy Your First App

| Step | Command | What It Does |
|------|---------|-------------|
| 1 | `kind create cluster --name lab1` | Create a fresh cluster |
| 2 | `kubectl get nodes` | Verify cluster is running |
| 3 | `kubectl run hello --image=nginx --port=80` | Create your first pod |
| 4 | `kubectl get pods` | See your pod running |
| 5 | `kubectl expose pod hello --type=NodePort --port=80` | Expose the pod |
| 6 | `kubectl get svc` | See the service created |
| 7 | `kubectl describe pod hello` | Deep dive into pod details |
| 8 | `kubectl logs hello` | View pod logs |
| 9 | `kubectl delete pod hello` | Clean up the pod |

---

### 🧪 Lab 2 — Deployment and Scaling

| Step | Command | What It Does |
|------|---------|-------------|
| 1 | `kubectl create deployment webapp --image=nginx --replicas=3` | Create deployment |
| 2 | `kubectl get deployments` | See the deployment |
| 3 | `kubectl get pods` | See 3 pods running |
| 4 | `kubectl scale deployment webapp --replicas=5` | Scale UP to 5 pods |
| 5 | `kubectl get pods` | See 5 pods now |
| 6 | `kubectl scale deployment webapp --replicas=2` | Scale DOWN to 2 pods |
| 7 | `kubectl rollout status deployment/webapp` | Check rollout status |
| 8 | `kubectl rollout undo deployment/webapp` | Rollback to previous version |
| 9 | `kubectl delete deployment webapp` | Clean up |

---

### 🧪 Lab 3 — Namespaces

| Step | Command | What It Does |
|------|---------|-------------|
| 1 | `kubectl create namespace dev` | Create dev namespace |
| 2 | `kubectl create namespace staging` | Create staging namespace |
| 3 | `kubectl get namespaces` | List all namespaces |
| 4 | `kubectl run app --image=nginx -n dev` | Deploy pod in dev namespace |
| 5 | `kubectl get pods -n dev` | See pods in dev only |
| 6 | `kubectl get pods --all-namespaces` | See pods in ALL namespaces |
| 7 | `kubectl delete namespace dev` | Delete namespace and all its resources |

---

## 🎮 kubectl Master Cheat Sheet

### 📋 View and List Resources

| Command | What It Does |
|---------|-------------|
| `kubectl get nodes` | List all nodes in the cluster |
| `kubectl get pods` | List pods in default namespace |
| `kubectl get pods -A` | List ALL pods in ALL namespaces |
| `kubectl get pods -n dev` | List pods in specific namespace |
| `kubectl get svc` | List all services |
| `kubectl get deployments` | List all deployments |
| `kubectl get all` | List all resources |
| `kubectl get ns` | List all namespaces |
| `kubectl get events` | See cluster events |

---

### 🔍 Inspect and Debug

| Command | What It Does |
|---------|-------------|
| `kubectl describe pod podname` | Full details of a pod |
| `kubectl describe node nodename` | Full details of a node |
| `kubectl logs podname` | View pod logs |
| `kubectl logs podname -f` | Stream pod logs live |
| `kubectl exec -it podname -- /bin/bash` | SSH into a running pod |
| `kubectl top nodes` | Show node CPU and memory usage |
| `kubectl top pods` | Show pod CPU and memory usage |

---

### 🛠️ Create and Manage

| Command | What It Does |
|---------|-------------|
| `kubectl apply -f file.yml` | Create or update resource from YAML |
| `kubectl delete -f file.yml` | Delete resource from YAML |
| `kubectl create namespace name` | Create a namespace |
| `kubectl scale deployment app --replicas=5` | Scale a deployment |
| `kubectl rollout status deployment/app` | Check rollout progress |
| `kubectl rollout undo deployment/app` | Rollback to previous version |
| `kubectl set image deployment/app app=nginx:1.25` | Update container image |

---

### 🧹 Clean Up

| Command | What It Does |
|---------|-------------|
| `kubectl delete pod name` | Delete a specific pod |
| `kubectl delete deployment name` | Delete a deployment |
| `kubectl delete svc name` | Delete a service |
| `kubectl delete all --all -n default` | Delete everything in default namespace |
| `kubectl delete namespace name` | Delete namespace and all its resources |
| `kind delete cluster --name name` | Delete entire KIND cluster |
| `kind delete clusters --all` | Delete ALL KIND clusters |

---

## 📂 Repository Structure

```
📁 kubestarter/
├── 📄 README.md
├── 📄 install.sh
├── 📁 cluster-configs/
│   ├── 📄 single-node.yml
│   ├── 📄 multi-node.yml
│   └── 📄 ha-cluster.yml
├── 📁 pods/
│   ├── 📄 simple-pod.yml
│   ├── 📄 multi-container-pod.yml
│   └── 📄 resource-limited-pod.yml
├── 📁 deployments/
│   ├── 📄 nginx-deployment.yml
│   ├── 📄 app-deployment.yml
│   └── 📄 rolling-update.yml
├── 📁 services/
│   ├── 📄 clusterip-svc.yml
│   ├── 📄 nodeport-svc.yml
│   └── 📄 loadbalancer-svc.yml
├── 📁 namespaces/
│   ├── 📄 dev-namespace.yml
│   ├── 📄 staging-namespace.yml
│   └── 📄 prod-namespace.yml
├── 📁 configmaps-secrets/
│   ├── 📄 configmap.yml
│   └── 📄 secret.yml
└── 📁 storage/
    ├── 📄 pv.yml
    └── 📄 pvc.yml
```

## 🗺️ Your Kubernetes Learning Roadmap

```
WEEK 1 TO 2 — BEGINNER
─────────────────────────────────────────────────
 ✅ Install Docker and KIND
 ✅ Create your first cluster
 ✅ Learn kubectl basics
 ✅ Understand Pods
 ✅ Write your first YAML
 ✅ Labels and Selectors

WEEK 3 TO 4 — INTERMEDIATE
─────────────────────────────────────────────────
 ✅ Deployments and ReplicaSets
 ✅ Services and Networking
 ✅ ConfigMaps and Secrets
 ✅ Namespaces and Quotas
 ✅ Persistent Volumes and Claims
 ✅ Rolling Updates and Rollbacks

WEEK 5 AND BEYOND — ADVANCED
─────────────────────────────────────────────────
 ✅ Helm Charts and Package Management
 ✅ Ingress Controllers
 ✅ RBAC and Security
 ✅ Network Policies
 ✅ Custom Resource Definitions
 ✅ Kubernetes Operators
 ✅ GitOps with ArgoCD
 ✅ Service Mesh with Istio
 ✅ CKA and CKAD Certification
```

---

## 🤝 Contributing to KubeStarter

We welcome contributions from every developer around the globe!

| Step | Action |
|------|--------|
| 1 | Fork this repository |
| 2 | Create a new branch: `git checkout -b feature/your-feature` |
| 3 | Make your changes and add new YAML configs or docs |
| 4 | Commit your changes: `git commit -m "Add your feature"` |
| 5 | Push to your branch: `git push origin feature/your-feature` |
| 6 | Open a Pull Request and describe your changes |

### Ways You Can Contribute

- 📝 Add new YAML configuration examples
- 📖 Improve or fix documentation
- 🧪 Add new hands-on lab exercises
- 🐛 Report bugs by opening an issue
- 🌐 Translate content to other languages
- ⭐ Star this repo to help others discover it

---

## ⭐ Support This Project

<div align="center">

**If KubeStarter helped you on your Kubernetes journey, please give it a star!**

**It is completely free and takes just one second — but it means everything to us!**

**Every single star helps another developer around the world discover Kubernetes!**

---

**🌍 Open to ALL developers worldwide**

Whether you are from 🇮🇳 India, 🇺🇸 USA, 🇬🇧 UK, 🇩🇪 Germany, 🇯🇵 Japan, 🇧🇷 Brazil, 🇦🇺 Australia, 🇨🇦 Canada, 🇿🇦 South Africa, or anywhere on Earth — you are welcome here!

---

### 💬 Words to Keep You Going

**"Every Kubernetes expert was once completely lost running their first kubectl command!"** 🚀

**"The only way to learn Kubernetes is to break things in Kubernetes!"** 🔥

**"Ship it. Break it. Fix it. Learn it. That is the DevOps way!"** ⚡

---

**Made with ❤️ by [Saatvik Bharija](https://github.com/bharijaSaatvik)**

**Happy Shipping! ⛵🚀**

<img src="https://komarev.com/ghpvc/?username=bharijaSaatvik&color=326CE5&style=for-the-badge&label=REPO+VISITORS" alt="Visitors"/>

</div>
