CD (Continuous Deployment) Part:

Remote Build Configuration:
The CD job is set up to execute remotely.

Triggering CD Job:
Once the Docker image is successfully published, a secure Jenkins API token triggers the Continuous Deployment (CD) job.

Kubernetes Manifest Handling:
The CD job retrieves the Kubernetes manifests (deployment configurations, services, etc.) from a dedicated GitHub repository.

Manifest Update with Latest Image:
The CD job intelligently updates the Kubernetes manifests with the latest Docker image tag.

ArgoCD Deployment:
Using ArgoCD, a powerful GitOps continuous delivery tool, the updated manifests are automatically applied to the Kubernetes cluster.
