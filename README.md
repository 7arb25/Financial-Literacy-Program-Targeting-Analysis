# Financial Literacy Program Targeting Analysis

![organization logo](https://github.com/7arb25/Financial-Literacy-Program-Targeting-Analysis/blob/4694beb9e102835503f3cfac178fde78f722eeb4/images/InvestInMinds.jpg)

### Table Of Contents

- [Project Overview](#project-overview)
- [Data Sources](#data-sources)
- [Tools](#tools)
- [Data Cleaning](#data-cleaning)
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

**Phase 2:**
    * `state_financial_literacy_data.csv`  - Contains state-level financial literacy data, including mean, median, standard deviation, IQR, and rankings.
    * `teacher_student_ratio_data.csv`
 - Contains state-level teacher-to-student ratio data.

  
##### Deliverables:

1. A cleaned dataset with documented changes.
2. A 1-2 page report summarizing findings and recommendations.
3. Two visualizations (embedded in the report or as separate files).
4. Machine Learning Analysis Summary:
   - **Descriptive Statistics (Data Understanding):** Before applying machine learning models, we explored the data's basic statistical properties.  This included calculating the mean, median, standard deviation, and interquartile range for financial literacy scores. Outlier detection was performed using two methods:
     - Q1 - 1.5IQR
     - Mean - 2 standard deviations This step provided a crucial understanding of the data's distribution and potential issues like outliers, which can impact model performance.
   - **Linear Regression Modeling (Relationship Exploration):**  To investigate potential relationships between financial literacy metrics and other factors, we employed linear regression models.  This allowed us to quantify the strength and direction of these relationships.
     - **Financial Literacy Metrics (Feature Engineering):** Three linear regression models were trained, each using a pair of financial literacy metrics as features (e.g., Total Score vs. Wallet Literacy Score). This helped identify potentially redundant or highly correlated features. Model performance was evaluated using R-squared and p-values.
     - **Financial Literacy and Teacher-to-Student Ratios (Predictive Modeling):** We explored the relationship between financial literacy and teacher-to-student ratios using linear regression. Two separate models were trained: one using financial literacy rankings as the independent variable, and the other using actual scores. This allowed us to assess the impact of using different representations of financial literacy on the model's predictive capability. R-squared and p-values were used for evaluation.
   - **Analysis of Your Chosen Data Source (Contextualization)**
5.  **Project Context (Optional but Recommended):**
   - Briefly explain the overall goal of your project, emphasizing the use of machine learning to understand and potentially predict financial literacy.
   - Mention the relevance of financial literacy and the purpose of exploring these datasets using regression techniques.
   - If applicable, describe how these findings might be used to inform the opening of high school chapters, perhaps by identifying areas where financial literacy interventions are most needed.

*Due Date: Next Monday 20 jan 2025 .*

This project is crucial for **InvestInMinds** Foundation as it provides data-driven insights to effectively target their programs and maximize their positive impact on financial literacy within underserved communities. The intern's analysis and recommendations will directly influence the organization's strategic planning and resource allocation.'


### Data Sources

The dataset is provided in an Excel file and includes the following variables:
#### `Phase1`
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

----
#### `Phase2`
Dataset Description: **Financial Literacy Scores by State**
This dataset provides a comprehensive overview of financial literacy across different states, offering insights into various aspects of financial knowledge and behavior.  It includes the following columns:

1. **Overall Rank:** The overall ranking of the state based on its composite financial literacy score. A lower rank indicates better overall financial literacy.
2. **State:** The name of the U.S. state.
3. **Total Score:** The overall financial literacy score for the state. This score likely represents a weighted combination of the other sub-scores. The specific methodology for calculating this score should be documented elsewhere.
4. **Wallet Literacy Score:** A score representing the state's performance in "wallet literacy." This likely encompasses practical financial skills related to managing money, budgeting, saving, and making informed purchasing decisions.
5. **Financial Knowledge & Education Rank:** The state's ranking based on financial knowledge and education. A lower rank indicates a higher level of financial knowledge and/or better access to financial education resources.
6. **Financial Planning & Habits Rank:** The state's ranking specifically related to financial planning and habits. A lower rank suggests better financial planning and habits within the state.
7. **Financial Knowledge & Education Rank:** The state's ranking based on financial knowledge and education. A lower rank indicates a higher level of financial knowledge and/or better access to financial education resources.
### Tools

- [Microsoft excel](https://www.microsoft.com/en-us/microsoft-365/excel)  A spreadsheet software widely used for data entry, organization, basic calculations, and creating simple visualizations.  It's often a starting point for data exploration and manipulation.

- **Python3:** A versatile and widely used programming language, especially popular in data science and machine learning due to its rich ecosystem of libraries.  It provides the foundation for more complex data analysis and modeling.
  - [matplotlib.pyplot](https://matplotlib.org/) A Python library for creating static, interactive, and animated visualizations in Python. It's essential for visualizing data insights and communicating findings effectively.
  - [numpy](https://numpy.org/) A Python library that adds support for large, multi-dimensional arrays and matrices, along with a large collection of high-level mathematical functions to operate on these arrays. 1  It's fundamental for numerical computing in Python and often used in conjunction with Pandas and other data science libraries.   
  - [pandas](https://pandas.pydata.org/)A Python library that provides data structures like DataFrames, which are crucial for efficiently working with and manipulating tabular data.  Pandas simplifies tasks like data cleaning, transformation, and analysis.
  - [seaborn](https://seaborn.pydata.org/) A Python data visualization library built on top of Matplotlib. It provides a higher-level interface for creating statistically informative and visually appealing graphics, often used for exploring relationships between variables.

  - [scikit-learn](https://scikit-learn.org/stable/) A Python library widely used for machine learning. It provides tools for various machine learning algorithms (including linear regression), model selection, preprocessing, and evaluation.  It streamlines the process of building and deploying machine learning models.
  - [scipy](https://scipy.org/) A Python library used for scientific and technical computing. It builds on NumPy and provides additional functions for tasks like optimization, linear algebra, integration, interpolation, and statistical analysis.


### Data Cleaning

This section details the data cleaning and formatting steps performed to prepare the financial literacy and teacher-student ratio datasets for analysis.  The process involved handling missing values, addressing outliers, and formatting data for consistency and compatibility with machine learning algorithms.

**1. Data Loading and Inspection:**

Data was loaded from multiple sources:

*   CSV files: Financial literacy data was initially provided in CSV format.
*   Google Sheets: Teacher-student ratio data was accessed via Google Sheets.  This data was then exported to Excel files for easier manipulation.
*   Excel Files: The exported teacher-student ratio data was loaded from the Excel files.

Initial inspection of the data was performed to understand the data types, identify missing values, and explore the distribution of variables. This involved examining summary statistics, distributions, and correlations between variables.  For the teacher-student ratio data, the initial format required significant transformation.

**2. Feature Engineering and Formatting:**

For the teacher-student ratio data, feature engineering was performed to create a consistent representation of the ratio:

*   **Ratio Extraction:** The teacher-student ratio was extracted from the original data, which was in a descriptive format (e.g., "1 to 20").  This involved parsing the text and converting it to a numerical ratio (e.g., 20).  Ratios were standardized to represent the number of students per teacher.
*   **Format Conversion:** The extracted ratios were converted to a numerical format suitable for analysis and machine learning models.  This ensured consistency and compatibility with other datasets.

**3. Handling Missing Values:**

![heatmap](https://github.com/7arb25/Financial-Literacy-Program-Targeting-Analysis/blob/677ff6d368d90749cefff90030b6e2fcccc875c8/images/task1/null%20heatmap.jpg)

*   **Numerical Features:** Missing values in numerical features were imputed using the K-Nearest Neighbors (KNN) imputer.  This method imputes missing values based on the values of similar data points, preserving the overall data distribution better than simpler imputation methods like mean or median imputation.
*   **Categorical Features:** Two approaches were used to handle missing values in categorical features:
    *   **Deletion:** Rows with missing categorical values were removed.  This approach was used when the number of missing values was relatively small and their removal did not significantly impact the dataset size.
    *   **Constant Value Imputation:** Missing categorical values were replaced with a new constant value (e.g., "Unknown" or "Missing"). This allowed for the preservation of more data points, especially when missing values were more frequent.
 

![heatmap](https://github.com/7arb25/Financial-Literacy-Program-Targeting-Analysis/blob/677ff6d368d90749cefff90030b6e2fcccc875c8/images/task1/full%20heatmap.jpg)

**4. Outlier Handling:**

Three different methods were employed to identify and handle outliers in the financial literacy data:

*   **Interquartile Range (IQR) Method:** Outliers were identified as values falling outside 1.5 times the interquartile range (IQR) below the first quartile (Q1) or above the third quartile (Q3).
*   **Standard Deviation Method:** Outliers were defined as values falling outside two standard deviations from the mean.
*   **Visual Inspection:** Box plots and scatter plots were used to visually inspect the data and identify potential outliers.  This provided a qualitative assessment of outliers beyond the automated methods.

**5. Comparison of Categorical Imputation Methods:**

The impact of the two different methods for handling missing categorical values (deletion and constant value imputation) was analyzed. This involved comparing the results of subsequent analyses (e.g., linear regressions) performed on the datasets resulting from each method.  The comparison focused on:

*   **Dataset Size:** The number of data points retained after each method.
*   **Impact on Model Performance:** The effect of each method on the performance of linear regression models, as measured by metrics like R-squared and p-values.
*   **Bias Introduction:** Assessing if either method introduced any bias into the data.

This analysis helped determine the most appropriate strategy for handling missing categorical data in the context of this project.  The chosen method was then used for the final analysis.



### Data Analysis

#### Phase1:

I included on the project notebook tables and graphs about ,
Calculated average financial literacy scores for each demographic group.
Compared scores across different groups to identify statistically significant differences.
![table housing_income_vs_place](https://github.com/7arb25/Financial-Literacy-Program-Targeting-Analysis/blob/677ff6d368d90749cefff90030b6e2fcccc875c8/images/task1/table%20housing_income_vs_erea.jpg)

**Findings:**

1. **Overall Financial Literacy:**
the distribution are spreading across a wide range ‘there are a relatively large number of each bin or ground of the Financial Literacy Score’ that makes nearly ‘but not accurately ‘ uniform or at least if the number of bins was small’.
That made also the affection of outliers ‘even before removing them relatively low’
![distribution](https://github.com/7arb25/Financial-Literacy-Program-Targeting-Analysis/blob/677ff6d368d90749cefff90030b6e2fcccc875c8/images/task1/FLS%20destribution.jpg)
and coming to IQR understanding
![BoxPlot](https://github.com/7arb25/Financial-Literacy-Program-Targeting-Analysis/blob/677ff6d368d90749cefff90030b6e2fcccc875c8/images/task1/FLS%20barplot.jpg)

2. **Financial Literacy by Age Group:**
The smallest group in financial literacy scale is the people from 45/54.
Then the youths 18/24
![Age](https://github.com/7arb25/Financial-Literacy-Program-Targeting-Analysis/blob/677ff6d368d90749cefff90030b6e2fcccc875c8/images/task1/barplot%20agegroup.jpg)

3. **Financial Literacy by Household Income:**
I found that the worst scale was for the HIGH INCOME i supposed at first that's was because of missing values but after repeating it with exclusion of them i found the same results.

![Household](https://github.com/7arb25/Financial-Literacy-Program-Targeting-Analysis/blob/677ff6d368d90749cefff90030b6e2fcccc875c8/images/task1/barplot%20income.jpg)

4. **Financial Literacy by Education Level:**
People with Bachelor's degree ‘in general found to be at the bottom, but when merging another factors i found that this result is fault.
![Education](https://github.com/7arb25/Financial-Literacy-Program-Targeting-Analysis/blob/677ff6d368d90749cefff90030b6e2fcccc875c8/images/task1/barplot%20education.jpg)

5. **Financial Literacy by Location:**
Urban is the worst in the scale, but again that's just a rush conclusion.
![Location](https://github.com/7arb25/Financial-Literacy-Program-Targeting-Analysis/blob/677ff6d368d90749cefff90030b6e2fcccc875c8/images/task1/barplot%20eres.jpg)
6. **Combined Analysis:** 
With considering all factors i found that People which is at those combinations,
(Rural, low income , bachelor's degree , under 18)
Are the worst case ones.
Then the second combination, (Rural, middle income, bachelor's degree, under 18),
Then ( Rural, middle income, college, under 18)
Then (suburban , low income, graduat degree , from 18/24)
![table](https://github.com/7arb25/Financial-Literacy-Program-Targeting-Analysis/blob/677ff6d368d90749cefff90030b6e2fcccc875c8/images/task1/lower_FLS_table.jpg)

----
#### Phase2:

- To begin with the data had no missing values 
- The data had no outliers “as the Jupiter notebook attached demonstrates”
- The statistics “as we asked to provide are also at notebook as

![img alt](https://github.com/7arb25/Financial-Literacy-Program-Targeting-Analysis/blob/286ab705f2de2fb6ef230d9eb01c7e0f6de0947e/images/task2/Screenshot_%D9%A2%D9%A0%D9%A2%D9%A5-%D9%A0%D9%A2-%D9%A0%D9%A4-%D9%A2%D9%A0-%D9%A0%D9%A6-%D9%A3%D9%A2-%D9%A4%D9%A9_40deb401b9ffe8e1df2f1cc5ba480b12.jpg)

- I trained the ols model both by scaled and unscaled features and the both results was like

  ![img alt](https://github.com/7arb25/Financial-Literacy-Program-Targeting-Analysis/blob/286ab705f2de2fb6ef230d9eb01c7e0f6de0947e/images/task2/table%20ols%20summary.jpg)

### Code

The code used for data cleaning, analysis, and visualization is available in the `Main` directory:

i just mention some important notes

- one ways of outliers filtering

``` python
mean = df[num_cols].mean()
std = df[num_cols].std()

lower_bound = mean - 3 * std
upper_bound = mean + 3 * std
inliers_mask = ~((df[num_cols] < lower_bound) | (df[num_cols] > upper_bound)).any(axis=1)

df_inliers = df[inliers_mask]
df_outliers = df[~inliers_mask]
```
- Ols Summary Table

``` python
metric_pairs = [
        ('Total Score ', 'WalletLiteracy Score '),
        ('Total Score ', 'Financial Planning & Habits Rank '),
        ('WalletLiteracy Score ', 'Financial Knowledge & Education Rank ')
                ]

def report(df):
        results_summary = []
        for x, y in metric_pairs:
          X = df_scaled[x]
          y = df_scaled[y]
          X = sm.add_constant(X)
          model = sm.OLS(y, X).fit()
          results_summary.append({
          'Pair': f"{x} ~ {y}",
          'Coefficient': model.params[1],
          'Intercept': model.params[0],
          'P-Value': model.pvalues[1],
          'R-Squared': model.rsquared
        })
    

        summary_df = pd.DataFrame(results_summary)
        display(summary_df)
report(df)
```
- relationship detection

```python

for i in range(len(num_cols)):
    for j in range(i+1,len(num_cols)):
        col1=df[num_cols[i]]
        col2=df[num_cols[j]]

        if abs(col1.corr(col2))>0.4:
            print (f',relattionship between {num_cols[i]} and {num_cols[j]} are {col1.corr(col2)}')
```
- Modelling

```python
results ={}

model = LinearRegression()
model.fit(X, y)
y_pred = model.predict(X)
mse = mean_squared_error(y, y_pred)
results['LinearRegression'] = mse
```
- polynomial
``` python
from sklearn.preprocessing import PolynomialFeatures
poly = PolynomialFeatures(degree=2) 
X_poly = poly.fit_transform(X)
model = LinearRegression()
model.fit(X_poly, y)
y_pred = model.predict(X_poly)
mse = mean_squared_error(y, y_pred)
results['Polynomial Regression (degree 2)'] = mse
```
- SGD

``` python
model = SGDRegressor()
model.fit(X, y)
y_pred = model.predict(X)
mse = mean_squared_error(y, y_pred)
results['SGDRegressor'] = mse
```
- Random Forest

```python
from sklearn.ensemble import RandomForestRegressor
model = RandomForestRegressor()
model.fit(X, y)
y_pred = model.predict(X)
mse = mean_squared_error(y, y_pred)
results['RandomForestRegressor'] = mse
```
- Feature Importance

``` python
feature_importances = model.feature_importances_
importance_df = pd.DataFrame({'Feature': X.columns, 'Importance': feature_importances})
importance_df = importance_df.sort_values(by='Importance', ascending=False)
print("Feature Importances:")
print(importance_df)
```

### Results
 
- Total Score ~ Financial Planning & Habits Rank:
  1. Coefficient (-1.49): Indicates a negative correlation, meaning that as the Financial Planning & Habits Rank increases, the Total Score decreases.
  2. P-Value (0.002789): Statistically significant (< 0.05), confirming a meaningful relationship.
  3. R-Squared (0.1683): The model explains 16.83% of the variation in Total Score, indicating a weak correlation.

- Total Score ~ Financial Knowledge & Education Rank:
  1. Coefficient (-1.82): Suggests a negative correlation, implying that higher Financial Knowledge & Education Rank leads to a lower Total Score.
  2. P-Value (0.000165): Highly significant, suggesting a strong statistical relationship.
  3. R-Squared (0.2537): The model explains 25.37% of the variation in Total Score, showing a moderate correlation.
 
- WalletLiteracy Score ~ Financial Knowledge & Education Rank:
  1. Coefficient (-0.21): Indicates a weak negative correlation.
  2. P-Value (0.1302): Not statistically significant (> 0.05), meaning the relationship may be due to chance.
  3. R-Squared (0.0461): The model explains only 4.61% of the variation, indicating a very weak correlation.

----

1. The Total Score has a moderate negative correlation with Financial Knowledge & Education Rank and a weaker correlation with Financial Planning & Habits Rank.
2. The WalletLiteracy Score shows no significant correlation with Financial Knowledge & Education Rank.
3. The R-Squared values indicate that these models do not strongly explain the variability in the dependent variables, suggesting that additional factors influence financial literacy metrics.

### Recommendations

#### Phase 

1. `For the Under 18 Groups (Rural, Low/Middle Income, Bachelor's/Some College):` Focus on Foundational Skills: These individuals are likely still in high school or just starting college.
The focus should be on building a strong foundation in personal finance.
   - **Recommendation 1:** Partner with Rural Schools: Collaborate with high schools and community colleges in rural areas to integrate financial literacy into the curriculum. This could be through workshops, guest lectures, or even incorporating modules into existing courses like math or social studies.
   - **Recommendation2:** Age-Appropriate Content: Develop engaging, age-appropriate content that resonates with teenagers. This could include using gamification, interactive online tools, or real-life scenarios relevant to their experiences (e.g., budgeting for social activities, understanding part-time job paychecks, planning for college expenses).
   - **Recommendation 3:** Emphasize Long-Term Planning: While immediate needs are important, introduce the concept of long-term financial planning, including saving for college, understanding debt, and the basics of investing.
   - **Recommendation 4:** Utilize Technology and Online Resources: Given the rural location, online resources and webinars could be particularly effective in reaching this demographic. Create easily accessible online modules and interactive tools.
   - **Recommendation 5:** Peer-to-Peer Mentorship: Pair older students or young professionals with younger students to provide mentorship and guidance on financial matters.

2. `Specific Recommendations for the "Bachelor's Degree" Subgroup (Under 18):`
Address Misconceptions: The fact that these individuals are pursuing a bachelor's degree but still exhibit low financial literacy suggests a potential disconnect between academic pursuits and practical financial knowledge. Address common misconceptions about debt, student loans, and the value of different degrees in terms of career prospects and earning potential.

3. `For the 18-24 Group (Suburban, Low Income, Graduate Degree):`
Focus on Practical Application and Debt Management: This group is likely navigating early adulthood, including managing student loan debt, starting careers, and potentially starting families.

   - **Recommendation 1:** Workshops on Debt Management: Offer workshops specifically focused on managing student loans, credit card debt, and other forms of debt. Provide tools and resources for creating budgets and repayment plans.
   - **Recommendation 2:** Career and Financial Planning Integration: Connect financial literacy with career planning. Help them understand the financial implications of different career paths, salary negotiation, and benefits packages.
   - **Recommendation 3:** Focus on Investing and Saving: Introduce basic investment concepts and strategies for building long-term wealth. Emphasize the importance of saving and budgeting, especially given their low-income status.
   - **Recommendation 4:** Targeted Outreach to Graduate Programs: Partner with graduate programs in suburban areas to offer workshops and resources specifically tailored to the financial challenges faced by graduate students.
  
4. `Overarching Recommendations:`
   - **Tailored Messaging:** Develop targeted messaging that speaks to the specific needs and concerns of each demographic group.
   - **Measure and Evaluate:** 
Track the effectiveness of programs and make adjustments as needed. Collect data on program participation, changes in financial knowledge, and behavioral changes.
   - **Community Partnerships: **
Collaborate with local community organizations, libraries, and other institutions in rural and suburban areas to expand reach and access to programs.
   - **Financial Aid Awareness:** 
Emphasize awareness of available financial aid, scholarships, and grants to reduce the financial burden on low-income individuals pursuing higher education

- **Consider exploring additional variables that may better explain financial literacy rankings**.
- **Further analysis with multiple regression could help identify the strongest predictors.**
   



### Limitations
the analysis has few limitations duo to
1. handling missing values through

   - KNN Imputer for numerical features
   - missing categorical feature replacement with constant

2. the size of data wasn't sufficient



### References


- for extra informations about the effect of KNN Imputer please refer to that reference about the algorithm 
[Documentation](https://en.m.wikipedia.org/wiki/K-nearest_neighbors_algorithm)


- for extra informations about the implementation chick [sklearn](https://scikit-learn.org/stable/modules/generated/sklearn.impute.KNNImputer.html)

- reference for the used model [random Forest](https://en.m.wikipedia.org/wiki/Random_forest)
- reference about the implication [Random Forest](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.RandomForestClassifier.html)

### Contact

* **Analyst:** [Abdelrahman Harb](3bd0.g0m3aa@gmail.com)
* **LinkedIn:** [link](https://LinkedIn.com/in/3bd0g0m3aa)
* **InvestInMinds Foundation:**
   - [Ava Jerman - `CEO`](investinmindsfoundation@gmail.com)
   - [Rafi Ptashny - `Data Manager`](rafiptashny@gmail.com)

  
