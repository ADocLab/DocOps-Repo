# Understanding the CI/CD Pipeline for Documentation

## Overview
Documentation-as-Code (DocOps) treats technical documentation with the same rigor as software development.  
This page explains the **complete CI/CD pipeline** that powers this documentation portal — from commit to live deployment.

The workflow is powered by:

- **MkDocs** for site generation
- **GitHub Actions** for CI/CD
- **GitHub Pages** for hosting
- **Automation** for reliability and repeatability

---

## Why CI/CD Matters for Documentation
Traditionally, documentation is manually:

- written  
- reviewed  
- exported  
- uploaded  
- deployed  

This causes:

❌ inconsistencies  
❌ outdated content  
❌ manual errors  
❌ deployment delays  

DocOps solves this using automation.

!!! info
    CI/CD brings **consistency**, **speed**, and **scalability** to documentation workflows.

---

## The High-Level Pipeline Flow

The documentation pipeline works as follows:

1. You write or update `.md` files in the repo  
2. You commit and push changes to the `main` branch  
3. GitHub Actions automatically triggers a workflow  
4. A fresh Ubuntu VM is created  
5. MkDocs builds the static site  
6. The generated HTML is pushed to the `gh-pages` branch  
7. GitHub Pages serves the updated site publicly  

✅ No manual uploads  
✅ Automatic deployment  
✅ Version-controlled documentation  

---

## Trigger: When the Pipeline Starts

The pipeline starts automatically when a commit is pushed to `main`:

```yaml
on:
  push:
    branches:
      - main
```