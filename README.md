# Netflix Data Analysis with DBT & Snowflake

<img width="1390" height="569" alt="image" src="https://github.com/user-attachments/assets/1ca751a9-8018-4ac6-a8bf-7533691573c2" />
<img width="1916" height="963" alt="Screenshot 2025-09-14 at 14 10 47" src="https://github.com/user-attachments/assets/e91a6777-4841-463f-b005-f868536ab4cf" />
<img width="1456" height="863" alt="Screenshot 2025-09-14 at 14 10 05" src="https://github.com/user-attachments/assets/3d3378e2-f446-4172-97a9-38dcce81a907" />

📌 `Project Overview`

This project demonstrates an end-to-end ELT pipeline using Amazon S3, Snowflake, and dbt (Data Build Tool).
We use the MovieLens dataset
 (simulating Netflix ratings and metadata) to:

- Extract and load raw data into Amazon S3.

- Ingest data into Snowflake (Raw Layer).

- Transform data with dbt (Staging & Serving Layers).

- Build analytics-ready tables for BI tools such as Looker Studio, Power BI, and Tableau.

🏗️ `Architecture`

Layers:

- Raw Layer – Direct dump of CSV data from S3 into Snowflake.

- Staging Layer – Clean, structured intermediate models.

- Serving Layer – Final transformed models for analytics & dashboards.

⚙️ `Tech Stack`

- Storage: Amazon S3

- Data Warehouse: Snowflake

- Transformation: dbt (models, snapshots, tests, macros, orchestration)

- Visualization: Looker Studio, Power BI, Tableau

📂 `Repository Structure`

<img width="1216" height="592" alt="image" src="https://github.com/user-attachments/assets/f7371a03-0995-4a85-bacb-e3610b6871ce" />

🚀 `Workflow`

Extract & Load

- Upload CSV dataset to Amazon S3.

- Load into Snowflake Raw Layer using COPY INTO.

- Transform with dbt

- Create staging models for cleaned, structured data.

- Build serving layer models (facts/dimensions).

- Apply dbt tests (e.g., uniqueness, not null).

- Use snapshots to track historical changes.

- Analytics & Visualization

- Run SQL scripts in analysis/ to validate transformations.

- Connect Snowflake to BI tools for dashboards.

📊 `Analyses (from analysis/)`

- Top 20 Movies by Average Rating

- User Engagement Distribution (active vs. inactive users)

- Ratings Over Time (trend analysis)

- Genre Popularity & Tag Insights

🔑 `Key Learnings & Highlights`

- Implemented modern ELT with dbt + Snowflake.

- Learned dbt concepts: models, snapshots, seeds, macros, testing, orchestration.

-  Practiced data quality enforcement with dbt tests.

-  Built analytics-ready layers enabling plug-and-play BI dashboards.

📌 `How to Run`

Clone the repo

git clone https://github.com/yourusername/netflix-dbt-snowflake.git
cd netflix-dbt-snowflake


Install dependencies (inside virtual environment)

pip install dbt-snowflake


Configure your profiles.yml with Snowflake credentials.

Run dbt models

dbt run
dbt test


Explore analysis queries in analysis/ folder.

🎯 `Note`

This project showcases hands-on skills in dbt, Snowflake, SQL, ELT pipelines.
The analysis/ folder contains business-oriented SQL queries simulating how analytics teams derive insights from curated models.
