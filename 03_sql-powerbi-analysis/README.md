# Customer Service Agent Performance Analysis
## Project Overview

This project visualizes customer service agent performance using productivity and efficiency metrics. The goal is to understand workload distribution.

The data was structured in SQL and visualized in Power BI to deliver a clear, interactive performance report.

Output: 

## Dataset.

The analysis uses an agent-level dataset with the following metrics:

AgentName

Tickets Closed — measure of productivity

Average Resolution Time (Hours) — measure of efficiency

Average Customer Satisfaction Score (CSAT)

Performance Quadrant — categorizing agents based on productivity × efficiency

The Performance Quadrant was calculated in SQL, reflecting the strategic understanding of who drives performance and who needs support.

The link below leads to my Google Drive, where you will find a folder containing;
1. Customer Service data (Only Agent and Team Performance was used here)
2. SQL Power BI report (showing KPIs and charts)

   Link 🔗 [Google Drive Folder](https://drive.google.com/drive/folders/1iQGRdqae2dy-rh1cUWNqd5nLfuXqdlpC?usp=drive_link)

## Data Preparation & Modeling

- Extracted and consolidated agent performance data using SQL

- Calculated Performance Quadrants to define agent segments

- Imported the cleaned dataset into Power BI

- Created key measures for dynamic KPIs: Total Tickets, Avg Tickets per Agent, Avg Resolution Time, Total Agents

## Key Metrics

The report highlights critical KPIs that management relies on:

- Total Agents

- Total Tickets Closed

- Average Tickets per Agent

- Average Resolution Time

## Visual Analysis
#### 1. Agent Productivity vs Resolution Efficiency

A scatter plot compares Tickets Closed against Average Resolution Time, with agents grouped by Performance Quadrant.

This visual immediately highlights:

Performance Quadrant appearance.

#### 2. Agent Distribution by Performance Quadrant

A bar chart shows the number of agents in each performance quadrant, giving a concise view of team composition and operational strengths/weaknesses.

This visual immediately highlights:

Performance Quadrant agent count

## Key Insights

- High-performing agents are clearly identifiable.

- Some agents deliver high volume but slower resolution, highlighting potential coaching opportunities.

- Visually, agent performance does not form distinct clusters, indicating heterogeneous behavior across the team. However, when the data is segmented using the average        number of tickets closed as a threshold, most agents fall within the average and above-average workload ranges. This suggests that high workload is the dominant             operational state rather than an exception.


## Tools & Workflow

SQL: Data extraction, consolidation, and quadrant calculation

Power BI: Data modeling, DAX measures, and interactive visualization

**This project showcases my ability to:**

- Transform raw operational data into strategic insights

- Apply analytical reasoning to highlight meaningful patterns

- Build clean, purposeful Power BI reports

- Communicate results in an actionable format
