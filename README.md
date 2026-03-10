
DevOps Monitoring System 📊

This project demonstrates how a production system is monitored in real-time. It sets up a Kubernetes cluster environment and deploys Prometheus for metric scraping and Grafana for visual dashboards to track system health, CPU, memory, and pod status.

🚀 Features

Server Monitoring: Tracks overall cluster node health.

CPU & Memory Usage: Real-time metrics for resource utilization.

Pod Health: Monitors the uptime, restarts, and status of Kubernetes workloads.

Sample Application: Includes a dummy application to generate actionable metrics.

🛠️ Tools Used

Prometheus: Time-series database for scraping and storing metrics.

Grafana: Visualization platform for creating comprehensive dashboards.

Kubernetes: Container orchestration platform.

📁 Repository Structure

monitoring-project/
├── README.md                           # Project documentation
├── prometheus-config/                  
│   └── prometheus-setup.yaml           # Roles, ConfigMap, Deployment, and Service for Prometheus
├── grafana-dashboard/                  
│   └── grafana-setup.yaml              # Deployment and Service for Grafana
└── kubernetes-yaml/                    
    └── sample-app.yaml                 # Sample Nginx app to monitor


⚙️ Setup Instructions

Prerequisites: You need a running Kubernetes cluster (like Minikube, kind, or an EKS/GKE cluster) and kubectl configured.

Deploy the Sample Application:

kubectl apply -f kubernetes-yaml/sample-app.yaml


Deploy Prometheus:

kubectl apply -f prometheus-config/prometheus-setup.yaml


Deploy Grafana:

kubectl apply -f grafana-dashboard/grafana-setup.yaml


Access the Dashboards:

Prometheus: kubectl port-forward svc/prometheus-service 9090:9090 (Access at http://localhost:9090)

Grafana: kubectl port-forward svc/grafana-service 3000:3000 (Access at http://localhost:3000)

Default Login: admin / admin

Add Prometheus as a Data Source: URL -> http://prometheus-service.default.svc.cluster.local:8080

💼 Resume Integration

Add this bullet point to your resume under your Projects or Experience section:

"Implemented real-time monitoring using Prometheus and Grafana for Kubernetes workloads, ensuring high availability by tracking CPU usage, memory consumption, and Pod health.
