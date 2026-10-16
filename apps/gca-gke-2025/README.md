# Applications: `gca-gke-2025`

This directory contains declarative Kubernetes workload manifests partitioned by target cluster in GCP project `gca-gke-2025`.

## Directory Index

| Cluster Directory | Primary Workloads | Target Cluster |
| :--- | :--- | :--- |
| `openrl-gpu-hub/` | `openrl-gpu-worker` (3x NVIDIA L4 GPUs for distributed RL) | `openrl-gpu-hub` |
