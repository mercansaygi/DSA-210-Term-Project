# DSA-210-Term-Project
This repository contains my term project for the DSA210 – Introduction to Data Science course at Sabancı University. 

Title: Gender Education Gap and Political Orientation in Democracies

1) Introduction

This project investigates whether cross-country differences in gender attainment at the secondary level (age 25+) are associated with a nation being governed by a left-leaning or right-leaning party. I focus on adults (25+) because they represent the core voting population, and I restrict attention to democratic elections.

2) Motivation

Gender equality in education is linked to civic participation and policy preferences. If smaller gaps indicate more equal opportunities, we might expect a shift toward parties that emphasize egalitarian policies. From a data-science perspective, this project covers the end-to-end pipeline (collection, cleaning, EDA, modeling, visualization) and explicitly enriches a public dataset with additional sources.

3) Hypotheses

To statistically validate the relationships in the dataset, the following hypotheses are tested using ANOVA, T-Tests, and Pearson Correlation:

* **H0 (Null):** The gender gap in secondary education is unrelated to whether a country is governed by left vs. right parties.
* **H1 (Alternative):** Countries with smaller gender gaps are more likely to be governed by left-leaning parties.

* **H0 (Null):** **"Geography is Destiny":** There is no significant difference in GDP per capita across different continents.
* **H1 (Alternative):** Economic wealth varies significantly by continent, suggesting structural/geographic inequalities.

* **H0 (Null):** **"Money Buys Health":** There is no correlation between a country's GDP and its Life Expectancy.
* **H1 (Alternative):** Higher GDP is strongly correlated with longer life expectancy.

* **H0 (Null):** **"Politics Affects Education":** There is no difference in female school enrollment rates among Right, Left, and Center-governed countries.
* **H1 (Alternative):** Political ideology significantly impacts female education levels.


4) Finding and Insights

Preliminary analysis and hypothesis testing have revealed:
* **Geography Matters:** Statistical tests confirm a significant income gap between continents, highlighting that geography is a key predictor of development.
* **Economy Drive Health:** A strong positive correlation was found between GDP and Life Expectancy, confirming that economic power directly translates to public health.
* **Education is Structural:** Surprisingly, political ideology (Right vs. Left) was found to have **no statistically significant impact** on female school enrollment rates, suggesting that education is driven more by economic development than political rhetoric.

  
5) Variables

Main independent variable:
Gender Secondary-Education Gap (25+) — the difference between the male and female percentages with secondary education among adults aged 25+. (Positive values mean men’s attainment is higher than women’s.)

Dependent variable:
Political Orientation (Left vs. Right) — whether the current governing party/coalition is left-leaning or right-leaning.

Controls / Covariates:

HDI (Human Development Index) — national development level (to separate equality effects from development effects).

Continent / Region — categorical fixed effects to absorb broad regional heterogeneity.

Filtering / Quality variables:

Winning Vote Share (%) — if the winning party’s share is > 90%, I exclude that election as likely non-democratic (data cleaning rule).
Democracy quality index (e.g., EIU/V-Dem) — used to restrict/weight the sample to democratic contexts.

6) Data 

UNDP Data Center:

Education by gender (secondary attainment, 25+).

HDI.

IDEA (International IDEA Elections):

Election outcomes (winning party/coalition, vote share).

Party ideology coding (for left/right labeling).

Country–continent mapping (World Bank/ISO).

7) Limitations

Cross-national left/right labels can be noisy; I will document coding rules.

Education and election years may misalign; I’ll prefer close years and test sensitivity.

Omitted variables (culture, religion, inequality) may bias estimates; I discuss this in the report.

