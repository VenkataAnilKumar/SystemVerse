
# Cloud-Native Considerations

Cloud-native design enables systems to scale, recover, and evolve rapidly. This section covers practical strategies, examples, and checklists for robust cloud-native systems.

## Containers
- Use Docker to package applications and dependencies for consistent deployment across environments. [Docker Best Practices](https://docs.docker.com/develop/dev-best-practices/)
- **Checklist:**
	- [ ] All services containerized with Docker
	- [ ] Images are scanned for vulnerabilities
	- [ ] Use multi-stage builds for smaller images

## Orchestration
- Use Kubernetes (EKS/GKE/AKS) for automated deployment, scaling, and management of containerized applications. [Kubernetes Official Docs](https://kubernetes.io/docs/)
- **Checklist:**
	- [ ] All deployments managed by Kubernetes manifests
	- [ ] Resource requests/limits set for all pods
	- [ ] Liveness/readiness probes configured

## Cloud Services
- **Storage:** Use S3 (AWS) or GCS (Google Cloud) for object storage.
- **Databases:** Use managed RDS/CloudSQL for relational data.
- **CDN:** Use CloudFront, Cloud CDN, or similar for global asset delivery.
- **Monitoring:** Use managed monitoring and alerting (CloudWatch, Stackdriver, Datadog).

## Best Practices
- Design for failure: use multi-AZ/multi-region deployments.
- Automate infrastructure with IaC (Terraform, CloudFormation).
- Secure by default: encrypt data at rest and in transit, use IAM roles.
- Regularly review cloud costs and optimize resources.

---

## Actionable Checklist
- [ ] All infrastructure is defined as code (IaC)
- [ ] Backups and disaster recovery plans in place
- [ ] Security groups and IAM roles reviewed regularly
- [ ] Cloud spend monitored and optimized

---

## References
- [AWS Well-Architected Framework](https://aws.amazon.com/architecture/well-architected/)
- [Google Cloud Architecture Framework](https://cloud.google.com/architecture/framework)
- [Kubernetes Official Docs](https://kubernetes.io/docs/)
- [Awesome Scalability](https://github.com/binhnguyennus/awesome-scalability)
