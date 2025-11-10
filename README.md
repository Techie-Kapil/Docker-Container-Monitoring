# 📊 Docker Monitoring Stack — Prometheus + Grafana + cAdvisor + Node Exporter

## 🧩 Overview
This project provides a **complete Docker monitoring solution** using **Prometheus**, **Grafana**, **cAdvisor**, and **Node Exporter**.  
It enables you to **visualize real-time metrics** from your Docker containers and host system — such as CPU usage, memory utilization, disk I/O, network traffic, and container health.

The stack is fully containerized and can be launched using **Docker Compose** with minimal setup.

---

## 🏗️ Architecture

<img width="508" height="577" alt="image" src="https://github.com/user-attachments/assets/854d44e6-ed76-4d56-b3a4-2122f2bbe2a7" />


## 🧰 Components

### **1. Prometheus**
Prometheus is an open-source monitoring system that collects and stores time-series metrics.  
It scrapes data from **cAdvisor**, **Node Exporter**, and itself.

### **2. cAdvisor (Container Advisor)**
cAdvisor collects **container-level metrics** such as CPU, memory, file system, and network usage.  
It exposes metrics on `/metrics` endpoint that Prometheus scrapes periodically.

### **3. Node Exporter**
Node Exporter exposes **host machine metrics** like CPU load, disk I/O, memory, and filesystem utilization.

### **4. Grafana**

Grafana visualizes all collected metrics from Prometheus into dashboards and graphs.  
You can import pre-built community dashboards or create custom ones.

---

## 🚀 Quick Start

## 🚀 Quick Start

### **1️⃣ Clone the Repository**
```bash
git clone https://github.com/<your-username>/Monitoring.git
cd Monitoring
```
### **2️⃣ Start the Stack**
```bash
docker-compose up -d
```
### **3️⃣ Access the Services**

| Service           | URL                                                            | Description                                             |
| ----------------- | -------------------------------------------------------------- | ------------------------------------------------------- |
| **Prometheus**    | [http://localhost:9090](http://localhost:9090)                 | Metric storage and queries                              |
| **Grafana**       | [http://localhost:3000](http://localhost:3000)                 | Visualization dashboards (user: `admin`, pass: `admin`) |
| **cAdvisor**      | [http://localhost:8080](http://localhost:8080)                 | Container metrics explorer                              |
| **Node Exporter** | [http://localhost:9100/metrics](http://localhost:9100/metrics) | Host system metrics                                     |




