# AZ-900 Module 3 Quiz: Describe cloud service types

**Exam domain:** Domain 1: Describe cloud concepts (25–30%)  
**Source module:** [Describe cloud service types](https://learn.microsoft.com/en-us/training/modules/describe-cloud-service-types/) (Microsoft Learn, course AZ-900T00)  
**Units covered:** Describe Infrastructure as a Service; Describe Platform as a Service; Describe Software as a Service  
**Questions:** 15 — Section A: 7 multiple choice · Section B: 6 true/false · Section C: 2 scenarios

Answer key and score guide are at the bottom — cover them while you work.

---

## Section A — Multiple choice

**A1.** In an IaaS model, what is the cloud provider responsible for?

- **A.** Database and storage configuration and tuning
- **B.** Hardware, physical security, and internet connectivity
- **C.** Operating system installation, configuration, and maintenance
- **D.** Network configuration within your environment

**A2.** In which model do you NOT have to worry about OS or database licensing and patching, but you still manage your own application code and data?

- **A.** On-premises datacenter
- **B.** Software as a service (SaaS)
- **C.** Platform as a service (PaaS)
- **D.** Infrastructure as a service (IaaS)

**A3.** Which statement correctly compares the service types?

- **A.** IaaS is the most flexible; SaaS is the easiest to get up and running
- **B.** IaaS is the least flexible but needs the least expertise
- **C.** SaaS is the most flexible; IaaS is the easiest to get running
- **D.** PaaS is both the most flexible and the easiest model to get up and running

**A4.** A team wants to move existing on-premises workloads to the cloud by recreating a similar environment, with minimal changes. Which service type fits?

- **A.** SaaS
- **B.** None — lift-and-shift requires redesigning the app first
- **C.** IaaS
- **D.** PaaS

**A5.** Which is a typical SaaS example?

- **A.** Renting virtual machines to host a custom app
- **B.** Provider-supplied tools to analyze and mine your own data
- **C.** A hosted email and messaging application
- **D.** A managed framework developers build custom cloud apps on

**A6.** In SaaS, what does the customer still primarily manage?

- **A.** Operating system updates and security fixes
- **B.** The runtime, middleware, and app servers
- **C.** Application patches and feature updates
- **D.** Their data, identities and access, and devices

**A7.** Which of these is NOT one of the common PaaS scenarios described in the module?

- **A.** Analytics or business intelligence tools
- **B.** A development framework to build or customize cloud apps
- **C.** Building apps with built-in scalability and high availability
- **D.** Lift-and-shift migration of existing servers

## Section B — True or false

**B1.** In PaaS, the customer is responsible for patching the operating system.

**B2.** Moving from IaaS to SaaS increases the operational responsibility on the customer.

**B3.** SaaS requires the least technical knowledge to fully use.

**B4.** With IaaS, you're essentially renting hardware in a cloud datacenter, and what you do with it is up to you.

**B5.** In SaaS, the customer is no longer responsible for their data because the provider manages the application.

**B6.** PaaS includes cloud features like scalability and high availability, reducing how much code developers must write.

## Section C — Scenarios

**C1.** Scenario: A startup's developers want to build a custom web API. They don't want to manage OS patches or middleware, and they want scaling and high availability built in. Which model fits best?

- **A.** PaaS
- **B.** IaaS
- **C.** An on-premises private cloud
- **D.** SaaS

**C2.** Scenario: A company wants to (1) replace its on-premises email server with a hosted email service, and (2) move a legacy app that needs a custom OS configuration to the cloud as-is. Which pairing fits best?

- **A.** SaaS for email; PaaS for the legacy app
- **B.** SaaS for email; IaaS for the legacy app
- **C.** IaaS for both
- **D.** PaaS for email; SaaS for the legacy app

---

## Answer key

**Quick key:** A1 B, A2 C, A3 A, A4 C, A5 C, A6 D, A7 D, B1 F, B2 F, B3 T, B4 T, B5 F, B6 T, C1 A, C2 B

### Section A

**A1 — B.** *Concept: IaaS responsibilities*  
In IaaS the provider keeps the hardware, internet connectivity, and physical security; you handle everything else.  
Why not the others: A — Yours in IaaS. · C — Yours in IaaS. · D — Yours in IaaS.

**A2 — C.** *Concept: PaaS identification*  
PaaS providers maintain the OS, middleware, development tools, and runtimes; you focus on your code, data, and access controls.  
Why not the others: A — On-premises, you're responsible for everything. · B — In SaaS you don't write or manage the application code. · D — In IaaS you patch and license the OS yourself.

**A3 — A.** *Concept: Flexibility vs ease of use*  
IaaS gives maximum control and flexibility. SaaS is the least flexible but needs the least technical expertise.  
Why not the others: B — IaaS is the most flexible and needs the most expertise. · C — Reversed. · D — PaaS is the middle ground on both.

**A4 — C.** *Concept: Lift-and-shift*  
Lift-and-shift migration is a named IaaS scenario: set up cloud resources similar to your datacenter and move workloads over.  
Why not the others: A — SaaS replaces the app with a finished product; it doesn't host your existing workloads. · B — The point of lift-and-shift is minimal redesign. · D — PaaS usually requires adapting the app to the managed platform.

**A5 — C.** *Concept: SaaS examples*  
Email, messaging, productivity, and finance/expense apps are the module's SaaS examples.  
Why not the others: A — IaaS. · B — Analytics/BI is listed as a PaaS scenario — a common trap. · D — PaaS (development framework scenario).

**A6 — D.** *Concept: SaaS customer responsibilities*  
The SaaS provider runs almost the whole stack, but your data, identities, and devices stay with you.  
Why not the others: A — Provider-managed in SaaS. · B — Provider-managed in SaaS (and PaaS). · C — The SaaS provider handles application maintenance.

**A7 — D.** *Concept: PaaS scenarios*  
Lift-and-shift is an IaaS scenario. PaaS scenarios are development frameworks and analytics/business intelligence.  
Why not the others: A — This IS a PaaS scenario. · B — This IS a PaaS scenario. · C — This is part of the PaaS development framework scenario.

### Section B

**B1 — False.** *Concept: PaaS OS patching*  
The PaaS provider maintains operating systems, middleware, and runtimes.

**B2 — False.** *Concept: Responsibility direction*  
The opposite — responsibility shifts toward the provider as you move IaaS → PaaS → SaaS.

**B3 — True.** *Concept: SaaS expertise*  
SaaS is the easiest model to get running and needs the least expertise.

**B4 — True.** *Concept: IaaS as renting hardware*  
Nearly word-for-word the module's description of IaaS.

**B5 — False.** *Concept: SaaS data responsibility*  
Data is ALWAYS the customer's responsibility, in every service type.

**B6 — True.** *Concept: PaaS built-in features*  
Part of the development framework scenario for PaaS.

### Section C

**C1 — A.** *Concept: Choosing PaaS*  
PaaS gives a managed platform for custom code, with scalability and HA included and no OS/middleware maintenance.  
Why not the others: B — They'd have to manage the OS and patching themselves. · C — Maximum management overhead — the opposite of the goal. · D — SaaS is a finished application; you can't build your own API on it.

**C2 — B.** *Concept: Mixing service types*  
Email is a textbook SaaS case. A legacy app needing custom OS settings needs IaaS control (lift-and-shift).  
Why not the others: A — PaaS doesn't give you control over the OS configuration. · C — Running your own email servers on VMs keeps all the maintenance — SaaS is the better fit. · D — SaaS can't host your custom legacy app.

---

## Score guide

| Score (out of 15) | What it means |
| --- | --- |
| 14–15 | Exam-ready on this module. Skim the misses and move on. |
| 12–13 | Solid. Re-read the units behind each miss before the domain review. |
| 9–11 | Shaky. Re-read the module, focusing on the comparisons and gotchas you missed. |
| 0–8 | Redo the module, then retake this quiz. |

The real exam needs 700 out of 1,000 (a scaled score, not a straight percentage), so aim for 80%+ on practice quizzes to leave a margin.
