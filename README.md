
# Midnight-Tee-Adventure-RPG

> **Core Developers Hub:** Contributors, Lore, Characters, and Engine Architecture for **Midnight-Tee-Adventure-RPG** (Discord Text-Based RPG).  
> *Zero-Trust Organization Architecture & Repository Hardening co-designed with **Google Gemini**.*

---

## 🛡️ Defense-in-Depth Repository & Organization Blueprint

To balance open-source community transparency with strict operational security across multi-IDE, CLI, and low-level runtime environments, this organization (`Midnight-Tee-Womp-Venture`) is hardened using a **7-Layer Zero-Trust Architecture**:

### 1. Account & Identity Isolation
* **Organization Container (`GitHub Free`):** Decouples public project infrastructure from private developer repositories without requiring secondary credentials.
* **Private Membership Visibility:** Organization roster visibility is explicitly locked to **Private** (`People` tab), preventing public profile cross-linking.
* **Cryptographic Commit Authorship:** Commits retain verifiable author attribution while keeping all unrelated private repositories strictly isolated.

### 2. Zero-Trust Member Privileges (Least-Privilege RBAC)
* **Default-Deny Base Permissions:** Set to **`No permission`** for both repositories and organization projects—new members see zero internal assets until explicitly scoped into a team.
* **Surface-Area Lockdown:** Disabled unauthorized public/private repository creation, `*.github.io` Pages publishing, and third-party OAuth/GitHub App access requests.
* **Owner-Only Structural Controls:** Restricted repository visibility changes, repository deletion/transfer, protected branch renames, and sub-team creation exclusively to **Organization Owners**.

### 3. Compartmentalized Team Access (`Secret` Teams)
* **Role-Based Grouping (`Dev-Contributor`):** Collaborators are managed via a dedicated **`Secret`** team rather than individual user grants, hiding internal team rosters from non-members.
* **Scoped `Write` Boundary:** The `Dev-Contributor` team holds **`Write`** access on this repository—allowing feature branch pushes and Pull Requests while keeping administrative settings locked.

### 4. Branch Rulesets & Pull Request Gates (`main`)
* **Default Branch Protection:** `main` is actively protected against branch deletion and force-pushes.
* **Mandatory Review Workflow:** Direct pushes to `main` are blocked for contributors. All changes require a Pull Request with **at least 1 approval**, automatic **dismissal of stale approvals** on new commits, and **conversation resolution** prior to merge.
* **Break-Glass Isolation:** Ruleset bypass exemptions are bound strictly to **`Organization admin`** (never `Repository admin`), preventing privilege escalation.

### 5. Whitelist-First `.gitignore` Policy
* **Default-Deny Dotfiles (`.*`):** All hidden configuration directories, local caches, `.env` secrets, IDE state folders, and low-level runtime binaries (`*.dex`, `*.py[cod]`) are blocked at the root `.gitignore` level unless explicitly whitelisted.

---

## 🤝 Contributor Workflow (`Dev-Contributor`)

1. **Verify Profile Privacy:** After accepting your organization invite, check the `People` tab if you wish to keep your membership visibility set to **Private**.
2. **Clone & Branch:** Never commit directly to `main`. Create a descriptive feature branch:
   ```bash
   git checkout -b feat/your-feature-name
   ```
3. **Commit & Push:** Keep secrets and local environment configs out of commits (enforced by `.gitignore`), then push your branch:
   ```bash
   git push -u origin feat/your-feature-name
   ```
4. **Open a Pull Request:** Target `main`, summarize your lore/character/code changes, and request a review.

---

## 📂 Repository Structure
* `/docs` — World lore, character sheets, and game mechanics
* `/src` — Core Discord bot engine and RPG state logic
* `/tests` — Automated test suites and validation probes

---

## 📄 License
Distributed under the **MIT License**. See `LICENSE` for more information.
