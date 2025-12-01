---
title: "Event 4"
type: "page"
---

# EVENT REPORT: **AWS Cloud Mastery Series #2 — DevOps on AWS**

&emsp;**Date:** Monday, November 17, 2025  
&emsp;**Time:** 8:30 AM – 5:00 PM  
&emsp;**Location:** AWS Vietnam Office, Bitexco Financial Tower, District 1, Ho Chi Minh City  
&emsp;**Objective:** Provide comprehensive understanding of DevOps culture, performance principles, and AWS DevOps tooling to build CI/CD pipelines, Infrastructure as Code (IaC), and full-stack observability.

---

## MORNING SESSION (8:30 AM – 12:00 PM): CI/CD & INFRASTRUCTURE AS CODE

### 1. Welcome & DevOps Mindset (8:30 – 9:00 AM)
- Recap of previous AI/ML session, shifting focus toward productionizing ML and application workloads.
- Emphasis on **DevOps culture and collaboration** between Development and Operations.
- Introduction to key performance metrics including **DORA metrics** and **MTTR (Mean Time To Recovery)**.

---

### 2. AWS DevOps Services — CI/CD Pipeline Building (9:00 – 10:30 AM)

Deep dive into AWS Code-family services for **Continuous Integration (CI)** and **Continuous Deployment (CD)** automation:

- **Source Control:**  
  AWS CodeCommit with discussion on **GitFlow** vs **Trunk-based** branching models.

- **Build & Test Automation:**  
  Using **CodeBuild** for compilation, unit testing, and automated test pipelines.

- **Deployment Strategies — CodeDeploy:**  
  Advanced rollout patterns including **Blue/Green**, **Canary**, and **Rolling updates**.

- **Pipeline Orchestration:**  
  **CodePipeline** for automating the full path from commit → test → deploy.

- **Live Demo:**  
  Full CI/CD pipeline showcase running on AWS.

---

### 3. Infrastructure as Code (IaC) (10:45 AM – 12:00 PM)

IaC as the foundation of modern scalable DevOps:

- **AWS CloudFormation:**  
  Understanding **Templates, Stacks, and Drift Detection** for reproducible environments.

- **AWS CDK — Modern IaC Approach:**  
  Defining infrastructure using programming languages (TypeScript, Python, etc.) with **Constructs and Reusable Patterns**.

- **Demo & Discussion:**  
  Hands-on demonstration deploying infrastructure via both CloudFormation & CDK, plus decision criteria for choosing each approach.

---

## AFTERNOON SESSION (1:00 PM – 5:00 PM): CONTAINERS, OBSERVABILITY & BEST PRACTICES

### 4. Container Services on AWS (1:00 – 2:30 PM)

- **Docker Fundamentals:**  
  Microservices architecture and containerization essentials.

- **Amazon ECR:**  
  Container image registry with image scanning & lifecycle policy management.

- **Amazon ECS vs EKS:**  
  Comparison of AWS-native ECS vs Kubernetes-powered EKS — deployment, scaling, and use cases.

- **AWS App Runner:**  
  Simplified container deployment focusing on code, not infrastructure.

- **Demo & Case Study:**  
  Microservices deployment walkthrough and service comparison.

---

### 5. Monitoring & Observability (2:45 – 4:00 PM)

- **Amazon CloudWatch:**  
  Metrics, logs, alarms, and dashboarding across AWS systems.

- **AWS X-Ray:**  
  Distributed tracing for identifying bottlenecks in microservices.

- **Demo:**  
  Building a full-stack observability setup.

- **Best Practices:**  
  Alerting strategy, dashboards, and on-call operational standards.

---

### 6. Best Practices & Real-World Case Studies (4:00 – 4:45 PM)

- Advanced Deployment Tools — **Feature Flags, A/B Testing** for release control.
- Automated testing deeply integrated with CI/CD pipelines.
- Incident management structures, including postmortems for continuous improvement.
- Case studies from successful DevOps transformations in startups and enterprises.

---

### 7. Q&A & Closing Remarks (4:45 – 5:00 PM)

- Deep-dive question handling.
- DevOps career roadmap & relevant AWS certifications.

---

## SUMMARY & APPLICABILITY

### Evaluation

The event covered the full DevOps lifecycle end-to-end — from culture, CI/CD automation, IaC provisioning, container orchestration, to observability and operational excellence. It provided a balanced mix of conceptual frameworks (DevOps principles, DORA metrics) and real AWS tooling (CodePipeline, CDK, X-Ray).

### Key Takeaways

- Understanding AWS CodeFamily for building automated CI/CD pipelines.
- Strengths and trade-offs of **CloudFormation vs CDK** in IaC.
- How to choose between ECS and EKS for container workloads.
- Implementing proactive monitoring using CloudWatch & X-Ray.

### Next Steps

1. **CI/CD Practice:**  
   Build a pipeline with **CodeCommit + CodeBuild + CodePipeline** for a project or sample repo.

2. **Explore AWS CDK:**  
   Begin infrastructure authoring using CDK with simple reusable Constructs.

3. **Deploy Observability:**  
   Integrate CloudWatch Logs + X-Ray tracing in project APIs and services.

---

## Event Photos

![](/images/4-Events/Event4.1.jpg)  
![](/images/4-Events/Event4.2.jpg)  
![](/images/4-Events/Event4.3.jpg)  
![](/images/4-Events/Event4.4.jpg)