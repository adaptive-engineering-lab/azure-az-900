# DP-700 Practice Quiz — Secure Data Access in Microsoft Fabric

Source module: https://learn.microsoft.com/en-us/training/modules/secure-data-access-in-fabric/
Units covered: Understand the Fabric security model | Configure workspace and item permissions | Apply granular permissions

DP-700 domain: **Implement and manage an analytics solution** — "Configure security and governance" broadly, consolidating workspace roles, item permissions, T-SQL granular permissions, and OneLake security roles into one unified model.

Note: This module overlaps with concepts from earlier modules (Intro to End-to-End Analytics, Medallion Architecture, Secure Data Warehouse) but frames them as one coherent three-level evaluation model — worth having that unified picture solid for the exam.

---

## Section A — Multiple Choice

**1.** What is the correct order of Fabric's three levels of access evaluation?
A. Entra ID authentication → Fabric access → Data security
B. Data security → Fabric access → Entra ID authentication
C. Fabric access → Data security → Entra ID authentication
D. Data security → Entra ID authentication → Fabric access

**2.** Which of the following is **NOT** one of the four primary access controls within the "Data security" level?
A. Item permissions
B. Network security groups
C. OneLake security
D. Workspace roles

**3.** Which workspace role allows a user to create, view, and modify all content and data in a workspace, but **NOT** share it or manage permissions?
A. Admin
B. Member
C. Contributor
D. Viewer

**4.** Which workspace role can create, view, modify, and share all content/data, but cannot manage workspace permissions (that capability is Admin-only)?
A. Viewer
B. Contributor
C. Admin
D. Member

**5.** By default, what access do Viewers have to the underlying data stored in OneLake for items in their workspace?
A. None — unless granted via OneLake security roles
B. Full read access
C. Full read/write access
D. Read access only to fact tables

**6.** When you share a lakehouse via item permissions, what does the baseline "Read" permission (always granted) allow?
A. Full query access to the SQL analytics endpoint
B. Viewing item metadata and associated reports only, not underlying data
C. Read and write access to OneLake files
D. Membership in the DefaultReader role

**7.** Which additional lakehouse sharing permission grants access to lakehouse data through Apache Spark and OneLake APIs?
A. Read all SQL endpoint data
B. Build reports on the default semantic model
C. Read all Apache Spark and subscribe to events
D. Manage OneLake security

**8.** Granting "Read all Apache Spark and subscribe to events" automatically adds the recipient to which OneLake security role?
A. Admin
B. Contributor
C. Custom reader
D. DefaultReader

**9.** Which T-SQL DCL commands are used to apply granular permissions at the SQL analytics endpoint?
A. GRANT, DENY, REVOKE
B. CREATE, ALTER, DROP
C. SELECT, INSERT, UPDATE
D. BEGIN, COMMIT, ROLLBACK

**10.** In OneLake security, what are the two permission levels a role can grant?
A. Admin and Viewer
B. Read and ReadWrite
C. Full and Partial
D. Public and Private

**11.** Which workspace roles already have full read and write access to all OneLake data, regardless of any OneLake security roles configured?
A. Viewer only
B. Only Admin
C. Admin, Member, and Contributor
D. Viewer and Contributor only

**12.** Who is permitted to create or modify OneLake security roles?
A. Any user with Viewer access
B. Anyone with Read item permission
C. Only the Fabric tenant administrator
D. Only workspace Admin and Member roles

---

## Section B — True / False

**13.** Granting the "Read all SQL endpoint data" item permission restricts access to only specific tables within a lakehouse by default, rather than all data. **(True/False)**

**14.** OneLake security role constraints can include row or column filters to restrict data further within a granted table or folder. **(True/False)**

**15.** A user granted only the baseline "Read" item permission on a lakehouse automatically has full Spark access to all lakehouse tables. **(True/False)**

**16.** If a user is restricted to a custom OneLake security role but not removed from the DefaultReader role, they will still retain full read access via DefaultReader. **(True/False)**

---

## Section C — Scenario / Choose the Best Option

**17.** A new hire needs to collaborate broadly across many items in a workspace — creating, viewing, and modifying content — but should not be able to share items or manage other users' permissions. Which approach fits?
A. Grant item permissions on each item individually
B. Assign the Contributor workspace role
C. Assign the Admin workspace role
D. Create a custom OneLake security role

