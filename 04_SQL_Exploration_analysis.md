# Case Ticket Management & Agent Performance 

### SQL Data Exploration & Analysis

## Project Overview

This project explores a **case and ticket management system** to understand how tickets are created, updated, categorized, and resolved,
and how **agent performance influences resolution efficiency**.

The goal of this is **structured data exploration**:
asking the right questions, establishing benchmarks, identifying patterns, and translating SQL outputs into operational insights.

The project demonstrates my ability to:

1. Explore unfamiliar datasets independently
2. Reason from raw SQL outputs
3. Connect multiple tables
4. move from observation to insight, even without prior industry experience

## Tools & Technologies

1. Aggregation functions: COUNT, SUM, AVG, MIN, MAX
2. GROUP BY, ORDER BY
3. Conditional logic using CASE
4. Subqueries and CROSS JOIN for benchmarks 
5. Temporary tables for reusable analysis (SELECT INTO Logic)
6. Logical joins (e.g., ProductID → ProductName)
7. SQL (SQL Server–style syntax)

The data was already in a clean state; no additional trimming or string cleaning was required.

## Dataset Description

This exploration and analysis uses **four related tables**:

## 1. Case_Ticket_Management_TicketLogCSV
**Columns:**
TicketID, CustomerID, AgentID, ProductID, Channel, Priority, Status, DateCreated, DateClosed, ResolutionTime_Hours, FirstResponseTime_Hours

## 2. Case_Ticket_Management_TicketTagsCSV
**Columns:**
TaggingID, TicketID, Tag

## 3. Case_Ticket_Management_Details_UpdateCSV
**Columns:**
DetailID, TicketID, UpdateTimestamp, UpdateText

## 4. Agent_Team_PerformanceCSV
**Columns:**
AgentID, AgentName, TicketsClosed, AverageResolutionTimeHours, Average_CSAT_Score

## Analysis Breakdown

## 1. Ticket Lifecycle & Operations (Ticketlogs)

**SQL file:** ticket_logs_analysis.sql

**My Thinking:**

I started by exploring the ticket log to understand the overall system behavior. Before slicing by channel, priority, or product, I wanted to know:

- What are my columns, and what is in them
- How long do tickets take to resolve
- How ticket lifecycles look in practical terms (days open)

This baseline guided the rest of my analysis.

**My Approach:**

- Calculated total tickets, minimum, average, and maximum FirstResponse and Resolution times.
- Converted resolution times into ticket lifecycle duration (days) to validate operational impact.
- Filtered to only Resolved and Closed tickets for meaningful resolution metrics.
- Broke down by channel, then priority within channel, then priority independently.
- Categorized resolution times into Fast / Average / Slow to see patterns beyond averages.
- Added ProductID to understand if certain products generate more workload or take longer to resolve.
  (To add the product name, I used **join** to the product master table)
  
**My Finding:**

- Total tickets analyzed: 1,000 (384 with resolution not null; 201 resolved)
- Average first response time: 2 hours
- Average resolution time: 178 hours (7 days)
- Ticket lifecycle duration: min 0 days, max 14 days, avg 7 days
- Channel patterns:
  Resolution time is similar across channels; Chat is slightly faster (158 h), Email (176 h), Phone (177), WebForm (210 h).
- Priority patterns: High/Urgent tickets exist in all channels; priority does not consistently shorten resolution time
- Resolution distribution: Slow resolutions dominate across channels, priorities, and statuses
- Product-level: Products have similar ticket counts and average resolution times, with differences between 1–8 hours

**Insights:**

- The system responds to tickets quickly, but resolution is the main holdup — delays happen after initial acknowledgment
- Resolution speed is influenced more by channel and product than by priority labels alone
- Slow resolution is systemic, not isolated to specific channels, priorities, or products

**Interpretation:**

Priority labels, including “Urgent,” do not guarantee faster resolution. 
This indicates capacity rather than flaws in prioritization logic

## 2. Ticket Tag Usage & Coverage (TicketTags)

