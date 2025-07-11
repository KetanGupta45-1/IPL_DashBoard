🔒 Due to the custom modeling and proprietary DAX logic used in this project, I’ve chosen not to share the .pbix file. However, detailed screenshots and a walkthrough video are provided to showcase the dashboard’s structure and insights.


📊 IPL Stats Dashboard — Power BI Project
An interactive and slicer-driven Power BI dashboard designed to analyze IPL performance data at a granular level. The project focuses on delivering deep player and team analytics not readily available on the internet.

🔍 Why This Project Matters
Most public IPL stats only show season-wise or match-level aggregates.

No platform allows users to easily analyze:

How a batsman performs vs specific teams or bowlers

How a bowler performs vs a specific team or batsman

How teams compare across phases, seasons, or match conditions

This dashboard provides a custom, in-depth analysis platform using ball-by-ball data and advanced filtering.

✅ What This Project Delivers
A complete IPL data model using Power BI + DAX + Power Query

Granular statistics at batsman vs bowler, team vs team, and match-phase levels

Dynamic KPI cards and visuals that update based on:

Selected player, team, opponent, season, and over phase

Visual storytelling with slicers and bookmarks — optimized for analyst or fan exploration

🎯 Project Objectives
The primary objective of this project is to create an in-depth, interactive IPL performance analysis dashboard that empowers users to explore granular statistics and answer complex cricketing questions. This dashboard goes beyond traditional summaries and enables multi-dimensional analysis using dynamic filters and DAX-based metrics.

🔧 Specific Goals
Provide a comprehensive year-wise overview of IPL performance for teams, batsmen, and bowlers.

Enable “My Team” vs “Opponent Team” comparison across different seasons and match conditions.

Allow batsman-centric analysis:

vs specific bowlers

vs specific opponent teams

across selected seasons and match phases

Enable bowler-centric analysis:

vs specific batsmen

vs specific teams

with filters for over phase, year, and innings

❓ Key Questions Answered
How has a specific batsman performed against a team or bowler over multiple seasons?

Which bowlers have consistently troubled a certain batsman?

How does a team perform when batting vs bowling first, or across different over phases?

Which players dominate during powerplays or death overs?

What are the average metrics for selected player/team filters?

📈 Metrics Tracked (Depending on Role)
Batting: Runs, 4s, 6s, Strike Rate, Average, Dot Ball %, Boundary Count

Bowling: Wickets, Economy Rate, Average, Strike Rate, Dot Ball %, 4s/6s conceded

Team: Total Runs, Wickets Lost, Toss Win %, Bat First/Bowl First Outcomes


🗂️ Dataset Details & Data Transformation
This project uses structured, ball-by-ball match data from Cricsheet.org to build a comprehensive IPL performance analysis dashboard. The raw data, in JSON format, was converted, transformed, and modeled entirely within Power BI using Power Query and DAX.

📥 Data Sources
Raw Input: JSON match files from Cricsheet

Derived Files (via transformation in Power BI):

Match_Data – delivery-level facts including player, over, and outcome details

Match_Summary – match-level metadata including date, venue, teams, result, toss

Manual lookup tables for:

BattingStyleFilter – maps batsman to batting style

Bowling_Style – maps bowler to bowling type

🔄 Data Preparation & Cleaning (Handled in Power Query)
All data preparation was done in Power BI's Power Query Editor, including:

Parsing nested JSON structure into flat delivery-level rows

Filling missing match numbers manually for consistency

Standardizing:

Stadium names across different matches

Team names across different seasons

Creating and merging custom CSVs to enrich player information:

batter → batting style

bowler → bowling style

🧠 Modeling & DAX-Based Transformations
After loading and cleaning, extensive transformations were applied using DAX and calculated columns:

Created Over Phase tags (Powerplay, Middle, Death)

Added flags for:

Is Legal Delivery, Is Wicket, Is Dot Ball, Is Boundary

Created cumulative columns:

Runs by batsman, runs conceded by bowler, team runs

Built disconnected slicer tables:

Teams, OpponentTeams, BatsmanStats, BowlerStats

Added performance metrics:

Economy Rate, Batting Average, Bowling SR, Strike Rate, etc.

Established a star schema model for optimized performance and slicer interaction

📊 Final Power BI Model (Snapshot)
Your data model includes the following major tables (see screenshots above):