**18.** A Viewer-role user needs to query only two specific tables in a lakehouse containing sensitive patient data, and should not see any other tables. What is the most appropriate approach?
A. Upgrade the user to Contributor
B. Grant "Read all Apache Spark and subscribe to events" item permission
C. Create a OneLake security role scoped to those two tables and add the user as a member (removing them from DefaultReader if present)
D. Share the lakehouse with "Build reports on the default semantic model" permission

---

## Answer Key & Rationale

**1. A — Entra ID authentication → Fabric access → Data security.** Fabric evaluates access sequentially in this exact order: first, can the user authenticate at all; second, can they access Fabric; third, can they perform the requested action on a specific table or file.

**2. B — Network security groups.** The four primary access controls within the Data security level are workspace roles, item permissions, compute/granular permissions, and OneLake security — network security groups aren't part of this model.

**3. C — Contributor.** Contributor can create, view, and modify all content and data in a workspace, but lacks the share and permission-management capabilities that Member and Admin have respectively.

**4. D — Member.** Member adds sharing on top of Contributor's capabilities (create/view/modify/share), but still can't manage workspace permissions — that's reserved for Admin.

**5. A — None — unless granted via OneLake security roles.** Viewers can see items listed in the workspace, but have zero access to the underlying OneLake data by default; OneLake security roles are specifically how you grant them access to particular tables or folders.

**6. B — Viewing item metadata and associated reports only, not underlying data.** This baseline Read permission is always granted when sharing an item, but it's deliberately limited — actual data access requires one of the additional permissions layered on top.

**7. C — Read all Apache Spark and subscribe to events.** This is the specific additional permission for Spark and OneLake API access to lakehouse data, distinct from "Read all SQL endpoint data" (which covers T-SQL access instead).

**8. D — DefaultReader.** This is an important side effect worth remembering — granting Spark/OneLake API access via item permissions automatically enrolls the recipient in the lakehouse's DefaultReader OneLake security role, giving them full read access unless later restricted.

**9. A — GRANT, DENY, REVOKE.** These are the Data Control Language (DCL) commands used to apply granular permissions at the SQL analytics endpoint — the same mechanism you'd use for RLS, CLS, and dynamic data masking configuration.

**10. B — Read and ReadWrite.** These are OneLake security's two permission levels: Read for viewing data, ReadWrite for viewing *and* editing specific tables or folders without needing a full workspace write role.

**11. C — Admin, Member, and Contributor.** These three roles already have full OneLake read/write access by virtue of their workspace role — OneLake security roles don't restrict them. OneLake security specifically exists to grant *additional* access to users who otherwise have none (Viewers, or users with only Read item permission).

**12. D — Only workspace Admin and Member roles.** This is an explicit restriction — Contributors and Viewers cannot create or modify OneLake security roles, even though Contributors do have broader data access by virtue of their workspace role.

**13. False.** The opposite is true — both "Read all SQL endpoint data" and "Read all Apache Spark and subscribe to events" grant access to *all* data in the lakehouse by default. To restrict access to specific tables, you need T-SQL granular permissions (for SQL access) or OneLake security roles (for Spark/OneLake API access).

**14. True.** OneLake security role constraints are explicitly described as optional row or column filters applied to the data within the role — letting you narrow access even further than just which tables/folders are included.

**15. False.** The baseline Read permission only covers viewing item metadata and associated reports — it does not grant Spark data access. Spark access specifically requires the separate "Read all Apache Spark and subscribe to events" permission.

**16. True.** This is explicitly called out as an important gotcha — DefaultReader membership persists independently, so restricting someone to a custom role without also removing them from DefaultReader leaves their original full read access intact through that default role.

**17. B — Assign the Contributor workspace role.** This matches the scenario precisely: broad create/view/modify access across the workspace, without the share or permission-management capabilities that Member or Admin would add — exactly the described need, and exactly the principle of least privilege in action.

**18. C — Create a OneLake security role scoped to those two tables and add the user as a member (removing them from DefaultReader if present).** This is the only option that achieves table-level restriction for a Viewer — the other options either grant access to the whole lakehouse (B) or don't address data access at the table level at all (A, D).

---

**Score guide:** 16–18 correct = strong grasp, ready to move to the next module. 12–15 = solid but review the item permission types (and what each actually grants) and the DefaultReader role behavior. Below 12 = re-read units 2–4 before moving on.
