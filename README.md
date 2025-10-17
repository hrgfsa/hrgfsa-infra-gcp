# HRGFSA Infrastructure on GCP

This repository contains Terraform code and configurations to provision and manage the Google Cloud Platform (GCP) infrastructure for the HRGFSA project.

## Overview

- Provision GKE clusters to host Kubernetes workloads.
- Configure networking, firewall rules, IAM roles, and service accounts.
- Designed to support Helm-based deployments in Kubernetes.
- Infrastructure deployment is automated using GitHub Actions workflows.
- The nginx controller and helm configurations are also installed using terraform on GCP.

## GitHub Actions Integration

- Uses a **Google Cloud service account** with necessary permissions.
- The service account credentials are securely stored as GitHub Secrets in this repo.
- The workflow automates Terraform commands (`init`, `plan`, `apply`) triggered on push to main branches.
- Ensures infrastructure is provisioned or updated consistently and repeatably.

## Getting Started

1. Clone the repo and configure your GitHub Secrets with your GCP service account JSON.
2. Modify variables and environment-specific files as needed.
3. Push changes to trigger GitHub Actions for automated provisioning.

## Repository Structure

- `main.tf`, `variables.tf`, `outputs.tf`: Core Terraform files.
- `environments/prod`: Variable files scoped to runtime environments.
- `.github/workflows/infra.yml`: GitHub Actions pipeline.

## Support & Contribution

Please raise issues for infrastructure bugs or enhancements. Pull requests are welcome.

---
