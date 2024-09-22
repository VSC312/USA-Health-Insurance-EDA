# US Health Insurance Exploratory Data Analysis (EDA) Project
## [Dataset Link](https://www.kaggle.com/datasets/teertha/ushealthinsurancedataset)
## Table of Contents
1. [Project Overview](#project-overview)
2. [Data Description](#data-description)
3. [Objectives](#objectives)
4. [Methodology](#methodology)
    - [Data Collection](#data-collection)
    - [Data Preparation](#data-preparation)
    - [Exploratory Data Analysis](#exploratory-data-analysis)
    - [Statistical Hypothesis Testing](#statistical-hypothesis-testing)
5. [Techniques and Tools Used](#techniques-and-tools-used)
6. [Key Findings and Results](#key-findings-and-results)
7. [Industry Relevance](#industry-relevance)
8. [Conclusion](#conclusion)
9. [Future Work](#future-work)
10. [Acknowledgments](#acknowledgments)

---

## Project Overview

The **US Health Insurance EDA Project** aims to analyze and uncover insights from a comprehensive dataset on US health insurance. Through meticulous data exploration and statistical analysis, this project seeks to understand patterns, trends, and relationships within the data to inform policy decisions, business strategies, and public health initiatives.

---

## Data Description

The dataset used in this project comprises **1,338 records** with the following attributes:

| Attribute   | Description |
|-------------|-------------|
| **age**     | Age of the insured individual (18-64 years) |
| **sex**     | Gender of the insured (`male`, `female`) |
| **bmi**     | Body Mass Index of the insured (float) |
| **children**| Number of children covered by the insurance (0-5) |
| **smoker**  | Smoking status (`yes`, `no`) |
| **region**  | Residential area (`southwest`, `southeast`, `northwest`, `northeast`) |
| **charges** | Medical insurance charges billed to the individual |

**Data Characteristics:**
- **No Missing Values:** All columns are fully populated with no null entries.
- **Data Types:**
  - Numerical: `age` (int), `bmi` (float), `children` (int), `charges` (float)
  - Categorical: `sex`, `smoker`, `region`

---

## Objectives

The primary objectives of this EDA project are:

1. **Understand Data Distribution:** Analyze the distribution of numerical and categorical variables.
2. **Identify Key Factors:** Determine factors influencing insurance charges.
3. **Assess Relationships:** Explore relationships between different attributes, such as smoking status, BMI, and charges.
4. **Statistical Validation:** Conduct hypothesis testing to validate observed patterns.
5. **Provide Insights:** Deliver actionable insights relevant to stakeholders in the health insurance industry.

---

## Methodology

### Data Collection

The dataset was obtained from a reliable public source, containing comprehensive information on US health insurance subscribers. It includes diverse attributes essential for analyzing insurance patterns and trends.

### Data Preparation

1. **Data Cleaning:**
   - Verified the absence of missing values.
   - Ensured data types were correctly assigned.
   
2. **Data Transformation:**
   - Converted categorical variables (`sex`, `children`, `smoker`, `region`) to category codes for analytical convenience.
   
3. **Data Integration:**
   - Merged any supplementary datasets if required (not applicable in this project).

### Exploratory Data Analysis

1. **Descriptive Statistics:**
   - Calculated mean, median, standard deviation, and other summary statistics for numerical attributes.
   
2. **Data Visualization:**
   - **Numerical Attributes:** Utilized density plots, boxplots, violin plots, and cumulative distribution plots to understand distributions and detect outliers.
   - **Categorical Attributes:** Employed count plots and pie charts to visualize category distributions.
   - **Pairwise Relationships:** Created pairplots and scatter plots to explore correlations between variables.
   - **Correlation Heatmap:** Generated a heatmap to visualize correlations among numerical variables.
   
3. **Segment Analysis:**
   - Analyzed subgroups based on gender, smoking status, and number of children to identify specific patterns.

### Statistical Hypothesis Testing

1. **Two-Sample T-Test:**
   - **Objective:** Determine if there is a significant difference in insurance charges between smokers and non-smokers.
   - **Result:** Significant difference observed; smokers have higher charges.
   
2. **Two-Sample T-Test for BMI:**
   - **Objective:** Assess if there is a significant difference in BMI between males and females.
   - **Result:** No significant difference found.
   
3. **Proportion Z-Test:**
   - **Objective:** Evaluate if the proportion of smokers differs significantly between genders.
   - **Result:** Significant difference; higher proportion of male smokers compared to females.

4. **ANOVA:**
   - **Objective:** Examine if BMI differs across groups based on the number of children.
   - **Result:** No significant differences found among groups.

---

## Techniques and Tools Used

- **Programming Language:** Python
- **Libraries:**
  - **Data Manipulation:** Pandas, NumPy
  - **Visualization:** Matplotlib, Seaborn
  - **Statistical Analysis:** SciPy, Statsmodels
- **Environment:** Google Colab for interactive analysis and visualization.

**Visualization Techniques:**
- **Boxplots and Violin Plots:** To assess data distribution and identify outliers.
- **Density Plots:** For understanding the distribution shape of numerical variables.
- **Pairplots:** To visualize relationships between multiple variables simultaneously.
- **Heatmaps:** To display correlation matrices effectively.

**Statistical Tests:**
- **Two-Sample T-Test:** For comparing means between two groups.
- **Proportion Z-Test:** For comparing proportions between categorical groups.
- **ANOVA:** For comparing means across multiple groups.
- **Tukey-Kramer HSD Test:** For post-hoc analysis following ANOVA.

---

## Key Findings and Results

1. **Age Distribution:**
   - Uniform distribution with no outliers.
   - **Mean Age:** 39.2 years; **Median Age:** 39 years.
   
2. **BMI Analysis:**
   - Approximately normally distributed.
   - **Mean BMI:** 30.66; **Median BMI:** 30.4.
   - Identified 9 outliers on the higher side.
   
3. **Charges Distribution:**
   - Heavily skewed with a significant number of outliers.
   - **Mean Charges:** \$13,270.42; **Median Charges:** \$9,382.03.
   - Highest charge: \$63,770.43 by a 54-year-old female smoker.
   
4. **Gender Distribution:**
   - Nearly equal distribution: **50.5% males** and **49.5% females**.
   
5. **Smoking Status:**
   - **20.5% smokers**; smokers have significantly higher charges.
   - **Average Charges:** \$32,050.23 (smokers) vs. \$8,434.27 (non-smokers).
   
6. **Regional Distribution:**
   - Even representation across all four regions.
   
7. **Children:**
   - Majority (85%) have **two or fewer children**.
   
8. **Correlation Insights:**
   - Strong positive correlation between **charges** and **smoking status**.
   - Moderate positive correlations between **charges** and **age/BMI**.
   
9. **Hypothesis Testing:**
   - **Smokers vs. Non-Smokers Charges:** Significant difference; smokers incur higher charges.
   - **BMI by Gender:** No significant difference between males and females.
   - **Proportion of Smokers by Gender:** Significant difference; higher proportion of male smokers.
   - **BMI by Number of Children:** No significant differences across groups.

---

## Industry Relevance

This EDA project holds substantial relevance for various stakeholders in the **health insurance industry**:

- **Insurance Companies:** Insights on factors influencing premium charges can aid in risk assessment and pricing strategies.
- **Policy Makers:** Understanding demographic disparities and the impact of smoking can inform public health policies and insurance regulations.
- **Healthcare Providers:** Correlations between BMI, smoking, and charges can guide preventive health initiatives.
- **Consumers:** Awareness of factors affecting insurance costs can help individuals make informed decisions about their health and insurance plans.

By identifying key drivers of insurance charges and understanding demographic trends, the industry can optimize offerings, enhance customer satisfaction, and promote healthier lifestyles among insured populations.

---

## Conclusion

The Exploratory Data Analysis of **US health insurance data** has unveiled critical insights into the factors influencing insurance charges. **Smoking status** emerges as a significant determinant of higher premiums, while **BMI** shows a moderate correlation with charges. **Gender disparities** exist in smoking proportions, though BMI does not significantly differ between males and females. The analysis underscores the importance of lifestyle factors in health insurance and provides a foundation for more targeted strategies in risk management and policy formulation.

---

## Future Work

To build upon the findings of this EDA project, the following avenues can be explored:

1. **Predictive Modeling:** Develop machine learning models to predict insurance charges based on individual attributes.
2. **Segmentation Analysis:** Perform clustering to identify distinct segments within the insured population for tailored services.
3. **Longitudinal Study:** Analyze trends over multiple years to assess the impact of policy changes on insurance dynamics.
4. **Incorporate Additional Variables:** Enhance the dataset with more attributes like income, education, or geographic mobility for a more comprehensive analysis.
5. **Causal Inference:** Investigate causal relationships between variables to inform more effective interventions.

---

## Acknowledgments

I would like to thank **Kaggle** and other public data repositories for providing access to this valuable dataset. Special thanks to the **open-source Python community** for the fantastic tools and libraries that made this project possible.
