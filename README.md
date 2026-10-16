# Kube-Agents Applications & Workloads (`kube-agents-apps`)

This repository manages declarative Kubernetes workload manifests, Deployments, Services, and batch jobs partitioned across the GKE fleet in projects `gca-gke-test` and `gca-gke-2025`.

---

## 1. Directory Structure

Every cluster has a dedicated directory matching the taxonomy established in [`kube-agents-infra`](https://github.com/fkc1e100/kube-agents-infra):

```text
kube-agents-apps/
├── apps/
│   ├── gca-gke-test/
│   │   ├── README.md
│   │   ├── simple-app-cluster/       # cost-dashboard & simple-app
│   │   ├── gke-a2-ultra/             # openrl (gateway, scheduler, worker, vLLM Gemma)
│   │   ├── ka-webconsole-pr2321/     # web-console, litellm, public proxy
│   │   ├── gke-tpuv6-dws/            # slm-trainer (TPU v6e JAX)
│   │   └── kcc-management-cluster/   # Management cluster tenant base
│   └── gca-gke-2025/
│       ├── README.md
│       └── openrl-gpu-hub/           # openrl worker (3x NVIDIA L4 GPUs)
└── README.md
```

---

## 2. GitOps Integration

This repository is continuously reconciled by Argo CD running on `kcc-management-cluster`. Application workloads are decoupled by cluster to prevent scheduling conflicts and resource cross-contamination.
