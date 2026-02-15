# Azure Policy Lab 1: Audit vs Deny (Allowed Locations)

This repository supports my lab walkthrough video on using **Azure Policy** to enforce governance by comparing **Audit** vs **Deny** effects using an **Allowed locations** policy assignment.  
📺 **Watch the lab video on YouTube:** (add your link)

---

## 🔍 Lab Overview

In this lab, you’ll learn how to:

- Create an Azure Policy assignment at **Resource Group** scope
- Configure the **Allowed locations** policy for governance controls
- Compare **Audit** vs **Deny** effects in Azure Policy
- Test deployments to validate compliance behavior
- Review compliance results in the **Policy Compliance** dashboard

These tasks are fundamental for implementing governance guardrails and enforcing standards across Azure environments.

---

## 🧪 Lab Scenario

Your organization is standardizing Azure deployments to reduce risk and ensure resources are created only in approved regions. You are responsible for implementing governance using Azure Policy to either **audit** non-compliant deployments or **deny** them entirely.

---

## 🛠️ Key Tasks

✅ **Task 1: Create the Lab Resource Group**
- Create a resource group named `rg-policy-lab`
- Identify one **allowed** region and one **blocked** region for testing

✅ **Task 2: Assign Policy in Audit Mode**
- Assign the built-in **Allowed locations** policy at `rg-policy-lab` scope
- Configure the allowed region list (example: `East US`)
- Deploy a resource in a blocked region to confirm:
  - Deployment succeeds
  - Resource becomes **non-compliant** (Audit)

✅ **Task 3: Assign Policy in Deny Mode**
- Assign the same policy again (or update effect) with **Deny**
- Attempt the same blocked-region deployment to confirm:
  - Deployment fails with a policy violation
- Deploy in an allowed region to confirm:
  - Deployment succeeds and is compliant

✅ **Task 4: Review Compliance Results**
- Use **Azure Policy → Compliance** to view compliance state
- Filter by `rg-policy-lab` scope and review non-compliance details

---

## 📁 Suggested Files

- `lab-guide.md`: Full lab steps in markdown format for offline use  
- `screenshots/`: Visuals of policy assignments, compliance results, and deployment errors  
- `notes.md` (optional): Quick “exam takeaways” like Audit vs Deny definitions  

---

## 🔗 Learn More

- [Azure Policy overview](https://learn.microsoft.com/azure/governance/policy/overview)  
- [Quickstart: Create a policy assignment in the Azure portal](https://learn.microsoft.com/azure/governance/policy/assign-policy-portal)  
- [Azure Policy compliance](https://learn.microsoft.com/azure/governance/policy/how-to/get-compliance-data)  
- [Tutorial: Manage tag governance with Azure Policy (related)](https://learn.microsoft.com/azure/governance/policy/tutorials/govern-tags)

---

## 🧵 Tags

`#Azure` `#AzurePolicy` `#Governance` `#Compliance` `#AZ104` `#AzureLabs`

Created by: **Zion Spearman**  
Use and modify this lab freely for study and practice.
