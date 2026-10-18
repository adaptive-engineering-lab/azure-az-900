# AZ-900 Module 8 Quiz: Describe Azure identity, access, and security

**Exam domain:** Domain 2: Describe Azure architecture and services (35–40%)  
**Source module:** [Describe Azure identity, access, and security](https://learn.microsoft.com/en-us/training/modules/describe-azure-identity-access-security/) (Microsoft Learn, course AZ-900T00)  
**Units covered:** Directory services; Authentication methods; External identities; Conditional Access; Role-based access control; Zero Trust; Defense-in-depth; Encryption and key management; Microsoft Defender for Cloud  
**Questions:** 24 — Section A: 13 multiple choice · Section B: 9 true/false · Section C: 2 scenarios

Answer key and score guide are at the bottom — cover them while you work.

---

## Section A — Multiple choice

**A1.** Which service synchronizes user identities between on-premises Active Directory and Microsoft Entra ID?

- **A.** Microsoft Entra Domain Services
- **B.** Microsoft Entra External ID
- **C.** Microsoft Entra Connect
- **D.** Microsoft Entra Conditional Access

**A2.** A legacy app can't use modern authentication and needs LDAP, group policy, and Kerberos/NTLM in Azure, without you deploying or managing domain controllers. Which service fits?

- **A.** Microsoft Entra Domain Services
- **B.** Microsoft Entra multifactor authentication
- **C.** Azure Key Vault
- **D.** Microsoft Entra Connect

**A3.** In multifactor authentication, a fingerprint scan belongs to which category?

- **A.** Something the user does
- **B.** Something the user is
- **C.** Something the user has
- **D.** Something the user knows

**A4.** Which is NOT one of the three passwordless options supported by Microsoft Entra ID?

- **A.** The Microsoft Authenticator app
- **B.** FIDO2 security keys
- **C.** One-time passcodes sent by SMS
- **D.** Windows Hello for Business

**A5.** Which passwordless option is an unphishable hardware device (USB, Bluetooth, or NFC) built on the WebAuthn standard?

- **A.** A phone call from Microsoft Entra MFA
- **B.** Windows Hello for Business
- **C.** Microsoft Authenticator app
- **D.** FIDO2 security keys

**A6.** Which External ID capability gives external users access to Teams shared channels through a mutual trust, WITHOUT representing them in your directory?

- **A.** B2B collaboration
- **B.** B2B direct connect
- **C.** Microsoft Entra Connect
- **D.** External ID for customers

**A7.** Which sequence describes how Conditional Access works?

- **A.** Assess → secure → defend
- **B.** Signals → decision → enforcement
- **C.** Physical → perimeter → data
- **D.** Verify explicitly → least privilege → assume breach

**A8.** Azure RBAC is enforced on which actions?

- **A.** Actions on Azure resources that go through Azure Resource Manager
- **B.** Data-level access inside your own custom application's code and database
- **C.** Only actions taken through the Azure portal interface
- **D.** Only network traffic flowing to virtual machines

**A9.** One role assignment grants you read access to a resource group and another grants write access to the same group. What's the result?

- **A.** Write only, because the newest assignment wins
- **B.** You have both read and write access
- **C.** No access until the conflict is resolved
- **D.** Read only, because the most restrictive assignment wins

**A10.** Which is NOT a guiding principle of Zero Trust?

- **A.** Assume breach and segment access to limit impact
- **B.** Verify explicitly using all available data points
- **C.** Trust devices that are on the internal corporate network
- **D.** Use least privilege access with just-in-time and just-enough access

**A11.** Which defense-in-depth layer uses DDoS protection to filter large-scale attacks before they cause a denial of service?

- **A.** Network
- **B.** Physical security
- **C.** Perimeter
- **D.** Application

**A12.** Microsoft Defender for Cloud fills which three needs?

- **A.** Verify explicitly, least privilege, and assume breach
- **B.** Signals, decision, and enforcement
- **C.** Identity, perimeter, and data
- **D.** Continuously assess, secure, and defend

**A13.** To extend Defender for Cloud protection to on-premises machines, what do you deploy?

- **A.** Azure Arc
- **B.** Azure ExpressRoute
- **C.** Microsoft Entra Connect
- **D.** Azure Migrate

## Section B — True or false

**B1.** Permissions granted at a parent scope in Azure RBAC are inherited by child scopes.

**B2.** In defense-in-depth, physical security is the outermost layer and data is at the center.

**B3.** Microsoft Defender for Cloud can only protect resources that run in Azure.

**B4.** Zero Trust grants access based on network location rather than authentication.

**B5.** Conditional Access can skip MFA at a known location but require it when sign-in signals are unusual.

**B6.** Resources created directly in a Microsoft Entra Domain Services managed domain sync back to Microsoft Entra ID.

**B7.** Azure RBAC enforces access at the application and data level inside your app.

**B8.** Single sign-on is only as secure as the initial authenticator.

**B9.** Azure Key Vault is the primary Azure service for securely storing secrets, encryption keys, and certificates.

## Section C — Scenarios

**C1.** Scenario: Security wants to (1) require MFA for administrators, (2) block sign-ins from unexpected countries, and (3) allow access to the HR app only from compliant, managed devices. Which tool fits?

- **A.** Azure RBAC role assignments
- **B.** Azure Policy definitions
- **C.** Defender for Cloud's secure score recommendations
- **D.** Microsoft Entra Conditional Access policies

**C2.** Scenario: (1) A supplier's staff need to collaborate on internal apps using their own work accounts, with access reviewed periodically. (2) A public customer app must let people sign up with Google or Facebook accounts. Which combination fits?

- **A.** B2B collaboration with access reviews; External ID for customers
- **B.** Local accounts for each supplier; Entra Connect for the customer app
- **C.** Entra Domain Services for suppliers; SSO for customers
- **D.** B2B direct connect for both groups

---

## Answer key

**Quick key:** A1 C, A2 A, A3 B, A4 C, A5 D, A6 B, A7 B, A8 A, A9 B, A10 C, A11 C, A12 D, A13 A, B1 T, B2 T, B3 F, B4 F, B5 T, B6 F, B7 F, B8 T, B9 T, C1 D, C2 A

### Section A

**A1 — C.** *Concept: Microsoft Entra Connect*  
Entra Connect bridges on-premises AD and Entra ID so users get one consistent identity (SSO, MFA, SSPR).  
Why not the others: A — Provides managed domain services (domain join, LDAP, Kerberos) — it isn't the AD-to-Entra sync tool. · B — Handles identities from outside your tenant. · D — Evaluates sign-in signals to allow/block/require MFA.

**A2 — A.** *Concept: Microsoft Entra Domain Services*  
Domain Services provides a managed domain (Azure deploys and manages two DCs as a replica set) for apps that can't use modern auth.  
Why not the others: B — Adds a sign-in factor; doesn't provide domain services. · C — Stores secrets, keys, and certificates. · D — Syncs identities; it doesn't provide Kerberos/LDAP domain services.

**A3 — B.** *Concept: MFA factor categories*  
Know = password or question. Have = phone or code. Are = biometric.  
Why not the others: A — Not one of the three categories. · C — A phone receiving a code. · D — Passwords and challenge questions.

**A4 — C.** *Concept: Passwordless options*  
The three passwordless options are Windows Hello for Business, the Microsoft Authenticator app, and FIDO2 security keys.  
Why not the others: A — This IS a passwordless option. · B — This IS a passwordless option. · D — This IS a passwordless option.

**A5 — D.** *Concept: FIDO2*  
FIDO2 is an open standard; the hardware key handles authentication with no password to expose.  
Why not the others: A — An MFA method, not a passwordless hardware key. · B — Biometric/PIN tied to the user's own Windows PC. · C — Turns an iOS/Android phone into the sign-in factor.

**A6 — B.** *Concept: B2B direct connect*  
B2B direct connect = mutual two-way trust between Entra tenants, currently for Teams shared channels; users aren't in your directory.  
Why not the others: A — B2B collaboration users ARE represented in your directory, typically as guests. · C — Syncs on-premises AD with Entra ID. · D — For publishing apps to consumers, not partner Teams channels.

**A7 — B.** *Concept: Conditional Access flow*  
It collects signals (user, location, device, app), decides, then enforces (allow, block, or require MFA).  
Why not the others: A — That's Microsoft Defender for Cloud's three needs. · C — Those are defense-in-depth layers. · D — Those are the Zero Trust principles.

**A8 — A.** *Concept: RBAC enforcement scope*  
RBAC applies to anything through Resource Manager (portal, Cloud Shell, PowerShell, CLI). It does NOT enforce app- or data-level access.  
Why not the others: B — Application security must be handled by your app. · C — Also CLI, PowerShell, Cloud Shell — anything via Resource Manager. · D — Network filtering is NSGs, not RBAC.

**A9 — B.** *Concept: RBAC allow model*  
Azure RBAC uses an allow model: permissions from multiple assignments add up.  
Why not the others: A — Assignment order doesn't matter. · C — Assignments don't conflict in an allow model. · D — RBAC is additive, not most-restrictive.

**A10 — C.** *Concept: Zero Trust principles*  
Zero Trust grants access based on authentication, not network location. The principles are verify explicitly, use least privilege, and assume breach.  
Why not the others: A — A Zero Trust principle. · B — A Zero Trust principle. · D — A Zero Trust principle.

**A11 — C.** *Concept: Defense-in-depth layers*  
Perimeter = DDoS protection and perimeter firewalls. Network = segmentation and deny-by-default between resources.  
Why not the others: A — Limits communication between resources (segmentation, deny by default). · B — Protects buildings and hardware in the datacenter. · D — Keeps apps secure and free of vulnerabilities.

**A12 — D.** *Concept: Defender for Cloud pillars*  
Assess = know your posture/vulnerabilities; Secure = harden with the Microsoft cloud security benchmark; Defend = alerts and threat protection.  
Why not the others: A — That's Zero Trust. · B — That's Conditional Access. · C — Those are defense-in-depth layers.

**A13 — A.** *Concept: Defender for Cloud and hybrid*  
Deploy Azure Arc and enable Defender's enhanced security features to protect non-Azure servers.  
Why not the others: B — Private connectivity, not security onboarding. · C — Syncs identities; it doesn't onboard machines. · D — Moves workloads into Azure rather than protecting them in place.

### Section B

**B1 — True.** *Concept: RBAC inheritance*  
Owner at a management group can manage everything in all of its subscriptions.

**B2 — True.** *Concept: Defense-in-depth order*  
Physical → identity & access → perimeter → network → compute → application → data.

**B3 — False.** *Concept: Defender scope*  
It also covers hybrid (via Azure Arc) and other clouds such as AWS and GCP.

**B4 — False.** *Concept: Zero Trust and location*  
The reverse — Zero Trust requires authentication and doesn't trust location.

**B5 — True.** *Concept: Conditional MFA*  
This is the 'more granular MFA experience' described in the module.

**B6 — False.** *Concept: Domain Services sync direction*  
Sync is one-way: from Microsoft Entra ID to the managed domain.

**B7 — False.** *Concept: RBAC at app level*  
RBAC covers Resource Manager actions; application security is your app's job.

**B8 — True.** *Concept: SSO strength*  
Every later connection relies on that first authentication.

**B9 — True.** *Concept: Key Vault role*  
Centralizes secrets and keys instead of hard-coding them in apps.

### Section C

**C1 — D.** *Concept: Choosing Conditional Access*  
All three are signal-based sign-in decisions — exactly Conditional Access's common scenarios.  
Why not the others: A — RBAC grants permissions on resources; it doesn't evaluate sign-in signals like location or device. · B — Azure Policy governs resource configuration, not user sign-ins. · C — Measures posture; it doesn't enforce sign-in conditions.

**C2 — A.** *Concept: External identities*  
B2B collaboration brings partners in as guests (with access reviews); External ID for customers handles consumer sign-up with social identities.  
Why not the others: B — Local accounts are what External ID avoids, and Entra Connect syncs on-prem AD. · C — Neither handles external or consumer identities. · D — Direct connect currently supports Teams shared channels only, not consumers.

---

## Score guide

| Score (out of 24) | What it means |
| --- | --- |
| 22–24 | Exam-ready on this module. Skim the misses and move on. |
| 18–21 | Solid. Re-read the units behind each miss before the domain review. |
| 15–17 | Shaky. Re-read the module, focusing on the comparisons and gotchas you missed. |
| 0–14 | Redo the module, then retake this quiz. |

The real exam needs 700 out of 1,000 (a scaled score, not a straight percentage), so aim for 80%+ on practice quizzes to leave a margin.
