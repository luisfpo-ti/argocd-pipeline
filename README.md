# ArgoCD Pipeline Repository

This repository provides a comprehensive example of how to use **ArgoCD** with **Kustomize** to manage GitOps workflows for Kubernetes deployments. It includes a structured setup with examples for creating ArgoCD applications, automating workflows with GitHub Actions, and deploying a microservice using GitOps principles.

## Repository Structure

The repository is organized into the following folders:

### 1. **argocd-application**
Contains YAML examples for creating ArgoCD applications. These examples define how to manage and deploy resources to your Kubernetes cluster using ArgoCD.

**Files:**
- ArgoCD Application manifests
- Examples showcasing linking Git repositories and Kustomize

---

### 2. **githubactions-workflows**
Includes example workflows for GitHub Actions. These workflows automate common tasks such as building container images and running Kustomize commands to generate Kubernetes manifests.

**Files:**
- GitHub Actions workflows for CI/CD automation
- Steps for building and pushing Docker images
- Examples of running `kustomize` commands within a pipeline

---

### 3. **microservice-example**
A GitOps example of a microservice deployment. This folder demonstrates the integration of Kustomize for managing Kubernetes manifests in a GitOps workflow.

**Files:**
- Kubernetes manifests for the example microservice
- Kustomization.yaml showcasing the structure and overlays for deployment

---

## Prerequisites

Before using this repository, ensure you have the following tools installed:

- [ArgoCD](https://argo-cd.readthedocs.io/en/stable/)
- [Kustomize](https://kustomize.io/)
- [GitHub CLI](https://cli.github.com/)
- [kubectl](https://kubernetes.io/docs/tasks/tools/)
- Docker (for building images)

---

## How to Use

### 1. **Set Up ArgoCD**
- Deploy ArgoCD on your Kubernetes cluster following the [official documentation](https://argo-cd.readthedocs.io/en/stable/getting_started/).
- Use the YAML examples in `argocd-application` to create ArgoCD applications pointing to the `microservice-example` folder.

```bash
kubectl apply -f argocd-application/your-application.yaml
```

---

### 2. **GitHub Actions Workflow**
- Configure the workflows in `githubactions-workflows` by providing your repository details and credentials.
- The workflows will:
  1. Build and push container images.
  2. Run `kustomize build` to prepare the manifests for deployment.

### 3. **Deploy Microservices**
- The `microservice-example` folder contains a basic structure for deploying an example microservice.

- Push the changes to your Git repository, and ArgoCD will automatically sync and deploy the updates.

---

## Contributions
Feel free to submit issues or pull requests to enhance this repository. Contributions are welcome!

---

## License
This project is licensed under the MIT License. See the `LICENSE` file for more details.

---

Happy GitOps! 🎉
