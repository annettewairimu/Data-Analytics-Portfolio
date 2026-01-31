# Project 1: Reasoning with Data

## Freelance Jobs & Housing Market Analysis

## Overview

This project demonstrates analytical reasoning using real-world datasets in Microsoft Excel. 
It explores:

Freelance jobs: skill demand across experience levels

Housing market: property pricing trends, feature impact, and market patterns

The goal is to derive actionable insights from semi-structured data through transformation and analysis.

### Datasets

Data Collected Manually From Job Listing and House Listing Sites.

**Freelance Jobs**

Listings: 41

Key columns: Experience Level, Project Type, Required Skills

**Housing Listings**

Listings: 282

Key columns: Estate, Bedrooms, Bathrooms, Price, Features, Listing Type (Rent/Sale)

Both datasets required transformation and the creation of derived metrics before analysis.


## Freelance Jobs

**Questions.**

- How is Excel demanded across experience levels?

- How does experience influence skill requirements?

- Are expert-level jobs more skill-heavy?

**Analyses Performed**

Dataset transformation:

- Parsed text fields into skill categories: Excel, BI/Visualization, Programming, Statistics/Data Analysis, Database, Domain Knowledge

- Created derived metrics: skill counts, skill flags

Analysis examples:

- Jobs requiring Excel by experience level

- Skill sets demanded at entry, intermediate, and expert levels

<img width="580" height="411" alt="image" src="https://github.com/user-attachments/assets/c6cfd9c0-d1f2-4efe-8029-260e149ef7f4" />


**Overall Insight:**

Entry: Excel-focused, minimal visualization/programming/domain exposure

Intermediate: Excel + Visualization/BI + some Programming + Database + Domain knowledge

Expert: Excel + Visualization + Programming + Statistics + Domain knowledge

**Key Takeaways**

Excel proficiency is almost universal for freelance roles at all experience levels.

Intermediate/expert jobs require a mix of BI, programming, statistics, and domain knowledge.


## Housing Listings

**Questions.**

- How does the price change with bedrooms?

- How do prices vary across estates for similar units?

- Do additional features increase price?

- What bedroom configurations dominate the market?


**Derived features**

Features_Count

**Insight:**

Bedrooms & Price: Prices rise with the number of bedrooms; ownership sees sharper price increases than rent.

Estate Patterns:

Kitisuru: strong rental yields for 1–3 bedrooms

Kilimani: highest capital values, strong rental for studios & 5-bedroom units

Hurlingham/Kileleshwa: perform well for 4–5 bedrooms

Lavington: high sale prices, limited small-unit rentals

Features & Pricing: More features → higher price, especially for larger units

Bedroom Distribution: Mid-sized units (2–3 bedrooms) dominate; studios and 5-bedroom units are rare

[<img width="697" height="661" alt="image" src="https://github.com/user-attachments/assets/d95aa601-3374-4d49-b794-4aca56c70451" />]

**Key Takeaways**

Price and features strongly influence value; 2-3 bedroom unit form the market core.

Housing prices correlate with the number of bedrooms, features, and estate location.

## Tools Used

Microsoft Excel: transformation, text parsing, formulas, and analysis


