
📈 Monitoring Stack with Prometheus, Grafana & Node Exporter
This project sets up a monitoring system using Docker containers for:

Prometheus (metrics collection)

Grafana (visualization)

Node Exporter (system metrics)

🧰 Technologies Used
Docker

Prometheus

Grafana

Node Exporter

GitHub Actions (CI/CD)

🚀 Getting Started
1. Clone the Repo
bash
Copy
Edit
git clone https://github.com/your-username/monitoring-stack.git
cd monitoring-stack
2. Start Containers
bash
Copy
Edit
docker run -d --name=prometheus -p 9090:9090 -v $PWD/prometheus.yml:/etc/prometheus/prometheus.yml prom/prometheus
docker run -d --name=node-exporter -p 9100:9100 prom/node-exporter
docker run -d --name=grafana -p 3000:3000 -e "GF_SECURITY_ADMIN_PASSWORD=admin" grafana/grafana
📊 Access Dashboards
Prometheus UI: http://localhost:9090

Grafana UI: http://localhost:3000

Login: admin / admin (or your custom password)

Add Prometheus data source

Import dashboard ID 1860 (Node Exporter Full)

🔄 GitHub Actions (CI/CD)
GitHub Actions runs CI jobs automatically on push.

Example workflow:
📁 .github/workflows/monitoring.yml

yaml
Copy
Edit
name: Docker Image CI

on:
  push:
    branches: [ main ]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - name: Build Docker image
        run: docker build -t monitoring-stack .
![image](https://github.com/user-attachments/assets/0f65142c-235d-4ad8-a5d5-6ba837177bd3)
![image](https://github.com/user-attachments/assets/9f9fb2bd-ceca-40bc-8e6c-66585c0d4e8a)
![image](https://github.com/user-attachments/assets/bee4b8e3-3b9d-4843-ad10-b9a3ebf4b685)
![image](https://github.com/user-attachments/assets/63737683-70aa-4650-b836-9b7a528e069f)
![image](https://github.com/user-attachments/assets/22de99d3-d9d8-4810-8bd4-ff274277276a)




# prometheusAndGrafana
