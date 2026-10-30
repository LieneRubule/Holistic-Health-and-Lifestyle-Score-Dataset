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

EDA and HYPOTHESIS TESTING

## **<u>Hypothesis Validation</u>**

For each research question EDA and HYPOTHESIS TESTING

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

Throughout the analytical workflow, attention is given to the ethical implications of reducing complex health and wellbeing outcomes to numerical scores. The project distinguishes between patterns identified within a synthetic dataset and evidence derived from real-world populations, acknowledging the limitations of formula-based health scores, predefined health-status thresholds, and predictive modelling. 

Feature importance is interpreted in the context of the dataset's underlying scoring system, rather than as evidence of causal relationships or clinically significant factors. The findings are intended for educational and exploratory purposes only and should not be used for clinical assessment, individual health profiling, or healthcare decision-making.

## **<u>Acknowledgements</u>**

