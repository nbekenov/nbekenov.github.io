---
layout: default
title: Projects
description: git log
---

## Projects

Selected infrastructure and platform engineering work.

---

<div class="project-card">

### AWS Cloud Migration

**Problem:** Legacy on-premises applications had high operational overhead,
limited scalability, and no disaster recovery capability.

**Solution:** Led end-to-end migration to AWS. Designed target architecture,
provisioned infrastructure from scratch using Terraform and CloudFormation,
and implemented disaster recovery across multiple availability zones.

**Outcome:** Eliminated on-premises hardware costs, achieved 99.9% uptime SLA,
and reduced mean time to recovery from hours to minutes.

<span class="stack-tag">AWS</span>
<span class="stack-tag">Terraform</span>
<span class="stack-tag">CloudFormation</span>
<span class="stack-tag">Disaster Recovery</span>

</div>

---

<div class="project-card">

### Terraform Module Library

**Problem:** Infrastructure was provisioned inconsistently across teams,
leading to security drift, cost overruns, and unreviewed configurations.

**Solution:** Authored a library of reusable Terraform modules enforcing
organizational security standards, tagging policies, and cost guardrails.
Modules cover VPCs, EKS clusters, RDS instances, S3 buckets, and IAM roles.

**Outcome:** Reduced infrastructure provisioning time by 60% and eliminated
security review back-and-forth for compliant resource types.

<span class="stack-tag">Terraform</span>
<span class="stack-tag">AWS</span>
<span class="stack-tag">IaC</span>
<span class="stack-tag">Security</span>

</div>

---

<div class="project-card">

### Backstage Internal Developer Platform

**Problem:** Developers waited days for platform team involvement to create
new services and provision underlying infrastructure.

**Solution:** Architected and deployed an internal developer platform using
Backstage, including software templates, a service catalog, and integrated
Terraform-backed infrastructure provisioning.

**Outcome:** Engineering teams self-provision new services in under 10 minutes.
Platform team toil reduced by ~40%.

<span class="stack-tag">Backstage</span>
<span class="stack-tag">Terraform</span>
<span class="stack-tag">AWS</span>
<span class="stack-tag">IDP</span>

</div>

---

<div class="project-card">

### Full-Stack Observability — Datadog

**Problem:** Engineering teams had limited visibility into production system
health, leading to slow incident response and reactive firefighting.

**Solution:** Designed and rolled out Datadog across the organization covering
APM, RUM, distributed tracing, log management, and synthetic testing.
Built dashboards and SLO monitors for all critical services.

**Outcome:** Mean time to detect (MTTD) reduced by 70%. On-call engineers
now have full context within seconds of an alert firing.

<span class="stack-tag">Datadog</span>
<span class="stack-tag">APM</span>
<span class="stack-tag">Prometheus</span>
<span class="stack-tag">Grafana</span>

</div>

---

<div class="project-card">

### GitHub Actions Organization Framework

**Problem:** Each repository had bespoke, unmaintained CI/CD pipelines
with inconsistent security scanning, testing, and deployment patterns.

**Solution:** Designed a library of reusable GitHub Actions workflows
covering build, test, security scan, and deploy stages. Migrated all
repositories to the shared framework with repo-specific overrides.

**Outcome:** Org-wide pipeline maintenance consolidated to a single repo.
New repositories get compliant CI/CD in under 5 minutes.

<span class="stack-tag">GitHub Actions</span>
<span class="stack-tag">CI/CD</span>
<span class="stack-tag">GitLab CI</span>
<span class="stack-tag">Bitbucket</span>

</div>

---

<div class="project-card">

### EKS & ECS Cluster Operations

**Problem:** Container workloads ran on ad-hoc clusters with no standardized
networking, autoscaling, or lifecycle management.

**Solution:** Standardized cluster provisioning for EKS (Kubernetes) and ECS
using Terraform modules. Implemented cluster autoscaler, Karpenter node
provisioning, and service mesh for traffic management.

**Outcome:** Infrastructure costs reduced by 30% through right-sizing.
Zero unplanned cluster downtime over 12 months.

<span class="stack-tag">EKS</span>
<span class="stack-tag">ECS</span>
<span class="stack-tag">Kubernetes</span>
<span class="stack-tag">Karpenter</span>

</div>

---

<div class="project-card">

### AI Tooling — Claude Code Skills Registry & Agents

**Problem:** AI-assisted development workflows were inconsistent and
undocumented, leading to duplicated effort and poor quality outputs.

**Solution:** Built a centralized Claude Code skills registry with reusable
hooks and prompt patterns. Developed autonomous agents integrated with
AWS Bedrock Knowledge Bases and AgentCore services for infrastructure
automation tasks.

**Outcome:** Engineering teams adopt AI tooling via a governed, versioned
registry. Infrastructure automation tasks that previously took 2 hours
now complete in under 5 minutes.

<span class="stack-tag">Claude Code</span>
<span class="stack-tag">AWS Bedrock</span>
<span class="stack-tag">AgentCore</span>
<span class="stack-tag">AI Agents</span>

</div>
