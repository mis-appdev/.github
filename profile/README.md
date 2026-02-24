# 🏛️ Team Development & Style Guide

Welcome to the MIS APP DEV Team Repo. Follow these standards to ensure consistency across all  projects.

---

## 🚀 The Team Workflow
This is the loop the team must follow to ensure production stability.

### 1. Start of Day: Sync Your Code
* **Action:** Switch to `main` → **Pull**.
* **Why:** Prevents "Merge Conflicts" later by ensuring you aren't working on an outdated version.

### 2. Start of Task: Branch Out
* **Rule:** Never work directly on the `main` branch.
* **Format:** Use `feature/`, `bugfix/`, or `docs/` prefixes.
* **Example:** `feature/cams-login-ui`

### 3. During Work: Commit Small & Often
* **Frequency:** Save your progress in "chunks." Don't wait until the end of the day.
* **Action:** Open **Git Changes** window → Click **Commit All**.
* **Message:** Use clear descriptions (e.g., `feat: added email validation to Blazor form`).
> 🛑 **DO NOT COMMIT CHANGES TO MAIN BRANCH.**

### 4. End of Task: Push & Propose (PR)
* **Push:** Click the **Up Arrow** in Visual Studio to send your branch to GitHub.
* **Pull Request (PR):** Click the **Gold Banner** in Visual Studio or go to GitHub to "Open Pull Request."
* **Details:** Add a title, describe what you changed, and **assign a reviewer**.

### 5. Review & Fix
* **Feedback:** Address teammate comments by making fixes on your local machine.
* **Update:** Commit and **Push again** to the *same* branch; the PR updates automatically.

### 6. Merge
* **Approval:** Once you see the green "Approved" checkmark.
* **Merge:** Click **Merge Pull Request** on GitHub.
* **Cleanup:** Delete the feature branch once merged to keep the repo clean.

---

## 🛠️ Standards & Conventions

### 📂 Repository Naming (Kebab-case)
All repositories must follow the **Kebab-case (hyphenated)** format for URL compatibility.
* **Format:** `[project]-[framework]-[platform/type]`
* **Rules:** Lowercase letters, numbers, and hyphens only. No spaces, underscores, or caps.
* **Examples:**
    * ✅ `bencare-core-api`
    * ✅ `cams-blazor-web-app`
    * ❌ `BenCare_API`

### 🌿 Branching Strategy
| Prefix | Purpose | Example |
| :--- | :--- | :--- |
| `feature/` | New development | `feature/login-ui` |
| `bugfix/` | Fixing a bug | `bugfix/sql-timeout` |
| `hotfix/` | Urgent production fixes | `hotfix/patch-v1` |
| `docs/` | Documentation only | `docs/update-readme` |

### 💬 Commit Message Standards
* **Format:** `[Type]: [Short Description]`
* **Example:** `feat: add biometric login to MAUI app`
* **Example:** `fix: resolve null reference in CAMS API`

---

## 💻 Visual Studio (Step-by-Step)

### 1. Create a New Branch
1. Click **main** in the bottom-right **Status Bar**.
2. Select **New Branch...**
3. **Name:** `feature/your-task-name`
4. **Based on:** `main`
5. Click **Create**.

### 2. Verify Your Branch
* Glance at the bottom-right corner before coding.
* If it says `feature/your-task`, you are safe.
* If it says `main`, **STOP** and switch branches.

### 3. Switching Between Branches
* Click the branch name in the status bar to swap.
* Visual Studio will automatically "shelve" unfinished work and swap your files.

---

> [!IMPORTANT]
> * Nothing goes into `main` without a Pull Request and at least one approval.
> * **NEVER** commit `appsettings.json` with real passwords or SQL connection strings.
> * **Sync Often:** If on a branch for >1 day, pull `main` into your branch to stay updated.
