# Karpenter Configuration

This repository contains the configuration files for Karpenter in our Kubernetes cluster.

## Directory Structure

- `karpenter/`: Contains Karpenter configuration files
  - `provisioner.yaml`: Karpenter provisioner configuration
  - `aws-node-template.yaml`: AWS node template configuration
  - `sa.yaml`: Service account and RBAC configuration
- `argocd/`: Contains ArgoCD application configuration
  - `karpenter-app.yaml`: ArgoCD application for Karpenter
- `hpa/`: Contains Horizontal Pod Autoscaler configurations

## Prerequisites

- AWS EKS cluster
- ArgoCD installed
- AWS IAM roles configured for Karpenter

## Configuration

1. Update the AWS account ID in `karpenter/sa.yaml`
2. Apply the ArgoCD application configuration
3. Karpenter will be automatically deployed and configured

## Usage

Karpenter will automatically provision nodes based on the configured provisioner settings when pods are scheduled. 