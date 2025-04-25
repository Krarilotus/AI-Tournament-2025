# Stronghold Crusader AI Tournament 2025 - Official Rules & Setup

## Overview

This tournament challenges modders to create compelling AI characters that compete in various scenarios. Participants submit teams of two complementary AIs, which are then evaluated through individual challenges and team-based combat. The goal is to create not only effective AIs but also engaging characters with distinct personalities and strategies, all operating within the framework established by the tournament plugin.

## I. Setup & Starting Resources

* **Mandatory Plugin:** All participants must install and use the official **AI-Tournament-2025** plugin to create their AIs. This ensures consistent starting conditions and provides necessary files for AI opponents.
* **Standard Match Resources (Phase 2 - FFA/2v2):** Unless specified otherwise, the **Normal Game** starting conditions are used as configured in the plugin:
    * Gold: 2000
    * Wood: 100
    * Stone: 50
    * Food: 60 Bread
* **Note:** The Economic and Defensive Gauntlets in Phase 1 the **Deathmatch** and **Crusader Game** starting conditions respectively, as detailed in Section IV.

## II. Participant Submissions: AI Teams

Each participant (or participating duo) must submit a **team of two AI characters**. It is encouraged to fit their AI castles to complete each other on those maps, that provide very close starting locations.

* **Complementary Design:** The two AIs within a team should be designed to complement each other strategically.
* **Character Assets:** Each *individual* AI character requires:
    * **At least three unique `.aiv` (AI Village) files**. These multiple `.aiv` files will be autoamtically chosen on the different Skirmish maps based on the map layout by the default AI choice. They must fit in the provided AIV template.
    * An **`.aic` (AI Character) file**
    * Unique **portrait, video (`.bik`), lines and speech files**. These assets should portray the character's personality and are integrated using the AI Swapper extension within the UCP.

## III. AI Team Restrictions

### A. Building & Troop Exclusivity

* **Exclusive Buildings:** Apart from Walls, Crenellations, Stairs, Stockpiles, Granaries, recruitment buildings (Engineers’ Guild, Mercenary Post, Barracks), the Marketplace and Houses—​which both AIs may construct—​**all other building types are exclusive to one partner**. If one AI places a particular building type (e.g., a specific tower design or any Gatehouse), its partner AI **may not** place the same type.  
  * *Note:* This exclusivity applies only to buildings placed via the `.aiv` files; buildings generated through the `.aic` file are exempt and may be used by either AI.
* **Housing Limit:** The **total** number of houses built by **both** AIs in a team combined cannot exceed **17**.
* **Exclusive Troop Types:** Troop types are also exclusive between partners. If one AI recruits a specific troop type (e.g., Archers, Pikemen), the other AI cannot recruit that type.
    * *Note:* Engineers are excluded from this role!

### B. Wall Defense Limit ("WallDef")

* A team's combined defensive troop presence on walls and towers is limited to **160 WallDef points** total.
* **Troop Costs:**
    * Fire Throwers: **6 points** each
    * Crossbowmen: **3 points** each
    * Arabian Archers: **2 points** each
    * European Archers: **1 point** each
    * Armored Melee (Arabian Swordsmen, Swordsmen, Pikemen, Knights): **1 point** each
    * Slingers, Macemen, Assassins: **0.5 points** each
    * Other Non-Armored Melee (Spearmen, Slaves): **0.25 points** each
* **Defensive Siege Engine Costs (Base):**
    * Tower-mounted Ballistae/Mangonels: **5 points** each
    * Ground Fire Ballistae: **5 points** each
    * Ground Trebuchets: **3 points** each
* **Escalating Siege Engine Cost:** The cost for defensive siege engines increases cumulatively for the team. The Nth defensive siege engine placed by the team (regardless of type - tower or ground) costs its **Base Cost + (N-1)** points.
    * *Example:* A team places 2 Ground Fire Ballistae and 3 Tower Ballistae (total 5 defensive siege engines). The *next* defensive siege engine they place, for instance a Ground Trebuchet (base cost 3), would cost 3 + 5 = **8 WallDef points**.
* **Harassing Siege Engines:** The number of harassing siege engines an AI is allowed to build is limited to the number of *defensive* siege engines it has placed plus 1.

