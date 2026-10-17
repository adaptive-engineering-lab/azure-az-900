# DP-700 Practice Quiz — Implement Continuous Integration and Continuous Delivery (CI/CD) in Microsoft Fabric

Source module: https://learn.microsoft.com/en-us/training/modules/implement-cicd-in-fabric/
Units covered: Understand CI/CD | Implement version control and Git integration | Implement deployment pipelines | Automate CI/CD using Fabric APIs

DP-700 domain: **Implement and manage an analytics solution** — "Implement lifecycle management in Fabric": Configure version control, Implement database projects, Create and configure deployment pipelines.

---

## Section A — Multiple Choice

**1.** What is the primary goal of Continuous Integration (CI)?
A. To automatically release code to production without testing
B. To frequently merge code into a shared branch with automated build/test validation, catching conflicts early
C. To replace the need for version control
D. To manually test code once per quarter

**2.** What happens during Continuous Delivery, and when does it occur relative to CI?
A. It happens before CI; code is built and tested in isolation
B. It happens after CI; code is deployed to a staging environment for further automated testing
C. It replaces CI entirely
D. It only applies to database projects

**3.** What distinguishes Continuous Deployment from Continuous Delivery?
A. Continuous Deployment requires manual approval at every stage
B. Continuous Deployment automatically releases updates to production once they pass automated tests, without manual intervention
C. Continuous Deployment only applies to Git, not deployment pipelines
D. There is no difference between the two

**4.** In Fabric's CI/CD model, which capability specifically implements the "integration" part?
A. Deployment pipelines
B. Git
C. Fabric REST APIs
D. Dataflow Gen2

**5.** In Fabric's CI/CD model, which capability specifically implements the "deployment" part?
A. Git
B. Deployment pipelines
C. Notebooks
D. KQL Querysets

**6.** Which version control systems does Fabric support for Git integration?
A. Only GitHub
B. Only Azure DevOps
C. GitHub and Azure DevOps
D. Any Git provider, with no restriction

**7.** At what level in Fabric is Git integration configured?
A. Item level only
B. Workspace level
C. Tenant level only
D. Capacity level

**8.** In the Fabric Source control window, which selection do you use to push your workspace changes into the connected Git branch?
A. Updates
B. Changes
C. Deploy
D. Branch out

**9.** In the Fabric Source control window, which selection do you use to pull new commits from the Git branch into your workspace?
A. Changes
B. Deploy
C. Updates
D. Merge queries

**10.** Why is it recommended to develop in an isolated workspace rather than directly in a shared, live workspace?
A. Isolated workspaces are cheaper
B. Direct changes in a shared workspace override and affect all other workspace users immediately
C. Shared workspaces don't support Git integration at all
D. Isolated workspaces automatically deploy to production

**11.** What does "Branch out to new workspace" do?
A. Deletes the current branch
B. Creates a new isolated branch and syncs a new workspace with it, giving you an isolated environment for development
C. Merges all branches into main automatically
D. Converts a workspace into a deployment pipeline

**12.** Where is a Pull Request (PR) created to merge changes from an isolated branch into the main branch?
A. In the Fabric Source control window
B. In Git (GitHub or Azure DevOps), not in Fabric directly
C. In the deployment pipeline interface
D. In the Fabric REST API console only

**13.** What happens when you select Deploy between two stages in a Fabric deployment pipeline?
A. Only new items are copied; existing items are left unchanged
B. All workspace content from the source stage is copied into the target stage
C. Only Git commits are synced, not actual Fabric items
D. The source stage is deleted after deployment

**14.** What is a common recommended approach to combining Git integration with deployment pipelines, to avoid sync conflicts?
A. Connect every stage's workspace (Dev, Test, and Production) to Git
B. Connect only the Development workspace to Git; use deployment pipelines to promote content to Test and Production
C. Never use Git and deployment pipelines together
D. Connect only the Production workspace to Git

---

## Section B — True / False

**15.** Fabric REST APIs can be used to commit workspace changes to a connected remote Git branch programmatically. **(True/False)**

**16.** The Git status API lets you see which items have incoming changes and which have uncommitted changes. **(True/False)**

**17.** A deployment pipeline can only be created from the Workspaces icon in the left navigation pane — there is no other way to create one. **(True/False)**

**18.** Deployment pipeline REST APIs can list the items in a specific stage and deploy content from one stage to another programmatically. **(True/False)**

---

## Section C — Scenario / Choose the Best Option

