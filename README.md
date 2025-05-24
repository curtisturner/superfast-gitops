# superfast-gitops

This repository stores GitOps manifests for managing a GKE Autopilot cluster using Flux.

Terraform code for provisioning the cluster and Flux is managed separately.

## Directory structure

- clusters/
  - gke-autopilot/
    - kustomization.yaml      # Root kustomization for the cluster
    - flux-system/            # Flux system manifests (generated externally)
- apps/                      # Application-specific manifests (Kustomize overlays/bases)
- infrastructure/            # Shared infrastructure manifests (networking, monitoring, etc.)
- docs/                      # Documentation

Flux will reconcile the cluster state based on this repo.
