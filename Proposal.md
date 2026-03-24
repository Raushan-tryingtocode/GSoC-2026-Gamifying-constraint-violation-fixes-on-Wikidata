# Wikidata Gamification: Constraint Violation Fixer
### GSoC 2026 Project Proposal | Distributed Game Framework

## 🚀 Introduction
I am **Raushan**, a 2nd-year CSE student specializing in AI/ML at SITS. I am a backend-focused developer and an active Wikimedia contributor with **4 patches merged on Gerrit** across Pywikibot and MediaWiki. 

I am passionate about gaming mechanics and their potential to improve data quality, which is why I am specifically interested in integrating Wikidata constraint violations into the Distributed Game framework.

---

## 📚 Project Understanding & Research
* **Goal:** Increase the efficiency of fixing Wikidata constraint violations by integrating them into the Distributed Game framework.
* **Current Status:**
* For security, I’m using Wikimedia OAuth 2.0. This means the app never even touches a user's password. Instead, it uses temporary 'keys' (access tokens) to perform edits. It’s the gold standard for Wikimedia apps and keeps everything 100% secure and compliant.
* I’ve been looking at how XTools handles data. Instead of just "asking" the standard API for info (which is slow and would make the game laggy), I'm planning to use Direct Database Access through Toolforge. This lets the backend pull a whole bunch of item labels at once directly from the SQL replicas, making the game feel way faster for the player.
* Since I am assuming most users will play on their phone, adding a neat dark mode seems to be the next step in the UI phase.
* I'm planning to add a simple "Report" button on each task so, if a user thinks a violation fix is wrong or the instructions are confusing, they can flag it. It would help improve the quality of the game
* Adding a community also seems like a good option but I am not sure about increasing the complexity of the project yet.

### Technical Stack
* **Python:** Primary language for backend logic and Pywikibot integration.
* **JavaScript & Frontend:** Secondary focus for UI development (React.js, CSS).
* **Version Control:** Expert use of Git, GitHub, and Gerrit.
* **Databases:** Proficient in SQL; currently leveling up in SPARQL for Wikidata queries.

---
  
## 🛠 Microtask Progress

### Microtask 1: Analysis Report
I've identified the core technical challenge: the game needs a seamless "bridge" to Wikidata's constraint system.
* **Data Source:** Utilizing the MediaWiki API (`action=wbcheckconstraints`) to fetch items with active violations.
* **The Fix:** Researching `wbeditentity` to automate backend edits so users can submit fixes without leaving the game UI.
* **Next Steps:** Setting up a local environment to plug Wikidata Constraints into the existing Decision logic flow.

### Microtask 2: Improving Game #90 Readability
* **Status:** Work-in-Progress (WIP).
* **Details:** Testing regex locally to handle edge cases (nested brackets) in Wikiquote articles. Findings will be posted to Phabricator shortly.

---

## 🎮 Gamification Logic

### Violation Ranking System
| Violation Type | Rank | Experience (XP) |
| :--- | :--- | :--- |
| Format, Unique Value, or Type Constraints | **Rare** | +20 XP / fix |
| Range or Contemporary Constraints | **Unique** | +45 XP / fix |
| Inverse or Conflicts-With Constraints | **Legendary** | +80 XP / fix |
| Multiple Constraints | **Mythic** | +150 XP / fix |

### Leveling Structure
Users start as an **Apprentice** (Lvl 1). The XP cap increases by **15%** per level.
* *Example:* Lvl 1 = 100XP cap. Lvl 5 = 175XP cap.

| User Rank | Level Range | Access Level |
| :--- | :--- | :--- |
| **Apprentice** | Lvl 1 - 10 | Rare violations only |
| **Junior** | Lvl 11 - 25 | Unique and below |
| **Senior** | Lvl 26 - 50 | Legendary and below |
| **Champion** | Lvl 51 - 99 | **All Levels (Mythic Access)** |

> 👑 **Note:** Reaching **Level 99** grants the ultimate badge: **"Data King"**.

---

## 📅 Detailed Timeline

| Phase | Dates | Goals |
| :--- | :--- | :--- |
| **Proposal & Microtasks** | March 17 – March 31 | Finalizing proposal and finishing Microtasks 1 & 2. |
| **Community Bonding** | April 1 – May 4 | Mentor consultation and local environment setup. |

### Coding Phase 1: Foundation & Data Pipeline (Week 1 - 3)
* **Research:** Map `wbcheckconstraints` API schemas to difficulty tiers.
* **Coding:** Develop the **Backend Fetcher Module** (Python) for OAuth handshakes and secure violation fetching.
* **Documentation:** Create the "Developer README" for backend components.

### Coding Phase 2: The Core Game (Week 4 - 6)
* **Research:** UI/UX responsiveness for mobile devices.
* **Coding:** Build the primary interface using **React.js**. Ensure "Apprentice" fixes take <1 minute.
* **Deliverable:** Working UI with login and functional Level 1 fixes.

### Coding Phase 3: XP Engine & Leveling (Week 7 - 9)
* **Research:** Sorting property constraints into tiers based on complexity.
* **Coding:** Implement the leveling math: `Next LVL XP = Current XP + 15%`.
* **Documentation:** Publish the "Gamification Spec" detailing the ranking logic.

### Coding Phase 4: Deployment & Consensus (Week 10 - 12)
* **Research:** Implementing **Consensus Models**. Requiring 3-point consensus for low-level edits.
* **Coding:** Deploy entire stack on **Wikimedia Toolforge**.
* **Documentation:** Final GSoC Report and "How to Contribute" manual.

---

## 📊 Availability & Commitment
* **Weekly Commitment:** 35-40 hours.
* **Exam Strategy:** My semester exams fall during the transition to Coding Phase 1. I will front-load research in April to ensure a 100% focus on high-output coding starting June 4th.

## 🔗 Contact & Links
* **Gerrit:** [Merged Patches](https://gerrit.wikimedia.org/r/q/owner:Raushan31+(status:open+OR+status:merged))
* **GitHub:** [Raushan-tryingtocode](https://github.com/Raushan-tryingtocode)
* **Email:** raushanh31@gmail.com
