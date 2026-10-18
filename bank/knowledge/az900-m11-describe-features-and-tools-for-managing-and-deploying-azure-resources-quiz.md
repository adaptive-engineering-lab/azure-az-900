# AZ-900 Module 11 Quiz: Describe features and tools for managing and deploying Azure resources

**Exam domain:** Domain 3: Describe Azure management and governance (30–35%)  
**Source module:** [Describe features and tools for managing and deploying Azure resources](https://learn.microsoft.com/en-us/training/modules/describe-features-tools-manage-deploy-azure-resources/) (Microsoft Learn, course AZ-900T00)  
**Units covered:** Describe tools for interacting with Azure; Describe the purpose of Azure Arc; Describe Azure Resource Manager and Azure ARM templates  
**Questions:** 15 — Section A: 7 multiple choice · Section B: 6 true/false · Section C: 2 scenarios

Answer key and score guide are at the bottom — cover them while you work.

---

## Section A — Multiple choice

**A1.** Which statement describes Azure Cloud Shell?

- **A.** A desktop app you install locally that supports PowerShell only
- **B.** A shell that requires a separate sign-in using a service principal account
- **C.** A GUI dashboard that replaces the Azure portal
- **D.** A browser-based, pre-authenticated shell for PowerShell or Azure CLI

**A2.** What is the PRIMARY difference between Azure PowerShell and the Azure CLI?

- **A.** The Azure CLI is graphical, PowerShell is text-based
- **B.** Syntax: the CLI uses Bash-style commands; PowerShell uses cmdlets
- **C.** Azure PowerShell can't be installed on Linux or macOS
- **D.** The Azure CLI can only handle one-off tasks, not repeatable automation

**A3.** Which service receives every request from the portal, CLI, PowerShell, APIs, and SDKs, then authenticates and authorizes it?

- **A.** Azure Resource Manager
- **B.** Azure Arc
- **C.** Azure Cloud Shell
- **D.** Microsoft Entra Connect

**A4.** How do ARM templates define what to deploy?

- **A.** As a YAML pipeline that runs in Azure DevOps
- **B.** As imperative PowerShell commands executed step by step
- **C.** In declarative JSON that describes the desired end state
- **D.** As Bash scripts that run inside Cloud Shell

**A5.** What is Bicep?

- **A.** A declarative language that deploys through ARM, simpler than JSON
- **B.** An imperative scripting language that replaces the Azure CLI and PowerShell
- **C.** A query language for Azure Monitor logs
- **D.** A deployment engine that bypasses Resource Manager

**A6.** How does Azure Arc let you manage resources outside Azure?

- **A.** By creating a private network circuit to Azure
- **B.** By replicating resources to the paired region
- **C.** By migrating on-premises servers into Azure VMs
- **D.** By projecting non-Azure resources into Resource Manager

**A7.** Why is the Azure portal resilient to individual datacenter failures?

- **A.** It goes offline during scheduled maintenance windows
- **B.** It runs in every Azure datacenter and updates without downtime
- **C.** It's hosted in a single primary region with a standby
- **D.** It's accessible only through Cloud Shell during outages

## Section B — True or false

**B1.** Copilot in Azure recommendations can be applied straight to production without review because they come from Azure.

**B2.** You must install the Azure CLI locally before you can use Azure Cloud Shell.

**B3.** Azure Arc can manage Kubernetes clusters and SQL Server instances that run outside Azure.

**B4.** With ARM templates, Resource Manager handles dependency order and parallel deployment.

**B5.** Infrastructure as code means configuring each resource manually in the portal and documenting the steps.

**B6.** Because RBAC is built into Azure Resource Manager, you can apply access control to all services.

## Section C — Scenarios

**C1.** Scenario: A team must deploy identical dev, test, and prod environments repeatedly, in a consistent state, with dependencies deployed in the right order, using syntax that's easy to read. What should they use?

- **A.** Azure Arc
- **B.** Manual configuration in the Azure portal for each environment
- **C.** Bicep files deployed through Azure Resource Manager
- **D.** Commands typed by hand into Cloud Shell each time

**C2.** Scenario: An organization runs servers on-premises and Kubernetes clusters in another public cloud. It wants to apply the same Azure Policy rules and keep one inventory, managed from Azure. What should it use?

- **A.** Azure Migrate
- **B.** Azure ExpressRoute
- **C.** ARM templates
- **D.** Azure Arc

---

## Answer key

**Quick key:** A1 D, A2 B, A3 A, A4 C, A5 A, A6 D, A7 B, B1 F, B2 F, B3 T, B4 T, B5 F, B6 T, C1 C, C2 D

### Section A

**A1 — D.** *Concept: Azure Cloud Shell*  
No local install, it knows who you are and your permissions, and you choose PowerShell or Bash (CLI).  
Why not the others: A — It's browser-based and supports both. · B — It's authenticated with your Azure credentials. · C — It's a command-line shell inside the portal.

**A2 — B.** *Concept: CLI vs PowerShell*  
They're functionally equivalent; the choice mostly comes down to which language you know.  
Why not the others: A — Both are command-line tools. · C — Both install on Windows, Linux, and Mac. · D — Both can orchestrate complex operations through scripts.

**A3 — A.** *Concept: Azure Resource Manager*  
Resource Manager is Azure's deployment and management layer — every tool goes through the same API, so results are consistent.  
Why not the others: B — Extends management to non-Azure resources; it isn't the request-handling layer. · C — One of the tools that sends requests to Resource Manager. · D — Syncs on-premises identities.

**A4 — C.** *Concept: ARM templates*  
You define WHAT you want; Resource Manager handles HOW (ordering, dependencies, parallel deployment).  
Why not the others: A — Not the ARM template format. · B — That's scripting, not a declarative template. · D — Templates CAN call scripts, but the template itself is declarative JSON.

**A5 — A.** *Concept: Bicep*  
Bicep is an easier-to-read alternative to JSON ARM templates; deployments still go through Resource Manager.  
Why not the others: B — Bicep is declarative and doesn't replace the CLI. · C — That's the query language used in Log Analytics. · D — Bicep deploys THROUGH Resource Manager.

**A6 — D.** *Concept: How Azure Arc works*  
Arc makes servers, Kubernetes clusters, SQL Server, and more appear in Resource Manager so you can use Azure governance and monitoring on them.  
Why not the others: A — That's ExpressRoute. · B — That's geo-redundancy, not Arc. · C — That's Azure Migrate.

**A7 — B.** *Concept: Azure portal resiliency*  
That also keeps it close to users, which avoids network slowdowns.  
Why not the others: A — It updates continuously with no downtime. · C — It's present in every datacenter. · D — Cloud Shell is accessed through the portal, not the other way around.

### Section B

**B1 — False.** *Concept: Copilot validation*  
Treat Copilot as an assistant — validate recommendations, confirm permissions, and review changes first.

**B2 — False.** *Concept: Cloud Shell install*  
Cloud Shell is browser-based and requires no local installation.

**B3 — True.** *Concept: Arc resource types*  
Arc supports servers, Kubernetes clusters, Azure data services, SQL Server, and VMs (preview).

**B4 — True.** *Concept: ARM orchestration*  
Orchestration is one of the listed template benefits.

**B5 — False.** *Concept: Infrastructure as code*  
IaC manages infrastructure through code and templates instead of manual configuration.

**B6 — True.** *Concept: RBAC in Resource Manager*  
Listed as a Resource Manager benefit.

### Section C

**C1 — C.** *Concept: Choosing IaC*  
Bicep gives declarative, repeatable (idempotent) deployments with built-in orchestration and simpler syntax than JSON.  
Why not the others: A — Manages non-Azure resources; it isn't a deployment template. · B — Not repeatable or consistent. · D — Not declarative or reliably repeatable.

**C2 — D.** *Concept: Choosing Azure Arc*  
Arc extends Azure governance, policy, and inventory to hybrid and multicloud resources from one place.  
Why not the others: A — Moves workloads into Azure; doesn't manage them where they are. · B — Provides connectivity, not governance. · C — Deploy Azure resources; don't bring outside resources under Azure management.

---

## Score guide

| Score (out of 15) | What it means |
| --- | --- |
| 14–15 | Exam-ready on this module. Skim the misses and move on. |
| 12–13 | Solid. Re-read the units behind each miss before the domain review. |
| 9–11 | Shaky. Re-read the module, focusing on the comparisons and gotchas you missed. |
| 0–8 | Redo the module, then retake this quiz. |

The real exam needs 700 out of 1,000 (a scaled score, not a straight percentage), so aim for 80%+ on practice quizzes to leave a margin.
