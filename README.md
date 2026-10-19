# AI Usage and Impact on Students and Professionals

**Exploratory Data Analysis of AI Usage Among Students and Professionals**

**Team:** Amelia, Jerome, Kazuko, Sahil

**Course:** AI Methods I – Day 1: Data Cleaning and EDA (IAAC MaAI 2026/27)

## Use case

Artificial intelligence is increasingly integrated into educational and professional workflows, yet its relationship with productivity, efficiency, and user satisfaction remains unclear. This project uses data cleaning and exploratory data analysis (EDA) to investigate AI usage patterns among students and professionals, examining productivity scores, time savings, satisfaction, and associated costs. By comparing different user groups, AI tools, and purposes of use, the analysis identifies patterns and relationships that may inform more effective AI adoption. These findings also provide a starting point for considering AI’s potential role in architectural education and built-environment workflows, although the dataset is not specific to these fields.

## Research questions

The project investigates eight research questions:

1. AI usage and outcomes: Are more daily AI-use hours associated with higher productivity scores, satisfaction, accuracy ratings, or time saved?
2. Students vs. professionals: Do students and professionals report different usage, time savings, costs, or ratings?
3. AI purpose and outcomes: Do people using AI for studying, coding, writing, or research report different productivity or satisfaction scores?
4. AI tools and ratings: Do reported outcomes vary by the AI tool used?
5. AI usage and cost: Are more AI-usage hours associated with higher monthly AI costs?
6. Income and AI cost: Does monthly AI cost vary with monthly income?
7. Ratings and recommendations: Are people with higher satisfaction, accuracy, or productivity scores more likely to recommend AI?
8. Background and usage: Do usage patterns differ by age, education level, profession, or country?

The notebook explores all eight research questions through descriptive statistics, visualizations, and correlation analysis. The findings identify patterns and associations rather than establishing causal relationships.

## Dataset

