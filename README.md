<h2 align="center">Mohammed Zafeeruddin</h2>

<p align="center">
  SDE II · Platform / DevOps / MLOps · Hyderabad, India
</p>

<p align="center">
  <a href="https://zafeer.dev"><img src="https://img.shields.io/badge/portfolio-zafeer.dev-2f7d1e?style=flat-square" alt="Portfolio"></a>
  <a href="https://zafeer.dev/resume"><img src="https://img.shields.io/badge/resume-view_%2F_download-12160f?style=flat-square" alt="Resume"></a>
  <a href="https://www.linkedin.com/in/mohammed-zafeeruddin-3b5a82265"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
  <a href="mailto:mohammed.xafeer@gmail.com"><img src="https://img.shields.io/badge/email-mohammed.xafeer%40gmail.com-555?style=flat-square" alt="Email"></a>
  <a href="https://x.com/itsZafeer"><img src="https://img.shields.io/badge/@itsZafeer-000?style=flat-square&logo=x" alt="X"></a>
</p>

---

I write the Python services, pipelines and Kubernetes clusters behind production AI systems.

At work I own the platform side of **Baseer Builder**, a no-code computer-vision product. It runs on **50+ GPU nodes** and **2,000+ cameras** for a Saudi municipality, and I also deploy it into air-gapped government clusters. In my own time I build tools for awkward networks and Kubernetes on laptops.

```yaml
$ kubectl get engineer zafeer -o yaml
spec:
  writes:  [python, bash, typescript]
  runs:    [kubernetes, argocd, jenkins, vault, ansible, terraform]
  ships:   [training jobs, notebooks, device fleets, camera pipelines]
status:
  phase: Running   # since 2024-05, intern → SDE II
```

### 🔧 Open source

| Project | What it does |
| --- | --- |
| **[causeway](https://github.com/Zafeeruddin/causeway)** | View and record cameras behind VPNs, jump hosts and SSH tunnels. Each customer gets its own network namespace, live view uses WebRTC with HLS fallback, and recordings survive a dropped link. 298 tests. |
| **[kuiqctl](https://github.com/Zafeeruddin/kuiqctl)** | A single-node kubeadm cluster that stays `Ready` when your laptop changes Wi-Fi or gets a new DHCP lease. |
| **[cloudDoc](https://github.com/Zafeeruddin/cloudDoc)** | Private AWS EKS document pipeline: API Gateway → VPC Link → internal ALB, with workers on SQS, files in S3 and Pod Identity instead of static keys. |
| **[scribblr](https://github.com/Zafeeruddin/scribblr)** | A full-stack blog with comments, live notifications and Google/OTP auth on Cloudflare Workers + R2. Live at [codesphere.live](https://codesphere.live). |
| **[k8s-ops-toolkit](https://github.com/Zafeeruddin/k8s-ops-toolkit)** · **[k8s-monitoring](https://github.com/Zafeeruddin/k8s-monitoring)** | Ansible playbooks for k8s operations, and a Prometheus + Grafana monitoring stack. |
| **[Floating-IP](https://github.com/Zafeeruddin/Floating-IP)** · **[wireguard-vpn-setup](https://github.com/Zafeeruddin/wireguard-vpn-setup)** · **[ssh-tunnel](https://github.com/Zafeeruddin/ssh-tunnel)** | Small networking tools: Keepalived VIP failover, a WireGuard site link, and RTSP tunnels through jump hosts. |

### 🏗️ At work

- **Model training.** Training runs as a Kubernetes Job with pause, resume and priority, live MLflow metrics and Kafka progress events. PyTorch DDP cut a run from **55h to 5h**.
- **Notebooks and cameras.** Jupyter runs as StatefulSets, each on its own subdomain, and idle notebooks shut down automatically. A MediaMTX RTSP → HLS service handles thousands of cameras.
- **Device fleet.** A deploy-manager service runs Ansible from k8s Jobs to onboard, patch and deboard GPU machines, reporting a 7-phase lifecycle over Kafka.
- **Delivery.** Jenkins builds images and bumps tags in an infra repo that Argo CD syncs to dev, prod and EPM. Every secret lives in Vault, and a self-hosted Harbor registry serves 8 teams.
- **Platform setup.** Moved every service into k8s, cutting full platform deploy from **5 days to 2 hours**. Built HA NGINX on Keepalived and migrated from InfluxDB to ClickHouse.
- **Client deployments.** Air-gapped RAG and meeting-bot platforms for a Saudi ministry. An approval-gated Alibaba + Azure DevOps setup for Expro that saves **SAR 300K/yr**. Multi-VPC ACK for Monsha'at.

<details>
<summary><b>A few bugs I've enjoyed killing</b></summary>

<br>

- **Meeting bots stuck on one node.** A shared ReadWriteOnce volume plus a required podAffinity pinned every bot pod to one node. Bots now record to local disk and stream recordings back as a tar over `kubectl exec`, so they spread across all 4 workers.
- **A manifest that would have deleted 22 live secrets.** I caught it before apply, shipped a strategic-merge patch instead and reconciled the repo to zero drift.
- **The office subnet was blackholed.** A Docker bridge was allocating a /16 that overlapped it.
- **Deploys silently lost their config.** A Vault token expired with nothing renewing it.

</details>

### 🧰 Stack

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white) ![Bash](https://img.shields.io/badge/Bash-4EAA25?style=flat-square&logo=gnubash&logoColor=white) ![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white) ![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white) ![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white) ![Argo CD](https://img.shields.io/badge/Argo_CD-EF7B4D?style=flat-square&logo=argo&logoColor=white) ![Jenkins](https://img.shields.io/badge/Jenkins-D24939?style=flat-square&logo=jenkins&logoColor=white) ![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white) ![Terraform](https://img.shields.io/badge/Terraform-844FBA?style=flat-square&logo=terraform&logoColor=white) ![Ansible](https://img.shields.io/badge/Ansible-EE0000?style=flat-square&logo=ansible&logoColor=white) ![Vault](https://img.shields.io/badge/Vault-000000?style=flat-square&logo=vault&logoColor=white) ![NGINX](https://img.shields.io/badge/NGINX-009639?style=flat-square&logo=nginx&logoColor=white) ![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white) ![MLflow](https://img.shields.io/badge/MLflow-0194E2?style=flat-square&logo=mlflow&logoColor=white) ![Kafka](https://img.shields.io/badge/Kafka-231F20?style=flat-square&logo=apachekafka&logoColor=white) ![ClickHouse](https://img.shields.io/badge/ClickHouse-FFCC01?style=flat-square&logo=clickhouse&logoColor=black) ![Postgres](https://img.shields.io/badge/Postgres-4169E1?style=flat-square&logo=postgresql&logoColor=white) ![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white) ![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=flat-square&logo=prometheus&logoColor=white) ![Grafana](https://img.shields.io/badge/Grafana-F46800?style=flat-square&logo=grafana&logoColor=white) ![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonwebservices&logoColor=white) ![Alibaba Cloud](https://img.shields.io/badge/Alibaba_Cloud-FF6A00?style=flat-square&logo=alibabacloud&logoColor=white) ![Cloudflare](https://img.shields.io/badge/Cloudflare-F38020?style=flat-square&logo=cloudflare&logoColor=white)

---

<sub>Open to Platform, MLOps and AI-infrastructure roles: remote, UAE or KSA. The fastest way to reach me is [email](mailto:mohammed.xafeer@gmail.com).</sub>
