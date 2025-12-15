# Project 1: Reasoning with Data. Freelance Jobs & Housing Market Analysis
## Project Overview

This project demonstrates reasoning with real-world, semi-structured datasets using Microsoft Excel.
It analyzes freelance job listings and housing listings, focusing on skill demand, pay patterns, property pricing, and market trends.

The emphasis is on analytical thinking, reasoning, pattern recognition, and actionable insights.

## Datasets
Dataset	Observations	Key Columns	Focus
(I collected these datasets myself from job listings and house listing platforms)
###  Freelance Jobs	101 listings	
Location, Experience, Project Type, Required Skills, Platform, Job Title, Bids, Clients' Stated Budget, Avg Bid Amount, Currency, Bid Type (hourly/fixed)

###  Housing Listings 282 listings 
Estate, Bedrooms, Bathrooms, Price, Kind/Features, Rent/Sale

Both datasets required cleaning, transformation, and derived metrics before analysis.

## Analytical Questions
### Freelance Jobs

Which skills are most frequently requested in freelance data analyst roles?

Which skill combinations attract higher pay?

How does experience level influence skill requirements and budgets?

Are high-paying, skill-heavy jobs more competitive?

### Housing Listings

a) How does price change as the number of bedrooms increases?

b) How do prices compare across estates for similar house types?

c) Do additional features increase housing prices?

d) What are the most commonly available bedroom configurations (studio, 1, 2,3...)?

## Analyses Performed

Standardized numeric fields (budgets, prices)

Parsed semi-structured text fields into analyzable categories (skills, features)

Created derived metrics:

Skill count and skill category flags (Excel, SQL, Power BI, BI tools, Programming)



Pivot tables and summary statistics for trend analysis:

Skills vs average pay

Skill count vs competition

Excel was used for data cleaning, transformation, and pivot-based analysis only.

#### House Listing Analyses

Created features for analysis (Count of Features in each Listing).

Bedrooms vs price

Features vs price

Feature count and price-per-bedroom

Listing Counts

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

2. Kitisuru offers the strongest rental yields for 1–3 bedroom units, making it ideal for landlords. Kilimani has the highest capital values, with attractive rental income for studios and 5-bedroom units, making it suitable for those seeking both appreciation and rent. Hurlingham and Kileleshwa perform well for larger units (4–5 bedrooms). Some estates, such as Lavington for studios or Kileleshwa for 5-bedroom units, display zero or identical values for average, min, and max prices, indicating limited listings, possibly only one property. Lavington commands high sale prices but has limited rental opportunities for smaller units.
  
3. Housing prices generally rise with the number of features. Larger units (3–5 bedrooms) show a clear increase in median rent and sale prices as features are added, indicating that additional amenities significantly add value. Smaller units such as studios and 1-bedroom apartments show less consistent trends, largely due to limited listings with multiple features. Overall, the data suggests that both house size and feature count influence pricing, but the effect of features is more pronounced for larger houses.

4. The most commonly available bedroom configurations vary slightly by estate but generally show a strong concentration in 2- and 3-bedroom units. Studios and 5-bedroom houses are rare across all areas, while 1-bedroom units are consistently present but less dominant. For example, Kitisuru listings are dominated by 2-bedroom units (57%), whereas Hurlingham, Lavington, and Kileleshwa have more 3-bedroom units (35–42%). This distribution indicates that mid-sized units are the primary focus of the market, with smaller and larger units being less common.


## Tools Used

Microsoft Excel:

Data cleaning & standardization

Text parsing & categorization

Pivot tables for trend and comparative analysis

Summary statistics & mini charts
