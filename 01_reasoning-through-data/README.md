Project 1: Reasoning with Data

Freelance Jobs & Housing Market Analysis

Project Overview

This project demonstrates analytical reasoning using real-world, semi-structured datasets analyzed in Microsoft Excel.
It examines freelance job listings and housing listings, focusing on skill demand, pay patterns, property pricing, and market trends.

The emphasis is on analytical thinking, pattern recognition, and deriving actionable insights from data.

Datasets

Both datasets were self-collected from online job listing and housing platforms.

Freelance Jobs Dataset

101 listings

Key columns:
Location, Experience Level, Project Type, Required Skills, Platform, Job Title, Number of Bids, Client Stated Budget, Average Bid Amount, Currency, Bid Type (Hourly / Fixed)

Housing Listings Dataset

282 listings

Key columns:
Estate, Bedrooms, Bathrooms, Price, Features, Listing Type (Rent / Sale)

Both datasets required data cleaning, transformation, and the creation of derived metrics before analysis.

Analytical Questions
Freelance Jobs

Which skills are most frequently requested in freelance data analyst roles?

Which skill combinations attract higher pay?

How does experience level influence skill requirements and budgets?

Are high-paying, skill-heavy jobs more competitive?

Housing Listings

How does price change as the number of bedrooms increases?

How do prices compare across estates for similar house types?

Do additional features increase housing prices?

What bedroom configurations (studio, 1, 2, 3, etc.) are most commonly available?

Analyses Performed
Freelance Jobs

Standardized numeric fields (budgets, bid amounts)

Parsed semi-structured text fields into analyzable categories (skills)

Created derived metrics:

Skill count per listing

Skill category flags (Excel, SQL, Power BI, BI tools, Programming)

Used pivot tables and summary statistics to analyze:

Skills vs average pay

Skill count vs competition

Excel was used for data cleaning, transformation, and pivot-based analysis only.

Housing Listings

Created derived features for analysis (feature count per listing)

Analyzed:

Bedrooms vs price

Features vs price

Feature count vs price-per-bedroom

Listing counts by category

Key Insights
Freelance Jobs
1. Excel Skills

Overall requirement: 36 out of 41 listings require Excel → 87.8%

By experience level:

Entry level: 4 / 6 → 66.7%

Intermediate: 24 / 27 → 88.9%

Expert: 8 / 8 → 100%

Insight:
Excel is almost universally required across roles, and proficiency becomes increasingly mandatory at higher experience levels.

2. Data Visualization / BI Tool Skills

Overall requirement: 31 / 41 → 75.6%

By experience level:

Entry level: 2 / 6 → 33.3%

Intermediate: 22 / 27 → 81.5%

Expert: 7 / 8 → 87.5%

Insight:
Visualization and BI skills are emphasized at intermediate and expert levels. Entry-level roles tend to focus more on Excel or basic reporting.

3. Programming Knowledge

Entry-level roles: rarely required (2 listings)

Intermediate roles: moderately required (7 listings)

Expert roles: more frequently required (6 listings)

Insight:
Programming functions as a differentiating skill, especially at intermediate and expert levels. Many entry-level roles still rely primarily on Excel and visualization skills.

4. Statistics / Data Analysis

All intermediate and expert listings require statistics or data analysis knowledge.

Insight:
Core analytical skills are non-negotiable for non-entry roles and are consistently required across sectors.

5. Database Knowledge

Required only in intermediate and expert roles.

Insight:
Database skills become more important as analysts progress beyond entry-level, particularly for roles involving reporting and complex analysis.

6. Domain Knowledge

Required across intermediate and expert roles.

Insight:
Understanding the business domain is critical, even as technical requirements vary. Some entry-level roles may still require limited domain exposure depending on project type.

7. Overall Skill Pattern

Entry level: Excel-focused, limited visualization/BI, minimal programming

Intermediate: Excel + visualization/BI + some programming + database + domain knowledge

Expert: Excel + visualization + programming + statistics + domain knowledge, with greater problem-solving responsibility

Housing Listings
1. Bedrooms and Price

Prices increase with the number of bedrooms for both rent and sale.
Rent grows steadily, while sale prices increase more sharply for larger units, indicating that additional bedrooms add more value to ownership than to rental income.

2. Estate-Level Price Patterns

Kitisuru shows strong rental yields for 1–3 bedroom units.

Kilimani has the highest capital values, with strong rental performance for studios and 5-bedroom units.

Hurlingham and Kileleshwa perform well for larger units (4–5 bedrooms).

Some estate–unit combinations show identical minimum, maximum, and average prices, indicating limited listings rather than stable pricing.

Lavington commands high sale prices but has limited rental availability for smaller units.

3. Features and Pricing

Housing prices generally rise with the number of features.

Larger units (3–5 bedrooms) show clear increases in median rent and sale prices as features are added.

Smaller units (studios and 1-bedroom apartments) show less consistent trends due to limited listings with multiple features.

Insight:
Both house size and feature count influence pricing, with features having a stronger effect on larger houses.

4. Bedroom Configuration Distribution

Listings are concentrated in 2- and 3-bedroom units across estates.

Studios and 5-bedroom houses are rare.

One-bedroom units are consistently present but less dominant.

Examples:

Kitisuru: 2-bedroom units dominate (57%)

Hurlingham, Lavington, Kileleshwa: 3-bedroom units dominate (35–42%)

Insight:
Mid-sized units form the core of the housing market, with smaller and larger units being less common.

Tools Used

Microsoft Excel

Data cleaning and standardization

Text parsing and categorization

Excel Formulas.