* **Note on WallDef Calculation:** Defense troops recruited by an AI are typically based on the ratios defined in the `.aic` file's defense troop slots. Arbiters may review these ratios. For example, if an AI rarely builds Barracks but fills 7/8 defense slots with Archers and 1/8 with late-game Fire Throwers, tests might show Fire Throwers constitute a higher *actual* percentage of the WallDef points than 1/8 suggests. If testing (e.g., on the economic map) reveals a team significantly exceeds the 120 WallDef budget due to such recruitment timings and ratios, arbiters may adjust the effective WallDef calculation or impose penalties.

### C. Starting Troops Limit

* Each **team** has a maximum budget of **30 points** (using WallDef costs) for selecting starting troops across both AIs. This budget is configured via the plugin or pre-match setup.
* **Defensive Challenge Exception:** For the **Defensive Challenge setup only** (Phase 1), the team shares a larger starting troop budget of **150 points**. This budget is used when configuring the starting troops for this specific challenge scenario, even though only one AI runs the challenge at a time.
* **Escalating Cost for Ranged Units:** Each *ranged* unit added to the starting army selection increases the cost of *subsequent ranged units*. The added cost equals the **sum of the base costs** of all previously added ranged units.
    * *Example 1:* 2 European Archers (1pt base), 1 Crossbowman (3pt base).
        * Archer 1: Cost 1. (Running penalty = 0)
        * Archer 2: Cost 1 (base) + 1 (penalty from Archer 1) = 2. (Running penalty = 1+1 = 2)
        * Crossbowman 1: Cost 3 (base) + 1 (penalty from Archer 1) + 1 (penalty from Archer 2) = 5.
        * Total Cost = 1 + 2 + 5 = **8 points**.
    * *Example 2:* 2 Crossbowmen (3pt base).
        * Crossbowman 1: Cost 3. (Running penalty = 0)
        * Crossbowman 2: Cost 3 (base) + 3 (penalty from Crossbowman 1) = 6.
        * Total Cost = 3 + 6 = **9 points**.
    * *Example 3:* 2 Arabian Swordsmen (1pt base, melee), 2 Slingers (0.5pt base, ranged), 1 Fire Thrower (6pt base, ranged).
        * A. Swordsman 1: Cost 1. (Running penalty = 0)
        * A. Swordsman 2: Cost 1. (Running penalty = 0)
        * Slinger 1: Cost 0.5. (Running penalty = 0)
        * Slinger 2: Cost 0.5 (base) + 0.5 (penalty from Slinger 1) = 1. (Running penalty = 0.5 + 0.5 = 1)
        * Fire Thrower 1: Cost 6 (base) + 0.5 (penalty from Slinger 1) + 0.5 (penalty from Slinger 2) = 7.
        * Total Cost = 1 + 1 + 0.5 + 1 + 7 = **10.5 points**.

### D. Exploit Prevention

* No placing troops in unattackable locations.
* No constructing excessively long or abusive pitch traps.
* General fair play is expected. Avoid abusing game mechanics, such as building nearly closed gatehouses in hard-to-reach spots, creating moat labyrinths solely for pathfinding abuse, or excessive static pitch usage unrelated to reasonable defense.

## IV. Tournament Structure

The tournament proceeds in two main phases, followed by a subjective judging phase.

### Phase 1: Individual AI Gauntlet

**This phase tests each AI character individually; the team partner AI is not present.** Scores for each challenge are scaled from 0 to 10, rounded to the nearest integer. Scores are recorded across all challenges for each AI, typically presented together. The scaling is normalized based on performance across all participants in that specific challenge: the best performance receives 10 points, the worst receives 0 points, and others are scored proportionally.

* *Normalization Example:* In the Defensive Challenge, the worst AI survived 15 years, while the best survived the full 50 years. An AI surviving 40 years would score: `round(((40 - 15) / (50 - 15)) * 10) = round((25 / 35) * 10) = round(7.14) = 7 points`.

* **Challenge 1: Economic Gauntlet - "The Barren Boom"**
    * *Objective:* Achieve the highest economic score within the time limit.
    * *Map:* `ChallengeMap_Eco_v1.map` (Example Name) - Features scarce starting resources.
    * *Opponents ("Economy Challenge Lords"):* Multiple rich, heavily defended AI opponents ("Fortified Neighbors") who are largely passive but launch small, periodic harassing attacks (especially arsonists) targeting the player AI's economy. Direct assault on them is discouraged.
    * *Time Limit:* **30 Years** (in-game time).
    * *Starting Conditions (Based on "Deathmatch Game" setup):* Resources: 400 Gold, 50 Wood, 0 Stone, 30 Food (15 units Bread, 15 units Fruit). Starting troops budget: 20 points (per AI).
    * *Scoring Parameters:* Score = `(Total Value of Placed Buildings (by cost goods sell price)) + (Total Gold Earned / 5) - (Number of Buildings Lost to Harassment * 10)`.