**SQL file:** ticket_tags_analysis.sql

**My Thinking:**

I explored ticket tags to understand how tickets are categorized and whether tagging adds insight. I checked overall tag usage and compared total tag counts to unique ticket counts to see if tickets have multiple tags applied.

**Key Findings:**

- All Tags are within the same range Counts. billing(297), feature_request(308), bug_report(310), refund(315), urgent(321), shipping(327)
- Unique ticket counts per tag are slightly lower than total tag counts billing(269), feature_request(281), bug_report(282), refund(289), urgent(290), shipping(292)

**Insights:**

- Tags are slightly applied multiple times to the same tickets, indicating that there are tickets that evolve rather than belong to a single category




## 3. Ticket Update Activity & Behavior (TicketUpdates)

**SQL file:** ticket_updates_analysis.sql

**My Thinking:**

I explored the ticket updates table to understand how tickets progress operationally. I began by identifying the most frequent update actions, then examined update volume over time, and finally checked whether update behavior changed year by year.

**My Findings:**

- Updates fall into three actions: ticket creation, agent response, and ticket closure
- Tickets created are (1,000), agent responses (405), with far fewer closures (201)
- Yearly update volume is within the same range from 2022 to 2025. 2022	(412), 2023	(390), 2024	(430), 2025	(374)
- Across all years, the same update pattern repeats: many tickets created, fewer agent responses, and even fewer closures

**Insights:**

- Ticket handling follows a consistent operational pattern over time.
- The gap between tickets created and tickets closed aligns with the longer resolution times observed in the ticket log analysis.
- Update activity reflects progressive ticket handling, not immediate resolution/improvement.

**Interpretation:**  

The steep drop from tickets created to tickets responded to and closed suggests
potential inefficiencies in ticket handling capacity or workflow execution.



## 4. Agent Performance & Workload Segmentation (Agent_Team_Performance)

**SQL file:** agent_performance_analysis.sql

**My Thinking:**

I analyzed agent performance to understand how workload, resolution efficiency, and customer satisfaction interact. 
My approach was structured:
* Explored the table to understand available metrics and confirm data quality.
* Established baseline statistics for tickets closed, resolution time, and CSAT.
* Classified agents by workload: above average, average, and below average tickets closed.
* Created performance quadrants combining workload (tickets closed) and efficiency (average resolution time):
    High Workload & Fast Resolution
    High Workload & Slow Resolution
    Low Workload & Fast Resolution
    Low Workload & Slow Resolution
* Analyzed the distribution and contribution of each quadrant to overall ticket closure.
* Drill-downs to identify top performers, risk groups, and underutilized agents.

**My Findings:**

- Agent workload varies: some agents close many tickets (13), others very few (3).
- All agents fall under the same range of CSAT Score.
- High workload does not always equal fast resolution: some agents close many tickets slowly.

**Quadrant distribution:**

- High Workload & Slow Resolution: 10 agents, 93 tickets
- High Workload & Fast Resolution: 8 agents, 64 tickets
- Low Workload & Fast Resolution: 4 agents, 17 tickets
- Low Workload & Slow Resolution: 3 agents, 17 tickets
- Efficiency & quality (average resolution time) differ by quadrant: top performers maintain fast resolution and high CSAT,
  while some high-load agents are slower despite similar CSAT.
- All Quadrants have more than 4 CSAT Scores.
- Drill-downs show specific agents in each quadrant, highlighting top performers, potential risk groups(low & slow), and underutilized efficiency.

**Insights:**

- Ticket handling capacity is unevenly distributed across agents.
- High-workload, fast-resolution agents represent operational strength.
- High-workload, slow-resolution agents may indicate process inefficiencies or strain since more tickets are closed than all quadrants.
- Low-workload, fast-resolution agents suggest untapped potential, while low-workload, slow-resolution agents contribute minimally.

**Interpretation:**
Agent performance patterns reveal capacity imbalances rather than uniform inefficiency. Supporting high-load agents and redistributing workload could improve overall ticket resolution throughput without adding staff.
