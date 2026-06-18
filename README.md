🚀 Open-Source Data Platform — Built on Kubernetes from scratch

A production-grade, self-hosted Modern Data Platform deployed on virtual machines,
bootstrapped with a manually configured Kubernetes cluster (AWS EKS + EC2 worker nodes),
complete with custom network setup and static IP assignment.

## Architecture Overview
- **Orchestration** — Airflow with Kubernetes Executor for scalable pipeline execution
- **Streaming** — Apache Kafka with source/sink connectors for real-time CDC pipelines
- **Storage** — AWS S3 (Data Lake) · Delta Lake format (Lakehouse) · Data Warehouse/Data Mart
- **Processing** — Apache Spark (local cluster per pod)
- **Credential & Image Mgmt** — Harbor (container registry) · Kubernetes Secrets per namespace
- **Monitoring** — Prometheus for cluster-level metrics per container
- **CI/CD** — Version control, CI pipeline, and automated deployment (CD)

## Data Architecture
All pipelines follow the **Medallion Architecture** (Bronze → Silver → Gold),
supporting both **batch ETL** and **real-time CDC streaming** workflows.

Built for scalability, reproducibility, and observability — end to end.
