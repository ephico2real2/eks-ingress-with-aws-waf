### Title: Collaborative Implementation of EKS Ingress Controller with AWS WAF

---

#### Slide 1: Project Overview and Team Collaboration
- **Objective**: Seamlessly integrate AWS EKS Ingress Controller with AWS WAF for enhanced security and traffic management.
- **Teams Involved**:
  - Application Team (My Role): Responsible for application-specific configurations and deployments.
  - DevOps Team: Focused on infrastructure, EKS setup, and AWS WAF integration.
- **Collaboration Strategy**: Maintaining clear communication channels, regular updates, and coordinated efforts between teams.

---

#### Slide 2: Strategic Deployment by DevOps Team
- **Task**: Deploying a new Ingress Controller in the AWS EKS cluster.
- **Key Approach**:
  - Introduction of a new Ingress class with a "-waf" suffix.
  - Ensured no disruption or override of existing Ingress configurations, preserving current operations.
- **Outcome**: Successful deployment with minimal interference to ongoing services.

---

#### Slide 3: Application Team's Adaptive Configuration
- **My Role**: Adapting and optimizing the application deployment to leverage the new Ingress Controller.
- **Actions Taken**:
  - Modified the Helm chart to create a new Ingress resource.
  - Named and configured the new Ingress to utilize the "-waf" Ingress class.
- **Result**: This methodical approach ensured no technical debt and prevented accidental overrides of existing applications.

---

#### Slide 4: Validation, DNS Cutover, and Seamless Transition
- **Validation**: Thoroughly tested the application with the new AWS WAF-backed URL, ensuring functionality and security enhancements.
- **DNS Cutover**: Carefully planned and executed DNS cutover.
  - Redirected the public FQDN of the apps to point to the new AWS Load Balancer.
- **Zero Downtime**: Achieved a smooth transition with no service interruptions, maintaining optimal user experience and service continuity.
