# U23 Midfielders Scouting: Team vs Individual Defensive Output

A data-driven scouting project designed to identify promising under-23 defensive midfielders in the Premier League. By crossing individual defensive volume with collective defensive solidity, this analysis helps map out different player profiles—from dominant anchor mans to high-exposure "firefighters".

## Project Overview

In football analytics, looking at raw defensive stats (like total tackles) can be misleading. A high number of tackles might just mean a player is constantly out of position or playing in a team under non-stop pressure. 

This project solves that by analyzing two axes:
1. **X-Axis (Individual Volume):** Defensive Actions (Tackles Won + Interceptions) per 90 minutes.
2. **Y-Axis (Collective Solidity):** Team Goals Conceded per 90 minutes while the player is on the pitch (Inverted, so better teams are at the top).

### Key Methodology & Data Cleaning
* **Data Source:** FBref via `soccerdata` scraping pipeline.
* **Anti-Garbage Time Filter:** To eliminate tactical substitutes who only play when the match is already settled, a strict threshold was applied: **Players with >45 minutes per game and >=500 total minutes in the season**.
* **Data Flattening:** Handled complex Pandas MultiIndex column structures to clean, merge, and rename defensive and playing-time metrics smoothly.

---

## Scouting Insights

<img width="1143" height="689" alt="U23 midfielders" src="https://github.com/user-attachments/assets/4df99c6d-8aff-4bc7-8b56-573fc34dcaff" />

### Key Findings:
* **The Elite Outlier:** **Tim Iroegbunam** completely detaches from the pack, showing an absurdly high defensive volume (~4.0 actions/90) while maintaining top-tier collective solidity.
* **The Defensive Anchors:** Players like **Moisés Caicedo** and **Mateus Fernandes** show immense individual work rates but operate in systems that leave them exposed, resulting in a higher rate of goals conceded.
* **The Positional/Sustained Profiles:** Highly technical or positional players (e.g., **Florian Wirtz**, **Rayan Cherki**, **Nico O'Reilly**) naturally drift to the top-left quadrant—low individual tackling volume but protected by dominant team possession.
* **The Firefighters (High Exposure):** **Soungoutou Magassa** and **Oliver Scarler** have an amazing defensive output, but their teams have a high rate of goals conceded.
---

## Tech Stack & Libraries

* **Python 3.12.13**
* **Pandas** (Data manipulation and MultiIndex flattening)
* **Matplotlib & Seaborn** (Advanced data visualization, custom gridlines, editorial design)
* **Soccerdata** (FBref scraper pipeline)

---

## How to Run the Project

1. Clone the repository:
   ```bash
   git clone https://github.com/luipmesquita/U23-Midfields-in-Premier-League-Defensive-Output.git
