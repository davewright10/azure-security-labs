# 🔐 Azure Security Labs
Hands-on Azure security governance labs — Policy as Code, IaC, CI/CD, and identity governance.

![Azure](https://img.shields.io/badge/Azure-0078D4?style=flat&logo=microsoft-azure&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-623CE4?style=flat&logo=terraform&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/CI%2FCD-GitHub_Actions-2088FF?style=flat&logo=github-actions&logoColor=white)

## 👤 About Me
Application owner at a Fortune 500 bank, working in cybersecurity governance and IAM. Currently building hands-on Azure security engineering skills to transition into cloud security, backed by CompTIA Security+ and ISC2 CC certifications.

[LinkedIn](https://www.linkedin.com/in/davianw/) · [dwright2198@gmail.com](mailto:dwright2198@gmail.com)

## 🚀 Getting Started
Requires an active Azure subscription and Azure CLI installed. Each lab folder contains the commands used — clone the repo and run them against your own subscription to reproduce.

## 🎯 Why This Exists
I currently handle compliance evidence, patching, configuration management, and change management manually. Each lab maps that governance work to the cloud-native tooling that automates it:
- **Azure Policy** replaces manual CM checks
- **Terraform** makes change management declarative and reviewable
- **CI/CD pipelines** enforce the segregation of duties I currently verify by hand

## 🧪 Labs

| Day | Lab | What it demonstrates | Status |
|-----|-----|----------------------|--------|
| 1 | [RBAC Foundations](./day1-rbac) | Least privilege and role scoping in Azure | ✅ Complete |
| 2 | [Azure Policy (Built-in)](./day2-azure-policy-builtin) | Detective controls and compliance dashboards | ✅ Complete |
| 3 | [Policy as Code](./day3-policy-as-code) | Preventive controls: custom deny policies + remediation | ✅ Complete |
| 4 | GitHub Actions CI/CD | Pipeline-enforced change management | 📋 Planned |
| 5 | Defender for Cloud | Posture management and secure score | 📋 Planned |
| 6 | Entra ID Governance | Identity lifecycle and access reviews | 📋 Planned |
| 7 | Terraform IaC | Declarative, auditable infrastructure | 📋 Planned |




