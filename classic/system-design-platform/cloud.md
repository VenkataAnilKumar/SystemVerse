# Cloud-Native Considerations

Cloud-native design enables systems to scale, recover, and evolve rapidly. Leverage managed services and automation to maximize reliability and minimize operational overhead.

## Containers
- Use Docker to package applications and dependencies for consistent deployment across environments. [Docker Best Practices](https://docs.docker.com/develop/dev-best-practices/)

## Orchestration
- Use Kubernetes (EKS/GKE/AKS) for automated deployment, scaling, and management of containerized applications. [Kubernetes Official Docs](https://kubernetes.io/docs/)

## Cloud Services
- **Storage:** Use S3 (AWS) or GCS (Google Cloud) for object storage.
- **Databases:** Use managed RDS/CloudSQL for relational data.
- **CDN:** Use CloudFront, Cloud CDN, or similar for global asset delivery.
- **Monitoring:** Use managed monitoring and alerting (CloudWatch, Stackdriver, Datadog).

## Best Practices
- Design for failure: use multi-AZ/multi-region deployments.
- Automate infrastructure with IaC (Terraform, CloudFormation).
- Secure by default: encrypt data at rest and in transit, use IAM roles.

## References
- [AWS Well-Architected Framework](https://aws.amazon.com/architecture/well-architected/)
- [Google Cloud Architecture Framework](https://cloud.google.com/architecture/framework)
- [Kubernetes Official Docs](https://kubernetes.io/docs/)
- [Awesome Scalability](https://github.com/binhnguyennus/awesome-scalability)