Match_Data_08-25: Core delivery facts

Match_Summary: Match-level metadata

Calender_Table: Year/date slicer

BatsmanStats, BowlerStats: Player-wise statistics

Teams, OpponentTeams: For comparative slicers

VenueTable, Bowling_Style, BattingStyleFilter, InningsSummary

Each table was designed to support dynamic KPIs, cross-filtering, and custom visual interactions.

🖼️ Dashboard Structure & Features
The dashboard consists of 4 interactive pages, each focused on a specific layer of IPL performance analysis. Slicers across all pages allow for dynamic filtering by Season, Teams, Striker (Batsman), and Bowler, enabling targeted insights.

📌 Page 1: IPL Yearly Analysis
A season-wise summary dashboard showing standout performers and key stats for each IPL year.

Key Features:

Orange Cap (Most Runs), Purple Cap (Most Wickets)

Best batting average, strike rate, economy rate

Most 4s, 6s, lowest team score, highest team score

Player and team rankings by performance

Filterable by season (Year slicer)

📌 Page 2: Your Team vs Opponent Team Over Years
Compare head-to-head performance between any two teams across multiple seasons.

Key Features:

Matches won/lost by your team

Toss outcome vs match result

Win stats when batting first or bowling first

Top scorers and wicket-takers in the rivalry

Slicers: Your Team, Opponent Team, Year

📌 Page 3: Batsman vs Bowler / Opponent Team
Analyze a batsman’s performance across specific bowlers and/or teams.

Key Features:

Runs scored, strike rate, average, 4s, 6s

Performance broken down by selected seasons and opponents

Compare performance vs different bowling styles

Slicers: Striker (Batsman), Bowler, Opponent Team, Year

📌 Page 4: Bowler vs Batsman / Opponent Team
Evaluate a bowler’s effectiveness against different batsmen or teams across selected seasons.

Key Features:

Wickets taken, economy rate, average, strike rate

Dismissals by batsman, opponent team, and over phase

Bowling style vs batting style trends

Slicers: Bowler, Striker (Batsman), Opponent Team, Year

🧠 Additional Interactive Features
Disconnected slicers for team/player comparisons

Conditional formatting on KPIs and tables

Custom calculated measures for dot ball %, boundary %, and match-phase-based performance

Dynamic visuals that respond instantly to multiple filters

 Analytical Insights
Batting performance varied significantly by bowling style — some batsmen performed better against pace, while struggling against spin, and vice versa.

Players demonstrated venue-specific strengths and weaknesses, indicating that ground conditions influenced batting and bowling outcomes.

Teams showed consistent performance patterns against specific opponents — with some rivalries favoring one side strongly when batting or bowling first.

Bowler vs Batsman dynamics revealed clear matchups, where certain bowlers consistently outperformed or contained key batsmen.

Certain teams consistently struggled during specific over phases (e.g., death overs) across seasons — highlighting tactical weaknesses.

🧠 Technical Learnings
Built a flexible data model using disconnected slicers to allow team-to-team and player-to-player comparisons.

Used Power Query for heavy preprocessing of nested JSON into a usable star schema.

Developed complex DAX measures to compute contextual KPIs like dot ball %, economy rate, and performance by over phase.

Learned to manage data inconsistency across seasons by standardizing names, formats, and enriching missing attributes manually.

🛠️ Tools & Skills Used
🧩 Tools & Technologies
Power BI Desktop – Data modeling, visual design, KPI development

Power Query Editor – JSON parsing, data cleaning, transformation

DAX (Data Analysis Expressions) – Custom measures, dynamic filtering, time intelligence

Cricsheet JSON Data – Raw IPL ball-by-ball match data

🧠 Core Skills Demonstrated
End-to-end data transformation using Power Query (no external scripts)

Building a star schema model optimized for cross-filtering and performance

Designing and using disconnected slicers for comparative views (Team vs Opponent, Player vs Player)

Creating advanced DAX measures for:

Strike Rate, Economy Rate, Dot Ball %, Boundary Count, Cumulative Runs/Wickets

Match-phase tagging (Powerplay/Middle/Death overs)

Building multi-page dashboards with page navigators, conditional formatting, and slicer interactions

Handling data inconsistencies and enrichment manually (venue/team/player standardization)

