Real Estate Liquidity Analysis for Property Flipping in Mexico City (CDMX)

## Summary

This project explores how residential properties (apartmens) in Mexico City behave in terms of liquidity, focusing on how fast assets convert into capital and under what pricing conditions. In a flipping or resale context, liquidity is critical because faster transactions allow investors and operators to reinvest capital sooner, increasing total return over time.

Using a synthetic dataset designed to reflect CDMX apartment markets, the analysis studies **Time on Market (TOM)** and **pricing efficiency** across different property characteristics such as parking, floor level, size, metro access and condition.

Rather than searching for a single “perfect property”, the project shows that liquidity is multifactorial. Through SQL-driven analysis and visual storytelling, it maps how different features trade off between speed and price, providing a practical framework to understand which configurations tend to rotate capital faster while preserving value.


## Business Context

In real estate resale operations, the business is not only about price, but also about time. Capital that stays trapped in inventory limits how fast an investor can reinvest and scale returns.

For a company focused on fast property resale (flipping), understanding what makes an apartment sell faster — and with less discount — becomes a strategic advantage. Instead of relying only on intuition, this project uses data to explore how different property features affect:

- Time on Market (TOM)
- Price discounts relative to zone benchmarks

The goal is to move to a structured view of how product configuration, accessibility and pricing interact to drive liquidity in CDMX apartment markets.


## Dataset & Design

The project uses a **synthetic dataset** designed to simulate the behavior of apartment listings in Mexico City (CDMX). The data does not represent real transactions, but it is structured to reflect realistic market dynamics for exploratory and portfolio purposes.

The dataset focuses exclusively on apartments and includes around 1,200 properties across multiple boroughs.

Each record represents a property with attributes commonly used in real estate analysis, such as:

- Location (borough)
- Physical features (size in m², floor level, parking spots)
- Accessibility (near metro, near main avenues)
- Condition (renovated, good, fair, poor)
- Pricing context (zone average price per m², relative price, percentage discount)
- Market outcome (days on market)

The design goal is not prediction accuracy, but analytical flexibility: having enough structure to explore how Time on Market and pricing efficiency interact with property configuration in a flipping / resale context.

## Methodology

The project follows a practical exploratory workflow focused on business understanding :

- **Data Cleaning & Audit**  
  Basic validation of data types, missing values and consistency to ensure the dataset is usable for analysis.

- **Liquidity Exploration (TOM)**  
  Analysis of Time on Market distributions across boroughs.

- **Feature Advantage Testing**  
  Evaluation of individual characteristics (parking, floor level, metro access, size, condition) to detect which ones provide liquidity advantages.

- **Core Market Analysis**  
  Identification of the central part of the market (Q1–Q3) to check whether advantaged features actually represent a large portion of typical liquidity behavior.

- **Liquidity Landscape Construction**  
  Visual mapping of both advantaged and friction segments into a single space defined by speed (TOM) and pricing efficiency (discount vs zone), providing a global view of how features trade off in real estate resale.

The goal is not prediction, but interpretation: understanding how product configuration and pricing interact to drive capital rotation in CDMX apartment markets.

Throughout the project, the analytical structure was refined. Each step informed the next one: initial findings led to new questions, visualizations were adjusted as patterns emerged, and the focus shifted based on what the data revealed. Rather than following a fixed script, the workflow evolved with the analysis, reflecting how real-world business questions are explored and improved over time.


## Skills Demonstrated

- Exploratory Data Analysis (EDA)  
- SQL for Analytics  
- Python (pandas, matplotlib)  
- Data Cleaning & Auditing  
- Feature Engineering  
- Data Visualization  
- Business-Oriented Storytelling  
- Iterative Analytical Thinking   
- Analytical Project Design  

## Key Insights & Findings

- **Time on Market is multifactorial.**  
  No single feature explains liquidity by itself. Speed emerges from combinations of accessibility, configuration and pricing.

- **Parking is one of the strongest marginal drivers of liquidity.**  
  Apartments with parking sell faster on average and require smaller discounts compared to units without parking.

- **Ground floor and metro access provide secondary advantages.**  
  These features reduce Time on Market slightly, but do not eliminate long-tail risk by themselves.

- **Only ~10% of the core market matches an ideal combined profile.**  
  This shows that fast liquidity does not come from a rigid formula, but from multiple viable configurations.

- **Renovated and premium-priced units behave like proxy signals.**  
  These segments cluster near efficient zones because they usually bundle several positive characteristics rather than acting alone.

- **Speed and pricing efficiency move together.**  
  Properties that take longer to sell usually require deeper discounts, revealing a structural link between time and price pressure.

- **The Liquidity Landscape provides a strategic view of trade-offs.**  
  Instead of ranking features individually, the landscape shows how different product types balance speed, price and market relevance.

## Liquidity Landscape

reports/liquidity_landscape.png

## Limitations & Next Steps

### Limitations

- The dataset is synthetic, designed for portfolio purposes and not sourced from real market transactions.  
- Analysis combines multiple boroughs and price segments, which mixes different micro-markets into a single view.  
- Time on Market (TOM) is influenced by many factors not included here (negotiation behavior, broker strategy, demand cycles, seasonality).  
- Some features act as proxies (e.g. renovated, above zone price) and may group multiple hidden variables.  
- The project focuses on exploratory and visual insights rather than predictive modeling.

### Next Steps

- Run the same analysis at **micro-market level (by neighborhood) to isolate local dynamics.  
- Segment properties by **budget ranges per zone** to avoid mixing very different price behaviors.  
- Build a simple **supervised model** to estimate TOM using the engineered features.  
- Integrate real transaction data and historical price evolution for stronger business conclusions.  
