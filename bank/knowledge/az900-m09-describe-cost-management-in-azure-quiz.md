# AZ-900 Module 9 Quiz: Describe cost management in Azure

**Exam domain:** Domain 3: Describe Azure management and governance (30–35%)  
**Source module:** [Describe cost management in Azure](https://learn.microsoft.com/en-us/training/modules/describe-cost-management-azure/) (Microsoft Learn, course AZ-900T00)  
**Units covered:** Factors that can affect costs in Azure; Explore the pricing calculator; Describe the Microsoft Cost Management tool; Describe the purpose of tags; Describe cost optimization options  
**Questions:** 16 — Section A: 8 multiple choice · Section B: 6 true/false · Section C: 2 scenarios

Answer key and score guide are at the bottom — cover them while you work.

---

## Section A — Multiple choice

**A1.** Which of these is NOT one of the factors the module lists as affecting Azure costs?

- **A.** Resource type and the settings you choose
- **B.** The number of people who sign in to the Azure portal
- **C.** Third-party solutions bought in Azure Marketplace
- **D.** The geography (Azure region) where your resources are deployed

**A2.** How is data transfer (bandwidth) generally priced in Azure?

- **A.** Some inbound transfers are free; outbound transfers are priced by billing zone
- **B.** Outbound transfers are free; inbound transfers are charged
- **C.** All data transfer is free within the same geography
- **D.** Inbound and outbound data transfers are always charged at one identical flat rate

**A3.** What is the difference between a billing zone and an availability zone?

- **A.** A billing zone is an availability zone located inside a paid region
- **B.** They're two names for the same physical datacenter concept
- **C.** Billing zones group regions for pricing; AZs are datacenters
- **D.** A billing zone is another name for a pair of Azure regions

**A4.** Which statement about the Azure Pricing Calculator is TRUE?

- **A.** It produces your exact final invoice in advance
- **B.** It still includes the TCO calculator for comparing against on-premises costs
- **C.** It provisions a trial version of the resources you select
- **D.** It only estimates costs; nothing is provisioned and you aren't charged

**A5.** Which is NOT one of the three types of alerts shown in Cost Management's cost alerts?

- **A.** Resource health alerts
- **B.** Credit alerts
- **C.** Department spending quota alerts
- **D.** Budget alerts

**A6.** When are credit alerts generated?

- **A.** At any threshold you configure in the portal
- **B.** At 50% and 75% of the credit balance
- **C.** Only once the credit balance reaches 100%
- **D.** Automatically at 90% and 100% of the credit balance

**A7.** Which service can require new resources to have an Owner tag, and can reapply tags that were removed?

- **A.** Resource locks
- **B.** Azure Advisor
- **C.** Azure Policy
- **D.** Cost Management budgets

**A8.** Which option has you commit to an hourly SPEND amount on eligible compute for 1 or 3 years, with flexibility across compute types?

- **A.** Pay-as-you-go consumption pricing
- **B.** Azure savings plan for compute
- **C.** Reserved capacity (Azure Reservations)
- **D.** Azure Spot Virtual Machine pricing

## Section B — True or false

**B1.** Department spending quota alerts are specific to Enterprise Agreement customers.

**B2.** Deprovisioning a VM always automatically removes its associated storage and networking resources.

**B3.** The same VM configuration can cost different amounts in different regions.

**B4.** Reservations can apply to services such as VMs, databases, and storage, for one- or three-year terms.

**B5.** Microsoft sets the billing structure for third-party solutions bought through Azure Marketplace.

**B6.** Resources automatically inherit tags from their resource group.

## Section C — Scenarios

**C1.** Scenario: Match each workload to the best pricing option. (1) A production SQL workload running 24/7 with stable needs. (2) Batch rendering jobs that can restart if interrupted. (3) A web/API workload with steady total usage that shifts among compute services.

- **A.** (1) Azure savings plan for compute, (2) Spot pricing, (3) Reservations
- **B.** (1) Spot pricing, (2) Reservations, (3) Azure savings plan for compute
- **C.** (1) Reservations, (2) Azure savings plan for compute, (3) Spot pricing
- **D.** (1) Reservations, (2) Spot pricing, (3) Azure savings plan for compute

**C2.** Scenario: A dev/test subscription keeps overspending. The team wants a notification at 80% of a monthly budget, automatic shutdown of nonproduction resources when the threshold is hit, and a view of costs by resource group. What should they use?

- **A.** Credit alerts, which fire at 90% and 100% of the balance
- **B.** Azure Advisor cost recommendations reviewed every week
- **C.** A Cost Management budget with an 80% alert, automation, and cost analysis
- **D.** A Pricing Calculator estimate, plus resource locks on the whole subscription

---

## Answer key

**Quick key:** A1 B, A2 A, A3 C, A4 D, A5 A, A6 D, A7 C, A8 B, B1 T, B2 F, B3 T, B4 T, B5 F, B6 F, C1 D, C2 C

### Section A

**A1 — B.** *Concept: Cost factors*  
Listed factors: resource type, consumption, maintenance, geography, subscription type, and Azure Marketplace.  
Why not the others: A — A listed factor. · C — A listed factor — you may also pay the third-party vendor. · D — A listed factor — prices and data transfer vary by region.

**A2 — A.** *Concept: Bandwidth pricing*  
Data going INTO Azure is often free; data LEAVING Azure is priced based on zones.  
Why not the others: B — Reversed. · C — Not stated — outbound pricing depends on zones. · D — Inbound and outbound are treated differently.

**A3 — C.** *Concept: Billing zones vs availability zones*  
Same word, different concepts. Billing zones exist only for pricing; availability zones are physical isolation.  
Why not the others: A — Billing zones are groups of regions, not datacenters. · B — They're explicitly different. · D — Region pairs are for resiliency, not pricing.

**A4 — D.** *Concept: Pricing calculator*  
The calculator is for information only. Also note: the Total Cost of Ownership (TCO) calculator has been RETIRED.  
Why not the others: A — It's an estimate only. · B — The TCO calculator has been retired — an older-material trap. · C — Nothing is provisioned.

**A5 — A.** *Concept: Cost alert types*  
The three cost alert types are budget alerts, credit alerts, and department spending quota alerts. Resource Health belongs to Azure Service Health.  
Why not the others: B — A cost alert type (EA prepayment). · C — A cost alert type (EA customers). · D — A cost alert type.

**A6 — D.** *Concept: Credit alerts*  
Credit alerts track Azure Prepayment for Enterprise Agreements and fire automatically at 90% and 100%.  
Why not the others: A — Credit alert thresholds are fixed. · B — Those percentages are examples of department spending quota thresholds. · C — They also fire at 90%.

**A7 — C.** *Concept: Enforcing tags*  
Azure Policy enforces tagging rules and conventions, including requiring and reapplying tags.  
Why not the others: A — Prevent deletion or changes; they don't add tags. · B — Gives recommendations; it doesn't enforce rules. · D — Track spend; they don't enforce tags.

**A8 — B.** *Concept: Savings plan vs reservations*  
Savings plan = commit to spend, flexible across compute. Reservations = commit to specific resources. Spot = unused capacity that can be evicted.  
Why not the others: A — No commitment and no discount. · C — Commit to specific resource capacity, not a flexible spend amount. · D — No commitment; discounted capacity that Azure can reclaim.

### Section B

**B1 — True.** *Concept: EA quota alerts*  
They notify department owners when spending reaches a fixed threshold of the quota.

**B2 — False.** *Concept: Orphaned resources*  
Those resources may not be deprovisioned at the same time — that's why maintenance is a cost factor.

**B3 — True.** *Concept: Regional pricing*  
Power, labor, taxes, and fees vary by location.

**B4 — True.** *Concept: Reservation terms*  
Listed in the consumption factor and the cost optimization unit.

**B5 — False.** *Concept: Marketplace billing*  
Billing structures are set by the vendor.

**B6 — False.** *Concept: Tag inheritance*  
Resources don't inherit tags from subscriptions or resource groups. Use Azure Policy if you need tags applied consistently.

### Section C

**C1 — D.** *Concept: Matching pricing options*  
This matches the module's decision guide exactly: stable/predictable → Reservations; interruptible → Spot; steady but flexible → savings plan.  
Why not the others: A — Reservations lock you to specific resources — bad for a workload that shifts across services. · B — Spot for 24/7 production risks eviction; Reservations add no value for restartable batch jobs. · C — Spot for steady web/API traffic risks evictions, and batch is the ideal Spot candidate.

**C2 — C.** *Concept: Cost Management tooling*  
Budgets set limits and alerts and can trigger automation; cost analysis shows costs by subscription, resource group, or service.  
Why not the others: A — Credit alerts are for EA prepayment balances and use fixed thresholds. · B — Advisor suggests savings but doesn't alert at a budget threshold or automate shutdown. · D — Estimates don't monitor live spend, and locks don't shut anything down.

---

## Score guide

| Score (out of 16) | What it means |
| --- | --- |
| 15–16 | Exam-ready on this module. Skim the misses and move on. |
| 12–14 | Solid. Re-read the units behind each miss before the domain review. |
| 10–11 | Shaky. Re-read the module, focusing on the comparisons and gotchas you missed. |
| 0–9 | Redo the module, then retake this quiz. |

The real exam needs 700 out of 1,000 (a scaled score, not a straight percentage), so aim for 80%+ on practice quizzes to leave a margin.
