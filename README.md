# <u>Measuring Holistic Lifestyles and Wellbeing</u>
## Synthetic Data-Driven Insights for Human-Centred Research 

*Measuring Holistic Lifestyles and Wellbeing* is a collaborative team analysis to address hypothetical research questions concerning holistic lifestyle and wellbeing factors. 

The project uses an end-to-end analytical approach by combining exploratory data analysis, statistical methods and machine learning to investigate relationships between lifestyle indicators and synthetic health scores, while examining the potential benefits, limitations and ethical implications of using data-driven insights to inform healthcare decisions.

## **<u>Stakeholder Summary</u>**

The analysis demonstrates how data analytics can identify patterns and evaluate predictive models while highlighting the limitations of reducing complex human wellbeing to a numerical score.

For stakeholders, *Measuring Holistic Lifestyles and Wellbeing*  illustrates the importance of transparent scoring methods, appropriate model evaluation and human oversight when interpreting health-related data. 

Although this project uses synthetic data to explore relationships between lifestyle factors and overall health scores, applying a similar approach to verified real-world data could help public health researchers identify health trends, healthcare providers understand behavioural risk factors, and wellbeing organisations develop targeted prevention programmes to address lifestyle-related health patterns.

## **<u>Dataset</u>**

**Dataset Used:** Holistic Health & Lifestyle Score Dataset 

**Source:** Kaggle - Synthetic datset supplied for educational and analytical usage. 

**License:** CC0 1.0 Universal

**Dataset Link:** https://www.kaggle.com/datasets/miadul/holistic-health-and-lifestyle-score-dataset

**Format:** CSV (Comma-Separated Values)

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

## **<u>Project Plan</u>**

**Data Collection** – A synthetic health and lifestyle dataset is loaded for analysis. Each record represents a simulated individual, with physical and lifestyle indicators alongside an Overall Health Score and categorical Health Status.

**Data Cleaning and Preperation** – Data integrity is assessed before analysis by inspecting the dataset's structure, standardising column names where necessary, checking data types, and validating missing values, duplicate records and numerical ranges. The overall health scores are checked against the supplied scoring formula. The validated dataset is exported for subsequent analysis.

**Exploratory Data Analysis (EDA)** – Relationships between lifestyle indicators and overall health scores are explored using Pandas, NumPy, Matplotlib and Seaborn. 

**Statistical Analysis** – Descriptive statistics and appropriate statistical tests are used to investigate differences and associations between lifestyle indicators and overall health scores.

**Feature Engineering** – The validated dataset is prepared for machine learning by selecting relevant lifestyle variables and defining the target variable. The relationship between the input variables, Overall Health Score and Health Status is examined to identify potential target leakage. Features are selected with consideration of the scoring methodology and the limitations of predicting a formula-derived outcome.

**Machine-Learning Model** – Select Machine-Learning model following EDA. Train/Test and evaluate model performance.

**Dashboard Creation** – An interactive dashboard presents the main findings through visualisations of lifestyle indicators, overall health score distributions and health-status categories. 

**Ethical Considerations** - Throughout the workflow, attention is given to the implications of reducing complex wellbeing to numerical scores. The project distinguishes between patterns within synthetic data and evidence derived from real populations, highlighting the limitations of formula-based scores, inferred health-status thresholds and predictive modelling. The findings are intended for educational and exploratory purposes, not clinical assessment or healthcare decision-making.

## Template Instructions

Welcome,

This is the Code Institute student template for the three Data Analytics capstone projects. We have preinstalled all of the tools you need to get started. It's perfectly okay to use this template as the basis for your project submissions. Click the `Use this template` button above to get started.

You can safely delete the Template Instructions section of this README.md file and modify the remaining paragraphs for your own project. Please do read the Template Instructions at least once, though! It contains some important information about the IDE and the extensions we use.

If you are working on the first capstone project, you can also delete `.python-version`, `.slugignore`, `Procfile` and `setup.sh` as they are only required for later dashboard projects. 

## How to use this repo

1. Use this template to create your GitHub project repo. Click the **Use this template** button, then click **Create a new repository**.

1. Copy the URL of your repository to your clipboard.

1. In VS Code, select **File** -> **Open Folder**.

1. Select your `vscode-projects` folder, then click the **Select Folder** button on Windows, or the **Open** button on Mac.

1. From the top menu in VS Code, select **Terminal** > **New Terminal** to open a new terminal.

1. In the terminal, type `git clone` followed by the URL of your GitHub repository. Then hit **Enter**. This command will download all the files in your GitHub repository into your vscode-projects folder.

1. In VS Code, select **File** > **Open Folder** again.

1. This time, navigate to and select the folder for the project you just downloaded. Then, click **Select Folder**.

1. A virtual environment is necessary when working with Python projects to ensure each project's dependencies are kept separate. You need to create your virtual environment, also called a venv, and then activate it whenever you return to your workspace.
Click the gear icon in the lower left-hand corner of the screen to open the Manage menu and select **Command Palette** to open the VS Code command palette.

1. In the command palette, type: *create environment* and select **Python: Create Environment…**

1. Choose **Venv** from the dropdown list.

1. Choose the Python version you installed earlier. Currently, we recommend Python 3.12.8

1. **DO NOT** click the box next to `requirements.txt`; you need to complete additional steps before installing your dependencies. Click **OK**.

1. You will see a `.venv` folder appear in the file explorer pane, indicating that the virtual environment has been created.

1. **Important**: Note that the `.venv` folder is in the `.gitignore` file so that Git won't track it.

1. Return to the terminal by clicking on the TERMINAL tab, or click on the **Terminal** menu and choose **New Terminal** if no terminal is currently open.

1. In the terminal, use the command below to install your dependencies. This may take several minutes.

 ```console
 pip3 install -r requirements.txt
 ```

1. Open the `jupyter_notebooks` directory, and click on the notebook you want to open.

1. Click the **Kernel** button, then choose **Python Environments**.

Note that the kernel says `Python 3.12.8` as it inherits from the venv, so it will be Python-3.12.8 if that is what is installed on your PC. To confirm this, you can use the command below in a notebook code cell.

```console
! python --version
```

## Deployment Reminders

* The `.python-version`, `.slugignore`, `Procfile` and `setup.sh` files are necessary only if you are deploying a Streamlit app to Heroku as part of your submission for units 2 and 3. 
* Set the `.python-version` Python version to a [Heroku-22](https://devcenter.heroku.com/articles/python-support#supported-runtimes) stack, currently supported version that most closely matches what you used in this project.
* The project can be deployed to Heroku using the following steps.

1. Log in to Heroku and create an App
2. At the **Deploy** tab, select **GitHub** as the deployment method.
3. Select your repository name and click **Search**. Once it is found, click **Connect**.
4. Select the branch you want to deploy, then click **Deploy Branch**.
5. The deployment process should happen smoothly if all deployment files are fully functional. Click the button **Open App** at the top of the page to access your App.
6. If the slug size is too large, then add large files not required for the app to the `.slugignore` file.
