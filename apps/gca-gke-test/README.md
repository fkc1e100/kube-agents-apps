# Applications: `gca-gke-test`

This directory contains declarative Kubernetes workload manifests partitioned by target cluster in GCP project `gca-gke-test`.

## Directory Index

| Cluster Directory | Primary Workloads | Target Cluster |
| :--- | :--- | :--- |
| `simple-app-cluster/` | `cost-dashboard` (UI & Cloud SQL Proxy), `simple-app` (2-tier demo) | `simple-app-cluster` |
| `gke-a2-ultra/` | `openrl-system` (Redis, Gateway, Scheduler, Trainer Worker, vLLM Gemma) | `gke-a2-ultra` |
| `ka-webconsole-pr2321/` | `web-console`, `litellm` inference gateway, `public-proxy` | `ka-webconsole-pr2321` |
| `gke-tpuv6-dws/` | `slm-trainer` (Gemma 2B / Keras 3 JAX on TPU v6e Trillium) | `gke-tpuv6-dws` |
| `kcc-management-cluster/` | Fleet tenant root namespace & cluster metadata | `kcc-management-cluster` |
