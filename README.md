# 🚀 Docker Projects & Experiments 🐳  

Welcome to the **Docker Projects Repository**! This collection features **Dockerized applications**, including **ML apps, databases, network experiments, and AWS deployments**.  

Each project showcases **real-world use cases** of containerization, helping you master **Docker for software development & cloud deployments**.  

---



## 📚 Learning Resources

Here are some useful resources I frequently refer to:

📖 [Official Docker Docs](https://docs.docker.com/)  
🎥 [Docker YouTube Playlist](https://www.youtube.com/c/Docker)  
📜 [Docker Cheat Sheet](https://dockerlabs.collabnix.com/docker/cheatsheet/)  

---

## 🛠 Prerequisites  

Make sure you have the following installed:  

✅ **Docker** → `docker --version`  
✅ **Python** (for Streamlit apps)  
✅ **AWS CLI** (for EC2 deployment)  

---

## 🚀 Projects & Experiments

Here are some exciting projects and experiments you can explore:

🔷 **[Streamlit Spiral Visualization](https://github.com/BhavyaDhimxn/container-experiments/tree/main/Exp-1)**: A Dockerized Streamlit app to generate interactive spiral patterns.

🔷 **[Binary Classification WebApp](https://github.com/BhavyaDhimxn/container-experiments/tree/main/Exp-2)**: A Streamlit-based ML app for binary classification using Logistic Regression.

🔷 **[Python Logging with Docker](https://github.com/BhavyaDhimxn/container-experiments/tree/main/Exp-3)**: Demonstrates best practices for logging inside a Dockerized Python environment.

🔷 **[Streamlit + PostgreSQL](https://github.com/BhavyaDhimxn/container-experiments/tree/main/Exp-4)**: Connect Streamlit with PostgreSQL database inside a Docker container.

🔷 **[MySQL Docker Container](https://github.com/BhavyaDhimxn/container-experiments/tree/main/Exp-5)**: Deploy a MySQL database container and connect it to applications.

🔷 **[Docker Network Experiment](https://github.com/BhavyaDhimxn/container-experiments/tree/main/Exp-6)**: Understand networking in Docker by connecting multiple containers.

🔷 **[ML Model Deployment with Evidently](https://github.com/BhavyaDhimxn/container-experiments/tree/main/Exp-7)**: Deploy an ML model with Evidently AI inside a Docker container.

🔷 **[Deploying on AWS EC2](https://github.com/BhavyaDhimxn/container-experiments/tree/main/Exp-8)**: Deploy Dockerized applications on an AWS EC2 instance.

🔷 **[Minikube with Docker](https://github.com/BhavyaDhimxn/container-experiments/tree/main/Exp-9)**: Run Kubernetes locally using Minikube with Docker.

🔷 **[Docker Bake](https://github.com/BhavyaDhimxn/container-experiments/tree/main/Exp-10)**: A Docker Bake implementation.

🔷 **[Titanic Survival Predictor](https://github.com/BhavyaDhimxn/container-experiments/tree/main/Exp-11)**: A machine learning application that predicts whether a passenger would have survived the Titanic disaster

🔷 **[Microservices Architecture with Docker Swarm ⚓](https://github.com/BhavyaDhimxn/container-experiments/tree/main/Exp-12)**: how to deploy a microservices architecture using Docker Swarm

---

### 🌟 **Spiral Visualization**  
📌 **Description:** A **Dockerized Streamlit app** to generate interactive spiral patterns.  
🛠 **How to Run:**  
```bash  
docker build -t streamlit-spiral .  
docker run -p 8501:8501 streamlit-spiral  
```
🔗 **[View Project](https://github.com/BhavyaDhimxn/container-experiments/tree/main/Exp-1)**  

---

### 🌟 **Binary Classification WebApp**  
📌 **Description:** A **Streamlit-based ML app** for binary classification using Logistic Regression.  
🛠 **How to Run:**  
```bash  
docker build -t binary-classifier .  
docker run -p 8501:8501 binary-classifier  
```
🔗 **[View Project Code](https://github.com/BhavyaDhimxn/container-experiments/tree/main/Exp-2)**  

---

### 🌟 **Python Logging with Docker**  
📌 **Description:** Demonstrates **best practices for logging** inside a **Dockerized Python environment**.  
🛠 **How to Run:**  
```bash  
docker build -t python-logging .  
docker run python-logging  
```
🔗 **[View Project](https://github.com/BhavyaDhimxn/container-experiments/tree/main/Exp-3)**  

---

### 🌟 **Streamlit + PostgreSQL**  
📌 **Description:** Connect **Streamlit with PostgreSQL database** inside a **Docker container**.  
🔗 **[View Project](https://github.com/BhavyaDhimxn/container-experiments/tree/main/Exp-4)**  

---

### 🌟 **MySQL Docker Container**  
📌 **Description:** Deploy a **MySQL database container** and connect it to applications.  
🔗 **[View Project](https://github.com/BhavyaDhimxn/container-experiments/tree/main/Exp-5)**  

---

### 🌟 **Docker Network Experiment**  
📌 **Description:** Understand **networking in Docker** by connecting multiple containers.  
🔗 **[View Project](https://github.com/BhavyaDhimxn/container-experiments/tree/main/Exp-6)**  

---

### 🌟 **ML Model Deployment with Evidently**  
📌 **Description:** Deploy an ML model with **Evidently AI** inside a Docker container.  
🔗 **[View Project](https://github.com/BhavyaDhimxn/container-experiments/tree/main/Exp-7)**  

---

### 🌟 **Deploying on AWS EC2**  
📌 **Description:** Deploy **Dockerized applications** on an **AWS EC2 instance**.  
🔗 **[View Project](https://github.com/BhavyaDhimxn/container-experiments/tree/main/Exp-8)**  

---

### 🌟 **Minikube with Docker**  
📌 **Description:** Run **Kubernetes locally** using Minikube with Docker.  
🔗 **[View Project](https://github.com/BhavyaDhimxn/container-experiments/tree/main/Exp-9)**  

---

### 🌟 **Docker Bake**  
📌 **Description:** A **Docker Bake** implementation.  

🔗 **[View Project](https://github.com/BhavyaDhimxn/container-experiments/tree/main/Exp-10)** 

---

### 🌟 **Titanic Survival Predictor**  
📌 **Description:** The **Titanic Survival Prediction Model** is a machine learning application that predicts whether a passenger would have survived the Titanic disaster based on various input features.   
🔗 **[View Project](https://github.com/BhavyaDhimxn/container-experiments/tree/main/Exp-11)**  

---

### 🌟 **Microservices Architecture with Docker Swarm ⚓**  
📌 **Description:** This guide explains how to deploy a microservices architecture using **Docker Swarm**, featuring an **API Gateway** and a **Backend Service**.  
🔗 **[View Project](https://github.com/BhavyaDhimxn/container-experiments/tree/main/Exp-12)**  

## 📚 Learning Resources  

📖 **[Docker Docs](https://docs.docker.com/)**  
📖 **[Streamlit Docs](https://docs.streamlit.io/)**  
📖 **[AWS CLI Setup](https://aws.amazon.com/cli/)**  

---



## 🤝 Contributions  

💡 Found a bug? **Open an issue!**  
✨ Have an idea? **Submit a PR!**  
📖 Want to improve docs? **Contribute!**  

---

🔥 **Happy Learning & Containerizing!** 🐳🚀

