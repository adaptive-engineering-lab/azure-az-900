# AZ-900 Module 2 Quiz: Describe the benefits of using cloud services

**Exam domain:** Domain 1: Describe cloud concepts (25–30%)  
**Source module:** [Describe the benefits of using cloud services](https://learn.microsoft.com/en-us/training/modules/describe-benefits-use-cloud-services/) (Microsoft Learn, course AZ-900T00)  
**Units covered:** High availability and scalability; Reliability and predictability; Security and governance; Manageability; Sustainability considerations  
**Questions:** 16 — Section A: 8 multiple choice · Section B: 6 true/false · Section C: 2 scenarios

Answer key and score guide are at the bottom — cover them while you work.

---

## Section A — Multiple choice

**A1.** Which action is an example of vertical scaling?

- **A.** Using a load balancer to spread traffic across servers
- **B.** Adding more virtual machines when demand spikes
- **C.** Deploying a copy of the app in another region for failover
- **D.** Adding more CPUs or RAM to an existing virtual machine

**A2.** What does it mean to 'scale in'?

- **A.** Choosing a service with a lower SLA tier
- **B.** Reducing the number of instances, such as removing VMs
- **C.** Reducing the CPU or RAM of an existing VM
- **D.** Consolidating all resources into a single region

**A3.** Where are Azure's uptime guarantees for each service defined?

- **A.** In the Azure Pricing Calculator
- **B.** In service-level agreements (SLAs)
- **C.** In the Azure Well-Architected Framework
- **D.** In resource tags

**A4.** Which definition describes RELIABILITY in the cloud?

- **A.** Recovering from failures and continuing to function
- **B.** Forecasting future cloud spend accurately
- **C.** Adjusting resources to meet changing demand
- **D.** Maximizing uptime regardless of disruptions, backed by SLAs

**A5.** Which of these supports PERFORMANCE predictability (rather than cost predictability)?

- **A.** Analyzing spending trends to plan future deployments
- **B.** Tracking resource use and spend in real time
- **C.** Autoscaling and load balancing
- **D.** Estimating spend with the Azure Pricing Calculator

**A6.** Which is an example of management IN the cloud (how you manage), rather than management OF the cloud?

- **A.** Deploying resources from a preconfigured template
- **B.** Receiving automatic alerts based on configured metrics
- **C.** Automatically scaling resources based on need
- **D.** Managing resources through PowerShell

**A7.** Which type of attack are cloud providers described as typically well suited to handle, making your network more robust?

- **A.** Misuse of admin accounts by your own staff
- **B.** SQL injection flaws in your custom application code
- **C.** Distributed denial of service (DDoS) attacks
- **D.** Phishing attacks against your users' passwords

**A8.** Which practice supports BOTH sustainability and cost efficiency?

- **A.** Overprovisioning VMs so you never have to scale
- **B.** Automatically shutting down a dev environment outside business hours
- **C.** Keeping unused resources allocated in case they're needed later
- **D.** Always choosing the largest VM size for extra headroom

## Section B — True or false

**B1.** Cloud-based auditing can flag resources that are out of compliance with your baseline and suggest mitigations.

**B2.** After a regional disaster in Azure, you always have to move workloads to another region manually.

**B3.** Vertical scaling means adding or removing resources, such as VMs or containers.

**B4.** Because the cloud is consumption-based, reducing resources when demand drops also reduces your costs.

**B5.** The Azure Pricing Calculator is a tool for performance predictability.

**B6.** Horizontal scaling can be done automatically or manually.

## Section C — Scenarios

**C1.** Scenario: An online store sees 5x traffic for a few hours on flash-sale days and normal traffic otherwise. Leadership wants to handle the spikes without paying for idle capacity the rest of the time. What should the team do?

- **A.** Autoscale out during spikes, then scale back in
- **B.** Use the Pricing Calculator to forecast the spike
- **C.** Deploy a second copy in another region for reliability
- **D.** Permanently scale every VM up to the largest available size

**C2.** Scenario: An operations team wants to (1) deploy consistent resources without manual configuration, (2) get notified automatically when performance metrics cross thresholds, and (3) automate recurring tasks with scripts. Which combination fits?

- **A.** Templates for deployment, metric-based alerts, and CLI or PowerShell scripts
- **B.** The Pricing Calculator, tags, and budgets
- **C.** Manual portal configuration for every resource, plus daily dashboard checks
- **D.** Region pairs, SLAs, and DDoS protection

---

## Answer key

**Quick key:** A1 D, A2 B, A3 B, A4 A, A5 C, A6 D, A7 C, A8 B, B1 T, B2 F, B3 F, B4 T, B5 F, B6 T, C1 A, C2 A

### Section A

**A1 — D.** *Concept: Vertical vs horizontal scaling*  
Vertical scaling changes the capability of a resource (scale up/down). Horizontal scaling changes the number of resources (scale out/in).  
Why not the others: A — Load balancing supports performance predictability; it isn't vertical scaling. · B — That's horizontal scaling (scaling out). · C — That's a reliability design choice, not scaling.

**A2 — B.** *Concept: Scale in vs scale down*  
Scale in is the horizontal direction (fewer instances). Scale down is vertical (smaller CPU/RAM).  
Why not the others: A — Not scaling; SLAs are availability guarantees. · C — That's scaling down (vertical). · D — Not a scaling operation.

**A3 — B.** *Concept: SLAs*  
Azure uptime guarantees vary by service and are part of the SLAs — key to high availability planning.  
Why not the others: A — That estimates cost, not uptime. · C — That's design guidance, not a contractual uptime guarantee. · D — Tags are metadata you add; they don't define Azure's guarantees.

**A4 — A.** *Concept: Reliability vs high availability*  
Reliability = recover and keep functioning (a pillar of the Well-Architected Framework). High availability = maximize uptime regardless of disruptions. Close, but tested separately.  
Why not the others: B — That's cost predictability. · C — That's scalability. · D — That's high availability — the near-miss distractor.

**A5 — C.** *Concept: Performance vs cost predictability*  
Autoscaling, load balancing, and high availability are the module's examples of performance predictability.  
Why not the others: A — Cost predictability. · B — Cost predictability. · D — Cost predictability.

**A6 — D.** *Concept: Management OF vs IN the cloud*  
Management IN the cloud = the tools you use: web portal, CLI, APIs, PowerShell. Management OF the cloud = what the cloud does for your resources: autoscale, templates, health monitoring, alerts.  
Why not the others: A — Management OF the cloud. · B — Management OF the cloud. · C — Management OF the cloud.

**A7 — C.** *Concept: Security benefits*  
The module calls out DDoS specifically — provider scale lets them absorb and filter large attacks.  
Why not the others: A — Managing your accounts and access is always your responsibility. · B — Your own app code is your responsibility. · D — Protecting your users' credentials is your identity responsibility.

**A8 — B.** *Concept: Sustainability*  
Turning off or deallocating unused resources reduces unnecessary consumption — the module's own example.  
Why not the others: A — Overprovisioning is waste — the opposite of right-sizing. · C — Idle resources waste energy and money. · D — Same problem — avoid overprovisioning.

### Section B

**B1 — True.** *Concept: Governance auditing*  
Called out directly in the security and governance unit.

**B2 — False.** *Concept: Regional failover*  
You can design apps to fail over automatically, and in some cases Azure shifts to another region for you with no action needed.

**B3 — False.** *Concept: Vertical scaling definition*  
That's horizontal scaling. Vertical scaling changes a resource's capabilities (CPU/RAM).

**B4 — True.** *Concept: Scaling and cost*  
Scalability means you aren't overpaying — scale down/in and you pay less.

**B5 — False.** *Concept: Pricing Calculator purpose*  
The Pricing Calculator supports COST predictability by estimating spend.

**B6 — True.** *Concept: Horizontal scaling automation*  
Resources can be scaled out or in either automatically or manually.

### Section C

**C1 — A.** *Concept: Choosing a scaling approach*  
Horizontal autoscaling matches capacity to demand, and the consumption model means you stop paying when you scale in.  
Why not the others: B — Forecasting cost doesn't add capacity during the spike. · C — Improves reliability, but doesn't address demand or cost. · D — Pays for peak capacity 24/7 — exactly what they want to avoid.

**C2 — A.** *Concept: Manageability*  
This combines management OF the cloud (templates, alerts) with management IN the cloud (CLI/PowerShell), matching the module's ops example.  
Why not the others: B — These are cost-management tools. · C — Manual and reactive — fails requirements 1 and 2. · D — These address reliability and security, not deployment or automation.

---

## Score guide

| Score (out of 16) | What it means |
| --- | --- |
| 15–16 | Exam-ready on this module. Skim the misses and move on. |
| 12–14 | Solid. Re-read the units behind each miss before the domain review. |
| 10–11 | Shaky. Re-read the module, focusing on the comparisons and gotchas you missed. |
| 0–9 | Redo the module, then retake this quiz. |

The real exam needs 700 out of 1,000 (a scaled score, not a straight percentage), so aim for 80%+ on practice quizzes to leave a margin.
