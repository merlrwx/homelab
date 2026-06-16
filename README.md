# Homelab 🏠

A simple GitOps repo for my homelab Kubernetes setup.

## What is here

- `clusters/` contains Flux cluster entry points.
- `apps/` contains application manifests.
- `monitoring/` contains monitoring controllers and configuration.

## Current setup

- Environment: `staging`
- GitOps: Flux
- Apps: Linkding
- Monitoring: kube-prometheus-stack

## Secrets

Secrets are stored as SOPS-encrypted manifests using age recipients. Flux decrypts them in-cluster with the `sops-age` secret, so plaintext values stay out of the repo.
