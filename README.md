# Server CPU Monitoring with Prometheus, Grafana & Alertmanager

This project provides a minimal monitoring setup to track **CPU usage** on a Windows machine using the Prometheus ecosystem. All services run through **Docker Compose**, making the environment easy to start, stop, and reproduce.

---

## 📌 Features

* Collects CPU metrics using **Node Exporter**
* Stores time-series data in **Prometheus**
* Visualizes CPU usage with **Grafana dashboards**
* Sends alerts for high CPU usage using **Alertmanager**
* Fully containerized with **Docker Compose**

---

## 🛠 Technologies Used

* **Prometheus**
* **Grafana**
* **Alertmanager**
* **Node Exporter**
* **Docker Compose**
* **Windows (host environment)**

---

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/<your-username>/<your-repo>.git
cd <your-repo>
```

### 2. Start the Monitoring Stack

```bash
docker-compose up -d
```

This will start:

* Prometheus on **localhost:9090**
* Grafana on **localhost:3000**
* Alertmanager on **localhost:9093**

### 3. Access Grafana

Open your browser:

```
http://localhost:3000
```

Default login:

* **User:** admin
* **Password:** admin

You can import or create dashboards to visualize CPU usage.

---

## 📊 Alerting

Alertmanager is configured to send alerts when CPU usage exceeds a defined threshold.
You can modify alert rules inside:

```
./prometheus/alert.rules.yml
```

---

## 📁 Project Structure

```
.
├── docker-compose.yml
├── prometheus/
│   ├── prometheus.yml
│   └── alert.rules.yml
├── grafana/
│   └── provisioning/
└── README.md
```

---

## 🧹 Stopping the Stack

```bash
docker-compose down
```


This project is for educational and demonstration purposes.

---

If you want, I can also generate diagrams, improve the structure, or add screenshots.
