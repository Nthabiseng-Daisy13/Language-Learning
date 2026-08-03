---
id: intro
title: Team Handbook
sidebar_label: 👋 Welcome
slug: /
---

# Software Design Web Application — Team Handbook

Welcome! This site is the single source of truth for how our 6-person team works together for the next **3 months**.

:::info Quick facts
- **Repository hosting:** Gitea (University Server)
- **Branching model:** `main` + `develop` + short-lived task branches
- **Versioning:** Calendar Versioning (CalVer) — `YYYY.MM.REVISION`
- **CI/CD platform:** Gitea Actions
:::

## What's in here

<div className="row">
  <div className="col col--6">

### 🌱 [Git Methodology](/git-methodology)
Branching strategy, naming conventions, commit rules, Pull Request workflow, code review, squash merging, and versioning.

  </div>
  <div className="col col--6">

### ⚙️ [CI/CD Strategy](/cicd-strategy)
What CI/CD means for us, the automated pipeline stages, testing policy, coverage targets, and branch protection rules.

  </div>
</div>

## The golden rule

:::danger Never do this
Never commit directly to `main` or `develop`. All work happens on a task branch and lands via a reviewed, passing Pull Request.
:::

## Daily workflow at a glance

```mermaid
flowchart LR
    A[Pull latest develop] --> B[Create/switch branch]
    B --> C[Implement one task]
    C --> D[Write tests]
    D --> E[Commit regularly]
    E --> F[Push branch]
    F --> G[CI pipeline runs]
    G -->|✅ pass| H[Open Pull Request]
    G -->|❌ fail| C
    H --> I[Code review]
    I --> J[Squash merge into develop]
    J --> K[Delete branch]
```

Use the sidebar (or the cards above) to dive into either document.
