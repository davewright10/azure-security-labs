# azure-security-labs
Hands-on Azure security governance labs. (Policy as Code, IaC, CI/CD, Entra ID)

# Who I am
Application owner at a Fortune 500 bank building hands-on Azure security
governance skills — Policy as Code, Infrastructure as Code, CI/CD, and
identity governance.

## Labs

| Day | Lab | What it demonstrates |
|-----|-----|----------------------|
| 1 | [RBAC Foundations](./day1-rbac-foundations/) | Least privilege and role scoping in Azure |
| 2 | [Azure Policy (Built-in)](./day2-azure-policy-builtin/) | Detective controls and compliance dashboards |
| 3 | [Policy as Code](./day3-policy-as-code/) | Preventive controls: custom deny policies + remediation |
| 4 | [Entra ID Governance](./day4-entra-id-governance/) | Identity lifecycle and access reviews |
| 5 | [Terraform IaC](./day5-terraform-iac/) | Declarative, auditable infrastructure |
| 6 | [GitHub Actions CI/CD](./day6-github-actions-cicd/) | Pipeline-enforced change management |
| 7 | [Defender for Cloud](./day7-defender-for-cloud/) | Posture management and secure score |

## Why these labs

I currently own compliance deliverables, patching evidence, configuration
management remediation, and change management for enterprise applications —
manually. Each lab maps that exact governance work to the cloud-native
tooling that automates it: Azure Policy replaces manual CM checks, Terraform
makes change management declarative and reviewable, and CI/CD pipelines
enforce the segregation of duties I currently verify by hand.
