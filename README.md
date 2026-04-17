🎬 Netflix Content Intelligence Dashboard


An interactive 3-page business intelligence dashboard analyzing 8,800+ Netflix titles to uncover content strategy patterns, global distribution trends, and audience targeting insights.


Tools: Power BI Desktop · DAX · Power Query
Dataset: Netflix Movie and TV show dataset by Shivam Bansal - Kaggle
Author: Adarsh Pandey

📊 Dashboard Pages


Page 1 — Overview
High-level snapshot of Netflix's entire catalog with KPI cards, content type distribution, yearly growth trends, and top producing countries.
Show Image

Visuals:

<img width="1330" height="769" alt="image" src="https://github.com/user-attachments/assets/a3dddd33-d159-4426-b799-767bc3edbadc" />


4 KPI Cards — Total Titles (9K), Total Movies (6K), Total TV Shows (3K), Avg Movie Duration (99.59 min)
Donut Chart — Movies (69.6%) vs TV Shows (30.4%) content split
Line Chart — Year-wise content addition from 2010 to 2021 with separate lines for Movies and TV Shows
Horizontal Bar Chart — Top 10 content-producing countries by number of titles


Page 2 — Content Deep Dive
Detailed breakdown of what type of content Netflix produces and how it is distributed across genres, ratings, duration, and time.
Show Image

Visuals:

<img width="1326" height="763" alt="image" src="https://github.com/user-attachments/assets/612ad596-0c44-4843-83e4-5d5299aa33bc" />


Treemap — Top 15 genres with Dramas & International Movies leading at 362 titles, followed by Documentaries (359) and Stand-Up Comedy (334)
Column Chart — Content ratings distribution showing TV-MA as the dominant rating (~3K titles), confirming Netflix's adult-focused content strategy
Histogram — Movie duration distribution showing 91–120 min as the most common runtime bucket
Matrix Heatmap — Monthly content addition patterns across all years showing seasonal upload trends


Page 3 — Director & Global Insights
Deep dive into the people and geographies behind Netflix's catalog.
Show Image

Visuals:

<img width="1324" height="766" alt="image" src="https://github.com/user-attachments/assets/f23ce1ca-a4bb-446b-9eeb-8dcadb822d9f" />




Bar Chart — Top 10 Directors by number of titles (Zoya Akhtar leading among filtered results)
Bar Chart — Top 10 Cast Members by appearances across the catalog
Filled Map — Global content distribution showing USA and India as the dominant production hubs, with strong coverage across Europe and East Asia


🔍 Key Business Insights

Movies dominate at 69.6% but TV Shows are growing faster post-2019 — Netflix is investing in serialized content to improve subscriber retention
Explosive growth between 2016–2019 — content additions grew from ~250 titles/year to 1,400+/year, reflecting the peak of the global streaming war
USA leads with 2,817 titles — but India (972) ranks a strong second, showing Netflix's aggressive push into South Asian markets
Dramas and International content top the genre chart — Netflix's biggest differentiator is non-English original content, not just Hollywood productions
TV-MA is the most common rating (~3K titles) — Netflix's core demographic is adults 18+, and the platform consistently targets mature storytelling
Average movie runtime is ~99 minutes — aligned with standard cinema expectations, suggesting Netflix movies are built for the same audience as theatrical releases
Content additions peak in Q4 (Oct–Dec) — strategic timing to maximize subscriber acquisition during the holiday season


🛠️ Technical Details
Data Preparation (Power Query)

Handled ~30% missing values in director column by replacing nulls with "Unknown Director"
Parsed date_added column into year, month number, and month name using Date functions
Created duration_value and duration_unit derived columns by splitting the duration text field
Created duration_bin calculated column for histogram bucketing (0–60, 61–90, 91–120, 121–150, 150+ min)

DAX Measures Created

Total Titles — COUNTROWS

Total Movies — CALCULATE with type filter

Total TV Shows — CALCULATE with type filter

Movies % — DIVIDE measure

TV Shows % — DIVIDE measure

Avg Movie Duration — CALCULATE + AVERAGE filtered to movies in minutes

Added in 2021 — CALCULATE with year filter

YoY Growth % — VAR-based year-over-year calculation using DATEADD




📄 Dataset Credit
Netflix Movies and TV Shows by Shivam Bansal.

Thank you Shivam Bansal Sir for providing such a valuable Dataset.
