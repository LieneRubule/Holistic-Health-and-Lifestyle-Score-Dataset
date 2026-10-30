# <u>Measuring Holistic Lifestyles and Wellbeing</u>
## Synthetic Data-Driven Insights for Human-Centred Research 

*Measuring Holistic Lifestyles and Wellbeing* is a collaborative team analysis to address hypothetical research questions concerning holistic lifestyle and wellbeing factors. 

The project uses an end-to-end analytical approach by combining exploratory data analysis, statistical methods and machine learning to investigate relationships between lifestyle indicators and synthetic health scores, while examining the potential benefits, limitations and ethical implications of using data-driven insights to inform healthcare decisions.

## **<u>Stakeholder Summary</u>**

The analysis demonstrates how data analytics can identify patterns and evaluate predictive models while highlighting the limitations of reducing complex human wellbeing to a numerical score.

For stakeholders, *Measuring Holistic Lifestyles and Wellbeing*  illustrates the importance of transparent scoring methods, appropriate model evaluation and human oversight when interpreting health-related data. 

Although this project uses synthetic data to explore relationships between lifestyle factors and overall health scores, applying a similar approach to verified real-world data could help public health researchers identify health trends, healthcare providers understand behavioural risk factors, and wellbeing organisations develop targeted prevention programmes to address lifestyle-related health patterns.

## **<u>Dataset</u>**

