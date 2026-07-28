## ✅ Day 2: Azure Policy

**🎯 Objective:** Assign built-in Azure Policies at the resource group scope and observe preventive enforcement — the cloud-native equivalent of the compliance deliverables I produce manually today.

### 🛠️ What was built
- Created resource group `rg-lab-policy` in East US
- Assigned two built-in policies at the resource group scope:
  - **Allowed locations** — restricts deployments to East US (Deny effect)
  - **Require a tag and its value on resources** — requires `env=lab` on all resources (Deny effect)
- Tested enforcement by attempting non-compliant deployments:
  - 🌍 Storage account in West Europe → blocked by policy
  - 🏷️ Storage account missing the `env=lab` tag → blocked by policy
  - ✅ Storage account in East US with the correct tag → succeeded
- Reviewed the Compliance dashboard and confirmed both policies at 100% compliant, with zero non-compliant resources — since Deny prevents violations from ever being created

### 🧠 Security concept demonstrated
This lab focused on **preventive controls via Policy as Code**. In my current role, I produce audit evidence and track compliance deliverables manually, on a quarterly cycle. Azure Policy automates that same function — the policy definition *is* the control, and the compliance dashboard *is* the evidence, generated continuously rather than produced by hand. Both policies I assigned used a Deny effect, meaning violations are blocked before they exist rather than flagged after the fact — a stronger posture than the detective/audit controls I'd originally planned to test, and a good real-world illustration of why "shift left" matters in cloud governance.

**Screenshots:** 


<img width="501" height="420" alt="02-tagged-resource-json" src="https://github.com/user-attachments/assets/1b80edbf-0aa6-4035-9a00-99c6b36fe964" />
<img width="1356" height="178" alt="01-westeurope-deny-error" src="https://github.com/user-attachments/assets/5e2fa541-eb6b-46ef-93c0-611050e73fd2" />
<img width="1355" height="137" alt="03-missing-tag-deny-error-redacted" src="https://github.com/user-attachments/assets/368ecdd8-e168-468f-80b3-d13d0f5cbc30" />
<img width="1477" height="493" alt="04-compliance-dashboard" src="https://github.com/user-attachments/assets/ac7e1f36-b18f-44e7-a689-9ed9eefa405e" />
<img width="1471" height="460" alt="05-policy-assignments" src="https://github.com/user-attachments/assets/e1d16f0c-f05a-4f4c-906d-aa3313cb4682" />






