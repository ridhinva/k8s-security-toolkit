# Kubernetes Security Toolkit

<p align="center">
  ![Stars](https://img.shields.io/github/stars/ridhinva/k8s-security-toolkit?style=for-the-badge)
  ![Forks](https://img.shields.io/github/forks/ridhinva/k8s-security-toolkit?style=for-the-badge)
  ![Issues](https://img.shields.io/github/issues/ridhinva/k8s-security-toolkit?style=for-the-badge)
  ![License](https://img.shields.io/github/license/ridhinva/k8s-security-toolkit?style=for-the-badge)
  ![Last Commit](https://img.shields.io/github/last-commit/ridhinva/k8s-security-toolkit?style=for-the-badge)
  ![Build Status](https://img.shields.io/github/actions/workflow/status/ridhinva/k8s-security-toolkit/ci.yml?style=for-the-badge)
  ![Kubernetes](https://img.shields.io/badge/Kubernetes-Security-critical?style=for-the-badge)
  ![Python](https://img.shields.io/badge/Python-3.10%2B-blue?style=for-the-badge&logo=python)
</p>

---

## 🎯 Overview

**Kubernetes security toolkit** for RBAC privilege escalation, container escape, admission controller bypass, ETCD exposure, and cloud metadata access.

| Check | Severity | Description |
|-------|----------|-------------|
| RBAC Privilege Escalation | 🔴 CRITICAL | cluster-admin bindings, role aggregation |
| Container Escape | 🔴 CRITICAL | runc/containerd CVEs, privileged pods |
| Admission Controller Bypass | 🟠 HIGH | ValidatingAdmissionWebhook misconfig |
| ETCD Unauthorized Access | 🔴 CRITICAL | Secrets dump via etcd |
| Kubelet Anonymous Auth | 🟠 HIGH | Pod/exec access without auth |
| Cloud Metadata Access | 🟠 HIGH | IMDSv2 bypass, IAM escalation |
| Service Mesh Misconfig | 🟡 MEDIUM | Istio/Linkerd mTLS bypass |
| CSI Driver Vulnerabilities | 🟡 MEDIUM | Volume mounting escapes |


---

## 🚀 Quick Start

```bash
git clone https://github.com/ridhinva/k8s-security-toolkit.git
cd k8s-security-toolkit
pip install requests kubernetes
python3 k8s_security_toolkit.py --target https://k8s-api:6443 --kubeconfig ~/.kube/config
```

---

## ⚖️ Disclaimer

For authorized security testing only.
