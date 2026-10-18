# AZ-900 Module 12 Quiz: Describe monitoring tools in Azure

**Exam domain:** Domain 3: Describe Azure management and governance (30–35%)  
**Source module:** [Describe monitoring tools in Azure](https://learn.microsoft.com/en-us/training/modules/describe-monitoring-tools-azure/) (Microsoft Learn, course AZ-900T00)  
**Units covered:** Describe the purpose of Azure Advisor; Describe Azure Service Health; Describe Azure Monitor  
**Questions:** 15 — Section A: 7 multiple choice · Section B: 6 true/false · Section C: 2 scenarios

Answer key and score guide are at the bottom — cover them while you work.

---

## Section A — Multiple choice

**A1.** Which is NOT one of Azure Advisor's five recommendation categories?

- **A.** Compliance
- **B.** Operational Excellence
- **C.** Reliability
- **D.** Cost

**A2.** Which Service Health view gives a global picture of Azure health across ALL services and regions?

- **A.** Azure Status
- **B.** Resource Health
- **C.** Azure Advisor
- **D.** Service Health

**A3.** Which tool tells you whether a SPECIFIC virtual machine is healthy, and whether a problem is on Azure's side or yours?

- **A.** Azure Advisor
- **B.** Service Health
- **C.** Resource Health
- **D.** Azure Status

**A4.** What is Log Analytics used for?

- **A.** Writing and running queries against data that Azure Monitor collects
- **B.** Recommending reliability and cost improvements
- **C.** Sending synthetic requests to check that your app is still responding
- **D.** Notifying you about Azure outages in your regions

**A5.** What two components make up an Azure Monitor alert setup?

- **A.** A signal plus an enforcement action at sign-in time
- **B.** A budget and a spending threshold percentage
- **C.** An alert rule (condition) and an action group (response)
- **D.** A policy initiative and a policy definition

**A6.** Action groups can be reused across which services?

- **A.** Azure Monitor and Cost Management only
- **B.** Azure Monitor, Service Health, and Azure Advisor
- **C.** Azure Monitor only
- **D.** Defender for Cloud and Azure Policy only

**A7.** What does Application Insights monitor?

- **A.** Only web apps hosted in Azure App Service
- **B.** Opportunities to reduce Azure spending
- **C.** Azure platform outages and planned maintenance in your regions
- **D.** Performance and usage of web apps, wherever they run

## Section B — True or false

**B1.** Azure Advisor recommendations must be acted on immediately; they can't be postponed or dismissed.

**B2.** Service Health shows outages, planned maintenance, and health advisories for the services and regions you use.

**B3.** A metric alert can email you when a VM's CPU stays above 80%.

**B4.** Azure Monitor works only with Azure resources.

**B5.** Resource Health gives a global view of Azure health across all regions.

**B6.** Application Insights can be enabled without code changes by using an agent.

## Section C — Scenarios

**C1.** Scenario: A web app is intermittently slow. The team wants to (1) know when response times and failure rates spike, and (2) confirm the app is still responding overnight, when real traffic is near zero. What should they use?

- **A.** Resource Health for the app's VM
- **B.** The Azure Status page
- **C.** Azure Advisor performance recommendations
- **D.** Application Insights, including availability tests

**C2.** Scenario: You hear about a major cloud outage in the news. You want to (1) find out if it affects the services and regions you use, with alerts for future events, and (2) check whether your specific VM is affected. Which combination fits?

- **A.** Azure Advisor alerts, plus Service Health alerts
- **B.** Service Health with alerts, plus Resource Health for the VM
- **C.** Log Analytics queries, plus Application Insights
- **D.** The Azure Status page, plus Azure Advisor alerts

---

## Answer key

**Quick key:** A1 A, A2 A, A3 C, A4 A, A5 C, A6 B, A7 D, B1 F, B2 T, B3 T, B4 F, B5 F, B6 T, C1 D, C2 B

### Section A

**A1 — A.** *Concept: Advisor categories*  
The five categories are Reliability, Security, Performance, Operational Excellence, and Cost.  
Why not the others: B — An Advisor category. · C — An Advisor category. · D — An Advisor category.

**A2 — A.** *Concept: Azure Status*  
Azure Status = global. Service Health = the services and regions YOU use. Resource Health = an individual resource.  
Why not the others: B — Scoped to an individual resource. · C — Gives recommendations, not health status. · D — Scoped to the services and regions you use.

**A3 — C.** *Concept: Resource Health*  
Resource Health zooms in on individual resources.  
Why not the others: A — Recommendations, not health status. · B — Services and regions you use, not a single resource. · D — Global view only.

**A4 — A.** *Concept: Log Analytics*  
Log Analytics is where you query logs, from simple filters to advanced trend analysis.  
Why not the others: B — That's Azure Advisor. · C — That's Application Insights availability tests. · D — That's Service Health.

**A5 — C.** *Concept: Azure Monitor alerts*  
The rule defines the condition; the action group defines the response.  
Why not the others: A — That's Conditional Access language. · B — That's Cost Management. · D — That's Azure Policy.

**A6 — B.** *Concept: Action group reuse*  
The module states action groups are reusable across all three.  
Why not the others: A — Not what the module lists. · C — They're reusable beyond Monitor. · D — Not what the module lists.

**A7 — D.** *Concept: Application Insights*  
Request rates, response times, failures, dependencies, page loads, users/sessions, and server counters — wherever the app runs.  
Why not the others: A — It works for apps in Azure, on-premises, or another cloud. · B — That's Advisor's Cost category. · C — That's Service Health.

### Section B

**B1 — False.** *Concept: Advisor actions*  
Each recommendation can be acted on right away, postponed, or dismissed.

**B2 — True.** *Concept: Service Health content*  
Because you're signed in, it knows which services matter to you, and you can set alerts.

**B3 — True.** *Concept: Metric alerts*  
The module's own metric alert example.

**B4 — False.** *Concept: Monitor scope*  
Azure Monitor works with Azure, on-premises, and multicloud environments.

**B5 — False.** *Concept: Resource Health scope*  
That's Azure Status. Resource Health covers individual resources.

**B6 — True.** *Concept: App Insights without code*  
You can add the SDK OR enable the agent without code changes.

### Section C

**C1 — D.** *Concept: Application Insights scenario*  
Application Insights tracks response times and failure rates; availability tests send synthetic requests even during low traffic.  
Why not the others: A — Shows whether the VM is healthy, not app response times. · B — Shows global Azure health, not your app's behavior. · C — Suggestions, not real-time app telemetry or uptime checks.

**C2 — B.** *Concept: Service Health scenario*  
Service Health covers your services/regions (with alerts); Resource Health covers the individual VM.  
Why not the others: A — Advisor doesn't check the health of a specific VM. · C — Your own telemetry won't tell you about Azure platform incidents. · D — Azure Status isn't personalized and has no alerts; Advisor doesn't report outages.

---

## Score guide

| Score (out of 15) | What it means |
| --- | --- |
| 14–15 | Exam-ready on this module. Skim the misses and move on. |
| 12–13 | Solid. Re-read the units behind each miss before the domain review. |
| 9–11 | Shaky. Re-read the module, focusing on the comparisons and gotchas you missed. |
| 0–8 | Redo the module, then retake this quiz. |

The real exam needs 700 out of 1,000 (a scaled score, not a straight percentage), so aim for 80%+ on practice quizzes to leave a margin.
