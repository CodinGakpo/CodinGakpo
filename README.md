# <!-- ===================== HEADER ===================== -->

<h1 align="center">
  Hey 👋, I'm Adidev Anand
</h1>

<p align="center">
  <img src="https://raw.githubusercontent.com/CodinGakpo/CodinGakpo/output/github-contribution-grid-snake-dark.svg" />
</p>

<h3 align="center">
  Backend & Cloud Engineer &nbsp;•&nbsp; Distributed Systems &nbsp;•&nbsp; Information Security
</h3>

<p align="center">
  I build production-deployed backend systems, cloud-native infrastructure, and security-focused applications with real-world impact.
</p>

<!-- ===================== HERO IMAGE 1 ===================== -->

<p align="center">
  <img src="./image.png" alt="Late night coding setup" width="100%" />
</p>

---

# About Me

- Final-year **B.Tech Information Security** student at VIT Vellore &nbsp;|&nbsp; CGPA: **9.11**
- Building distributed backend systems using **Python, Go, Django, FastAPI, PostgreSQL, Redis**
- **AWS Certified Solutions Architect (SAA-C03)** &nbsp;|&nbsp; exploring Security Specialty next
- Interested in **Cybersecurity, distributed systems, and cloud infrastructure**
- 🏆 2x Hackathon winner — DevSoc'26 & Yantra'26 &nbsp;|&nbsp; Rank **10 / 2000+** at Neo Codeathon, VIT
- Open to internships, collaborations, and open-source work

---

# 🏆 Hackathon Wins

| Event | Track | Role |
|---|---|---|
| DevSoc'26 — CodeChef | Tech for Good | Backend architecture & system stability |
| Yantra'26 Central Hack | CS/IT | Backend architecture & system stability |
| Neo Codeathon — VIT | Competitive Coding | **Rank 10 / 2000+** |

---

# Projects

## 🔒 Keyhole — Confidential Code Execution Sandbox

Runs untrusted or AI-generated code against private data and releases **only a small, typed,
cryptographically-attested answer** — so bulk data exfiltration is structurally impossible, not
just scanned for.

- **Bandwidth-bounded exit gate**: untrusted code may return only a caller-declared narrow schema
  (int / enum / bounded string) — a few-byte exit makes bulk exfiltration a bandwidth problem, not
  a content-scanning one
- **Signed attestations** (ed25519 / AWS KMS) verify exactly what code ran, on what data, with zero
  egress, and what bounded value came out
- **Cumulative exit-bandwidth budget** bounds drip exfiltration across many calls, not just per-run
- Deployed to a live AWS account (Lambda control plane, ECS Fargate sandbox, DynamoDB audit log,
  KMS-backed signing) via Terraform, on a **no-NAT, empty-IAM-role** network design — verified idle
  cost of **$0.12 over 2–3 days**
- Adversarial test suite (dump, encode-in-bounded-string, drip-exfiltration-across-runs) confirmed
  structurally blocked, not pattern-matched
- AI-paired development (architecture directed and iterated with Claude Code), personally reviewed,
  tested, and deployed end-to-end

**Stack:** Python · AWS Lambda · ECS Fargate · DynamoDB · KMS · Terraform

---

## 🛡 ShieldStream — Distributed API Security Gateway

A horizontally-scalable API security proxy enforcing distributed rate limiting, OWASP threat
detection, and real-time telemetry across concurrent gateway replicas.

- **Atomic sliding-window rate limiter** using Redis Sorted Sets + Lua scripting — eliminates race
  conditions across replicas without distributed locks
- **At-least-once event pipeline** via Redis Streams consumer groups (XREADGROUP / XACK /
  XAUTOCLAIM), feeding batched idempotent upserts into TimescaleDB
- Real-time threat telemetry dashboard (Next.js, WebSocket, Redis Pub/Sub fan-out)
- Fail-open circuit breakers, exponential-backoff retries, and consumer-lag alerting for graceful
  degradation under failure

**Stack:** FastAPI · Redis · PostgreSQL · TimescaleDB · Next.js · AWS ECS

---

## 🏛 JanSaathi — Civic Issue Reporting Platform

Full-stack civic reporting platform connecting citizens to local government departments, rebuilt
from an earlier prototype (ReportMitra) into a production-grade v2.

- **DigiLocker-first signup, OTP-first login** — UUID-based citizen identity replacing unverified
  phone numbers as the primary key
- AI-based issue classification routing reports to the correct department
- Production AWS stack (EC2 + RDS + S3 + CloudFront + Route53 + ACM) provisioned from scratch, with
  IAM OIDC-based GitHub Actions auth replacing long-lived access keys
- Zero-downtime rolling deploys via multi-repo CI/CD; cron-based EC2/RDS lifecycle automation to cut
  idle cost
