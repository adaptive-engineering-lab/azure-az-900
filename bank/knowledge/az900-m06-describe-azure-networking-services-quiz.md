# AZ-900 Module 6 Quiz: Describe Azure networking services

**Exam domain:** Domain 2: Describe Azure architecture and services (35–40%)  
**Source module:** [Describe Azure networking services](https://learn.microsoft.com/en-us/training/modules/describe-azure-networking-services/) (Microsoft Learn, course AZ-900T00)  
**Units covered:** Describe Azure virtual networking; Describe Azure virtual private networks; Describe Azure ExpressRoute; Describe Azure DNS  
**Questions:** 19 — Section A: 10 multiple choice · Section B: 7 true/false · Section C: 2 scenarios

Answer key and score guide are at the bottom — cover them while you work.

---

## Section A — Multiple choice

**A1.** What is a private endpoint?

- **A.** A DNS alias record that points to an Azure resource
- **B.** An endpoint with a public IP address that can be reached from anywhere in the world
- **C.** An endpoint in a virtual network, using a private IP from its address space
- **D.** A VPN gateway deployed in a dedicated gateway subnet

**A2.** Which describes a point-to-site VPN connection?

- **A.** An on-premises VPN device links to the Azure VPN gateway
- **B.** A single client computer opens an encrypted VPN to the virtual network
- **C.** A dedicated private link to Azure that avoids the internet
- **D.** Two virtual networks connecting directly over the Microsoft backbone network

**A3.** How does traffic travel between two peered virtual networks?

- **A.** Privately over the Microsoft backbone, never touching the internet
- **B.** Only between VNets in the same region
- **C.** Only through an ExpressRoute circuit
- **D.** Encrypted over the public internet through VPN gateways

**A4.** Which resource lets you allow or block traffic using inbound and outbound rules based on source/destination IP, port, and protocol?

- **A.** Route table
- **B.** Azure DNS
- **C.** Virtual network peering
- **D.** Network security group (NSG)

**A5.** How many VPN gateways can you deploy in a single virtual network?

- **A.** One per virtual network
- **B.** One per subnet
- **C.** As many as you need
- **D.** Two — one active and one standby

**A6.** You need point-to-site connections and coexistence with an ExpressRoute gateway. Which VPN gateway type is required?

- **A.** Route-based
- **B.** Zone-redundant
- **C.** Policy-based
- **D.** Active/standby

**A7.** By default, how are VPN gateways deployed for high availability?

- **A.** As two instances in active/active mode
- **B.** As a single instance with no failover
- **C.** As two instances in an active/standby configuration
- **D.** As a zone-redundant gateway in every region

**A8.** What does ExpressRoute Global Reach let you do?

- **A.** Reach Microsoft 365 and Dynamics 365 over a private ExpressRoute connection
- **B.** Link your own on-premises sites to each other via their circuits
- **C.** Fail over to an encrypted tunnel over the internet
- **D.** Connect two virtual networks in different Azure regions

**A9.** Even when you use ExpressRoute, which type of traffic is still sent over the public internet?

- **A.** Traffic to Dynamics 365
- **B.** DNS queries
- **C.** Traffic to Azure Storage
- **D.** Traffic to Azure Virtual Machines

**A10.** Which of the following can Azure DNS NOT do?

- **A.** Host DNS records for your domains on Azure name servers
- **B.** Create alias records that point to Azure resources
- **C.** Provide private DNS domains inside virtual networks
- **D.** Buy or register a domain name

## Section B — True or false

**B1.** Peered virtual networks can be in separate Azure regions.

**B2.** Policy-based VPNs are preferred for on-premises devices because they handle topology changes better.

**B3.** ExpressRoute connections travel over the public internet but are encrypted end-to-end.

**B4.** Azure DNS alias record sets automatically update when the underlying resource's IP address changes.

**B5.** The IP range defined for a virtual network is routable on the internet.

**B6.** Azure VPN gateways authenticate with a preshared key, whether policy-based or route-based.

**B7.** Site-to-site VPN connections are encrypted and travel over the internet.

## Section C — Scenarios

**C1.** Scenario: A bank needs a private connection between its datacenter and Azure with predictable latency and high throughput, avoiding the public internet. It also wants a backup path in case the circuit itself has an outage. What should it deploy?

- **A.** ExpressRoute alone, since its built-in redundancy makes any backup unnecessary
- **B.** Virtual network peering from the datacenter to Azure
- **C.** A point-to-site VPN connection from every server
- **D.** ExpressRoute as the primary link, with a site-to-site VPN gateway as failover

**C2.** Scenario: A web tier and a database tier are in separate subnets. Only the web subnet may reach the database on port 1433, and all outbound internet traffic must pass through a firewall appliance. What should you configure?

- **A.** ExpressRoute with Global Reach enabled on the circuit
- **B.** Private DNS zones plus virtual network peering between the web and DB tiers
- **C.** NSG rules on the DB subnet plus user-defined routes to a firewall NVA
- **D.** Public endpoints on both tiers with an alias record

---

## Answer key

**Quick key:** A1 C, A2 B, A3 A, A4 D, A5 A, A6 A, A7 C, A8 B, A9 B, A10 D, B1 T, B2 F, B3 F, B4 T, B5 F, B6 T, B7 T, C1 D, C2 C

### Section A

**A1 — C.** *Concept: Public vs private endpoints*  
Private endpoints live inside a VNet with a private IP. Public endpoints have a public IP reachable from anywhere.  
Why not the others: A — That's an Azure DNS feature. · B — That's a public endpoint. · D — That's a VPN gateway, not an endpoint type.

**A2 — B.** *Concept: Point-to-site VPN*  
Point-to-site = one device. Site-to-site = your on-premises VPN device to the Azure VPN gateway.  
Why not the others: A — That's site-to-site. · C — That's ExpressRoute. · D — That's virtual network peering.

**A3 — A.** *Concept: VNet peering*  
Peering traffic is private and stays on Microsoft's backbone — even when the VNets are in different regions.  
Why not the others: B — Peered VNets can be in separate regions. · C — Peering doesn't need ExpressRoute. · D — That's a VPN connection, not peering.

**A4 — D.** *Concept: Network security groups*  
NSGs hold multiple inbound/outbound security rules on exactly those factors.  
Why not the others: A — Controls where traffic is routed, not whether it's allowed. · B — Name resolution, not traffic filtering. · C — Connects VNets; it doesn't filter traffic.

**A5 — A.** *Concept: VPN gateways per VNet*  
Only one VPN gateway per VNet, but that one gateway can connect to multiple on-premises sites or other VNets.  
Why not the others: B — The gateway lives in one dedicated subnet; it's one per VNet. · C — The limit is one per VNet. · D — Active/standby is two INSTANCES behind one gateway resource, not two gateways.

**A6 — A.** *Concept: Route-based vs policy-based VPN*  
Route-based is required for VNet-to-VNet, point-to-site, multisite, and ExpressRoute coexistence. It's also the preferred type for on-premises devices.  
Why not the others: B — That's a deployment option for resilience, not a VPN type. · C — Policy-based gateways use static IP lists and don't support these connection types. · D — That's a high-availability configuration, not a VPN type.

**A7 — C.** *Concept: VPN gateway default HA*  
Even though you see one gateway resource, two instances run active/standby, and failover is automatic.  
Why not the others: A — Active/active is optional and uses BGP with a public IP per instance. · B — There's always a standby instance by default. · D — Zone-redundant requires specific SKUs and AZ-enabled regions.

**A8 — B.** *Concept: ExpressRoute Global Reach*  
Example: an office in Asia and a datacenter in Europe exchange data over the Microsoft network instead of the internet.  
Why not the others: A — That's standard ExpressRoute connectivity to Microsoft cloud services. · C — That's using a VPN gateway as backup for ExpressRoute. · D — That's global VNet peering.

**A9 — B.** *Concept: ExpressRoute exceptions*  
DNS queries, certificate revocation list checks, and Azure CDN requests still go over the public internet.  
Why not the others: A — Reachable over ExpressRoute. · C — Reachable over ExpressRoute. · D — Reachable over ExpressRoute.

**A10 — D.** *Concept: Azure DNS limits*  
Azure DNS hosts and manages records. To buy a domain, use App Service domains or a third-party registrar.  
Why not the others: A — That's its core purpose. · B — Supported. · C — Supported.

### Section B

**B1 — True.** *Concept: Cross-region peering*  
Peering across regions lets you build a globally interconnected network.

**B2 — False.** *Concept: Preferred VPN type*  
Route-based VPNs are preferred and are more resilient to topology changes such as new subnets.

**B3 — False.** *Concept: ExpressRoute and the internet*  
ExpressRoute connections don't go over the public internet at all. That's the point of a private circuit.

**B4 — True.** *Concept: Alias records*  
Alias records point to the service instance, so they track IP changes.

**B5 — False.** *Concept: VNet address space*  
The range exists only within the virtual network and isn't internet routable.

**B6 — True.** *Concept: VPN authentication*  
The module states the preshared key is used regardless of VPN type.

**B7 — True.** *Concept: Site-to-site path*  
A VPN is an encrypted tunnel over an untrusted network — usually the internet.

### Section C

**C1 — D.** *Concept: ExpressRoute with VPN failover*  
ExpressRoute meets the private/predictable requirement; a VPN gateway over the internet is the documented failover path for circuit outages.  
Why not the others: A — Built-in redundancy doesn't protect against cable or location-wide outages. · B — Peering connects Azure VNets, not on-premises networks. · C — Internet-based and per-device — doesn't meet the private requirement.

**C2 — C.** *Concept: Filtering and routing*  
NSGs filter by IP/port/protocol; user-defined routes steer traffic; a network virtual appliance performs the firewall function.  
Why not the others: A — That's on-premises connectivity, not subnet filtering. · B — Name resolution and VNet connectivity don't filter or force-route traffic. · D — Exposes the database publicly — the opposite of the goal.

---

## Score guide

| Score (out of 19) | What it means |
| --- | --- |
| 18–19 | Exam-ready on this module. Skim the misses and move on. |
| 15–17 | Solid. Re-read the units behind each miss before the domain review. |
| 12–14 | Shaky. Re-read the module, focusing on the comparisons and gotchas you missed. |
| 0–11 | Redo the module, then retake this quiz. |

The real exam needs 700 out of 1,000 (a scaled score, not a straight percentage), so aim for 80%+ on practice quizzes to leave a margin.
