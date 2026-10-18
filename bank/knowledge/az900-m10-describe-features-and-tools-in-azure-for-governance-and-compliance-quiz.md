# AZ-900 Module 10 Quiz: Describe features and tools in Azure for governance and compliance

**Exam domain:** Domain 3: Describe Azure management and governance (30–35%)  
**Source module:** [Describe features and tools in Azure for governance and compliance](https://learn.microsoft.com/en-us/training/modules/describe-features-tools-azure-for-governance-compliance/) (Microsoft Learn, course AZ-900T00)  
**Units covered:** Describe the purpose of Microsoft Purview; Describe the purpose of Azure Policy; Describe the purpose of resource locks; Describe the purpose of the Service Trust Portal  
**Questions:** 15 — Section A: 7 multiple choice · Section B: 6 true/false · Section C: 2 scenarios

Answer key and score guide are at the bottom — cover them while you work.

---

## Section A — Multiple choice

**A1.** What are the two main solution areas of Microsoft Purview?

- **A.** Risk and compliance, and unified data governance
- **B.** Identity management and access control
- **C.** Azure Policy definitions and resource locks
- **D.** Threat assessment and active threat defense

**A2.** Where can Microsoft Purview's unified data governance manage data?

- **A.** Microsoft 365 services such as Teams only
- **B.** On-premises, multicloud (e.g., Amazon S3), and SaaS
- **C.** On-premises SQL Server databases only
- **D.** Azure subscriptions only, not other clouds

**A3.** What is an Azure Policy initiative?

- **A.** A lock that prevents resources from being deleted
- **B.** A role assignment that grants permissions at a scope
- **C.** A group of related policy definitions toward a larger goal
- **D.** A JSON template that deploys resources

**A4.** What does a ReadOnly resource lock do?

- **A.** Authorized users can read the resource but can't update or delete it
- **B.** Users can't read the resource at all
- **C.** It applies only to users who aren't owners
- **D.** Authorized users can read and modify the resource but can't delete it

**A5.** You're an Owner of a resource that has a Delete lock, and you need to delete it. What must you do?

- **A.** Assign yourself the Contributor role, then delete it
- **B.** Remove the lock first, then delete the resource
- **C.** Nothing — Owners automatically bypass resource locks
- **D.** Open a support ticket, since locks can't be removed

**A6.** What is the Microsoft Service Trust Portal used for?

- **A.** Enforcing configuration rules and standards on your Azure resources
- **B.** Classifying sensitive data across your estate
- **C.** Tracking outages that affect your Azure services
- **D.** Reading Microsoft's security, privacy, and compliance reports

**A7.** You create a policy that allows only certain VM sizes. What happens to VMs that existed before the policy?

- **A.** They're ignored; only new VMs are evaluated
- **B.** Azure Policy evaluates them and flags any noncompliant VMs
- **C.** They're automatically exempt from all policies
- **D.** They're deleted automatically

## Section B — True or false

**B1.** Resource locks apply regardless of RBAC permissions.

**B2.** A Delete lock prevents authorized users from modifying a resource.

**B3.** A resource lock on a resource group doesn't affect the resources inside it.

**B4.** Azure Policy can automatically remediate some noncompliant resources, such as adding a missing tag.

**B5.** Some Service Trust Portal resources require signing in with a Microsoft cloud services account and accepting an NDA.

**B6.** Azure Policy can only report noncompliance; it can't prevent noncompliant resources from being created.

## Section C — Scenarios

**C1.** Scenario: (1) All resources must be deployed only to EU regions. (2) A production database must not be deleted accidentally, even by admins. (3) Auditors want Microsoft's independent audit reports. Which combination fits?

- **A.** (1) Azure Policy, (2) RBAC Reader role, (3) Service Trust Portal
- **B.** (1) Resource lock, (2) Azure Policy, (3) Microsoft Purview
- **C.** (1) Microsoft Purview, (2) Delete lock, (3) Azure Advisor
- **D.** (1) Azure Policy, (2) Delete lock, (3) Service Trust Portal

**C2.** Scenario: A data team needs an up-to-date map of all its data across Azure SQL, on-premises databases, and Amazon S3, including sensitive data classification and end-to-end lineage. Which service fits?

- **A.** Azure Monitor Log Analytics
- **B.** Azure Policy
- **C.** Microsoft Purview
- **D.** Microsoft Defender for Cloud

---

## Answer key

**Quick key:** A1 A, A2 B, A3 C, A4 A, A5 B, A6 D, A7 B, B1 T, B2 F, B3 F, B4 T, B5 T, B6 F, C1 D, C2 C

### Section A

**A1 — A.** *Concept: Purview solution areas*  
Purview is a family of data governance, risk, and compliance solutions.  
Why not the others: B — That's Microsoft Entra ID. · C — Those are Azure governance features, not Purview's areas. · D — Sounds like Defender for Cloud.

**A2 — B.** *Concept: Purview scope*  
Purview brings insights about on-premises, multicloud, and SaaS data together — not just Azure.  
Why not the others: A — Microsoft 365 is a core part of risk and compliance, but governance reaches further. · C — Too narrow. · D — Too narrow — Purview spans other clouds too.

**A3 — C.** *Concept: Policy initiatives*  
Initiatives bundle policies, e.g., 'Enable Monitoring in Azure Security Center' contains 100+ definitions.  
Why not the others: A — That's a resource lock. · B — That's Azure RBAC. · D — That's an ARM template.

**A4 — A.** *Concept: ReadOnly lock*  
ReadOnly is similar to restricting everyone to the Reader role's permissions. A Delete lock still allows reads and modifications.  
Why not the others: B — ReadOnly allows reading. · C — Locks apply regardless of RBAC role — even owners. · D — That's a Delete lock.

**A5 — B.** *Concept: Removing locks*  
Locks apply regardless of RBAC permissions. Modifying a locked resource is a two-step process.  
Why not the others: A — No RBAC role overrides a lock. · C — Even owners must remove the lock first. · D — Locks can be removed by anyone with permission to manage them.

**A6 — D.** *Concept: Service Trust Portal*  
It provides content about how Microsoft implements controls that protect its cloud services and customer data.  
Why not the others: A — That's Azure Policy. · B — That's Microsoft Purview. · C — That's Azure Service Health.

**A7 — B.** *Concept: Policy on existing resources*  
Azure Policy evaluates all current resources, including ones created before the policy, and highlights noncompliance.  
Why not the others: A — Existing VMs are evaluated too. · C — Exemptions are something you mark explicitly. · D — Policy doesn't delete existing resources.

### Section B

**B1 — True.** *Concept: Locks vs RBAC*  
Even an Owner must remove the lock before performing the blocked action.

**B2 — False.** *Concept: Delete lock behavior*  
A Delete lock still allows reads and modifications; only deletion is blocked. ReadOnly blocks modifications.

**B3 — False.** *Concept: Lock inheritance*  
Locks are inherited — a lock on a resource group applies to every resource in it.

**B4 — True.** *Concept: Policy remediation*  
The module's example: require an AppName tag and have Policy add it when missing.

**B5 — True.** *Concept: Service Trust Portal access*  
You must sign in with a Microsoft Entra work or school account and accept the NDA for compliance materials.

**B6 — False.** *Concept: Policy prevention*  
Azure Policy can prevent noncompliant resources from being created.

### Section C

**C1 — D.** *Concept: Choosing governance tools*  
Policy enforces allowed locations; a Delete lock blocks deletion regardless of role; the Service Trust Portal hosts Microsoft's compliance documents.  
Why not the others: A — RBAC doesn't stop admins (owners) from deleting; a lock does. · B — Locks don't restrict location; Purview governs YOUR data, not Microsoft's audit reports. · C — Purview doesn't enforce deployment locations; Advisor doesn't provide audit reports.

**C2 — C.** *Concept: Choosing Purview*  
Data map, classification, and lineage across on-premises, multicloud, and SaaS is Purview's unified data governance.  
Why not the others: A — Queries monitoring data, not data lineage. · B — Governs resource configuration, not data discovery or lineage. · D — Security posture and threat protection, not a data map.

---

## Score guide

| Score (out of 15) | What it means |
| --- | --- |
| 14–15 | Exam-ready on this module. Skim the misses and move on. |
| 12–13 | Solid. Re-read the units behind each miss before the domain review. |
| 9–11 | Shaky. Re-read the module, focusing on the comparisons and gotchas you missed. |
| 0–8 | Redo the module, then retake this quiz. |

The real exam needs 700 out of 1,000 (a scaled score, not a straight percentage), so aim for 80%+ on practice quizzes to leave a margin.
