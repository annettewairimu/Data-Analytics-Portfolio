# Project 1: Reasoning with Data. Freelance Jobs & Housing Market Analysis
## Project Overview

This project demonstrates reasoning with real-world, semi-structured datasets using Microsoft Excel.
It analyzes freelance job listings and housing listings, focusing on skill demand, pay patterns, property pricing, and market trends.

The emphasis is on analytical thinking, reasoning, pattern recognition, and actionable insights.

## Datasets
Dataset	Observations	Key Columns	Focus
(I collected these datasets myself from job listings and house listing platforms)
### - Freelance Jobs	101 listings	
Location, Experience, Project Type, Required Skills, Platform, Job Title, Bids, Clients' Stated Budget, Avg Bid Amount, Currency, Bid Type (hourly/fixed)

### - Housing Listings 282 listings 
Estate, Bedrooms, Bathrooms, Price, Kind/Features, Rent/Sale

Both datasets required cleaning, transformation, and derived metrics before analysis.

## Analytical Questions
### Freelance Jobs

Which skills are most frequently requested in freelance data analyst roles?

Which skill combinations attract higher pay?

How does experience level influence skill requirements and budgets?

Are high-paying, skill-heavy jobs more competitive?

### Housing Listings

How does price change as the number of bedrooms increases?

How do prices compare across estates for similar house types?

Do additional features increase housing prices?

What are the most commonly available bedroom configurations (studio, 1, 2,3...)?

Which realtor offers better value-for-money in each Estate?

## Analyses Performed

Standardized numeric fields (budgets, prices)

Parsed semi-structured text fields into analyzable categories (skills, features)

Created derived metrics:

Skill count and skill category flags (Excel, SQL, Power BI, BI tools, Programming)

Feature count and price-per-bedroom

Pivot tables and summary statistics for trend analysis:

Skills vs average pay

Skill count vs competition

Bedrooms vs price

Features vs price

Excel was used for data cleaning, transformation, and pivot-based analysis only.

#### House Listing Analyses

Created features for analysis (Count of Features in each Listing).

Started exploring price trends with respect to bedrooms.

## Key Insights
### Freelance Jobs
#### Insight	Description
Skill demand: Excel, SQL, and Power BI are the most frequently requested skills.
Skill breadth	Jobs requiring multiple analytical tools tend to offer higher pay.
Experience	Expert-level roles demand broader skill sets, commanding higher budgets.
Competition: High-paying, skill-heavy jobs attract more bids, indicating competition.
### Housing Listings
#### Insight	Description
1. Prices increase with the number of bedrooms for both rent and sale.
Rent grows steadily, while sale prices increase disproportionately for larger units, indicating that additional bedrooms add more value to ownership than rental income.



## Tools Used

Microsoft Excel:

Data cleaning & standardization

Text parsing & categorization

Pivot tables for trend and comparative analysis

Summary statistics & mini charts
