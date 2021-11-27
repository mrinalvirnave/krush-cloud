# Initialize Krush.Cloud Environments

The following instructions are for setting up krush.cloud environments from a locally pulled down git repo

## Prerequisite

* [Install kubectl](https://kubernetes.io/docs/tasks/tools/#kubectl)
* [Install helm](https://helm.sh/docs/intro/install/)
* Kubernetes Cluster with [ArgoCD installed](https://argo-cd.readthedocs.io/en/stable/getting_started/#1-install-argo-cd) in the namespace `argocd`
* Make sure you can log into ArgoCD

## Step 1: Initialize the environment and namespace

This example demonstrates the installation of the `qa` environement

```
helm upgrade --install qa env-init --namespace qa --create-namespace
```

## Step 2: Register the environment with ArgoCD

As part of the output from the previous step you will get instructions to  several commands. Copy paste them to get the environment registered with ArgoCD