* **Challenge 2: Defensive Gauntlet - "Rampart Resilience"**
    * *Objective:* Survive the longest against relentless attackers.
    * *Map:* `ChallengeMap_Def_v1.map` (Example Name) - Features a designated keep area needing fortification, largely surrounded by opponents.
    * *Opponents:* Aggressive Wolf (by Krarilotus), Lord Stauten (by Monsterfish), Alexios IV (by Nevikov), Apex Marshal (by Xander10alpha), and Emira (by Crusader Pilaw). These AIs start with more gold and apply constant pressure.
    * *Time Limit:* Max **50 Years** (in-game time), or until the AI's Lord died.
    * *Starting Conditions (Based on "Crusader Game" setup):* Resources: 1500 Gold, 100 Wood, 100 Stone, 125 Food (50 Bread, 25 Fruit, 25 Cheese, 25 Meat). Starting troops budget: 150 points (shared team budget for setup).
    * *Scoring Parameters:* Survival time (Years and Months). Reaching the 50-year limit guarantees a high score.

* **Challenge 3: Offensive Gauntlet - "Shatter the Alliance"**
    * *Objective:* Eliminate all enemy lords as quickly as possible.
    * *Map:* `ChallengeMap_Off_v1.map` (Example Name) - Features multiple enemy castles with scarce resources, while providing the applicant AI a resource-rich and easily defensible starting position.
    * *Opponents:* Lord Stauten (by Monsterfish), LotO Pig (by Crusader Pilaw), Alexios IV (by Nevikov), Aggressive Sultan (by Krarilotus), Slave Trader (by Tobbi), Apex Caliph (by Xander10alpha).
    * *Time Limit:* Max **50 Years** (in-game time), or until all 6 enemy lords are defeated.
    * *Starting Conditions (Based on "Normal Game" setup):* Resources: 2000 Gold, 100 Wood, 50 Stone, 60 units (Bread). Starting troops budget: 20 points (per AI).
    * *Scoring Parameters:* Score = `Number of Kills * Sum(10 / Time_to_Kill_N)` for each enemy N killed. Time is measured in years.
        * *Example:* An AI gets 2 kills, the first after 10 years, the second after 12 years. Score = `2 * ( (10 / 10) + (10 / 12) ) = 2 * (1 + 0.833) = 3.67`. An AI with 0 kills scores 0. Achieving more kills faster yields higher scores.

* **Phase 1 Team Scoring:**
    * The **team's** score for Phase 1 is calculated by **multiplying** the normalized total scores (0-30) of the two individual AIs.
    * *Example:* AI 'A' achieves a normalized total of 17 points across the 3 challenges. AI 'B' achieves 18 points. Team score = 17 * 18 = **306 points**.

### Phase 2: Team Battles

Teams compete directly against each other using standard match settings (see Section I), managed by the plugin setup. Assumes 8 teams participate.

* **Format 1: Free-For-All (FFA)**
    * *Structure:* Two initial 8-player FFAs with random seeding. Top 4 finishers (1st/2nd from each initial FFA) advance to a "Winners' Final FFA". Bottom 4 finishers compete in a "Consolation Final FFA". (4 FFA matches total). Expect intense battles with shifting alliances and potential backstabbing.
    * *Scoring:* Points awarded based on final placement in the Winners' and Consolation Finals (1st=100, 2nd=90... 8th=30). **Plus 10 points** per enemy AI kill secured by the team in *any* of the four FFA matches.

* **Format 2: 2v2 Swiss Tournament**
    * *Structure:* Teams compete in 2v2 matches using a Best-of-3 games format. A 3-round Swiss system is used, with initial seeding based on FFA results. Tests teamwork and adaptability across potentially different maps per round. (12 matches total played: 4 matches per round * 3 rounds).
    * *Scoring:* **40 points** per Best-of-3 match victory. **+10 points** per *match* awarded to the team with the most combined gold earned across all games played (up to 3) in that specific match-up. **+20 points** per *Swiss round* awarded to the team that destroyed the most buildings *within their specific match* during that round (compared across the 4 matches of the round).