- **Dataset:** Holistic Health & Lifestyle Score Dataset
- **Creator:** Arif Miah (Kaggle username: miadul)
- **Source:** [Kaggle dataset page](https://www.kaggle.com/datasets/miadul/holistic-health-and-lifestyle-score-dataset)
- **Download date:** [26/10/2026]
- **Licence:** [CC0 1.0 Universal — Public Domain](https://creativecommons.org/publicdomain/zero/1.0/)

The licence permits copying, modification and redistribution. The creator and source are acknowledged for transparency.

**Columns:**
- <code>Physical_Activity</code> - Minutes of moderate to vigorous exercise per day (0–120)

- <code>Nutrition_Score</code> - Diet quality (0–10) based on nutrient density, balance and variety

- <code>Stress_Level</code> - Self-reported stress (1–10), where 10 = very high stress

- <code>Mindfulness</code> - Minutes per day spent in meditation, journaling, or mindful activity (0–60)

- <code>Sleep_Hours</code> - Average hours of sleep per night (3–10)

- <code>Hydration</code> - Liters of water consumed per day (0.5–5.0)

- <code>BMI</code> - Body Mass Index (18–40)

- <code>Alcohol</code> - Units of alcohol per week (0–20)

- <code>Smoking</code> - Cigarettes per day (0–30)

**Limits:** Dataset is synthetic. Its variable definitions, measurement scales and score metric method require verification. The analysis descibes patterns in the generated data and should not be interpreted as established relationships for real-world populations or used for individual health assessments. 

## **Hypothesis Research Questions**

The following research questions combine correlation analysis, statistical hypothesis testing, and predictive modelling to investigate relationships between lifestyle factors and overall health scores, assess differences between smoking groups, and evaluate the predictive performance of machine learning.

1. Is higher physical activity associated with a higher overall health score? The hypothesis is that higher physical activity is positively associated with overall health scores. This is investigated through correlation analysis to examine the direction and strength of the relationship between physical activity and overall health scores.

2. Is a higher nutrition score associated with a higher overall health score? The hypothesis is that higher nutrition scores are positively associated with overall health scores. Correlation analysis is used to investigate whether improvements in nutrition scores correspond to higher overall health scores within the dataset.

3. Do overall health scores differ between smoking and non-smoking groups? The hypothesis is that mean overall health scores differ between records with smoking values greater than zero and those with smoking values equal to zero. A two-sample statistical test, using Welch's t-test where appropriate, is applied to assess whether the observed difference in group means is statistically significant.

4. How accurately can lifestyle factors predict health-status categories, and which factors contribute most to the model's predictions? The hypothesis is that a machine-learning classifier using lifestyle factors can predict the Poor, Average, and Good health-status categories more accurately than a baseline model that always predicts the most common category. Model performance is evaluated using classification metrics and a confusion matrix, while feature importance analysis explores which lifestyle factors contribute most to the model's predictions.

**Ethical and methodological considerations:** The dataset is synthetic and represents a constructed scoring system rather than independently measured real-world health outcomes. Consequently, the findings describe patterns within the dataset and should not be interpreted as evidence of real-world causal relationships or as a validated method for assessing individual health. Overall health scores are excluded from the model's predictor variables because the health-status categories are derived from these scores. This helps avoid target leakage and ensures that the model evaluates the predictive contribution of lifestyle factors rather than directly using the information from which the target categories were created.

## **<u>Project Plan</u>**

**Data Collection** – A synthetic health and lifestyle dataset is loaded for analysis. Each record represents a simulated individual, with physical and lifestyle indicators alongside an Overall Health Score and categorical Health Status.

**Data Cleaning and Preperation** – Data integrity is assessed before analysis by inspecting the dataset's structure, standardising column names where necessary, checking data types, and validating missing values, duplicate records and numerical ranges. The overall health scores are checked against the supplied scoring formula. The validated dataset is exported for subsequent analysis.

**Exploratory Data Analysis (EDA)** – Relationships between lifestyle indicators and overall health scores are explored using Pandas, NumPy, Matplotlib and Seaborn. 

**Statistical Analysis** – Descriptive statistics and appropriate statistical tests are used to investigate differences and associations between lifestyle indicators and overall health scores.

**Feature Engineering** – The validated dataset is prepared for machine learning by selecting relevant lifestyle variables and defining the target variable. The relationship between the input variables, Overall Health Score and Health Status is examined to identify potential target leakage. Features are selected with consideration of the scoring methodology and the limitations of predicting a formula-derived outcome.

## **<u>Analysis Techniques Used</u>**

**Descriptive Statistics** — Numerical statistics, including means, medians, standard deviations and percentiles, are reviewed to understand the distribution of lifestyle variables and overall health scores. This helps identify potential anomalies, assess data quality and understand the characteristics of the dataset before statistical testing and predictive modelling.

**Correlation Analysis** - Examine the relationships between physical activity, nutrition and overall health scores. Group comparisons are also used to investigate differences in mean overall health scores between smoking and non-smoking records.

**Hypothesis Testing** — Pearson correlation is used to assess the direction and strength of the relationships between physical activity, nutrition and overall health scores. Welch's independent-samples t-test examines whether mean overall health scores differ between smoking and non-smoking groups. Holm adjustment is applied across the three primary tests to account for multiple comparisons, while Spearman correlations and a Mann–Whitney U test provide sensitivity checks. Statistical significance is evaluated using p-values, alongside confidence intervals and effect sizes, to support interpretation of the findings.

**Predictive Modelling** — A machine-learning classifier is used to investigate how effectively lifestyle variables predict the Poor, Average and Good health-status categories. Model performance is evaluated against a baseline classifier using classification metrics and a confusion matrix. Feature importance is examined to identify which variables contribute most to the model's predictions. Overall health scores are excluded from the predictors because the target categories are derived from these scores, reducing the risk of target leakage.

## **<u>Hypothesis Validation</u>**

The hypothesis testing explored whether physical activity and nutrition scores were associated with calculated overall health scores, and whether health scores differed between smoking groups. The analysis revealed statistically significant relationships across all three investigations, although the strength of these relationships varied.

Nutrition demonstrated a stronger positive association with overall health scores than physical activity. The comparison between smoking groups also revealed a substantial difference in mean scores. However, these findings must be interpreted in the context of a synthetic dataset in which overall health scores are calculated from lifestyle factors rather than independently measured health outcomes.

**Is higher physical activity associated with a higher overall health score?**

**Result:** Supported

**Summary:** Pearson correlation analysis identified a weak positive association between physical activity and overall health scores (r = 0.146, 95% CI: 0.127–0.165). This suggests that higher physical activity scores tend to correspond to higher overall health scores, although the relationship is relatively weak.

The findings indicate that physical activity is associated with the calculated health score within the dataset. However, the strength of this relationship should not be interpreted as evidence of its independent contribution to real-world health outcomes, particularly because the score is generated using a formula based on lifestyle factors.

**Is a higher nutrition score associated with a higher overall health score?**

**Result:** Supported

**Summary:** Pearson correlation analysis identified a stronger positive association between nutrition and overall health scores (r = 0.386, 95% CI: 0.369–0.402) than was observed for physical activity.

This suggests that nutrition scores have a closer statistical relationship with the calculated overall health score within the dataset. The difference between the two correlations highlights how individual lifestyle variables may relate differently to a composite measure of wellbeing.

Nevertheless, this association does not establish that nutrition independently causes higher health scores. Because the overall score is formula-based, the relationship may partly reflect how nutrition contributes to its calculation.

**Do overall health scores differ between smoking and non-smoking groups?**

**Result:** Supported

**Summary:** Welch's independent-samples t-test identified a statistically significant difference in mean overall health scores between non-smokers and smokers. Among the 10,000 records, 1,996 were classified as non-smokers (Smoking == 0) and 8,004 as smokers (Smoking > 0).

The mean overall health score was 84.84 for non-smokers and 76.58 for smokers, representing a difference of 8.26 points. The 95% confidence interval for the smoker-minus-non-smoker difference was −9.11 to −7.42, with t(3635.7) = −19.17 and p = 4.05 × 10⁻⁷⁸. Hedges' g = −0.43 indicated a moderate standardised difference between the groups.

These findings support the hypothesis that mean health scores differ between smoking groups within the dataset. However, the difference cannot establish that smoking caused lower scores, as the analysis examines a synthetic scoring system rather than independently measured health outcomes.

**Multiple testing and sensitivity analysis**

Holm adjustment was applied across the three primary statistical tests, and all three remained statistically significant after adjustment. Spearman correlations and a Mann–Whitney U test were also conducted as sensitivity checks, producing patterns consistent with the primary analyses.

These checks provide additional confidence that the observed statistical patterns are not dependent solely on the selected parametric tests. However, statistical robustness within a synthetic dataset does not establish that the relationships generalise to real-world populations.

### 🤖 Machine Learning Model Performance & Summary
* **Classification Pipeline (`Health_Status`):** Evaluated a baseline against Logistic Regression and Random Forest models using stratified 5-fold cross-validation. **Logistic Regression** emerged as the best-performing classifier, achieving a test accuracy of $96.55\%$ and a Macro F1-score of $0.9043$.
* **Regression Pipeline (`Overall_Health_Score`):** Evaluated models predicting the numerical health score. Both **Linear Regression** and **Random Forest Regressor** demonstrated strong predictive performance (Test $R^2 \approx 0.94$, RMSE $\approx 5.44$), with **Mindfulness**, **Smoking**, and **Nutrition_Score** identified as the primary feature drivers.
* **Dashboard Portability & Governance:** In accordance with team governance standards, binary model binaries (`.joblib`) were replaced by clean, portable CSV exports containing feature importances, scaler parameters, and evaluation metrics for dashboard integration.
* **Limitations & Ethics:** Because the dataset is synthetic, models learn the underlying scoring formula rather than real biological phenomena. Findings must be interpreted strictly as exploratory dashboard insights and do not constitute clinical or medical advice.

## <u>**Dashboard Creation**</u>

The Tableau dashboard was designed to communicate the findings of the exploratory data analysis and machine-learning investigation using a synthetic health and lifestyle dataset. A dedicated cover page introduces the project's research questions, analytical purpose and ethical considerations. Across the dashboards, explanatory text contextualises observed relationships, highlights differences between smoking groups, and communicates the limitations of predictive modelling.

The dashboard explores associations between physical activity, nutrition and overall health scores; examines distributions and trends across lifestyle score ranges; compares average health scores and health-status distributions between smokers and non-smokers; and evaluates the performance of classification models in predicting Poor, Average and Good health-status categories. Feature importance visualisations identify which variables contribute most to the model's predictions.

Together, these visualisations investigate how lifestyle variables relate to the dataset's formula-derived health scores and how effectively those patterns can be classified. Ethical disclosures emphasise that statistical associations do not establish causation, feature importance does not demonstrate causal influence, and model performance within synthetic data cannot be assumed to generalise to real-world populations. The dashboard is intended for educational and portfolio purposes, not medical advice or clinical decision-making.

#### **Dashboard Features**

- **Lifestyle association analysis:** Scatter plots and trend lines explore relationships between physical activity, nutrition and overall health scores.

- **Trends and distributions:** Line charts and histograms examine average health scores and record distributions across physical activity and nutrition score ranges.

- **Smoking-group comparison:** KPI cards compare average health scores for smokers and non-smokers, supported by a box plot and a health-status comparison table.

- **Classification model evaluation:** Bar charts compare model accuracy, while feature importance visualises the relative contribution of lifestyle variables to predictions.

- **KPI cards:** Highlight key numerical summaries, including average health scores for selected groups.

- **Interactive exploration:** Tooltips and dashboard interactions support closer examination of score ranges, health-status categories and observed patterns.

- **Ethical disclosure:** Dedicated explanatory text addresses synthetic data limitations, predictive reliability, potential bias, interpretation and responsible use.

- **User-centred design:** A consistent turquoise, orange and charcoal palette, clear typography, concise annotations and structured layouts support readability and visual comparison.

**Live Dashboard Link:** https://public.tableau.com/views/HolisticHealthLifestyleAnalysis/00-Coverpage

**Dashboard Pages**

**Cover Page — Measuring Holistic Health and Wellbeing**
Introduces the project's research questions, analytical purpose and ethical disclaimer, highlighting the use of synthetic data and the limitations of interpreting health-related patterns.

![Holistic Lifestyles and Wellbeing and Dashboard](tableau_dashboard/00-cover-page.jpeg)

**Page 1 — Let's Get Physical & Food for Thought**
Explore the relationships between physical activity, nutrition and overall health scores using scatter plots and trend lines. Examine how these lifestyle variables are associated with the dataset's formula-derived health scores, without assuming causal relationships.

![Holistic Lifestyles and Wellbeing and Dashboard](tableau_dashboard/01-correlation-analysis.jpeg)

**Page 2 — Trending Towards Wellbeing**
Examine average health scores and record distributions across physical activity and nutrition score ranges. KPI cards highlight average scores, while line charts and histograms reveal patterns within the synthetic dataset.

![Holistic Lifestyles and Wellbeing and Dashboard](tableau_dashboard/02-trends.jpeg)

**Page 3 — The Burning Question: Smoking and Health**
Compare average health scores between smokers and non-smokers using KPI cards, a box plot and a health-status comparison table. Explore differences in score distributions and the representation of Poor, Average and Good health-status categories.

![Holistic Lifestyles and Wellbeing and Dashboard](tableau_dashboard/03-smoking.jpeg)

**Page 4 — A Healthy Guess?**
Evaluate classification model performance in predicting Poor, Average and Good health-status categories. Compare model accuracy and examine feature importance to identify which lifestyle variables contribute most to predictions, while acknowledging the limitations of synthetic data and the risks of overinterpreting model results.

![Holistic Lifestyles and Wellbeing and Dashboard](tableau_dashboard/04-predictive-model.jpeg)

## **<u>Technologies Used</u>**

## **<u>Project Management</u>**

## **<u>Development Roadmap</u>**

## **<u>AI Usage</u>**

## **<u>Ethical Considerations</u>** 

The analysis demonstrates how statistical methods can identify relationships and differences within structured data, but it also highlights the limitations of interpreting numerical health scores without understanding how they were constructed.

The overall health score is calculated from lifestyle factors and capped at 100. Consequently, the observed correlations may partly reflect the mathematical relationships embedded in the scoring formula rather than independent relationships between lifestyle and health. Similarly, statistically significant differences between smoking groups should not be interpreted as evidence of causation or as a clinical assessment of individual health.

The dataset's synthetic nature is central to interpreting the findings. Although the results support all three hypotheses within this dataset, they do not establish clinical validity or demonstrate that the same patterns would occur in real populations.

Ultimately, the project highlights the distinction between identifying statistical patterns and establishing meaningful evidence about human wellbeing. Numerical scores can make complex information easier to analyse, but their interpretation depends on the assumptions, definitions and calculations underlying them. The findings are therefore intended for educational and exploratory purposes, not clinical assessment or healthcare decision-making.

## **<u>Acknowledgements</u>**

