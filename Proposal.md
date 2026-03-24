**Introduction:** 
I am Raushan, a 2nd-year CSE student specializing in AI/ML. I am a backend-focused developer and an active Wikimedia contributor with 4 patches already merged on Gerrit across Pywikibot and MediaWiki. I am very passionate about gaming mechanics and their potential to improve data quality, which is why I am specifically interested in this project.

**Project Understanding & Research**: 
  - Goal: Increase the efficiency of fixing Wikidata constraint violations by integrating them into the Distributed Game framework.
  - Current Status: I am currently performing a deep dive into the Distributed Game codebase and exploring the Wikibase Quality Constraints extension.

**Skills:**

  - **Python:** This my primary language. I’m comfortable with backend logic and have experience working on the Pywikibot codebase.
  - **Javascript & Frontend:** My secondary language, used primarily for frontend along with CSS
  - **Version control:** I have a solid grasp with the workings of Git, GitHub and Gerrit through previous contributions.
  - **Databases (SQL & SPARQL):** Good grasp of SQL for data querying. I’m currently leveling up my SPARQL skills.








**Microtask Details:**

**Microtask 1: Analysis Report**
After looking through the project description and the Distributed Game framework, I’ve identified the core technical challenge: the game needs a way to "talk" to Wikidata's constraint system.
My current understanding is:
  - Data Source: We need to fetch items that have "violations" (errors). I'll be looking into using the MediaWiki API, specifically action=wbcheckconstraints, to find these items.
  - The Fix: When a user plays the game and picks the right answer, the backend needs to send an edit to Wikidata. I’m researching how to use wbeditentity to automate this so the user doesn't have to leave the game.
  - Next Steps: My next goal is to set up a local version of the Distributed Game to see how it handles current Decision logic and how I can plug the Wikidata Constraints into that same flow.

**Microtask 2: Improving Game #90 Readability (WIP):**
I am currently testing that regex locally to see if it handles edge cases like nested brackets etc. that might still show up in Wikiquote articles. I’ll post my findings or a follow-up patch once I’ve verified it.

**Project Ideas:**
**Sorting system:**


  - Every violation will get sorted into a rank. 
| Violation | Rank | Experience ||
| --- | --- | --- |
| Format Constraints, Unique Value Constraints or Type Constraints | Rare | +20XP/fix |
| Range Constraints or Contemporary Constraints | Unique | +45XP/fix |
| Inverse Constraints or Conflicts-With Constraints | Legendary | +80XP/fix |
|Multiple Constraints | Mythic | + 150XP/fix |


**Levelling System:**

  - The user starts as 'Apprentice ' at level 1. 
       - The 1st level has an 'Experience' cap of 100XP and after each level it increases by 15%. So. by the time the User/Player levels up to the 5th level his XP to level-up to the next level would be 175XP and so-on.
 
- **Stucture:**
| User Rank| Level-up Cap | Violation Limit||
| --- | --- | --- |
| **Apprentice ** | lvl.1-10 | Can only attempt Rare level violations |
| **Junior ** | lvl.11- 25 | Can only attempt Unique level violations and below  |
| **Senior ** | lvl.26-50 | Can only attempt Legendary level violations and below  |
|**Champion** | lvl.51-99 | Can attempt Mythic level violations and all the others below |

**Max level cap is 99 and anyone who reaches lvl.99 will get the Badge of 'Data King' **


**Detailed Timeline**
|** Pre-coding period Plans** | **Present - GSoC 2026** | **Goals**
| **Proposal & Microtasks** | March 17 – March 31 | Finalizing the proposal and finishing Microtasks 1 & 2. |
| **Community Bonding** | April 1 – May 4 | Chatting with mentors to finalize the plan and setting up my local dev environment. |

 |**Foundation & Data Pipeline** | Week 1- Week 3 

* **Research**: Documenting the transition from legacy PHP logic to a modern Python REST architecture. I will investigate the specific response schemas of the wbcheckconstraints API to map property types to initial difficulty tiers. 
* **Coding**: I will develop the core Backend Fetcher Module in python.  This Python script will handle the OAuth handshake and securely fetch live violations so that the users can access them and fix the violations according to the constraint.
* **Documentation**: I will be creating a neat documentation of User onboarding guide and a "Developer Readme" for the frontend components. 


 |** The Core of the Game **| Week 4 - Week 6

* **Research**:  I will research the UI/UX responsiveness on mobile devices and make sure the "Apprentice" level fixes are easy and can be done in less than a minute.
* **Coding**: Building the primary user interface in HTML, CSS and React.js for a smooth experience. By the end of this goal, a user should be able to log in, see a Level 1 task, and successfully push a fix to Wikidata.
* **Documentation**: I will create a fronted README.md for easier access of the UI/UX.

**Mid-term Deliverable: ** A simple game with working UI, log-in page and fast level 1 fixes.


 |** XP Engine & Leveling Logic ** | Week 7 - Week 9 


* **Research**:  I will be researching property constraints to sort them into various different level and assign their respective levels.
* **Coding**: In this phase I will build the level-up logic of the game consisting of the increase in the required XP to get to the next level
** **XP required to Level-up to the next level = current level's XP + 15% of current level's XP**
this will increase the difficulty and interest for the user as they fix higher level violations.
* **Documentation**: A comprehensive "Gamification Spec" detailing the math and logic behind the ranking system.


 |** Toolforge Deployment** | Week 10 - Week 12 

* **Research**:  Exploring the** 'Consensus Models'** for **Wikidata**. To ensure high data integrity, I was thinking of implementing a multi-tiered verification system requiring a three-point consensus from low-level contributors for automated commits, while any disputed edits are automatically escalated for High-level contributors review.
* **Coding**: Developing the multi-user verification system. The final week will be dedicated to deploying the entire stack on Wikimedia Toolforge and performing tests and pre-commits.
* **Documentation**: Final GSoC Project Report and a "How to Contribute" manual for future open-source developers.



**Availability & Commitment**
  - **Standard Hours:** 35-40 hours per week.
  - **Exam Strategy:** 
       My exams fall during the transition from Community Bonding to Coding Phase 1. I have scheduled my heavy lifting to begin on June 4th. To compensate for   the exam period, I will be front-loading my research in April so I can be more efficient in June after my exams.

**Additional Information:**
Gerrit: [[ https://gerrit.wikimedia.org/r/q/owner:Raushan31+(status:open+OR+status:merged)| Merged Patches]]
GitHub: [[ https://github.com/Raushan-tryingtocode | Profile]]
Email: raushanh31@gmail.com

**The timeline of this proposal is flexible and will be changed upon consultation with mentors.**





