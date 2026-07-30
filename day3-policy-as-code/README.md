## ✅ Day 3: Policy as Code — Custom Deny Policies

**Objective:** Write and deploy a custom Azure Policy definition (not a built-in) to enforce a preventive control, and verify it actually blocks non-compliant deployments — the shift from consuming a vendor control to authoring one, which maps to writing a custom control or exception in GRC work.

### What was built
- Wrote a custom policy definition in JSON denying storage accounts with public blob access enabled
- Verified the target property alias (`allowBlobPublicAccess`) against the Azure resource provider before writing the rule, rather than assuming the field name
- Created the policy definition via CLI and assigned it at resource group scope (`rg-lab-day3`)
- Attempted to deploy a non-compliant storage account with public blob access enabled — blocked by policy in real time
- Confirmed the assignment in the Azure Portal Compliance dashboard

### What Broke and how I fixed it
The CLI rejected my first attempt with `(InvalidPolicyRule) Could not find member 'properties' on object of type 'PolicyRuleDefinition'`. I'd passed the full policy definition (with the `properties` wrapper — displayName, mode, description, the works) to the `--rules` flag, which only wants the inner `if`/`then` rule block. The full definition and the CLI's expected rule format are two different shapes for the same concept, and the error message doesn't make that obvious on its own. Stripped it down to just `if`/`then`, re-ran, and the definition created cleanly.

### Security Concept Demonstrated
This lab moved from *using* a control someone else wrote (Day 2's built-in policy) to *authoring* one myself — the same shift as writing a custom control mapping instead of relying on a pre-built framework template. The deny effect is a preventive control: the non-compliant storage account was never created, not flagged after the fact. That's a stronger posture than most of what I evidence manually today, where I'm usually confirming after deployment that something was configured correctly rather than architecturally preventing the misconfiguration from being possible.

**Screenshots:**
<img width="2509" height="450" alt="day3-policy-portal-assignments" src="https://github.com/user-attachments/assets/f4be556d-434c-4a31-990d-f7565a271027" />
<img width="1704" height="896" alt="day3-deny-error" src="https://github.com/user-attachments/assets/0113b761-43f3-453a-9a8b-100e7a426fa9" />
<img width="1627" height="859" alt="day3-policy-definition-create" src="https://github.com/user-attachments/assets/04f82994-5517-42f2-a250-e731c4ccf06a" />
<img width="1713" height="540" alt="day3-policy-assignment-create" src="https://github.com/user-attachments/assets/978d468c-e884-4e69-87d9-93eaa884f0fb" />
<img width="735" height="326" alt="day3-policy-rule-json" src="https://github.com/user-attachments/assets/8a5d276b-c095-499a-a1bd-e9f5f4c0476c" />

