# AZ-900 Module 4 Quiz: Describe the core architectural components of Azure

**Exam domain:** Domain 2: Describe Azure architecture and services (35–40%)  
**Source module:** [Describe the core architectural components of Azure](https://learn.microsoft.com/en-us/training/modules/describe-core-architectural-components-of-azure/) (Microsoft Learn, course AZ-900T00)  
**Units covered:** What is Microsoft Azure; Get started with Azure accounts; Describe Azure physical infrastructure; Describe Azure management infrastructure  
**Questions:** 20 — Section A: 11 multiple choice · Section B: 7 true/false · Section C: 2 scenarios

Answer key and score guide are at the bottom — cover them while you work.

---

## Section A — Multiple choice

**A1.** What is an Azure availability zone?

- **A.** An isolated instance of Azure used for government or legal compliance needs
- **B.** A pair of regions in the same geography at least 300 miles apart
- **C.** A logical container for resources that share the same lifecycle
- **D.** Physically separate datacenters within one region, each with independent power and cooling

**A2.** How many availability zones are present, at minimum, in every availability zone-enabled region?

- **A.** Six
- **B.** Two
- **C.** Three
- **D.** Four

**A3.** Which of these is a ZONE-REDUNDANT service, where the platform replicates across zones automatically?

- **A.** Managed disks
- **B.** Virtual machines deployed to a zone
- **C.** Public IP addresses
- **D.** Azure SQL Database

**A4.** Most Azure regions are paired with another region in the same geography that is at least how far away?

- **A.** 300 miles
- **B.** 500 miles
- **C.** 1,000 miles
- **D.** 100 miles

**A5.** Which region is paired in only ONE direction, with a secondary region outside its own geography?

- **A.** Italy North
- **B.** Brazil South (secondary: South Central US)
- **C.** West US (paired with East US)
- **D.** Southeast Asia (paired with East Asia)

**A6.** Which service is global and does NOT require you to choose a region?

- **A.** Azure Virtual Machines
- **B.** Azure Storage accounts
- **C.** Microsoft Entra ID
- **D.** Azure Virtual Network

**A7.** How are the Azure China sovereign regions (such as China East and China North) operated?

- **A.** Directly by Microsoft as one part of the single, global Azure public instance
- **B.** Via a 21Vianet partnership; Microsoft doesn't directly run the datacenters
- **C.** By screened U.S. personnel with extra compliance certifications
- **D.** As standard public regions paired with US regions

**A8.** Which statement about resource groups is TRUE?

- **A.** A resource can belong to several resource groups at once
- **B.** Resource groups can be nested inside other resource groups
- **C.** A resource group can be renamed after it's created
- **D.** Deleting a resource group deletes every resource inside it

**A9.** Which two types of boundaries does an Azure subscription provide?

- **A.** A billing boundary and an access control boundary
- **B.** A geographic boundary and a data residency boundary
- **C.** A network boundary and a DNS boundary
- **D.** A fault boundary and an update boundary

**A10.** How many levels deep can management groups be nested (not counting the root level or the subscription level)?

- **A.** Ten
- **B.** 10,000
- **C.** Six
- **D.** Three

**A11.** What is the correct hierarchy, from top to bottom?

- **A.** Management groups → subscriptions → resource groups → resources
- **B.** Subscriptions → management groups → resource groups → resources
- **C.** Management groups → resource groups → subscriptions → resources
- **D.** Resource groups → subscriptions → management groups → resources

## Section B — True or false

**B1.** An Azure account can have only one subscription.

**B2.** Each management group and each subscription can have only one parent.

**B3.** All Azure services automatically replicate data and fail over to the paired region.

**B4.** Every Azure region supports availability zones.

**B5.** Every Microsoft Entra tenant has a single top-level Tenant Root Group.

**B6.** Planned Azure updates are rolled out to paired regions one region at a time.

**B7.** A policy applied at a management group can be overridden by the owner of a subscription beneath it.

## Section C — Scenarios

**C1.** Scenario: An app must keep running if a single datacenter in its region fails. Data must stay in the same region, and the team wants the simplest design that meets this goal. What should they do?

- **A.** Place all VMs in a single availability zone
- **B.** Split the resources across several resource groups in the region
- **C.** Move the workload to a sovereign region
- **D.** Spread resources across availability zones in the region

**C2.** Scenario: The IT department has eight subscriptions. You must (1) restrict VM deployments to approved regions in all of them and (2) give the security team Reader access to all of them, with the least ongoing effort. What should you do?

- **A.** Create a separate Azure account for the IT department
- **B.** Group them under an IT management group; assign policy and Reader role there
- **C.** Merge all of the IT resources into one resource group in a single subscription
- **D.** Assign the policy and role separately on every resource group

---

## Answer key

**Quick key:** A1 D, A2 C, A3 D, A4 A, A5 B, A6 C, A7 B, A8 D, A9 A, A10 C, A11 A, B1 F, B2 T, B3 F, B4 F, B5 T, B6 T, B7 F, C1 D, C2 B

### Section A

**A1 — D.** *Concept: Availability zones*  
Availability zones are isolation boundaries inside one region: if one zone goes down, the others keep working.  
Why not the others: A — That's a sovereign region. · B — That's a region pair. · C — That's a resource group.

**A2 — C.** *Concept: Minimum zones per region*  
A minimum of three separate zones ensures resiliency. Note: not every region supports zones.  
Why not the others: A — Six is the management group nesting depth — a different number. · B — Too few — the minimum is three. · D — More than the guaranteed minimum.

**A3 — D.** *Concept: Zonal vs zone-redundant services*  
Zone-redundant services (the module's examples are zone-redundant storage and SQL Database) replicate across zones for you. Zonal services are pinned to one zone you choose.  
Why not the others: A — Zonal. · B — Zonal — you pin a VM to a specific zone. · C — Listed as zonal in the module.

**A4 — A.** *Concept: Region pair distance*  
Region pairs sit at least 300 miles apart so a single regional disaster is unlikely to hit both.  
Why not the others: B — Not the stated minimum. · C — Not the stated minimum. · D — Too close.

**A5 — B.** *Concept: Region pair exceptions*  
Brazil South's secondary is South Central US, but South Central US's secondary is NOT Brazil South. It's the classic one-direction exception.  
Why not the others: A — Italy North has no traditional pair; it relies on availability zones and geo-redundant storage instead. · C — A standard two-way pair. · D — A standard two-way pair in the same geography.

**A6 — C.** *Concept: Global services*  
Microsoft Entra ID, Azure Traffic Manager, and Azure DNS are named as global services that don't need a region selection.  
Why not the others: A — VMs are deployed into a region you choose. · B — You choose a primary region for a storage account. · D — Virtual networks are regional resources.

**A7 — B.** *Concept: Sovereign regions*  
This is the distinguishing fact for the China sovereign regions.  
Why not the others: A — Sovereign regions are isolated, and Microsoft doesn't directly maintain the China datacenters. · C — That describes US government regions (US DoD Central, US Gov Virginia). · D — They're isolated from the main instance of Azure.

**A8 — D.** *Concept: Resource group rules*  
Actions on a resource group apply to everything in it — including deletion. That's why grouping by lifecycle is useful.  
Why not the others: A — Every resource belongs to exactly one resource group at a time. · B — Resource groups can't be nested. · C — Resource groups can't be renamed.

**A9 — A.** *Concept: Subscription boundaries*  
Each subscription gets separate billing reports/invoices, and access-management policies are applied at the subscription level.  
Why not the others: B — Those relate to regions and geographies. · C — Those relate to virtual networks and DNS zones. · D — Fault and update domains belong to VM availability sets.

**A10 — C.** *Concept: Management group limits*  
Six levels of depth. Don't confuse it with 10,000, the maximum number of management groups in a single directory.  
Why not the others: A — Not the limit. · B — That's the max NUMBER of management groups per directory, not nesting depth. · D — Too few.

**A11 — A.** *Concept: Hierarchy*  
Resources live in resource groups, resource groups in subscriptions, subscriptions under management groups (all under the Tenant Root Group).  
Why not the others: B — Management groups sit ABOVE subscriptions. · C — Resource groups sit inside subscriptions. · D — Upside down.

### Section B

**B1 — False.** *Concept: Subscriptions per account*  
An account can have multiple subscriptions; only one is required.

**B2 — True.** *Concept: Single parent*  
Listed as an important fact about management groups.

**B3 — False.** *Concept: Automatic replication*  
Not all services do. In those cases, the customer must configure recovery and replication.

**B4 — False.** *Concept: AZ support*  
Not all regions currently support availability zones.

**B5 — True.** *Concept: Tenant Root Group*  
All other management groups and subscriptions fold up to it, so you can apply governance globally.

**B6 — True.** *Concept: Region pair update rollout*  
This minimizes downtime and the risk of an application outage.

**B7 — False.** *Concept: Management group policy override*  
Inherited management-group policies can't be overridden by the resource or subscription owner — that's what strengthens governance.

### Section C

**C1 — D.** *Concept: Choosing availability zones*  
Availability zones are physically separate datacenters in one region, so they protect against a datacenter failure without leaving the region.  
Why not the others: A — One zone failing would take everything down. · B — Resource groups are logical containers, not physical isolation. · C — Sovereign regions are about compliance isolation, not datacenter resilience.

**C2 — B.** *Concept: Using management groups*  
Policy and RBAC assignments at a management group inherit to every subscription, resource group, and resource beneath it.  
Why not the others: A — A new account doesn't apply governance across the existing subscriptions. · C — Disruptive and unnecessary — management groups exist for this. · D — Works, but it's high effort and new resource groups can be missed.

---

## Score guide

| Score (out of 20) | What it means |
| --- | --- |
| 18–20 | Exam-ready on this module. Skim the misses and move on. |
| 15–17 | Solid. Re-read the units behind each miss before the domain review. |
| 12–14 | Shaky. Re-read the module, focusing on the comparisons and gotchas you missed. |
| 0–11 | Redo the module, then retake this quiz. |

The real exam needs 700 out of 1,000 (a scaled score, not a straight percentage), so aim for 80%+ on practice quizzes to leave a margin.
