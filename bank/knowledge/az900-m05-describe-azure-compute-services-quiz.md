# AZ-900 Module 5 Quiz: Describe Azure compute services

**Exam domain:** Domain 2: Describe Azure architecture and services (35–40%)  
**Source module:** [Describe Azure compute services](https://learn.microsoft.com/en-us/training/modules/describe-azure-compute-networking-services/) (Microsoft Learn, course AZ-900T00)  
**Units covered:** Describe Azure virtual machines; Describe Azure Virtual Desktop; Describe Azure containers; Describe Azure Functions; Describe AI, machine learning, and IoT/Edge services; Describe application hosting options  
**Questions:** 20 — Section A: 10 multiple choice · Section B: 8 true/false · Section C: 2 scenarios

Answer key and score guide are at the bottom — cover them while you work.

---

## Section A — Multiple choice

**A1.** In the VM size name Standard_D2s_v5, what does the 's' indicate?

- **A.** It belongs to the storage-optimized family
- **B.** It's eligible for Spot pricing
- **C.** The size supports Premium SSD storage
- **D.** It's a small size within the D family

**A2.** Which VM family is designed for GPU workloads such as AI training and graphics?

- **A.** E-series
- **B.** N-series
- **C.** B-series
- **D.** F-series

**A3.** Which feature creates and manages a group of identical, load-balanced VMs that can automatically add or remove instances as demand changes?

- **A.** Azure Virtual Desktop
- **B.** Virtual Machine Scale Sets
- **C.** Availability sets
- **D.** Availability zones

**A4.** How do availability sets group VMs?

- **A.** By resource group and subscription
- **B.** By region and region pair
- **C.** By availability zone and datacenter
- **D.** By update domain and fault domain

**A5.** Which Azure container service is an ORCHESTRATION service that manages the lifecycle of a fleet of containers?

- **A.** Azure Container Instances
- **B.** Azure App Service
- **C.** Azure Kubernetes Service (AKS)
- **D.** Azure Container Apps

**A6.** Which container option is PaaS AND includes built-in load balancing and scaling?

- **A.** Azure Container Instances
- **B.** Azure Kubernetes Service
- **C.** Virtual Machine Scale Sets
- **D.** Azure Container Apps

**A7.** How are you typically charged for Azure Functions in the serverless model?

- **A.** A flat monthly fee per function app
- **B.** Only for the CPU time used while the function runs
- **C.** For the VM hours your app consumes, whether or not events occur
- **D.** Per container instance hour

**A8.** Which App Service feature runs a program or script in the same context as a web app, often for background tasks?

- **A.** WebJobs
- **B.** Azure Functions
- **C.** Mobile apps
- **D.** API apps

**A9.** A team needs to build, train, and manage its own CUSTOM machine learning model. Which service fits?

- **A.** Azure Machine Learning
- **B.** Azure IoT Central
- **C.** Azure IoT Hub
- **D.** Azure AI services

**A10.** Which service provides secure, bi-directional communication between cloud services and IoT devices?

- **A.** Azure AI services
- **B.** Azure IoT Central
- **C.** Azure IoT Edge
- **D.** Azure IoT Hub

## Section B — True or false

**B1.** Agentic AI is its own separate Azure compute service category.

**B2.** Azure Container Instances is a platform as a service (PaaS) offering.

**B3.** With containers, you manage the operating system of each container just as you would for a VM.

**B4.** Azure VMs are IaaS, so you still manage patching and configuration inside the VM.

**B5.** Azure Functions are stateless by default.

**B6.** Azure App Service supports only Windows as the host operating system.

**B7.** Availability sets add cost on top of the VMs you place in them.

**B8.** Azure Virtual Desktop supports both single-session and multi-session Windows experiences.

## Section C — Scenarios

**C1.** Scenario: A website is split into a front end, a back end, and a storage component. The back end regularly hits capacity while the others are idle. The team wants to scale and update each part independently, without managing operating systems, and will run a large fleet of containers that needs lifecycle management. What fits best?

- **A.** Deliver the app through an Azure Virtual Desktop host pool
- **B.** Host everything on one large VM and scale it up vertically when it's needed
- **C.** Containerize each component as a microservice and run the fleet on AKS
- **D.** Put identical VMs in an availability set

**C2.** Scenario: Whenever a user uploads an image to storage, a thumbnail must be generated, which takes under two seconds. Uploads are unpredictable and there are often none for hours. The goal is to pay as little as possible while idle. What should you use?

- **A.** Azure Functions triggered by the upload event
- **B.** An AKS cluster with a dedicated node pool
- **C.** An always-on App Service web app
- **D.** A Virtual Machine Scale Set with two instances minimum

---

## Answer key

**Quick key:** A1 C, A2 B, A3 B, A4 D, A5 C, A6 D, A7 B, A8 A, A9 A, A10 D, B1 F, B2 T, B3 F, B4 T, B5 T, B6 F, B7 F, B8 T, C1 C, C2 A

### Section A

**A1 — C.** *Concept: VM size naming*  
Decode: D = family (general purpose), 2 = vCPUs, s = Premium SSD support, v5 = hardware generation.  
Why not the others: A — Storage-optimized is the L-series. · B — Spot isn't encoded in the size name. · D — The number (2) indicates size via vCPU count.

**A2 — B.** *Concept: VM families*  
N-series = GPU enabled. Memorize the family letters: B burstable, D general purpose, E memory, F compute, M large memory, L storage, N GPU.  
Why not the others: A — Memory optimized. · C — Burstable, cost-efficient dev/test. · D — Compute optimized (CPU-intensive).

**A3 — B.** *Concept: Scale sets*  
Scale sets centralize configuration and autoscale based on demand or schedules, integrated with load balancing.  
Why not the others: A — Desktop and app virtualization for users. · C — These improve resiliency via update and fault domains; they don't autoscale. · D — Physical datacenter isolation within a region, not a VM scaling feature.

**A4 — D.** *Concept: Availability sets*  
Update domain = VMs that can reboot together during planned maintenance. Fault domain = VMs sharing a power/network failure point.  
Why not the others: A — Those are management/organization concepts. · B — Those are geography concepts. · C — That's zone-based design, which availability sets aren't.

**A5 — C.** *Concept: Container orchestration*  
AKS is the orchestration option. ACI is the fastest/simplest way to run a container; Container Apps add built-in scaling without you managing orchestration.  
Why not the others: A — Simplest way to run a single container; no orchestration. · B — Web/API hosting platform, not container orchestration. · D — PaaS with built-in load balancing and scaling, but not the orchestration answer.

**A6 — D.** *Concept: Container Apps vs ACI*  
Container Apps are similar to Container Instances but add built-in load balancing and scaling.  
Why not the others: A — PaaS and simple, but the module doesn't credit it with built-in scaling and load balancing. · B — An orchestration service; you take on more management. · C — Scale VMs, not containers as a PaaS service.

**A7 — B.** *Concept: Functions billing*  
Functions are woken by events and automatically deallocated when finished — you pay only while code executes.  
Why not the others: A — Not the serverless model. · C — That's VM billing — Functions don't need running VMs. · D — Functions don't require you to maintain containers.

**A8 — A.** *Concept: App Service WebJobs*  
WebJobs run programs (.exe, Java, PHP, Python, Node.js) or scripts (.cmd, .bat, PowerShell, Bash), scheduled or triggered.  
Why not the others: B — A separate serverless service, not an App Service app type. · C — A back end for iOS/Android apps. · D — Host REST APIs with Swagger support.

**A9 — A.** *Concept: AI services vs Azure Machine Learning*  
Azure Machine Learning = custom model development and lifecycle. Azure AI services = prebuilt AI through APIs.  
Why not the others: B — A SaaS IoT platform. · C — Device-to-cloud messaging. · D — Prebuilt capabilities (language, speech, vision) — no custom training required.

**A10 — D.** *Concept: IoT services*  
IoT Hub is the messaging backbone. IoT Central is a SaaS IoT platform; IoT Edge runs workloads near the devices.  
Why not the others: A — Prebuilt AI APIs, not device communication. · B — Simplified SaaS IoT platform for solution builders. · C — Extends cloud workloads to edge devices.

### Section B

**B1 — False.** *Concept: Agentic AI*  
The module says to treat agentic AI as an application pattern built from Azure AI capabilities, not a separate compute category.

**B2 — True.** *Concept: ACI service type*  
You upload containers and the service runs them for you.

**B3 — False.** *Concept: Container OS management*  
Unlike VMs, you don't manage the OS for a container — that's part of why they're lightweight.

**B4 — True.** *Concept: VM patching*  
VMs remove hardware maintenance, not OS maintenance.

**B5 — True.** *Concept: Functions statelessness*  
Stateless is the default; stateful functions are Durable Functions, where the runtime passes context to track prior activity.

**B6 — False.** *Concept: App Service OS*  
App Service supports both Windows and Linux.

**B7 — False.** *Concept: Availability set cost*  
Availability sets themselves don't add cost; you pay for the VM instances.

**B8 — True.** *Concept: AVD sessions*  
Listed as a key point of Azure Virtual Desktop.

### Section C

**C1 — C.** *Concept: Microservices and AKS*  
Containers suit microservice architectures (scale the back end alone), and AKS manages the lifecycle of a container fleet.  
Why not the others: A — AVD delivers desktops to users, not web app components. · B — Scales everything together, and you manage the OS. · D — Adds resiliency, but doesn't let each component scale independently.

**C2 — A.** *Concept: Choosing serverless*  
Event-driven, short-running, variable-demand work is the textbook Functions case, and you pay only while the code runs.  
Why not the others: B — Overkill, and nodes cost money while idle. · C — Pays for a running plan around the clock. · D — Those instances bill even when no uploads occur.

---

## Score guide

| Score (out of 20) | What it means |
| --- | --- |
| 18–20 | Exam-ready on this module. Skim the misses and move on. |
| 15–17 | Solid. Re-read the units behind each miss before the domain review. |
| 12–14 | Shaky. Re-read the module, focusing on the comparisons and gotchas you missed. |
| 0–11 | Redo the module, then retake this quiz. |

The real exam needs 700 out of 1,000 (a scaled score, not a straight percentage), so aim for 80%+ on practice quizzes to leave a margin.
