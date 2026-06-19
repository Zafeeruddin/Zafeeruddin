<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Zafeer - GitHub Profile README HTML</title>
  <style>
    :root {
      --bg: #0d1117;
      --panel: #161b22;
      --panel-2: #21262d;
      --text: #e6edf3;
      --muted: #8b949e;
      --border: #30363d;
      --accent: #58a6ff;
      --green: #3fb950;
      --purple: #bc8cff;
      --orange: #f0883e;
    }

    * { box-sizing: border-box; }

    body {
      margin: 0;
      background: radial-gradient(circle at top, #1f2937 0, #0d1117 45%, #010409 100%);
      color: var(--text);
      font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, Arial, sans-serif;
      line-height: 1.6;
    }

    a { color: var(--accent); text-decoration: none; }
    a:hover { text-decoration: underline; }

    .container {
      max-width: 1040px;
      margin: 0 auto;
      padding: 40px 20px 80px;
    }

    .hero {
      text-align: center;
      padding: 46px 28px;
      border: 1px solid var(--border);
      background: linear-gradient(135deg, rgba(88, 166, 255, 0.14), rgba(188, 140, 255, 0.10)), var(--panel);
      border-radius: 24px;
      box-shadow: 0 24px 80px rgba(0, 0, 0, 0.35);
    }

    .hero h1 {
      margin: 0 0 12px;
      font-size: clamp(2.2rem, 6vw, 4.5rem);
      letter-spacing: -1.5px;
    }

    .hero p {
      max-width: 820px;
      margin: 0 auto 20px;
      color: var(--muted);
      font-size: 1.08rem;
    }

    .links {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 10px;
      margin-top: 22px;
    }

    .pill {
      border: 1px solid var(--border);
      background: rgba(33, 38, 45, 0.9);
      color: var(--text);
      padding: 8px 14px;
      border-radius: 999px;
      font-size: 0.95rem;
    }

    .section {
      margin-top: 26px;
      padding: 28px;
      border: 1px solid var(--border);
      background: rgba(22, 27, 34, 0.92);
      border-radius: 20px;
    }

    .section h2 {
      margin: 0 0 16px;
      font-size: 1.55rem;
      letter-spacing: -0.3px;
    }

    .section h3 {
      margin: 22px 0 10px;
      color: var(--text);
      font-size: 1.12rem;
    }

    .grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
      gap: 14px;
    }

    .card {
      border: 1px solid var(--border);
      background: var(--panel-2);
      border-radius: 16px;
      padding: 18px;
    }

    .card strong { color: #ffffff; }

    .metric {
      font-size: 1.75rem;
      color: var(--green);
      font-weight: 800;
      line-height: 1.2;
    }

    .muted { color: var(--muted); }

    .tags {
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
      margin-top: 10px;
    }

    .tag {
      display: inline-block;
      border: 1px solid var(--border);
      background: #0d1117;
      border-radius: 999px;
      padding: 6px 10px;
      color: var(--muted);
      font-size: 0.9rem;
    }

    code, pre {
      font-family: ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, "Liberation Mono", monospace;
    }

    pre {
      overflow-x: auto;
      padding: 16px;
      border-radius: 14px;
      background: #010409;
      border: 1px solid var(--border);
      color: #c9d1d9;
    }

    ul { padding-left: 22px; }
    li { margin: 5px 0; }

    .two-col {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 14px;
    }

    .timeline {
      border-left: 2px solid var(--border);
      padding-left: 18px;
    }

    .timeline-item {
      position: relative;
      margin-bottom: 22px;
    }

    .timeline-item::before {
      content: "";
      position: absolute;
      left: -26px;
      top: 6px;
      width: 12px;
      height: 12px;
      border-radius: 50%;
      background: var(--accent);
      box-shadow: 0 0 0 4px rgba(88, 166, 255, 0.16);
    }

    .cta {
      text-align: center;
      margin-top: 26px;
      padding: 28px;
      border-radius: 20px;
      border: 1px solid var(--border);
      background: linear-gradient(135deg, rgba(63, 185, 80, 0.10), rgba(88, 166, 255, 0.10)), var(--panel);
    }

    .copy-box {
      width: 100%;
      min-height: 520px;
      background: #010409;
      color: #d1d5db;
      border: 1px solid var(--border);
      border-radius: 14px;
      padding: 16px;
      resize: vertical;
      font-family: ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, "Liberation Mono", monospace;
      font-size: 13px;
      line-height: 1.5;
      white-space: pre;
    }

    .button-row {
      display: flex;
      gap: 10px;
      flex-wrap: wrap;
      margin-bottom: 12px;
    }

    button {
      cursor: pointer;
      border: 1px solid var(--border);
      background: var(--accent);
      color: #061322;
      font-weight: 700;
      border-radius: 10px;
      padding: 10px 14px;
    }

    button.secondary {
      background: var(--panel-2);
      color: var(--text);
    }

    .note {
      color: var(--muted);
      font-size: 0.92rem;
      margin-top: 8px;
    }

    @media print {
      body { background: white; color: #111827; }
      .section, .hero, .card, .cta { background: white; color: #111827; border-color: #d1d5db; box-shadow: none; }
      .muted, .tag, .hero p { color: #4b5563; }
      a { color: #0366d6; }
      pre, .copy-box { background: #f6f8fa; color: #111827; }
    }
  </style>
</head>
<body>
  <main class="container">
    <section class="hero">
      <h1>Hey, I'm Zafeer 👋</h1>
      <p><strong>Platform / DevOps Engineer specializing in Kubernetes-based AI Infrastructure, MLOps, GPU Workloads, CI/CD, and On-Prem / Air-Gapped Deployments.</strong></p>
      <div class="links">
        <a class="pill" href="https://www.linkedin.com/in/your-linkedin/">LinkedIn</a>
        <a class="pill" href="mailto:your-email@example.com">Email</a>
        <a class="pill" href="https://github.com/your-username">GitHub</a>
      </div>
    </section>

    <section class="section">
      <h2>🚀 About Me</h2>
      <p>I build and operate production-grade infrastructure for AI, computer vision, and MLOps platforms.</p>
      <p>My work sits at the intersection of Kubernetes platform engineering, GPU-based model training, CI/CD, GitOps, observability, secrets management, hybrid cloud, and on-prem / air-gapped deployments.</p>
      <p>I have worked on high-scale AI/CV platforms involving <strong>50+ Kubernetes nodes</strong>, <strong>2,000+ cameras</strong>, <strong>50+ GPU machines</strong>, and <strong>200+ computer vision use cases</strong> across government and enterprise environments.</p>
    </section>

    <section class="section">
      <h2>🧠 Core Engineering Focus</h2>
      <div class="tags">
        <span class="tag">AI Platform Engineering</span>
        <span class="tag">Kubernetes Infrastructure</span>
        <span class="tag">MLOps / ML Training Orchestration</span>
        <span class="tag">GPU Workload Scheduling</span>
        <span class="tag">CI/CD and GitOps</span>
        <span class="tag">On-Prem / Air-Gapped Deployments</span>
        <span class="tag">Computer Vision Infrastructure</span>
        <span class="tag">Cloud + Hybrid Infrastructure</span>
        <span class="tag">Observability and Reliability</span>
        <span class="tag">Infrastructure Automation</span>
        <span class="tag">Edge / Device Onboarding</span>
      </div>
    </section>

    <section class="section">
      <h2>🛠️ Tech Stack</h2>
      <div class="two-col">
        <div class="card"><strong>Platform & DevOps</strong><br>Kubernetes, Docker, ArgoCD, Jenkins, GitHub Actions, Azure DevOps, Terraform, Ansible</div>
        <div class="card"><strong>Cloud, Infra & Networking</strong><br>AWS, Alibaba Cloud, NGINX, HAProxy, MetalLB, Harbor, Keepalived, NFS/NAS</div>
        <div class="card"><strong>MLOps, AI & Data</strong><br>Python, PyTorch, MLflow, Kafka, Qdrant, Redis, InfluxDB, Postgres</div>
        <div class="card"><strong>Observability & Security</strong><br>Prometheus, Grafana, HashiCorp Vault, New Relic, Alerting</div>
      </div>
    </section>

    <section class="section">
      <h2>🏗️ Highlight: AI / Computer Vision Platform Infrastructure</h2>
      <p>I worked on a low-code / no-code computer vision platform covering the full AI lifecycle:</p>
      <pre>Data Collection
↓
Labelling
↓
Model Training
↓
Custom Notebook Training
↓
Real-Time Inference
↓
Camera Management
↓
Device Onboarding
↓
Analytics Dashboards</pre>
      <p>The platform supported large-scale government AI/CV infrastructure with:</p>
      <ul>
        <li>200+ AI/CV use cases</li>
        <li>2,000+ cameras</li>
        <li>50+ GPU machines</li>
        <li>Multi-environment Kubernetes deployments</li>
        <li>On-prem and air-gapped infrastructure</li>
        <li>Real-time camera inference</li>
        <li>Large-scale model training and deployment workflows</li>
      </ul>
    </section>

    <section class="section">
      <h2>⚡ Key Engineering Wins</h2>
      <div class="grid">
        <div class="card"><div class="metric">55h → 5h</div><strong>Reduced model training time by ~90%</strong><br><span class="muted">Built distributed training infrastructure using PyTorch DDP and GPU pooling.</span></div>
        <div class="card"><div class="metric">50+ nodes</div><strong>Operated Kubernetes infrastructure</strong><br><span class="muted">Administered multi-environment clusters for platform, training, inference, DBs, notebooks, and observability.</span></div>
        <div class="card"><div class="metric">$1k saved</div><strong>Self-hosted Harbor registry</strong><br><span class="muted">Hosted Harbor locally on NAS, proxied over NGINX, with team-based access and backups.</span></div>
        <div class="card"><div class="metric">300k SAR</div><strong>Saved yearly infra cost</strong><br><span class="muted">Architected a tightly scoped deployment environment for a Saudi government-related client.</span></div>
      </div>

      <h3>Built production CI/CD pipelines</h3>
      <ul>
        <li>Linting changed services</li>
        <li>Selecting deployment environments</li>
        <li>Building Docker images</li>
        <li>Pushing images to Harbor registry</li>
        <li>Updating image tags and Kubernetes manifests</li>
        <li>Deploying across dev, prod, and client environments</li>
        <li>Managing environment variables through HashiCorp Vault</li>
        <li>Maintaining semantic versioning</li>
        <li>Enabling multi-environment deployments</li>
      </ul>

      <h3>Built HA NGINX architecture</h3>
      <ul>
        <li>Removed a single point of failure using Keepalived and a virtual IP</li>
        <li>Used multiple NGINX machines for failover routing</li>
        <li>Kept NGINX configuration Git-backed and synced</li>
      </ul>

      <h3>Built device onboarding infrastructure</h3>
      <ul>
        <li>Migrated from Bash-heavy scripts to Python microservices, Kubernetes Jobs, Ansible roles, and Kafka-based status communication</li>
        <li>Supported single-device onboarding, bulk onboarding, device patching, device deboarding, destructive cleanup, and unified health monitoring</li>
        <li>Handled Kubernetes cluster creation or node joining, NVIDIA driver setup, container runtime setup, Docker setup, image pre-pulling, and persistent device services</li>
      </ul>
    </section>

    <section class="section">
      <h2>🔬 MLOps Systems I Have Built</h2>
      <h3>Model Training Orchestration</h3>
      <ul>
        <li>On-demand model training system running as Kubernetes Jobs</li>
        <li>Detection, classification, and segmentation support</li>
        <li>Multiple architectures and pretrained weights</li>
        <li>Distributed GPU training with PyTorch DDP</li>
        <li>MLflow integration and real-time metric reporting</li>
        <li>Pause, stop, resume, and priority controls</li>
        <li>Kafka-based progress tracking</li>
        <li>Logger and status microservices</li>
        <li>Resilience across interruptions and reboots</li>
      </ul>

      <h3>Jupyter Notebook Platform</h3>
      <ul>
        <li>Each notebook exposed through a live subdomain</li>
        <li>Ingress-based routing and ingress controller integration</li>
        <li>Persistent storage on NFS/NAS</li>
        <li>StatefulSet-based deployment</li>
        <li>Automatic idle monitoring, warning, and cleanup</li>
        <li>MetalLB load balancing for on-prem Kubernetes</li>
        <li>Persistent notebook code across restarts</li>
      </ul>

      <h3>Face Registration Service</h3>
      <ul>
        <li>On-demand Kubernetes Job-based execution</li>
        <li>Multiple face model support</li>
        <li>Embedding generation and Qdrant vector database integration</li>
        <li>Scalable face registration workflow</li>
      </ul>
    </section>

    <section class="section">
      <h2>🎥 Computer Vision / Camera Infrastructure</h2>
      <p>Built and optimized camera management services for real-time streaming workloads.</p>
      <ul>
        <li>RTSP streams and HLS conversion</li>
        <li>MediaMTX integration</li>
        <li>Custom camera management APIs</li>
        <li>Multi-camera inference workflows</li>
        <li>Stream lifecycle management</li>
        <li>Camera uptime metrics</li>
        <li>Prometheus/Grafana dashboards</li>
        <li>Add/remove camera APIs</li>
        <li>Stream expiration handling</li>
        <li>Real-time camera health monitoring</li>
      </ul>
    </section>

    <section class="section">
      <h2>🧪 Early Computer Vision PoCs</h2>
      <div class="timeline">
        <div class="timeline-item"><h3>Ajdan</h3><p>Built a camera-stream-based crowd detection PoC with model training, live inference, real-time counting, and male/female/children class detection.</p></div>
        <div class="timeline-item"><h3>King Salman Military Base</h3><p>Worked on employee availability, unauthorized access detection, child/person class detection, officer availability checks, and alert generation.</p></div>
        <div class="timeline-item"><h3>Gold Chain</h3><p>Worked on multi-class computer vision classification, employee availability, people entering/exiting shops, and multi-camera inference.</p></div>
        <div class="timeline-item"><h3>Dubai Airport</h3><p>Worked on a high-stakes turnaround management system PoC. Built automated stream recovery using Python, Selenium, and SMTP to monitor stream health, refresh cookies, restart streams, and send notifications.</p></div>
      </div>
    </section>

    <section class="section">
      <h2>☁️ Client / Deployment Experience</h2>
      <h3>Eastern Provincial Municipality — Saudi Arabia</h3>
      <p>Worked on infrastructure and MLOps execution for a high-scale computer vision project involving 200+ use cases, 2,000+ cameras, 50+ GPU machines, on-prem Kubernetes, training/inference workloads, device onboarding, monitoring, and alerting.</p>

      <h3>Ministry of Economy and Petroleum — Saudi Arabia</h3>
      <p>Worked on deployment architecture for AI platforms in air-gapped, on-prem environments.</p>
      <ul>
        <li><strong>AmplifAI — RAG Platform:</strong> Dockerized and deployed services across dev, staging, and production with Kubernetes YAML, DB connectivity, block storage, and ingress routing.</li>
        <li><strong>AmplifAI Meetings — Meeting Bot:</strong> Architected and deployed meeting bot services in an air-gapped on-prem Kubernetes environment.</li>
      </ul>

      <h3>Expro — Saudi Government-Related Expenditure Entity</h3>
      <ul>
        <li>Alibaba ECS deployments</li>
        <li>Alibaba Container Registry</li>
        <li>Azure DevOps blue-green CI/CD pipelines</li>
        <li>Approval-based deployments and rollback support</li>
        <li>Multi-environment deployment flow</li>
        <li>Local HashiCorp Vault setup</li>
        <li>Saved approximately 300k SAR yearly</li>
      </ul>

      <h3>Monsha'at — Saudi Government Entity</h3>
      <ul>
        <li>Deployed AI services on Alibaba ECS</li>
        <li>Deployed platform services on Alibaba ACK Kubernetes</li>
        <li>Created multiple VPCs</li>
        <li>Supported private connectivity between services</li>
      </ul>
    </section>

    <section class="section">
      <h2>🧱 Infrastructure Work</h2>
      <div class="tags">
        <span class="tag">On-prem Kubernetes architecture</span>
        <span class="tag">HAProxy high availability</span>
        <span class="tag">Kubernetes administration</span>
        <span class="tag">NGINX reverse proxying</span>
        <span class="tag">Keepalived virtual IP failover</span>
        <span class="tag">Harbor registry hosting</span>
        <span class="tag">NAS-mounted registry storage</span>
        <span class="tag">Vault secrets management</span>
        <span class="tag">Terraform automation</span>
        <span class="tag">Ansible provisioning</span>
        <span class="tag">Docker image optimization</span>
        <span class="tag">Multi-stage Docker builds</span>
        <span class="tag">Docker Compose packaging</span>
        <span class="tag">Prometheus scraping</span>
        <span class="tag">Grafana dashboards</span>
        <span class="tag">Alerting</span>
        <span class="tag">StatefulSets</span>
        <span class="tag">Redis / InfluxDB persistence</span>
        <span class="tag">Kubeflow Trainer integration</span>
        <span class="tag">Air-gapped Kubernetes deployment</span>
      </div>
    </section>

    <section class="section">
      <h2>📌 Featured Projects</h2>
      <h3>CloudPad — Kubernetes Sandbox Environment</h3>
      <p><strong>Tech:</strong> React, FastAPI, Kubernetes, Docker, AWS EC2, Ingress NGINX, Claude MCP</p>
      <pre>Two pods share the same persistent volume:

1. Code writer / editor pod
2. Code serving pod</pre>
      <ul>
        <li>Live code editing</li>
        <li>Chatbot-based code modification</li>
        <li>VS Code web server</li>
        <li>Live deployable links</li>
        <li>Kubernetes-based sandbox environments</li>
        <li>Persistent volume sharing between pods</li>
        <li>Real-time code reflection</li>
        <li>Isolated sandbox environments</li>
      </ul>

      <h3>Medium Clone — Full-Stack Blogging Platform</h3>
      <p><strong>Tech:</strong> React, HonoJS, Cloudflare Workers, Cloudflare Pages, Redis, Postgres, Prisma, New Relic</p>
      <ul>
        <li>Google authentication and OTP authentication</li>
        <li>Comments, replies, notifications, and blog engagement</li>
        <li>Cloudflare Workers backend and Cloudflare Pages deployment</li>
        <li>Postgres on Aiven and Prisma Accelerate</li>
        <li>GitHub Actions CI/CD and New Relic monitoring</li>
        <li>S3 + CDN frontend deployment and Cloudflare R2 image hosting</li>
      </ul>
      <p><strong>Live:</strong> codesphere.live</p>

      <h3>ReminderBot — WhatsApp Reminder System</h3>
      <p><strong>Tech:</strong> Python, Celery, Postgres, Twilio</p>
      <ul>
        <li>WhatsApp reminders</li>
        <li>Recurring daily reminders</li>
        <li>Single-use reminders</li>
        <li>Celery-based scheduling</li>
        <li>Postgres persistence</li>
        <li>Twilio integration</li>
      </ul>
    </section>

    <section class="section">
      <h2>🧩 Architecture Areas I Care About</h2>
      <pre>How do we deploy AI workloads safely?
How do we make Kubernetes usable for AI teams?
How do we reduce model training time?
How do we onboard edge/GPU devices reliably?
How do we deploy in air-gapped environments?
How do we make CI/CD safe, observable, and rollback-friendly?
How do we make infrastructure repeatable with Terraform and Ansible?
How do we monitor thousands of cameras and AI services?
How do we remove single points of failure?
How do we run GPU workloads reliably on Kubernetes?
How do we make on-prem AI infrastructure feel cloud-like?
How do we build platforms that developers actually enjoy using?</pre>
    </section>

    <section class="section">
      <h2>🎯 Roles I Am Best Aligned With</h2>
      <div class="tags">
        <span class="tag">Platform Engineer</span>
        <span class="tag">MLOps Engineer</span>
        <span class="tag">AI Infrastructure Engineer</span>
        <span class="tag">DevOps Engineer — Kubernetes</span>
        <span class="tag">Cloud Infrastructure Engineer</span>
        <span class="tag">Kubernetes Engineer</span>
        <span class="tag">SRE — AI / Platform / Infrastructure</span>
        <span class="tag">Infrastructure Engineer — On-Prem / Hybrid Cloud</span>
        <span class="tag">DevOps Engineer — GPU / ML Workloads</span>
        <span class="tag">Platform Engineer — Computer Vision / AI Products</span>
      </div>
    </section>

    <section class="section">
      <h2>🌍 Markets I Am Open To</h2>
      <ul>
        <li>UAE</li>
        <li>Saudi Arabia</li>
        <li>Gulf region</li>
        <li>Remote international teams</li>
        <li>Hybrid cloud / on-prem AI infrastructure teams</li>
        <li>AI platform teams</li>
        <li>Computer vision infrastructure teams</li>
        <li>DevOps / platform teams serving ML engineers</li>
      </ul>
    </section>

    <section class="section">
      <h2>📫 Reach Me</h2>
      <pre>Email: your-email@example.com
LinkedIn: https://www.linkedin.com/in/your-linkedin/
GitHub: https://github.com/your-username</pre>
    </section>

    <section class="cta">
      <h2>Building reliable infrastructure for AI systems that need to work outside demos — in real production environments.</h2>
      <p class="muted">Replace placeholder links/email before publishing.</p>
    </section>

    <section class="section">
      <h2>Copyable GitHub README HTML</h2>
      <p class="muted">This box contains the same profile content as raw HTML. Copy it into your GitHub profile README if you want an HTML-heavy README. GitHub supports HTML inside Markdown, but it strips some CSS/JS, so for GitHub README usage, keep it simple.</p>
      <div class="button-row">
        <button onclick="copyReadmeHtml()">Copy HTML</button>
        <button class="secondary" onclick="selectReadmeHtml()">Select All</button>
      </div>
      <textarea class="copy-box" id="readmeHtml" spellcheck="false"><h1 align="center">Hey, I'm Zafeer 👋</h1>

<p align="center">
  <b>Platform / DevOps Engineer specializing in Kubernetes-based AI Infrastructure, MLOps, GPU Workloads, CI/CD, and On-Prem / Air-Gapped Deployments.</b>
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/your-linkedin/">LinkedIn</a> •
  <a href="mailto:your-email@example.com">Email</a> •
  <a href="https://github.com/your-username">GitHub</a>
</p>

---

<h2>🚀 About Me</h2>

I build and operate production-grade infrastructure for AI, computer vision, and MLOps platforms.

My work sits at the intersection of Kubernetes platform engineering, GPU-based model training, CI/CD, GitOps, observability, secrets management, hybrid cloud, and on-prem / air-gapped deployments.

I have worked on high-scale AI/CV platforms involving <b>50+ Kubernetes nodes</b>, <b>2,000+ cameras</b>, <b>50+ GPU machines</b>, and <b>200+ computer vision use cases</b> across government and enterprise environments.

---

<h2>🧠 Core Engineering Focus</h2>

<pre>
AI Platform Engineering
Kubernetes Infrastructure
MLOps / ML Training Orchestration
DevOps Automation
GPU Workload Scheduling
CI/CD and GitOps
On-Prem / Air-Gapped Deployments
Computer Vision Infrastructure
Cloud + Hybrid Infrastructure
Observability and Reliability
Infrastructure Automation
Edge / Device Onboarding
</pre>

---

<h2>🛠️ Tech Stack</h2>

<h3>Platform & DevOps</h3>

Kubernetes • Docker • ArgoCD • Jenkins • GitHub Actions • Azure DevOps • Terraform • Ansible

<h3>Cloud, Infra & Networking</h3>

AWS • Alibaba Cloud • NGINX • HAProxy • MetalLB • Harbor • Keepalived • NFS / NAS

<h3>MLOps, AI & Data</h3>

Python • PyTorch • MLflow • Kafka • Qdrant • Redis • InfluxDB • Postgres

<h3>Observability & Security</h3>

Prometheus • Grafana • HashiCorp Vault • New Relic • Alerting

---

<h2>🏗️ Highlight: AI / Computer Vision Platform Infrastructure</h2>

I worked on a low-code / no-code computer vision platform covering the full AI lifecycle:

<pre>
Data Collection
↓
Labelling
↓
Model Training
↓
Custom Notebook Training
↓
Real-Time Inference
↓
Camera Management
↓
Device Onboarding
↓
Analytics Dashboards
</pre>

The platform supported large-scale government AI/CV infrastructure with:

<ul>
  <li>200+ AI/CV use cases</li>
  <li>2,000+ cameras</li>
  <li>50+ GPU machines</li>
  <li>Multi-environment Kubernetes deployments</li>
  <li>On-prem and air-gapped infrastructure</li>
  <li>Real-time camera inference</li>
  <li>Large-scale model training and deployment workflows</li>
</ul>

---

<h2>⚡ Key Engineering Wins</h2>

<h3>Reduced model training time by ~90%</h3>

Built distributed training infrastructure using <b>PyTorch DDP</b>, allowing GPU pooling for computer vision model training.

<pre>
Before: 55 hours
After:   5 hours
</pre>

<h3>Operated 50+ node Kubernetes infrastructure</h3>

Worked as Kubernetes administrator across multiple environments, supporting platform services, backend services, frontend services, databases, Redis / Redis Stack, Node-RED, agents, health services, model training jobs, inference services, notebooks, observability components, ingress, and routing layers.

<h3>Built production CI/CD pipelines</h3>

<ul>
  <li>Linting changed services</li>
  <li>Selecting deployment environments</li>
  <li>Building Docker images</li>
  <li>Pushing images to Harbor registry</li>
  <li>Updating image tags and Kubernetes manifests</li>
  <li>Deploying across dev, prod, and client environments</li>
  <li>Managing environment variables through HashiCorp Vault</li>
  <li>Maintaining semantic versioning</li>
  <li>Enabling multi-environment deployments</li>
</ul>

<h3>Built HA NGINX architecture</h3>

Removed a single point of failure by designing a highly available NGINX setup using Keepalived, virtual IP, multiple NGINX machines, Git-backed NGINX configuration, automated config sync, and failover routing.

<h3>Built device onboarding infrastructure</h3>

Designed and migrated device onboarding from Bash-heavy scripts to a more robust system using Python microservices, Kubernetes Jobs, Ansible playbooks and roles, Kafka-based status communication, Prometheus-based device monitoring, and a persistent deploy manager service.

The system supported single-device onboarding, bulk onboarding, device patching, device deboarding, destructive cleanup, unified health monitoring, multi-phase onboarding lifecycle, Kubernetes cluster creation or node joining, NVIDIA driver and container runtime setup, Docker setup, image pre-pulling through DaemonSets, and persistent device services.

<h3>Built self-hosted container registry</h3>

Hosted Harbor locally, mounted on NAS, proxied over NGINX, with team-based access and regular backups.

<pre>
Saved approximately $1,000 in cloud cost
</pre>

<h3>Reduced platform setup time</h3>

Created Docker Compose-based setup for platform services.

<pre>
Before: 2 hours
After:  5 minutes
</pre>

<h3>Saved 300k SAR yearly on client infrastructure</h3>

Architected a tightly scoped deployment environment for a Saudi government-related client, reducing yearly infrastructure cost.

---

<h2>🔬 MLOps Systems I Have Built</h2>

<h3>Model Training Orchestration</h3>

<ul>
  <li>On-demand model training system running as Kubernetes Jobs</li>
  <li>Detection, classification, and segmentation support</li>
  <li>Multiple architectures and pretrained weights</li>
  <li>Distributed GPU training with PyTorch DDP</li>
  <li>MLflow integration and real-time metric reporting</li>
  <li>Pause, stop, resume, and priority controls</li>
  <li>Kafka-based progress tracking</li>
  <li>Logger and status microservices</li>
  <li>Resilience across interruptions and reboots</li>
</ul>

<h3>Jupyter Notebook Platform</h3>

<ul>
  <li>Each notebook exposed through a live subdomain</li>
  <li>Ingress-based routing and ingress controller integration</li>
  <li>Persistent storage on NFS/NAS</li>
  <li>StatefulSet-based deployment</li>
  <li>Automatic idle monitoring, warning, and cleanup</li>
  <li>MetalLB load balancing for on-prem Kubernetes</li>
  <li>Persistent notebook code across restarts</li>
</ul>

<h3>Face Registration Service</h3>

<ul>
  <li>On-demand Kubernetes Job-based execution</li>
  <li>Multiple face model support</li>
  <li>Embedding generation and Qdrant vector database integration</li>
  <li>Scalable face registration workflow</li>
</ul>

---

<h2>🎥 Computer Vision / Camera Infrastructure</h2>

Built and optimized camera management services for real-time streaming workloads.

<ul>
  <li>RTSP streams and HLS conversion</li>
  <li>MediaMTX integration</li>
  <li>Custom camera management APIs</li>
  <li>Multi-camera inference workflows</li>
  <li>Stream lifecycle management</li>
  <li>Camera uptime metrics</li>
  <li>Prometheus/Grafana dashboards</li>
  <li>Add/remove camera APIs</li>
  <li>Stream expiration handling</li>
  <li>Real-time camera health monitoring</li>
</ul>

---

<h2>🧪 Early Computer Vision PoCs</h2>

<h3>Ajdan</h3>
Built a camera-stream-based crowd detection PoC with model training, live inference, real-time counting, and male/female/children class detection.

<h3>King Salman Military Base</h3>
Worked on employee availability, unauthorized access detection, child/person class detection, officer availability checks, and alert generation.

<h3>Gold Chain</h3>
Worked on multi-class computer vision classification, employee availability, people entering/exiting shops, and multi-camera inference.

<h3>Dubai Airport</h3>
Worked on a high-stakes turnaround management system PoC. Built automated stream recovery using Python, Selenium, and SMTP to monitor stream health, refresh cookies, restart streams, and send notifications.

---

<h2>☁️ Client / Deployment Experience</h2>

<h3>Eastern Provincial Municipality — Saudi Arabia</h3>

Worked on infrastructure and MLOps execution for a high-scale computer vision project involving 200+ use cases, 2,000+ cameras, 50+ GPU machines, on-prem Kubernetes, training/inference workloads, device onboarding, monitoring, and alerting.

<h3>Ministry of Economy and Petroleum — Saudi Arabia</h3>

Worked on deployment architecture for AI platforms in air-gapped, on-prem environments.

<ul>
  <li><b>AmplifAI — RAG Platform:</b> Dockerized and deployed services across dev, staging, and production with Kubernetes YAML, DB connectivity, block storage, and ingress routing.</li>
  <li><b>AmplifAI Meetings — Meeting Bot:</b> Architected and deployed meeting bot services in an air-gapped on-prem Kubernetes environment.</li>
</ul>

<h3>Expro — Saudi Government-Related Expenditure Entity</h3>

<ul>
  <li>Alibaba ECS deployments</li>
  <li>Alibaba Container Registry</li>
  <li>Azure DevOps blue-green CI/CD pipelines</li>
  <li>Approval-based deployments and rollback support</li>
  <li>Multi-environment deployment flow</li>
  <li>Local HashiCorp Vault setup</li>
  <li>Saved approximately 300k SAR yearly</li>
</ul>

<h3>Monsha'at — Saudi Government Entity</h3>

<ul>
  <li>Deployed AI services on Alibaba ECS</li>
  <li>Deployed platform services on Alibaba ACK Kubernetes</li>
  <li>Created multiple VPCs</li>
  <li>Supported private connectivity between services</li>
</ul>

---

<h2>🧱 Infrastructure Work</h2>

<pre>
On-prem Kubernetes cluster architecture
High availability using HAProxy
Kubernetes administration
NGINX routing and reverse proxying
HA NGINX with Keepalived
Docker registry hosting with Harbor
NAS-mounted registry storage
Registry backup strategy
Team-based registry access
Vault-based secrets management
Terraform-based infrastructure automation
Ansible-based device provisioning
Docker image optimization
Multi-stage Docker builds
Docker Compose platform packaging
Prometheus metrics scraping
Grafana dashboards
Alertmanager / open alerts
StatefulSets for persistent services
Redis / InfluxDB persistence
Kubeflow Trainer integration
GPU training persistence across reboots
Air-gapped Kubernetes deployment
</pre>

---

<h2>📌 Featured Projects</h2>

<h3>CloudPad — Kubernetes Sandbox Environment</h3>

<b>Tech:</b> React, FastAPI, Kubernetes, Docker, AWS EC2, Ingress NGINX, Claude MCP

<pre>
Two pods share the same persistent volume:

1. Code writer / editor pod
2. Code serving pod
</pre>

<ul>
  <li>Live code editing</li>
  <li>Chatbot-based code modification</li>
  <li>VS Code web server</li>
  <li>Live deployable links</li>
  <li>Kubernetes-based sandbox environments</li>
  <li>Persistent volume sharing between pods</li>
  <li>Real-time code reflection</li>
  <li>Isolated sandbox environments</li>
</ul>

<h3>Medium Clone — Full-Stack Blogging Platform</h3>

<b>Tech:</b> React, HonoJS, Cloudflare Workers, Cloudflare Pages, Redis, Postgres, Prisma, New Relic

<ul>
  <li>Google authentication and OTP authentication</li>
  <li>Comments, replies, notifications, and blog engagement</li>
  <li>Cloudflare Workers backend and Cloudflare Pages deployment</li>
  <li>Postgres on Aiven and Prisma Accelerate</li>
  <li>GitHub Actions CI/CD and New Relic monitoring</li>
  <li>S3 + CDN frontend deployment and Cloudflare R2 image hosting</li>
</ul>

<b>Live:</b> codesphere.live

<h3>ReminderBot — WhatsApp Reminder System</h3>

<b>Tech:</b> Python, Celery, Postgres, Twilio

<ul>
  <li>WhatsApp reminders</li>
  <li>Recurring daily reminders</li>
  <li>Single-use reminders</li>
  <li>Celery-based scheduling</li>
  <li>Postgres persistence</li>
  <li>Twilio integration</li>
</ul>

---

<h2>🧩 Architecture Areas I Care About</h2>

<pre>
How do we deploy AI workloads safely?
How do we make Kubernetes usable for AI teams?
How do we reduce model training time?
How do we onboard edge/GPU devices reliably?
How do we deploy in air-gapped environments?
How do we make CI/CD safe, observable, and rollback-friendly?
How do we make infrastructure repeatable with Terraform and Ansible?
How do we monitor thousands of cameras and AI services?
How do we remove single points of failure?
How do we run GPU workloads reliably on Kubernetes?
How do we make on-prem AI infrastructure feel cloud-like?
How do we build platforms that developers actually enjoy using?
</pre>

---

<h2>🎯 Roles I Am Best Aligned With</h2>

<ul>
  <li>Platform Engineer</li>
  <li>MLOps Engineer</li>
  <li>AI Infrastructure Engineer</li>
  <li>DevOps Engineer — Kubernetes</li>
  <li>Cloud Infrastructure Engineer</li>
  <li>Kubernetes Engineer</li>
  <li>SRE — AI / Platform / Infrastructure</li>
  <li>Infrastructure Engineer — On-Prem / Hybrid Cloud</li>
  <li>DevOps Engineer — GPU / ML Workloads</li>
  <li>Platform Engineer — Computer Vision / AI Products</li>
</ul>

---

<h2>🌍 Markets I Am Open To</h2>

<ul>
  <li>UAE</li>
  <li>Saudi Arabia</li>
  <li>Gulf region</li>
  <li>Remote international teams</li>
  <li>Hybrid cloud / on-prem AI infrastructure teams</li>
  <li>AI platform teams</li>
  <li>Computer vision infrastructure teams</li>
  <li>DevOps / platform teams serving ML engineers</li>
</ul>

---

<h2>📫 Reach Me</h2>

<pre>
Email: your-email@example.com
LinkedIn: https://www.linkedin.com/in/your-linkedin/
GitHub: https://github.com/your-username
</pre>

---

<p align="center">
  <b>Building reliable infrastructure for AI systems that need to work outside demos — in real production environments.</b>
</p></textarea>
      <p class="note" id="copyStatus"></p>
    </section>
  </main>

  <script>
    function copyReadmeHtml() {
      const box = document.getElementById('readmeHtml');
      box.select();
      box.setSelectionRange(0, box.value.length);
      navigator.clipboard.writeText(box.value).then(() => {
        document.getElementById('copyStatus').textContent = 'Copied HTML to clipboard.';
      }).catch(() => {
        document.execCommand('copy');
        document.getElementById('copyStatus').textContent = 'Copied HTML to clipboard.';
      });
    }

    function selectReadmeHtml() {
      const box = document.getElementById('readmeHtml');
      box.focus();
      box.select();
      box.setSelectionRange(0, box.value.length);
      document.getElementById('copyStatus').textContent = 'Selected all HTML. Press Ctrl+C / Cmd+C to copy.';
    }
  </script>
</body>
</html>