**19.** Two developers are both making changes to items in a shared Fabric workspace at the same time, and they keep unintentionally overwriting each other's work. What CI/CD practice should they adopt to resolve this?
A. Disable Git integration entirely
B. Each developer should work in their own isolated workspace/branch, then use pull requests to merge changes into the main branch
C. Only one developer should be allowed to use Fabric at a time
D. Use deployment pipelines instead of Git for all development work

**20.** Your organization wants to automatically trigger a deployment of the latest Test-stage content into Production every night as part of a scheduled process, without anyone manually clicking Deploy. What should you use?
A. The Source control Changes panel
B. Fabric REST APIs for deployment pipelines, called from an automated scheduled process
C. Branch out to new workspace
D. The Visual query editor

---

## Answer Key & Rationale

**1. B — To frequently merge code into a shared branch with automated build/test validation, catching conflicts early.** CI is specifically about avoiding the long-isolated-branch problem — frequent small commits mean conflicts surface early, when they're easier and faster to fix.

**2. B — It happens after CI; code is deployed to a staging environment for further automated testing.** CD is the next stage in the pipeline — once CI validates the merge, the code moves to staging for another round of automated testing before it's ready for production.

**3. B — Continuous Deployment automatically releases updates to production once they pass automated tests, without manual intervention.** This is the fully automated end of the pipeline — updates flow through structured deployment stages and into production automatically once they clear testing, no human click required.

**4. B — Git.** Git implements the integration half of CI/CD in Fabric — branching, committing, merging, and version history.

**5. B — Deployment pipelines.** These implement the deployment half — promoting content across development, test, and production environments.

**6. C — GitHub and Azure DevOps.** These are the two explicitly supported version control systems for Fabric's Git integration — no other Git providers are supported.

**7. B — Workspace level.** Git integration connects at the workspace level, and you version the items you develop within that workspace.

**8. B — Changes.** This selection in the Source control window is how you push your workspace's uncommitted changes out to the connected Git branch.

**9. C — Updates.** This is the reverse direction — pulling new commits that have landed in the Git branch back into your workspace to keep it in sync.

**10. B — Direct changes in a shared workspace override and affect all other workspace users immediately.** Since a shared workspace holds live items, any change ripples out to everyone using it — isolating your development work avoids stepping on other developers' work in progress.

**11. B — Creates a new isolated branch and syncs a new workspace with it, giving you an isolated environment for development.** This is the specific mechanism the module describes for spinning up an isolated dev environment directly from the Fabric web interface, without needing external tooling.

**12. B — In Git (GitHub or Azure DevOps), not in Fabric directly.** PRs are a Git-native concept — you commit your changes to your isolated branch via Fabric's Source control panel, but the actual pull request to merge into main happens in the Git provider itself.

**13. B — All workspace content from the source stage is copied into the target stage.** Deployment copies everything from the source stage's workspace into the target stage — it's a full content promotion, not a selective or partial copy.

**14. B — Connect only the Development workspace to Git; use deployment pipelines to promote content to Test and Production.** This is the module's explicitly recommended approach — Git handles version control during development, while deployment pipelines handle promoting content onward, avoiding the sync conflicts that could arise from connecting every stage to Git independently.

**15. True.** Fabric REST APIs let you commit workspace changes to the connected remote branch and update the workspace with new commits — the same actions the Source control window's Changes/Updates buttons perform, but programmatically.

**16. True.** The Git status API specifically shows which items have incoming changes (from Git) and which have changes not yet committed (from the workspace) — the automated equivalent of the Git status column you'd see in the Fabric UI.

**17. False.** A deployment pipeline can be created two ways: via the Workspaces icon in the left navigation pane, *or* via the Create deployment pipeline icon at the top of a workspace — either path works.

**18. True.** The module explicitly lists both capabilities among the deployment pipeline REST APIs: listing items in a specified stage, and deploying content from one stage to another — full programmatic control over the deployment process.

**19. B — Each developer should work in their own isolated workspace/branch, then use pull requests to merge changes into the main branch.** This directly addresses the described problem: working in a shared live workspace causes changes to override each other, while isolated branches plus PRs let developers work independently and merge changes in a controlled, conflict-aware way.

**20. B — Fabric REST APIs for deployment pipelines, called from an automated scheduled process.** This matches the described need precisely — a scheduled, unattended trigger for a deployment action, which requires programmatic automation rather than a manual UI click.

---

**Score guide:** 18–20 correct = strong grasp, ready to move to the next module. 14–17 = solid but review the Changes vs. Updates distinction in Source control, and where PRs actually happen (Git, not Fabric). Below 14 = re-read units 2–5 before moving on.
