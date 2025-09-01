
# 🚀 Kubernetes Minikube Demo Project  
This project demonstrates how to deploy and expose a simple **Nginx web application** using **Kubernetes** with **Minikube**.  
It’s a beginner-friendly project that shows the basics of working with Kubernetes deployments and services locally.  
---
## 📌 Project Overview  
In this project, we:  
1. Start a Kubernetes cluster locally using **Minikube**  
2. Create a **Deployment** for an Nginx container  
3. Expose the app using a **Service** so it can be accessed in a web browser  
---
## 🛠 Tools & Technologies  

- 🐳 Docker → Used as the container runtime (driver for Minikube)  
- ☸️ Kubernetes (Minikube)** → Local Kubernetes cluster  
- 🖥️ kubectl → Kubernetes command-line tool  
- 📄 YAML → Declarative configuration for Deployment & Service  
---
## 📂 Project Structure  
k8s-demo/
 ├── deployment.yaml    # Kubernetes Deployment (Nginx Pod)
 
 ├── service.yaml       # Kubernetes Service (NodePort)
 
 └── README.md          # Project documentation
 
⚙️ Setup & Usage

1️⃣ Start Minikube
minikube start --driver=docker

2️⃣ Create a Deployment
kubectl apply -f deployment.yaml
Expected output:
deployment.apps/my-app created

3️⃣ Create a Service
kubectl apply -f service.yaml
Expected output:
service/my-app-service created

4️⃣ Verify Deployment & Service
kubectl get pods
kubectl get services

5️⃣ Access the App in Browser
minikube service my-app-service
This will open the Nginx welcome page 🎉

📖 Key Learnings
1.Running Kubernetes locally with Minikube

2.Writing YAML manifests (Deployment & Service)

3.Managing Pods & Services with kubectl

4.Understanding how apps are deployed & exposed in Kubernetes

👨‍💻 Author
Gaurav Kumar
🔗 GitHub Repo: k8s-demo