* **Format 3: Sudden Death Gauntlet - "The Tri-Force Trial"**
    * *Structure:* A challenging multi-stage scenario run individually by each **team**, testing coordination and performance under pressure. Takes place on `ChallengeMap_SuddenDeath_v1.map` (Example Name) featuring distinct zones and pre-placed enemy AI factions. Each team attempts this gauntlet once.
    * *Setup Overview (Refer to setup image):*
        * Each team assigns one AI as the 'Defender' and one as the 'Attacker'. The primary goal is to earn 'Trophies' by completing objectives over the 50-year match duration.
        * There are three enemy factions (totaling five enemy AIs) one of which is a central dummy Sultan. One faction focuses on harassing the applicant team's Defender. Another faction competes with the applicant team's Attacker to kill the Sultan.
    * *Trophies to Earn (Scoring up to 50 points per category):*
        * **Aggressive Trophy (Max 50 pts):** Awarded for securing the kill on the Sultan. Points are based on the time taken relative to other teams: the fastest kill gets 50 points, the slowest kill gets 25 points. Failing to kill the Sultan yields 0 points in this category.
        * **Defensive Trophy (Max 50 pts):** Awarded if the team's Defender survives the full 50 years. Base score for survival is 25 points. Bonus points (up to 25 additional, for a total of 50) are awarded based on the number of enemy troops killed *by the defending AI*, minus the amount of troops killed by the attacking AI. Hence the best Difference gets 25 extra points, the worst 0. 0 Points in total if the defender Ai dies before the 50 years pass.
        * **Economic Trophy (Max 50 pts):** Calculated at the end of 50 years. Score is based on the team's "Gold per Capita" (`Total Team Gold / Combined Team Population`) compared to the Gold per Capita of the two non-Sultan enemy factions. If the applicant team's ratio is higher than both enemy factions, they score a minimum of 25 points. The larger the difference, the higher the score, up to a maximum of 50 points.
    * *The Catch:* Before the gauntlet runs, all applicant teams may vote on tactical priorities for the pre-placed enemy factions, choosing from the opponents teams. However, each enemy team can only be chosen once for the different challenger positions, giving the priority for choice to those teams who had the lowest scores so far.

## V. Subjective Judging: Immersion & Storytelling

* **Points:** A total of **1000 points** are allocated based on Caster and Viewer votes.
* **Criteria:** Votes are cast for the AI team deemed most immersive, well-characterized, and entertaining throughout the *entire* tournament. Considerations include AI personality (as conveyed through assets and behavior), visual design (castles, portrait), voice lines, strategic choices, and overall narrative potential.
* **Distribution:** The 1000 points are distributed proportionally based on the number of votes each team receives.

## VI. Final Score

The final tournament ranking is determined by the sum of points earned across all phases.

### VI.A Example Score Calculation (Hypothetical Team "Alpha")

This example illustrates how a team might score with solid but not perfect performance:

* **Phase 1 (Individual Gauntlet):**
    * AI Alpha-1 scores: 3 (Eco) + 8 (Def) + 1 (Off) = 12 points (normalized total)
    * AI Alpha-2 scores: 7 (Eco) + 3 (Def) + 7 (Off) = 17 points (normalized total)
    * Phase 1 Team Score = 12 * 17 = **204 points**
* **Phase 2 (Team Battles):**
    * FFA: Places 4th in Winners' Final (70 pts) + eliminates 4 opponents (4 * 10 = 40 pts) = **110 points**
    * Swiss: Wins 2/3 matches (2 * 40 = 80 pts), gets 'Most Gold' once (+10 pts), gets 'Most Buildings Destroyed' once (+20 pts) = **110 points**
    * Sudden Death: Defender survives, gets moderate kills (35 pts Defensive). Team fails to kill Sultan (0 pts Aggressive). Achieves good Gold per Capita relative to opponents (40 pts Economic). Total = 35 + 0 + 40 = **75 points**
* **Subjective Judging:**
    * Receives a decent share of votes = **161 points** (out of 1000 total)
* **Total Score for Team Alpha:** 204 + 110 + 110 + 75 + 161 = **660 points**

*(Note: Scores can vary significantly. Top teams might exceed 1000 points, while others might struggle to break 500. Maximum possible score is 900 (P1) + 220 (FFA) + 210 (Swiss) + 150 (SD) + 1000 (Subj) = 2480 points, which is practically unattainable).*

Good luck to all participants! Ensure the AI Tournament Plugin is correctly installed and configured according to instructions and visual guides.
