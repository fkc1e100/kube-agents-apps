# Kube-Agents Applications & Workloads (`kube-agents-apps`)

This repository manages declarative Kubernetes workload manifests, Deployments, Services, and Helm releases for applications running across the GKE fleet in project `gca-gke-test`.

---

## 1. Directory Structure

```text
kube-agents-apps/
├── apps/
│   ├── cost-dashboard/   # GKE Cost Dashboard UI & backend manifests
│   ├── openrl/           # OpenRL reinforcement learning scheduler & gateway
│   └── simple-app/       # Two-tier reference web application
└── README.md
```

---

## 2. GitOps Integration

This repository is continuously reconciled by the Argo CD `fleet-applications` controller running on `kcc-management-cluster`.
