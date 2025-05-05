---
layout: project
type: project
image: img/api-transform-square.png
title: "Internal API Proxy Transformer"
date: 2024
published: true
labels:
  - Node.js
  - API
  - CronJob
  - Internal Tools
summary: "An internal tool that automatically fetches and transforms JSON data from an internal website into a structured API for cross-team use."
---

<img class="img-fluid" src="../img/api-thumb.png">

**Internal API Proxy Transformer** is a lightweight internal service I developed at my current company to solve a data integration challenge under tight constraints. The company did not want to invest in developing new backend APIs, so I created a Node.js service that periodically fetches JSON data from an internal web page using cron jobs, transforms and enriches the structure (e.g., adds missing `description` fields, renames unclear keys), and exposes a cleaned, structured internal API.

This allowed our Taiwan team to reliably consume up-to-date data without requiring changes to the legacy system.

<hr>

**🔧 What It Does:**
- Fetches JSON data from internal web pages that do not have dedicated APIs
- Transforms the data (e.g., enriches with new fields, restructures for clarity)
- Exposes a new internal API for consumption by cross-regional teams
- Runs automatically on a defined schedule using CronJob

**🛠 Tech Stack:**
- Node.js + Express
- CronJob (node-cron)
- HTTP/JSON request and parsing
- Internal hosting environment

**💡 What I Learned:**
- Designing pragmatic solutions within organizational limitations
- Implementing automated data enrichment pipelines
- Building internal middleware to connect systems and teams without disrupting upstream sources

---

*Note: The source code is proprietary and cannot be shared publicly, but I'm happy to explain the architecture or development process if needed.*