### Primary dataset

	
| Field | Details |
|---|---|
| Name | AI Usage and Impact on Students and Professionals |
| Source | [Kaggle – AI Usage and Impact on Students and Professionals](https://www.kaggle.com/datasets/eishatuzzuhra/ai-usage-and-impact-on-students-and-professionals) |
| Description | AI usage patterns and reported outcomes among students and professionals |
| Format | CSV |
| Rows × columns (raw) | 300 rows x 19 columns |
| Unit of observation | One record representing a student or professional respondent |
| Licence | [Creative Commons CC0 1.0 Universal](https://creativecommons.org/publicdomain/zero/1.0/) |

The dataset includes variables such as AI usage hours per day, AI tools, AI purpose, productivity score, accuracy rating, satisfaction score, weekly time saved, monthly AI cost, income, and user type.

## Repository structure

The repository is organized as follows:

```text
1-day-assignment/
├── AI_Usage_and_Impact_on_Students_and_Professionals.csv
├── clean_data_AI_Usage_and_impact_on_students_and_professors.ipynb
├── figures/
│   ├── Fig.01_missing_values.png
│   ├── Fig.02_daily_AI_usage_hour_vs_productivity_score.png
│   ├── Fig.03_daily_AI_usage_vs_time_saved_per_week.png
│   ├── Fig.04_AI_usage_vs_time_saved.png
│   ├── Fig.06_AI_use_reported_outcome.png
│   ├── Fig.07_ave_productivity_score.png
│   ├── Fig.08_daily_AI_use_monthly_AI_cost.png
│   └── Fig.09_monthly_income_monthly_AI_cost.png
├── data/
│   └── .gitkeep
├── notebook/
│   └── .gitkeep
├── .gitignore
├── LICENSE
├── README.md
└── requirements.txt
```

### File and folder descriptions

- **Main CSV:** Dataset used for cleaning and exploratory analysis.
- **Jupyter notebook:** Contains the Python code, data cleaning, analysis, visualizations, and interpretations.
- **`figures/`:** Contains eight exported visualizations.
- **`data/`:** Placeholder directory maintained using `.gitkeep`.
- **`notebook/`:** Placeholder directory maintained using `.gitkeep`.
- **`.gitignore`:** Specifies files and folders Git should ignore.
- **`requirements.txt`:** Lists the Python dependencies required to run the notebook.
- **`LICENSE`:** Contains the repository's MIT License.
- **`README.md`:** Documents the project, methodology, findings, limitations, and AI usage.
  
## How to run

### Requirements

- Python 3.12
- Git
- VS Code with Python and Jupyter extensions, or Jupyter Notebook

Clone the repository:

```bash
git clone https://github.com/iaac-maai/1-day-assignment.git
cd 1-day-assignment
```

Create a virtual environment:

```bash
python -m venv .venv
```

Activate the environment.

**Windows:**

```bash
.venv\Scripts\activate
```

**macOS/Linux:**

```bash
source .venv/bin/activate
```

Install the dependencies:

```bash
python -m pip install -r requirements.txt
```

Open `clean_data_AI_Usage_and_impact_on_students_and_professors.ipynb` from the repository root, select the `.venv` kernel, and run all cells.

**Execution and reproducibility:** The notebook has been successfully executed by the team, including data cleaning, exploratory analysis, and visualisation generation. It uses relative paths and loads AI_Usage_and_Impact_on_Students_and_Professionals.csv from the repository root. The required dependencies are listed in `requirements.txt`.

## Data quality summary

The dataset initially contained **300 records and 19 columns**. After identifying and removing **12 exact duplicate rows**, 288 records remained for exploratory data analysis.

| Check | Result | Action taken |
|---|---|---|
| Duplicate records | 12 exact duplicates | Removed, leaving 288 records |
| Missing values | Missing observations detected | Counted and visualized; no dedicated imputation performed |
| Numeric inconsistencies | Some numerical values contained text, units, or currency symbols | Converted relevant fields into numeric formats |
| Outliers | Unusual values identified in AI usage and time saved | Flagged using the interquartile range (IQR) method for review |
| AI tool names | Inconsistent naming conventions | Standardized tool names |
| Education and country labels | Different representations of the same categories | Standardized labels |
| Age | Age values required conversion for demographic analysis | Created `Age_numeric` and `Age_Group` for analysis |

The analysis uses the available observations for each comparison. Missing values were not systematically imputed, and flagged outliers were not automatically removed.

## Exploratory Data Analysis

The exploratory data analysis (EDA) investigates patterns, differences, and relationships in AI usage among students and professionals. The notebook explores eight research questions using descriptive statistics, visualizations, group comparisons, and correlation analysis.

The analysis includes:

- **Descriptive statistics:** Counts, averages, and medians for AI usage, productivity, satisfaction, accuracy, time saved, and monthly AI costs.
- **Univariate analysis:** Examination of individual variables, including AI usage hours and reported outcomes.
- **Bivariate analysis:** Relationships between daily AI usage, productivity scores, weekly time saved, and monthly AI costs.
- **Grouped comparisons:** Differences between students and professionals, AI purposes, and AI tools.
- **Demographic analysis:** Comparisons across age groups, education levels, professions, and countries.
- **Correlation analysis:** Measurement of the strength and direction of selected numerical relationships.

The findings are presented through tables, charts, and written interpretations in the notebook. All reported relationships are observational and do not establish causation.

## Key findings

The following findings are based on the saved outputs of our exploratory data analysis (EDA). They describe associations, not causal relationships.

1. **AI usage and productivity:** Daily AI-use hours and productivity scores show a positive correlation (r = 0.660; n = 267).
2. **AI usage and time saved:** Daily AI-use hours and reported weekly time saved are positively correlated (r = 0.775; n = 271). This association is stronger among students (r = 0.923; n = 143) than professionals (r = 0.608; n = 128), although statistical significance of this difference has not been established.
3. **Students versus professionals:** Students average 3.01 hours of AI use per day compared with 2.87 hours for professionals. Students report 6.04 hours saved per week versus 5.55 hours for professionals. Average productivity scores are similar: 5.19 for students and 5.28 for professionals.
4. **AI purpose and productivity:** Office Work has the highest reported average productivity score (5.95), followed by Customer Support (5.56), while Coding has a lower average (4.94). Some categories have small sample sizes, limiting generalization.
5. **AI usage and costs:** Daily AI-use hours show almost no linear correlation with monthly AI cost (r = 0.034). Monthly income and AI cost also show almost no linear relationship (r = -0.053).
6. **Recommendation and satisfaction:** Respondents who would recommend AI report higher average productivity, satisfaction, and accuracy ratings than those answering Maybe or No.

Overall, greater AI use is associated with higher self-reported productivity and time savings in this dataset. The results do not demonstrate that AI usage causes these improvements.

### Figures

The notebook includes exported visualizations in the figures/ directory.

**Figure 1 — Missing values across dataset columns**

![Percentage of missing values by column](https://raw.githubusercontent.com/iaac-maai/1-day-assignment/main/figures/Fig.01_missing_values.png)

This visualization shows the percentage of missing observations across dataset columns. Missing values were inspected but were not specifically treated during the cleaning process.

**Figure 2 — AI usage and productivity**

![AI usage hours versus productivity](https://raw.githubusercontent.com/iaac-maai/1-day-assignment/main/figures/Fig.02_daily_AI_usage_hour_vs_productivity_score.png)

The analysis reports a positive correlation between daily AI usage and productivity scores (r = 0.660). This is an association, not evidence of causation.

Additional visualizations are available in the figures/ directory.


## Limitations

- **Self-reported data:** Productivity, satisfaction, accuracy, and time savings are based on participants' own assessments and may contain reporting bias.
- **Correlation is not causation:** The observed relationships do not establish that AI usage directly improves productivity or saves time.
- **Sample representativeness:** The dataset may not represent the wider population of students and professionals.
- **Missing values:** Missing observations were identified but not imputed. Different analyses therefore use different numbers of valid responses.
- **Outliers:** Unusually high values, including a reported 23 hours of AI usage per day, may influence the results. Flagged outliers were not automatically removed.
- **Small sample groups:** Some AI purposes, professions, and demographic categories contain relatively few responses, limiting the reliability of comparisons.
- **Built-environment relevance:** The dataset covers students and professionals across multiple fields. Its findings cannot automatically be generalized to architecture, engineering, or construction.
- **Dataset provenance:** The original sampling methodology and collection conditions still need to be verified.

### Ready for modelling

The completed exploratory data analysis provides a foundation for potential future machine learning applications, such as predicting productivity scores, time savings, satisfaction, or willingness to recommend AI.

Before developing a predictive model, further preparation would be required:

- **Target selection:** Define the specific outcome the model should predict.

- **Missing data:** Determine an appropriate strategy for handling missing observations.

- **Feature preparation:** Encode categorical variables and select relevant predictors.

- **Outlier assessment:** Review unusual values and their potential influence on model performance.

- **Model validation:** Split the data into training and testing sets, prevent data leakage, and evaluate predictive performance.

**Current status:** Data cleaning and exploratory analysis have been completed. No predictive machine learning model has been trained or evaluated as part of this assignment.

## AI usage disclosure

AI tools were used as assistants during the development and documentation of this project. The team remained responsible for reviewing the outputs and completing the assignment.

| Field | Details |
|---|---|
| Tools | GitHub Copilot (VS Code) and ChatGPT (OpenAI) |
| Why | To support understanding Python code, data cleaning, troubleshooting, GitHub workflows, documentation, and assignment requirements |
| Where | Python notebook development and data cleaning; README drafting and revision; repository organization and submission preparation |
| How | GitHub Copilot assisted a team member in understanding Python operations and implementing data-cleaning steps. ChatGPT assisted another team member with interpreting assignment instructions, navigating GitHub, structuring and refining the README, and checking documented findings against the notebook |
| Verification | The team executed the notebook, reviewed its outputs, and checked the README against the implemented code and reported results |

### Example AI prompts and interactions

**GitHub Copilot (VS Code):**
- Used to understand Python code and assist with data-cleaning operations.
- Assisted with identifying and resolving coding issues during notebook development.

**ChatGPT (OpenAI):**
- "Review our IAAC AI Methods I assignment requirements and help structure a README that follows the professor's instructions."
- "Check the main notebook code and verify that the README accurately describes the cleaning steps, missing values, and age analysis."
- "Help organize the GitHub repository and prepare the documentation for submission."

### Reflection

AI assistance helped the team understand unfamiliar coding and GitHub workflows, troubleshoot issues, and improve the clarity of the project documentation. However, AI-generated suggestions required verification against the actual Python notebook, dataset, and assignment instructions.

The team takes responsibility for the final code, analysis, findings, documentation, and submission.

## License

The original project code and documentation are covered by the MIT License included in this repository.

The dataset, **AI Usage and Impact on Students and Professionals**, was obtained from Kaggle and is distributed under the [Creative Commons CC0 1.0 Universal (Public Domain Dedication)](https://creativecommons.org/publicdomain/zero/1.0/) licence.

**Dataset source:** [eishatuzzuhra – Kaggle](https://www.kaggle.com/datasets/eishatuzzuhra/ai-usage-and-impact-on-students-and-professionals)

CC0 permits copying, modification, redistribution, and commercial use without requiring attribution. The original dataset creator is credited here for academic transparency.

---

IAAC – AI Methods I | Day 1: Data Cleaning and Exploratory Data Analysis | Group 1
