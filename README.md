# Big Five Personality Traits: Statistical Analysis in R

An end-to-end quantitative data analysis project exploring the relationships between demographic characteristics and the Big Five personality traits using R and Quarto.

## Project Overview

The purpose of this project is to investigate personality differences across demographic groups and examine the relationships between the five major personality dimensions:

- Agreeableness
- Conscientiousness
- Extraversion
- Neuroticism
- Openness

The analysis focuses on gender differences, educational attainment, and the predictive relationships between personality dimensions.

## Dataset

This project uses the 25-item `bfi` dataset from the R `psych` package.

- **Sample size:** 2,556 observations after cleaning in the original analysis.
- **Measurement:** 25 personality items.
- **Scale:** 1–6 Likert scale.
- **Dimensions:** Five Big Five personality traits.

The dataset is loaded directly through the `psych` package, so no separate CSV file is required.

## Methodology

The analysis follows a structured statistical workflow.

### 1. Data Cleaning and Preparation
- Data inspection and cleaning.
- Reverse-scoring negatively keyed items.
- Handling missing responses.
- Calculation of composite personality scores.

### 2. Reliability Analysis
- Internal consistency assessment using Cronbach's alpha.

### 3. Descriptive Statistics
- Summary statistics for the five personality dimensions.
- Exploration of demographic characteristics.

### 4. Inferential Statistics
- **Welch's Independent Samples t-test:** Examining gender differences in Neuroticism.
- **One-Way ANOVA:** Investigating differences in Conscientiousness across educational groups.
- **Tukey HSD:** Post-hoc comparisons following ANOVA.

### 5. Multiple Linear Regression
- Predicting Neuroticism using age and the remaining four personality dimensions.
- Multicollinearity assessment using VIF.
- Examination of standardized regression coefficients.

## Key Findings

The original rendered analysis reported the following findings:

- Female participants reported significantly higher Neuroticism scores than male participants (*p* < .001, *d* = -0.25).
- Participants with some college education showed significantly higher Conscientiousness scores than those with a high school diploma (*p* < .001).
- Conscientiousness (β = -0.17) and Extraversion (β = -0.14) emerged as the strongest negative predictors of Neuroticism.

**Note:** The corrected Quarto source uses a minimum of four valid responses out of five items to calculate each personality dimension. This may affect the final sample size and statistical results. The corrected source has not yet been re-rendered and verified, so the findings above should be treated as results from the original rendered analysis.

## Technologies and Packages

- **Programming Language:** R
- **Reporting:** Quarto
- **Statistical Analysis:** `psych`, `car`, `effectsize`
- **Data Manipulation, Visualization etc.:** `tidyverse`

## Project Structure

- `Basic_Data_Analysis_&_Statistics_Pipeline_(Big_Five_Inventory).qmd` — Quarto source file containing the analysis, R code, and explanatory text.
- `references.bib` — Bibliographic references.
- `README.md` — Project documentation.

## How to Run

### Requirements
- R
- RStudio 
- Quarto

### Install Required Packages

Run the following command in the R console:

```r
install.packages(c(
  "tidyverse",
  "psych",
  "car",
  "effectsize"
))
```

### Render the Analysis

Open `Basic_Data_Analysis_&_Statistics_Pipeline_(Big_Five_Inventory).qmd` in RStudio and render it using Quarto.

Alternatively, run:

```r
quarto::quarto_render("Basic_Data_Analysis_&_Statistics_Pipeline_(Big_Five_Inventory).qmd")
```

## Purpose

This project demonstrates the application of quantitative research methods, psychometric assessment, statistical inference, and regression modeling in psychological research.