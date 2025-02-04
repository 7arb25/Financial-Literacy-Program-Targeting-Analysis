# Financial Literacy Program Targeting Analysis

![organization logo](https://github.com/7arb25/Financial-Literacy-Program-Targeting-Analysis/blob/4694beb9e102835503f3cfac178fde78f722eeb4/images/InvestInMinds.jpg)

### Table Of Contents

- [Project Overview](#project-overview)
- [Data Sources](#data-sources)
- [Tools](#tools)
- [Data Cleaning](#data-cleaning)
- [EDA](#eda)
- [Data Analysis](#data-analysis)
- [Results](#results)
- [Recommendations](#recommendations)
- [Limitations](#limitations)
- [References](#references)

---

### Project Overview 
##### Identifying Financial Literacy Gaps for InvestInMinds Foundation `phase1`
This project aims to analyze survey data to pinpoint key demographics with the greatest need for **financial literacy programs**, directly informing **InvestInMinds** Foundation's initiatives and maximizing their impact on underserved communities. As a Research and Data Analyst Intern, the core responsibilities will revolve around data analysis, visualization, and strategic recommendations.

**`Phase 2`: State-Level Financial Literacy and Correlation Analysis**

This phase expands the analysis to a state level, examining correlations between financial literacy scores, rankings, teacher-to-student ratios, and other relevant metrics. We perform linear regression analysis to explore potential relationships and identify factors influencing financial literacy at the state level.  This phase also includes the exploration of an external dataset relevant to InvestInMinds' mission, focusing on economic indicators. This broader perspective aims to provide a more nuanced understanding of the factors impacting financial literacy across different states.

Specifically, Phase 2 includes the following sub-tasks:

1. **Descriptive Statistics of State-Level Financial Literacy:**  Calculate and interpret descriptive statistics (mean, median, standard deviation, interquartile range) for state-level financial literacy scores. Identify any outliers and discuss their potential impact on the analysis.  This provides a baseline understanding of the distribution of financial literacy across states.

2. **Correlation Analysis with Rankings and Teacher-Student Ratios:** Conduct linear regression analysis to explore the relationship between financial literacy scores and the following variables:
    * **Financial Literacy Rankings:**  Investigate the correlation between reported financial literacy rankings and actual scores.  This analysis will assess the validity and consistency of existing ranking systems.
    * **Teacher-Student Ratios:** Analyze the correlation between teacher-student ratios and financial literacy scores.  This explores the potential role of educational resources in influencing financial literacy at the state level.  We will perform separate regressions using both the rankings and the actual scores for financial literacy.

3. **External Dataset Integration and Analysis:** Integrate the approved external [dataset](https://github.com/7arb25/Financial-Literacy-Program-Targeting-Analysis/blob/db4392d5067e23cc3bde1431659bd723a6ac4c76/data/input/Financial%20Literacy%20By%20State.xlsx) into the analysis.  Perform exploratory data analysis (EDA) and potentially additional statistical tests to understand the relationship between this dataset and state-level financial literacy.  This step aims to uncover deeper insights into contextual factors affecting financial literacy.  For example, we might investigate whether states with higher access to financial institutions also exhibit higher financial literacy scores.

4. **Comprehensive Report and Visualization:**  Compile the findings from all sub-tasks into a comprehensive report, including clear visualizations to illustrate key relationships and trends. This report will provide actionable insights for InvestInMinds' strategic planning.
5. **Machine Learning Modeling:**  Explore and evaluate different machine learning models to predict financial literacy scores based on available features (rankings, teacher-student ratios, external dataset variables).  This will involve:
    * **Feature Selection:**  Identify the most relevant features for the models.
    * **Model Training:** Train and evaluate several models, including but not limited to:
        * Linear Regression (as a baseline)
        * Ridge Regression/Lasso Regression (to handle potential multicollinearity)
        * Support Vector Regression (SVR)
        * Random Forest Regression
        * Gradient Boosting Regression (e.g., XGBoost, LightGBM)
    * **Model Evaluation:** Use appropriate metrics (e.g., R-squared, Mean Squared Error, Root Mean Squared Error) and cross-validation techniques to assess model performance and avoid overfitting.
    * **Model Comparison:** Compare the performance of different models and select the best-performing model based on the evaluation metrics.


##### Key Project Objectives:

Identify demographic groups most in need of financial literacy programs.
Guide InvestInMinds Foundation's program targeting and resource allocation.
Project Tasks:

- Data Cleaning: This involves identifying and addressing inconsistencies and missing data within the provided dataset. A documented process of handling these issues is required.
- Data Analysis: This includes calculating average financial literacy scores for various demographic segments (age, income, education, and location) and identifying patterns, particularly focusing on groups with significantly lower scores.
- Data Visualization: Creating at least two visualizations (e.g., bar charts, pie charts, tables) to effectively communicate key findings. Examples include comparing financial literacy scores by age group or segmenting scores by income level and location.
- Recommendations: Developing a concise report (1-2 pages) summarizing the findings, highlighting 2-3 demographic groups with the lowest financial literacy levels, and providing actionable suggestions for InvestInMinds Foundation to address these gaps.
##### Provided Dataset:

The dataset includes the following variables:

**Phase 1 Dataset:**

* `Age Group`: Categorical variable representing the age range of survey respondents.
* `Household Income`: Categorical variable representing the annual household income.
* `Education Level`: Categorical variable representing the highest level of education attained.
* `Financial Literacy Score`: Numerical score (0-100) representing financial knowledge.
* `Location`: Categorical variable indicating urban, suburban, or rural location.


* **Phase 2:**
    * `state_financial_literacy_data.csv` (From Google Docs link) - Contains state-level financial literacy data, including mean, median, standard deviation, IQR, and rankings.  *(Include a brief description of the source of this data, e.g., "National Survey of Financial Capability")*
    * `teacher_student_ratio_data.csv` (From Google Docs link) - Contains state-level teacher-to-student ratio data. *(Include a brief description of the source of this data, e.g., "National Center for Education Statistics")*
    * `[Name of External Dataset].csv` (Chosen by Analyst) - Contains data on [Description of data, e.g., number of banks per capita, unemployment rates, median household income]. *(Include a detailed description of the source of this data, e.g., "Federal Deposit Insurance Corporation (FDIC) - Summary of Deposits")*

  
##### Deliverables:

1. A cleaned dataset with documented changes.
2. A 1-2 page report summarizing findings and recommendations.
3. Two visualizations (embedded in the report or as separate files).

*Due Date: Next Monday 20 jan 2025 .*

This project is crucial for **InvestInMinds** Foundation as it provides data-driven insights to effectively target their programs and maximize their positive impact on financial literacy within underserved communities. The intern's analysis and recommendations will directly influence the organization's strategic planning and resource allocation.'


### Data Sources

The dataset is provided in an Excel file and includes the following variables:

1. **Age Group:** 
 - Under 18
 - 18-24
 - 25-34
 - 35-44
 - 45-54
 - 55+
2. **Household Income:**
 - Low (<$30,000)
 - Middle ($30,000-$70,000)
 - High (>$70,000)
3. **Education Level:**
 - High School or Less
 - Some College
 - Bachelor’s Degree
 - Graduate Degree
4. **Financial Literacy Score:**
 - Numerical scores (0-100) representing survey responses.
5. **Location:**
 - Urban
 - Suburban
 - Rural

### Tools

- [Microsoft excel](https://www.microsoft.com/en-us/microsoft-365/excel)

- Python3
  - [matplotlib.pyplot](https://matplotlib.org/)
  - [numpy](https://numpy.org/)
  - [pandas](https://pandas.pydata.org/)
  - [seaborn](https://seaborn.pydata.org/)
  - [scikit-learn](https://scikit-learn.org/stable/)
  - [scipy](https://scipy.org/)


### Data Cleaning

1. Data Loading And Inspection :

2. Handling Missing Values :

3. Data-Cleaning & Formatting :


### EDA 



### Data Analysis


### Code

The code used for data cleaning, analysis, and visualization is available in the `code` directory:

* `data_cleaning.py` (https://github.com/7arb25/Financial-Literacy-Program-Targeting-Analysis/blob/4694beb9e102835503f3cfac178fde78f722eeb4/financial-literacy-score.ipynb)
* `data_analysis.py` (Example)
* `visualization.py` (Example)

### Results



### Recommendations



### Limitations



### References







### Contact

* **Analyst:** [Abdelrahman Harb](3bd0.g0m3aa@gmail.com)
* **LinkedIn:** [link](https://LinkedIn.com/in/3bd0g0m3aa)
* **InvestInMinds Foundation:**
   - [Ava Jerman - `CEO`](investinmindsfoundation@gmail.com)
   - [Rafi Ptashny - `Data Manager`](rafiptashny@gmail.com)

  
