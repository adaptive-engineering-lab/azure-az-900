# AZ-900 Module 7 Quiz: Describe Azure storage services

**Exam domain:** Domain 2: Describe Azure architecture and services (35–40%)  
**Source module:** [Describe Azure storage services](https://learn.microsoft.com/en-us/training/modules/describe-azure-storage-services/) (Microsoft Learn, course AZ-900T00)  
**Units covered:** Describe Azure storage accounts; Describe Azure storage redundancy; Describe Azure storage services; Identify Azure data migration options; Identify Azure file movement options  
**Questions:** 21 — Section A: 11 multiple choice · Section B: 8 true/false · Section C: 2 scenarios

Answer key and score guide are at the bottom — cover them while you work.

---

## Section A — Multiple choice

**A1.** Which storage account type supports ALL redundancy options (LRS, GRS, RA-GRS, ZRS, GZRS, RA-GZRS)?

- **A.** Standard general-purpose v2
- **B.** Premium file shares
- **C.** Premium page blobs
- **D.** Premium block blobs

**A2.** Which rule applies to storage account names?

- **A.** May include uppercase letters, numbers, and hyphens
- **B.** Up to 63 characters, lowercase letters and numbers
- **C.** 3–24 lowercase letters and numbers, globally unique in Azure
- **D.** Unique within your subscription, and up to 24 characters long

**A3.** What is the endpoint format for Azure Files?

- **A.** https://<account>.blob.core.windows.net
- **B.** https://<account>.dfs.core.windows.net
- **C.** https://<account>.table.core.windows.net
- **D.** https://<account>.file.core.windows.net

**A4.** How does locally redundant storage (LRS) replicate data?

- **A.** Three times within a single datacenter in the primary region
- **B.** Synchronously across three availability zones in the primary region
- **C.** Three times locally, then asynchronously to a secondary region
- **D.** Across zones in the primary region, then to a secondary region

**A5.** How does geo-zone-redundant storage (GZRS) replicate data?

- **A.** ZRS in both the primary and secondary regions
- **B.** LRS in both the primary and secondary regions
- **C.** ZRS in the primary region, then LRS in the secondary region
- **D.** LRS in the primary region, then ZRS in the secondary

**A6.** What does choosing RA-GRS instead of GRS add?

- **A.** Synchronous replication to the secondary region
- **B.** Read access to secondary-region data without a failover
- **C.** Write access to both regions at the same time
- **D.** Zone redundancy in the primary region

**A7.** Customer invoices are accessed infrequently and stored for at least 30 days. Which blob access tier fits best?

- **A.** Cool
- **B.** Cold
- **C.** Archive
- **D.** Hot

**A8.** Which blob access tier can NOT be set as the default at the storage account level?

- **A.** Cold
- **B.** Archive
- **C.** Hot
- **D.** Cool

**A9.** Which storage service is designed for reliable messaging between application components, with messages up to 64 KB?

- **A.** Azure Files
- **B.** Azure Tables
- **C.** Azure Queues
- **D.** Azure Blobs

**A10.** Which tool keeps an on-premises Windows Server and your Azure cloud shares in TWO-WAY sync, acting as a local cache with optional cloud tiering?

- **A.** Azure Migrate
- **B.** Azure File Sync
- **C.** Azure Storage Explorer
- **D.** AzCopy

**A11.** Which tool does Azure Storage Explorer use on the back end to perform its file and blob tasks?

- **A.** Azure Migrate
- **B.** Azure File Sync
- **C.** Azure Data Box
- **D.** AzCopy

## Section B — True or false

**B1.** AzCopy synchronization is bi-directional, based on timestamps.

**B2.** The Archive tier has the lowest storage cost but the highest access cost and rehydration latency.

**B3.** Replication to the secondary region is asynchronous, so a regional failure could cause some data loss.

**B4.** NFS Azure file shares can be accessed from Windows clients.

**B5.** With GRS, data in the secondary region is readable at any time by default.

**B6.** All data written to an Azure storage account is encrypted by the service.

**B7.** Azure Migrate is a physical device that is shipped to your datacenter.

**B8.** Data in Azure Storage is always replicated three times in the primary region.

## Section C — Scenarios

**C1.** Scenario: A healthcare company must (1) survive a full regional outage, (2) read its data from the secondary region during an outage without waiting for failover, and (3) stay available through a zone failure in the primary region. Which redundancy option fits?

- **A.** RA-GZRS
- **B.** ZRS
- **C.** RA-GRS
- **D.** GZRS

**C2.** Scenario: A company must move a 70 TB on-premises archive to Azure once, over a slow internet link. Afterward, branch offices need fast local access to file shares that stay synced with Azure Files. Which combination fits?

- **A.** Azure Migrate for the transfer, then Azure Storage Explorer for access
- **B.** Azure Data Box for the transfer, then AzCopy sync
- **C.** AzCopy for both the transfer and the ongoing sync
- **D.** Azure Data Box for the bulk transfer, then Azure File Sync

---

## Answer key

**Quick key:** A1 A, A2 C, A3 D, A4 A, A5 C, A6 B, A7 A, A8 B, A9 C, A10 B, A11 D, B1 F, B2 T, B3 T, B4 F, B5 F, B6 T, B7 F, B8 T, C1 A, C2 D

### Section A

**A1 — A.** *Concept: Storage account types*  
Standard general-purpose v2 is recommended for most scenarios and supports every redundancy option. Premium types are limited to LRS/ZRS (page blobs: LRS only).  
Why not the others: B — LRS and ZRS only. · C — LRS only. · D — LRS and ZRS only.

**A2 — C.** *Concept: Storage account naming*  
The name forms part of a public endpoint URL, so it must be globally unique.  
Why not the others: A — Lowercase letters and numbers only. · B — Maximum is 24. · D — Must be unique across all of Azure.

**A3 — D.** *Concept: Storage endpoints*  
Each service has its own subdomain: blob, dfs (Data Lake Gen2), file, queue, table.  
Why not the others: A — Blob Storage. · B — Data Lake Storage Gen2. · C — Table Storage.

**A4 — A.** *Concept: LRS*  
LRS is the lowest-cost option and protects against rack/drive failures, but not a datacenter-level disaster.  
Why not the others: B — That's ZRS. · C — That's GRS. · D — That's GZRS.

**A5 — C.** *Concept: GZRS*  
GZRS = ZRS primary + LRS secondary. GRS = LRS primary + LRS secondary. The secondary is always LRS.  
Why not the others: A — The secondary region is always LRS. · B — That's GRS. · D — Reversed.

**A6 — B.** *Concept: Read-access geo-redundancy*  
By default, secondary data isn't readable until failover. RA- options let you read it anytime (it may lag due to RPO).  
Why not the others: A — Secondary replication is always asynchronous. · C — The secondary is read-only. · D — Zone redundancy is the 'Z' in GZRS, not the 'RA'.

**A7 — A.** *Concept: Blob access tiers*  
Minimum retention: Cool 30 days, Cold 90 days, Archive 180 days. The module uses invoices as its Cool example.  
Why not the others: B — For data stored at least 90 days. · C — For rarely accessed data stored at least 180 days, with flexible latency. · D — For frequently accessed data.

**A8 — B.** *Concept: Account-level tiers*  
Hot, Cool, and Cold can be account defaults. Archive can only be set at the blob level.  
Why not the others: A — Can be set at the account level. · C — Can be set at the account level. · D — Can be set at the account level.

**A9 — C.** *Concept: Azure Queues*  
Queue Storage holds millions of messages for asynchronous processing and is often paired with Azure Functions.  
Why not the others: A — Managed SMB/NFS file shares. · B — NoSQL structured, non-relational data. · D — Unstructured object storage.

**A10 — B.** *Concept: Azure File Sync*  
File Sync turns a Windows server into a local cache of Azure Files, synced in both directions, with optional cloud tiering.  
Why not the others: A — A migration hub for workloads, not ongoing file sync. · C — A GUI for managing files and blobs; it uses AzCopy under the hood. · D — AzCopy sync is one-direction only.

**A11 — D.** *Concept: Storage Explorer back end*  
Storage Explorer is a GUI over AzCopy.  
Why not the others: A — A migration hub. · B — A separate sync service for Windows file servers. · C — A physical device for bulk offline transfer.

### Section B

**B1 — False.** *Concept: AzCopy sync*  
AzCopy sync is one-direction: you designate source and destination.

**B2 — True.** *Concept: Archive tier costs*  
Cheapest to store, most expensive and slowest to get back.

**B3 — True.** *Concept: Async geo-replication*  
The gap is the recovery point objective (RPO) — typically under 15 minutes, with no SLA.

**B4 — False.** *Concept: NFS clients*  
NFS shares are accessible from Linux or macOS. SMB shares work with Windows, Linux, and macOS.

**B5 — False.** *Concept: GRS secondary readability*  
Secondary data isn't readable until failover unless you choose RA-GRS or RA-GZRS.

**B6 — True.** *Concept: Storage encryption*  
Listed under the 'Secure' benefit of Azure Storage.

**B7 — False.** *Concept: Azure Migrate vs Data Box*  
That's Azure Data Box. Azure Migrate is an online hub for assessment and migration.

**B8 — True.** *Concept: Primary copies*  
Both LRS and ZRS keep three copies in the primary region.

### Section C

**C1 — A.** *Concept: Choosing redundancy*  
GZRS covers zone failures (ZRS primary) and regional outages (geo-replication); the RA- prefix adds read access to the secondary.  
Why not the others: B — Meets 3 only — there's no secondary region. · C — Meets 1 and 2, but LRS in the primary doesn't survive a zone failure. · D — Meets 1 and 3, but you can't read the secondary without failover.

**C2 — D.** *Concept: Migration and file movement*  
Data Box handles large offline transfers when bandwidth is limited. File Sync provides local caches with bi-directional sync.  
Why not the others: A — Storage Explorer is a manual GUI, not a sync service. · B — AzCopy can't give branches a bi-directionally synced local cache. · C — Too slow for 70 TB here, and AzCopy sync is one-way with no local cache.

---

## Score guide

| Score (out of 21) | What it means |
| --- | --- |
| 19–21 | Exam-ready on this module. Skim the misses and move on. |
| 16–18 | Solid. Re-read the units behind each miss before the domain review. |
| 13–15 | Shaky. Re-read the module, focusing on the comparisons and gotchas you missed. |
| 0–12 | Redo the module, then retake this quiz. |

The real exam needs 700 out of 1,000 (a scaled score, not a straight percentage), so aim for 80%+ on practice quizzes to leave a margin.
