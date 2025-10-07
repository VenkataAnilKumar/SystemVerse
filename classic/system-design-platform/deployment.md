# CI/CD & Deployment

Continuous Integration (CI) and Continuous Deployment (CD) are essential for delivering reliable software at scale. Modern deployment strategies reduce risk and downtime.

## CI (Continuous Integration)
- Automate linting, testing, and building on every commit. Use tools like GitHub Actions, GitLab CI, or Jenkins.
- Run unit, integration, and end-to-end (e2e) tests. [See: Google Testing Blog](https://testing.googleblog.com/)

## CD (Continuous Deployment/Delivery)
- Automate deployment to staging and production environments. Use ArgoCD, Spinnaker, or Jenkins pipelines.
- Use infrastructure-as-code (IaC) tools (e.g., Terraform, CloudFormation) for repeatable, auditable deployments.

## Deployment Strategies
- **Blue/Green Deployments:** Deploy new version alongside old, switch traffic after validation. Enables instant rollback.
- **Rolling Deployments:** Gradually replace old instances with new ones. Minimizes downtime.
- **Canary Releases:** Release to a small subset of users before full rollout.

## Best Practices
- Monitor deployments and roll back on failure.
- Use feature flags for safe releases.
- Keep environments as similar as possible (dev ≈ prod).

## References
- [Continuous Delivery by Jez Humble](https://continuousdelivery.com/)
- [Google SRE Book: Release Engineering](https://sre.google/books/)
- [AWS Deployment Strategies](https://aws.amazon.com/whitepapers/deployment-strategies/)
- [Awesome Scalability](https://github.com/binhnguyennus/awesome-scalability)
