# ✅ Prometheus-Notes ✅

## 🔹 What is Prometheus?
### Ans: Prometheus is an open-source monitoring and alerting system designed for cloud-native and containerized applications. It collects metrics, stores them as time-series data, and allows powerful querying using PromQL.
  * Originally developed at SoundCloud and now part of the CNCF.

## 🔹 Key Features
### Ans: 
* Pull-based metrics collection
* Powerful query language (PromQL)
* Multi-dimensional data model (labels)
* Built-in alerting
* Service discovery support (Kubernetes, EC2, Consul)
* Scalable & highly reliable
* Tight integration with Grafana

## 🔹 Prometheus Architecture
* Applications / Exporters
*         ↓
*    Prometheus Server
*    - Scraping
*    - Storage
*    - PromQL Engine
*        ↓
*   Alertmanager → Email / Slack / PagerDuty
*        ↓
*      Grafana

# 🔹 Core Components
## 1️⃣ Prometheus Server
### Ans: 
* Scrapes metrics from targets
* Stores data in TSDB (Time-Series Database)
* Executes PromQL queries

## 2️⃣ Exporters
### Ans: Exporters expose metrics in Prometheus format.
* Common exporters:
* Node Exporter – CPU, memory, disk
* Blackbox Exporter – HTTP, TCP checks
* MySQL / PostgreSQL Exporter
* Kube-State-Metrics
  * Example: http://localhost:9100/metrics

## 3️⃣ Service Discovery
### Ans: Automatically discovers targets:
  * Kubernetes
  * AWS EC2
  * Docker
  * Static configs

## 4️⃣ PromQL (Query Language)
### Ans: Used to query and analyze metrics.

## 5️⃣ Alertmanager
### ANs: 
* Handles alerts sent by Prometheus
* Deduplication
* Grouping
* Routing
### Supports:
* Email
* Slack
* PagerDuty
* Webhooks

## 6️⃣ Grafana
### Ans:
* Visualization tool
* Creates dashboards using Prometheus as data source.

## 🔹 Metrics Types
| Type      | Description                       |
| --------- | --------------------------------- |
| Counter   | Always increases (requests count) |
| Gauge     | Value can go up/down (CPU usage)  |
| Histogram | Tracks distributions (latency)    |
| Summary   | Similar to histogram (quantiles)  |

## 🔹 Prometheus vs CloudWatch
| Prometheus        | CloudWatch        |
| ----------------- | ----------------- |
| Pull-based        | Push-based        |
| Open-source       | AWS managed       |
| PromQL            | Limited query     |
| Kubernetes-native | AWS services only |

## 🔹 Prometheus in Kubernetes
* Deployed via Helm
* Uses Service Monitors
* Auto-discovers pods/services
* Integrates with EKS
  * Popular Stack:
  *  Prometheus + Alertmanager + Grafana

# THE END...
