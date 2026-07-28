Day 1: Azure Foundations + RBAC (Governance Baseline)
Objective:
  The objective of this lab was to understand Azure's resource hierarchy and apply RBAC least-privilege at the resource group scope, the cloud equivalent of the access governance I run today.
  
What was Built:
- Created resource group rg-lab-day1 in East US.
- Created a Standard LRS storage account inside it.
- Applied tags to both resources:
    env=lab
    owner=dwright
- Created a second test user in Microsoft Entra ID.
- Assigned the Reader role to the test user at the resource group scope via Access control (IAM).
- Verified Reader permissions — observed what the test user could and couldn't do.
- Ran CLI equivalents:
  powershell
     az group list
     az role assignment list --resource-group rg-lab-day1
- Deleted the resource group at the end of the session:
  powershell
     az group delete -n rg-lab-day1 --yes

Security Concept Demonstrated:
- Today's session focused on Role-Based Access Control. In my current role, I apply the principle of least privilege through an internal access request management tool, ensuring users receive only the minimum permissions needed to perform their job duties. In the cloud, RBAC lets me manage that access directly by assigning roles at the resource or resource group level myself rather than routing through a request tool.

Evidence
<img width="1033" height="282" alt="image" src="https://github.com/user-attachments/assets/a7d43ede-afcb-4c70-8432-c83be1f9de37" />
<img width="1120" height="156" alt="image" src="https://github.com/user-attachments/assets/05ed717e-9ab5-4fb5-bc0b-faa8c1fd2df2" />
<img width="984" height="664" alt="image" src="https://github.com/user-attachments/assets/cdd7687b-594d-4474-8a2a-7ec25ed1407d" />
<img width="853" height="317" alt="image" src="https://github.com/user-attachments/assets/1cff2bb0-46f9-4407-b778-300d62e2b1f7" />
<img width="832" height="326" alt="image" src="https://github.com/user-attachments/assets/94af5c92-ab0e-46fe-955b-f09d0a67d2cd" />
<img width="1092" height="423" alt="image" src="https://github.com/user-attachments/assets/6e0e8817-57dd-4cd2-8616-c87845cef709" />
<img width="919" height="60" alt="image" src="https://github.com/user-attachments/assets/91ce7e9c-b75d-4707-9a95-3d890eeb7155" />










