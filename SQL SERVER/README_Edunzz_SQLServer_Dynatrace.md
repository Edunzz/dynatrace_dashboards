<div align="center">

# ✨ Edunzz — SQL Server Deep Review & Root Cause Dashboard ✨

![Dynatrace](https://img.shields.io/badge/Built%20for-Dynatrace-1496FF?style=for-the-badge)
![SQL Server](https://img.shields.io/badge/Focus-SQL%20Server-CC2927?style=for-the-badge)
![Status](https://img.shields.io/badge/Release-Community%20Ready-2ea44f?style=for-the-badge)
![License](https://img.shields.io/badge/Use-Open%20JSON-blueviolet?style=for-the-badge)

**A practical Dynatrace dashboard for SQL Server health analysis, failure detection, anomaly review, and root cause exploration.**

Designed and shared by **Edunzz** for teams that want a clearer, faster way to investigate database behavior across the **problem**, **DB**, **service**, **host**, and **cloud** layers.

</div>

---

## Overview

This repository contains a **Dynatrace dashboard JSON** focused on **SQL Server observability**.

The goal of this dashboard is simple:
- help engineers detect abnormal behavior quickly,
- correlate events across different layers,
- support faster troubleshooting,
- and provide a cleaner path to **root cause analysis**.

Instead of reviewing metrics in isolation, this dashboard brings together the most relevant operational signals in one place, including:
- problems and events,
- top detected issues,
- probable root causes,
- database layer health,
- connection trends,
- transaction activity,
- service-side request metrics,
- host resource usage,
- and cloud database capacity signals.

All shared assets in this repository were prepared for **safe public use**, with sensitive data **obfuscated**.

---

## What this dashboard helps you analyze

### 1) Problems and events at a glance
A high-level view of detected problems, event frequency, timestamps, issue types, and reported root causes.

This section is useful for:
- quickly understanding what happened,
- identifying repeated incidents,
- checking whether issues are isolated or recurring,
- and spotting the most important signals first.

### 2) Database layer health
A focused view of SQL Server database state and configuration-related indicators, such as:
- database state,
- instance mapping,
- recovery model,
- updateability,
- user access mode,
- backup recency,
- connection trends by instance,
- and transaction activity by database.

This section helps validate whether the database layer is healthy and behaving as expected.

### 3) Service layer behavior
A service-oriented perspective to understand how applications interact with SQL Server.

It includes metrics such as:
- request rate,
- request count,
- response time,
- request failures,
- failure rate,
- consumer mapping,
- database host name,
- service database name,
- and port visibility.

This area is especially helpful when the issue is not purely inside SQL Server, but in the way services consume it.

### 4) Host layer visibility
A host-focused section to inspect infrastructure conditions that may influence database behavior, such as:
- CPU usage,
- memory usage,
- disk usage,
- port,
- IP address,
- vendor,
- and last report timestamp.

This supports cross-checking whether resource pressure or host instability contributed to the incident.

### 5) Cloud layer indicators
A final layer for cloud database environments, helping review:
- reserved storage,
- used storage,
- storage usage percentage,
- CPU usage,
- endpoint/IP information,
- and last update time.

This is useful for finding platform-side capacity or storage constraints that may explain service degradation.

---

## Dashboard structure

The shared dashboard is organized in the following logical flow:

1. **Problems and Events**  
   Detect what happened and how often.

2. **DB Layer**  
   Validate core SQL Server health and workload behavior.

3. **Service Layer**  
   Review application-to-database interaction quality.

4. **Host Layer**  
   Check infrastructure resource conditions.

5. **Cloud Layer**  
   Inspect platform capacity and storage signals.

This layered design helps move from **symptom → impact → probable cause** in a more structured way.

---

## Key use cases

This dashboard can be useful for:
- SRE and observability teams
- database administrators
- platform engineers
- application support teams
- incident response teams
- performance analysis sessions
- post-incident reviews
- operational health reviews
- SQL Server monitoring initiatives in Dynatrace

---

## Included in this repository

This repository is intended to include:
- the **Dynatrace dashboard JSON**
- section screenshots
- this README
- optional notes for reuse or adaptation

Example structure:

```text
.
├── dashboard/
│   └── sql-server-deep-review-root-cause-dashboard.json
├── images/
│   ├── overview.png
│   ├── problems-events.png
│   ├── db-layer.png
│   ├── service-layer.png
│   ├── host-layer.png
│   └── cloud-layer.png
└── README.md
```

---

## Screenshots

You can replace the paths below with the final names of your exported images.

### Full dashboard
![Full Dashboard](./images/overview.png)

### Problems and events
![Problems and Events](./images/problems-events.png)

### DB layer
![DB Layer](./images/db-layer.png)

### Service layer
![Service Layer](./images/service-layer.png)

### Host layer
![Host Layer](./images/host-layer.png)

### Cloud layer
![Cloud Layer](./images/cloud-layer.png)

---

## Why I am sharing this

I built this dashboard to make SQL Server analysis in Dynatrace more actionable and more visual.

In many environments, useful data already exists, but it is spread across too many places. The real challenge is not only collecting telemetry — it is organizing it in a way that helps teams:
- understand issues faster,
- reduce investigation time,
- align technical and operational perspectives,
- and make root cause analysis less manual.

This dashboard is my contribution to the observability community.

If it helps your team, feel free to use it, adapt it, improve it, and share feedback.

---

## Notes before importing

Before using this dashboard in your own Dynatrace environment, please review the following:
- Some tiles may require you to adjust entity selectors, management zones, filters, or metric dimensions.
- You may need to map the queries to your own SQL Server entities, service names, or cloud resources.
- Screenshots in this repo use obfuscated data for safe public sharing.
- Depending on your environment, some fields or dimensions may differ.

---

## Recommended customization ideas

You may want to extend this dashboard with:
- environment filters (prod / non-prod)
- management zone filters
- region or cluster filters
- workload-specific transaction groups
- alert thresholds for response time and failure rate
- drilldown links to logs, traces, or notebooks
- service ownership tags
- backup SLA indicators
- latency percentile views

---

## How to use

1. Download the dashboard JSON from this repository.
2. Import it into Dynatrace.
3. Update filters, entity references, and selectors as needed.
4. Validate each section against your environment.
5. Save your customized version and iterate with your team.

---

## Community and feedback

If you use this dashboard and want to improve it, feedback is always welcome.

You can:
- open an issue,
- suggest improvements,
- fork the repo,
- or adapt it to your own SQL Server monitoring model.

---

## About the author

**Edunzz**  
Observability, troubleshooting, dashboards, and practical engineering assets for real operations.

If you found this useful, consider starring the repository and sharing it with others in the Dynatrace and SQL Server community.

---

## Mini note in Spanish

> **Comentario breve:** Este dashboard está pensado para analizar SQL Server en Dynatrace de forma más integral, conectando problemas, eventos, capa de base de datos, capa de servicios, host y cloud para facilitar el análisis y la búsqueda de causa raíz. El JSON publicado tiene datos sensibles ofuscados para que cualquiera pueda reutilizarlo y adaptarlo.

---

## Suggested repository title

**sql-server-dynatrace-deep-review-root-cause-dashboard**

## Suggested tags

`dynatrace` `sql-server` `observability` `dashboard` `monitoring` `root-cause-analysis` `database` `sre` `performance` `troubleshooting`