- 🏆 Winner, DevSoc'26 Tech for Good track (150+ participants)

**Stack:** Go · Gin · React · PostgreSQL · GCP · AWS EC2/S3/RDS · GitHub Actions

---

## 🩺 DrDeepti — Clinic Booking Platform & WhatsApp Assistant

Production-deployed appointment platform for a Delhi-based clinic — live with **30+ active users**.

- **Database-level row locking** in the booking transaction path, preventing double-bookings under
  concurrent access
- Phone number **OTP verification** on the patient booking flow to prevent spam and unauthorized
  bookings
- Dedicated authentication isolating doctor-facing endpoints from the public booking flow
- Conversational booking assistant on **WhatsApp Business API** (FastAPI, AWS Lambda) via the Meta
  Developer platform

**Stack:** Django · React · PostgreSQL (NeonDB) · FastAPI · AWS Lambda · Vercel · Render

---

## 📄 DocuMiner — AI-Powered Enterprise Security Analysis (Patent-Disclosed)

A three-phase autonomous intelligence pipeline that turns raw, unstructured enterprise documents
(PDFs, spreadsheets, scanned images) into executed security actions — OCR + NLP preprocessing with
intelligent PII pseudonymization, an agentic LLM layer for zero-shot document classification, and an
autonomous layer combining a stateful risk engine, a security knowledge graph, and a digital twin
simulation for pre-deployment mitigation validation.

- Patent disclosure filed (co-authored); the patentability search confirmed the architecture as
  **novel with a genuine inventive step** over all cited prior art
- Ultimately excluded from patentability under **Section 3(k) of the Indian Patents Act**, which
  categorically excludes software/algorithms from patent protection in India — a legal boundary, not
  a technical one
- Built the web backend end-to-end, configured the OCR/document-processing pipeline, and wired in
  the LangChain layer connecting extraction to agentic reasoning

**Stack:** Python · LangChain · spaCy · FastAPI · Pandas

---

# Tech Stack

## Languages
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![Go](https://img.shields.io/badge/go-%2300ADD8.svg?style=for-the-badge&logo=go&logoColor=white)
![JavaScript](https://img.shields.io/badge/javascript-%230A192F.svg?style=for-the-badge&logo=javascript&logoColor=F7DF1E)
![Java](https://img.shields.io/badge/java-%23007396.svg?style=for-the-badge&logo=openjdk&logoColor=white)

---

## 🌐 Backend & Full Stack
![Django](https://img.shields.io/badge/django-%23092E20.svg?style=for-the-badge&logo=django&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-%2300C7B7.svg?style=for-the-badge&logo=fastapi&logoColor=white)
![Gin](https://img.shields.io/badge/gin-%2300ADD8.svg?style=for-the-badge&logo=go&logoColor=white)
![React](https://img.shields.io/badge/react-%23007ACC.svg?style=for-the-badge&logo=react&logoColor=white)
![Next.js](https://img.shields.io/badge/next.js-%23000000.svg?style=for-the-badge&logo=next.js&logoColor=white)
![Postgres](https://img.shields.io/badge/postgres-%2300758F.svg?style=for-the-badge&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/redis-%23DC382D.svg?style=for-the-badge&logo=redis&logoColor=white)

---

## ☁️ Cloud & DevOps
![AWS](https://img.shields.io/badge/AWS-%230A192F.svg?style=for-the-badge&logo=amazon-aws&logoColor=FF9900)
![Terraform](https://img.shields.io/badge/terraform-%235835CC.svg?style=for-the-badge&logo=terraform&logoColor=white)
![Docker](https://img.shields.io/badge/docker-%23007ACC.svg?style=for-the-badge&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/github%20actions-%232671E5.svg?style=for-the-badge&logo=githubactions&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-%230A192F.svg?style=for-the-badge&logo=linux&logoColor=FCC624)
![Git](https://img.shields.io/badge/git-%230A192F.svg?style=for-the-badge&logo=git&logoColor=F05032)

---

# 📜 Certifications

| Certification | Domain |
|---|---|
| AWS Certified Solutions Architect – Associate (SAA-C03) | Cloud |
| Meta Back-End Developer Professional Certificate | Full Stack |
| Google Foundations of Cybersecurity | Cybersecurity |
| McKinsey Forward Program | Professional Development |

---

<!-- ===================== HERO IMAGE 2 ===================== -->

<p align="center">
  <img src="./image2.png" alt="Chill coding setup" width="100%" />
</p>

---

# 📫 Connect With Me

📧 anandadidev43@gmail.com

🔗 [linkedin.com/in/adidevanand](https://linkedin.com/in/adidevanand/)

🌐 [Portfolio](https://exec-adidev.vercel.app/)

---

<p align="center">
  <i>"Build. Break. Learn. Repeat."</i>
</p>
