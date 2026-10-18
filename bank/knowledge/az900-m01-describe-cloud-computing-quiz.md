# AZ-900 Module 1 Quiz: Describe cloud computing

**Exam domain:** Domain 1: Describe cloud concepts (25–30%)  
**Source module:** [Describe cloud computing](https://learn.microsoft.com/en-us/training/modules/describe-cloud-compute/) (Microsoft Learn, course AZ-900T00)  
**Units covered:** What is cloud computing; Describe the shared responsibility model; Define cloud models; Describe the consumption-based model  
**Questions:** 17 — Section A: 9 multiple choice · Section B: 6 true/false · Section C: 2 scenarios

Answer key and score guide are at the bottom — cover them while you work.

---

## Section A — Multiple choice

**A1.** Under the shared responsibility model, which of these is ALWAYS the cloud provider's responsibility, regardless of service type?

- **A.** The physical network
- **B.** The accounts and identities in your environment
- **C.** Operating system patching
- **D.** The devices allowed to connect to your cloud

**A2.** Which of these is ALWAYS the customer's responsibility, regardless of service type?

- **A.** The operating system on your servers
- **B.** Network controls between your resources
- **C.** The information and data stored in the cloud
- **D.** The physical hosts that run your workloads

**A3.** Which cloud SERVICE TYPE places the most responsibility on the customer?

- **A.** Software as a service (SaaS)
- **B.** Infrastructure as a service (IaaS)
- **C.** Hybrid cloud (mixing public and private)
- **D.** Platform as a service (PaaS)

**A4.** What is the key difference between a public cloud and a private cloud?

- **A.** Public cloud is open to any buyer; private cloud serves a single entity
- **B.** A private cloud requires no capital expenditure to scale up
- **C.** A public cloud gives you complete control over resources and security
- **D.** A private cloud must be hosted in your own on-site datacenter

**A5.** Which cloud model lets you decide where each application runs and keep control of security, compliance, or legal requirements while still using public cloud resources?

- **A.** Public cloud
- **B.** Hybrid cloud
- **C.** Multicloud
- **D.** Private cloud

**A6.** Which scenario describes a multicloud environment?

- **A.** Hosting a private cloud in a third party's dedicated datacenter
- **B.** Combining a private cloud and one public cloud in a single interconnected environment
- **C.** Running several subscriptions inside a single Azure account
- **D.** Using two or more public cloud providers and managing resources and security in each

**A7.** Which Azure offering helps you manage environments that are Azure-only, in your own private datacenter, hybrid, or spread across multiple cloud providers?

- **A.** Azure DNS
- **B.** Azure VMware Solution
- **C.** Azure Arc
- **D.** Azure Migrate

**A8.** Cloud computing is classified as which type of expense, and why?

- **A.** Capital expenditure (CapEx), because you rent compute and storage
- **B.** Operational expenditure (OpEx), because you pay for services as you consume them
- **C.** Operational expenditure (OpEx), because you buy hardware ahead of expected demand
- **D.** Capital expenditure (CapEx), because the provider buys hardware up front

**A9.** Which of the following is NOT a benefit of the consumption-based model?

- **A.** The ability to release resources when demand decreases
- **B.** No upfront costs for hardware or datacenter infrastructure
- **C.** The ability to add resources when demand increases
- **D.** A guaranteed fixed monthly bill regardless of how much you use

## Section B — True or false

**B1.** If you deploy a VM and install SQL Server on it yourself, the cloud provider is responsible for patching the database.

**B2.** In a private cloud, hardware must be purchased for startup and maintenance.

**B3.** In a traditional datacenter, overestimating capacity leads to degraded application performance.

**B4.** In a public cloud, you don't have complete control over resources and security.

**B5.** In PaaS and SaaS, identity and access is shared: you manage users, roles, and policies while the provider runs the authentication platform.

**B6.** A private cloud must be hosted in your organization's own on-site datacenter.

## Section C — Scenarios

**C1.** Scenario: A company runs its private cloud on VMware and wants to move those workloads into Azure with minimal re-platforming, keeping VMware integration. Which option fits best?

- **A.** Add a second public cloud provider to create a multicloud setup
- **B.** Azure Arc
- **C.** Rebuild every workload as a SaaS application
- **D.** Azure VMware Solution

**C2.** Scenario: A retailer's private cloud handles normal load well, but holiday traffic creates temporary surges. Regulations require customer payment data to stay on the company's private infrastructure. Which approach fits best?

- **A.** Stay private-only and buy enough hardware to cover the holiday peak
- **B.** Move everything to the public cloud
- **C.** Hybrid cloud: keep payment data private, burst to public for surges
- **D.** Adopt a multicloud design across two public providers

---

## Answer key

**Quick key:** A1 A, A2 C, A3 B, A4 A, A5 B, A6 D, A7 C, A8 B, A9 D, B1 F, B2 T, B3 F, B4 T, B5 T, B6 F, C1 D, C2 C

### Section A

**A1 — A.** *Concept: Shared responsibility: provider-owned layers*  
The provider always owns the physical datacenter, physical network, physical hosts, and infrastructure.  
Why not the others: B — Always the customer's responsibility. · C — Depends on the service type: yours in IaaS, the provider's in PaaS/SaaS. · D — Always the customer's responsibility, in every service type.

**A2 — C.** *Concept: Shared responsibility: customer-owned items*  
Data, connecting devices, and accounts/identities always stay with the customer — even in SaaS.  
Why not the others: A — Depends on the service type (yours in IaaS only). · B — Depends on the service type. · D — Always the provider's responsibility.

**A3 — B.** *Concept: Service types vs deployment models*  
IaaS leaves the OS, network configuration, and most of the stack to you; the provider handles only physical security, power, and connectivity.  
Why not the others: A — SaaS places the least responsibility on the customer. · C — Hybrid is a deployment model (where resources run), not a service type — a classic distractor. · D — PaaS sits in the middle and splits responsibility more evenly.

**A4 — A.** *Concept: Public vs private cloud*  
General public availability is the defining difference. A private cloud is dedicated to one organization.  
Why not the others: B — Backwards — private cloud requires buying hardware; 'no CapEx to scale' is a public-cloud trait. · C — That's a private-cloud trait; in public cloud you don't have complete control. · D — Wrong — a private cloud can be off-site, even run by a third party.

**A5 — B.** *Concept: Hybrid cloud*  
Hybrid combines public and private clouds in an interconnected environment and is described as the most flexible model — you choose where workloads run.  
Why not the others: A — You don't have complete control over resources and security in public cloud alone. · C — Multicloud means two or more PUBLIC providers; it doesn't imply a private component. · D — Gives control but doesn't by itself use public cloud resources.

**A6 — D.** *Concept: Multicloud*  
Multicloud = multiple public cloud providers, whether to use different features or mid-migration between providers.  
Why not the others: A — That's still a private cloud. · B — That's hybrid cloud. · C — Still one provider — not multicloud.

**A7 — C.** *Concept: Azure Arc*  
Azure Arc is a set of technologies for managing cloud environments across public, private, hybrid, and multicloud.  
Why not the others: A — Hosts DNS domains; unrelated to managing hybrid or multicloud resources. · B — Runs your VMware workloads in Azure; it isn't a cross-environment management layer. · D — A migration hub for moving on-premises workloads into Azure, not ongoing cross-cloud management.

**A8 — B.** *Concept: CapEx vs OpEx*  
Pay-as-you-consume spending over time is OpEx. CapEx is up-front spending on physical infrastructure.  
Why not the others: A — Renting/consuming services is OpEx, not CapEx. · C — Right category, wrong reason — buying hardware ahead of demand is CapEx thinking. · D — The provider's hardware purchase isn't your expense category.

**A9 — D.** *Concept: Consumption-based model*  
Consumption-based pricing means your bill tracks usage — it varies. That's the opposite of a fixed bill.  
Why not the others: A — This IS a listed benefit. · B — This IS a listed benefit. · C — This IS a listed benefit.

### Section B

**B1 — False.** *Concept: Shared responsibility: SQL on a VM*  
When you install the database yourself on IaaS, patches and updates are yours. With a managed cloud SQL database, the provider maintains the database itself.

**B2 — True.** *Concept: Private cloud costs*  
Listed in the comparison table — private cloud brings control but also hardware costs and maintenance.

**B3 — False.** *Concept: Capacity planning*  
Swapped on purpose: OVERestimating means overspending on idle infrastructure; UNDERestimating causes degraded performance.

**B4 — True.** *Concept: Public cloud control*  
This is one of the listed trade-offs of public cloud in the module's comparison table.

**B5 — True.** *Concept: Shared responsibility: identity in PaaS/SaaS*  
The module gives exactly this example — e.g., the provider runs Microsoft Entra ID while you manage your own users and policies.

**B6 — False.** *Concept: Private cloud hosting*  
A private cloud can be hosted on-site, in a dedicated off-site datacenter, or even by a third party. What makes it private is that it's used by a single entity.

### Section C

**C1 — D.** *Concept: Azure VMware Solution*  
Azure VMware Solution is built for exactly this: run VMware workloads in Azure with seamless integration and scalability.  
Why not the others: A — Doesn't move the VMware workloads into Azure at all. · B — Arc manages resources wherever they run; it doesn't host your VMware workloads in Azure. · C — Massive re-platforming — the opposite of the requirement.

**C2 — C.** *Concept: Choosing a cloud model*  
Hybrid lets a private cloud burst into public cloud for temporary demand while you choose which services stay private — meeting both requirements.  
Why not the others: A — Works, but leaves expensive capacity idle most of the year (classic overestimate problem). · B — Breaks the requirement that payment data stays on private infrastructure. · D — Multicloud is public-only; it doesn't keep payment data on private infrastructure.

---

## Score guide

| Score (out of 17) | What it means |
| --- | --- |
| 16–17 | Exam-ready on this module. Skim the misses and move on. |
| 13–15 | Solid. Re-read the units behind each miss before the domain review. |
| 11–12 | Shaky. Re-read the module, focusing on the comparisons and gotchas you missed. |
| 0–10 | Redo the module, then retake this quiz. |

The real exam needs 700 out of 1,000 (a scaled score, not a straight percentage), so aim for 80%+ on practice quizzes to leave a margin.
