# 📊 AI-Powered EDA Report Generator

> An intelligent Exploratory Data Analysis (EDA) application that automatically analyzes datasets, identifies data-quality issues, discovers statistical and correlation-based insights, performs business-focused GroupBy analysis, and generates a professional AI-powered EDA report using Google Gemini.

<p align="center">

[🚀 Live Demo](https://ai-powered-eda-report-generator-2ibmhfeuhulksiw6gvqemw.streamlit.app/) •
[📂 GitHub Repository](https://github.com/ay3944013-glitch/AI-Powered-EDA-Report-Generator)

</p>

---

## 🚀 Project Overview

**AI-Powered EDA Report Generator** is a Streamlit web application designed to simplify the Exploratory Data Analysis process.

Traditional EDA often requires analysts to manually inspect datasets, calculate statistics, identify missing values and duplicates, detect outliers, analyze correlations, and write a final report.

This project automates much of that workflow.

Users can upload a **CSV or Excel dataset**, run automated EDA, perform business-oriented GroupBy analysis, and generate an AI-powered report containing key insights and recommendations.

The application combines **Python-based data analysis with Generative AI** to transform raw datasets into structured analytical insights and a readable business report.

---

## ✨ Key Features

### 📁 Dataset Upload

* Upload CSV files
* Upload Excel files (`.xlsx`, `.xls`)
* Preview the uploaded dataset
* View dataset-level information
* Includes a default Titanic dataset for quick testing

### 🔍 Automated EDA

The application automatically performs:

* Missing-value analysis
* Duplicate-row detection
* Summary statistics
* Outlier detection
* Correlation analysis

EDA results are displayed in an interactive Streamlit interface.

### 📊 Business-Oriented GroupBy Analysis

Users can select:

* Numeric metric columns
* Categorical grouping columns

The application then performs GroupBy analysis to help identify business-level patterns across different categories.

The tool also suggests potentially relevant metric columns based on keywords such as:

`Sales`, `Revenue`, `Amount`, `Price`, `Profit`, `Income`, `Salary`, `Fare`, and `Cost`.

### 🤖 AI-Generated EDA Report

After the analytical pipeline is completed, the application creates a compact JSON summary and sends the relevant analytical information to **Google Gemini**.

The AI generates a structured report containing:

* Dataset Overview
* Data Quality Assessment
* Statistical Insights
* Correlation Analysis
* Outlier Analysis
* GroupBy Insights
* Business Recommendations
* Suggested Visualizations
* Conclusion

### 📥 Report Download

The generated report can be downloaded directly from the application as a Markdown (`.md`) file.

---

## 🧠 How It Works

```text
             ┌───────────────────┐
             │   Upload Dataset  │
             │   CSV / Excel     │
             └─────────┬─────────┘
                       │
                       ▼
             ┌───────────────────┐
             │ Dataset Overview  │
             └─────────┬─────────┘
                       │
                       ▼
             ┌───────────────────┐
             │ Automated EDA     │
             │                   │
             │ • Missing Values  │
             │ • Duplicates      │
             │ • Statistics      │
             │ • Outliers        │
             │ • Correlation     │
             └─────────┬─────────┘
                       │
                       ▼
             ┌───────────────────┐
             │ GroupBy Analysis  │
             │ Business Metrics  │
             └─────────┬─────────┘
                       │
                       ▼
             ┌───────────────────┐
             │ Compact JSON      │
             │ Summary           │
             └─────────┬─────────┘
                       │
                       ▼
             ┌───────────────────┐
             │ Google Gemini AI  │
             └─────────┬─────────┘
                       │
                       ▼
             ┌───────────────────┐
             │ Professional EDA  │
             │ Report            │
             └─────────┬─────────┘
                       │
                       ▼
             ┌───────────────────┐
             │ Download Markdown │
             │ Report            │
             └───────────────────┘
```

---

## 🛠️ Tech Stack

| Technology        | Purpose                             |
| ----------------- | ----------------------------------- |
| **Python**        | Core programming language           |
| **Streamlit**     | Interactive web application         |
| **Pandas**        | Data manipulation and analysis      |
| **NumPy**         | Numerical operations                |
| **Matplotlib**    | Data visualization                  |
| **Seaborn**       | Statistical visualization           |
| **Scikit-learn**  | Data-analysis / ML utilities        |
| **Google Gemini** | AI-powered report generation        |
| **OpenPyXL**      | Excel file processing               |
| **Python-dotenv** | Environment configuration           |
| **Git & GitHub**  | Version control and project hosting |

---

## 📂 Project Structure

```text
AI-Powered-EDA-Report-Generator/
│
├── 📁 data/
│   └── titanic.csv
│
├── 📄 app.py
├── 📄 streamlit_app.py
├── 📄 eda.py
├── 📄 ai_report.py
├── 📄 config.py
├── 📄 requirements.txt
├── 📄 .gitignore
│
└── 📁 output/
    ├── plots/
    ├── summary.json
    └── EDA_Report.md
```

### File Description

**`streamlit_app.py`**
Main Streamlit interface responsible for dataset upload, EDA execution, GroupBy analysis, AI report generation, and report download.

**`eda.py`**
Contains the core exploratory data analysis functions, including missing-value analysis, duplicate detection, summary statistics, outlier detection, correlation analysis, GroupBy analysis, and JSON summary generation.

**`ai_report.py`**
Handles preparation of the analytical summary, Gemini configuration, prompt generation, AI report generation, and saving the final report.

**`config.py`**
Stores application configuration such as the AI provider, Gemini model, dataset path, output paths, visualization settings, and outlier-detection parameters.

**`requirements.txt`**
Contains the Python dependencies required to run the project.

---

## ⚙️ Installation & Setup

### 1. Clone the Repository

```bash
git clone https://github.com/ay3944013-glitch/AI-Powered-EDA-Report-Generator.git
```

### 2. Navigate to the Project Directory

```bash
cd AI-Powered-EDA-Report-Generator
```

### 3. Create a Virtual Environment

```bash
python -m venv venv
```

Activate it on Windows:

```bash
venv\Scripts\activate
```

Activate it on macOS/Linux:

```bash
source venv/bin/activate
```

### 4. Install Dependencies

```bash
pip install -r requirements.txt
```

### 5. Configure Gemini API

The application requires a **Google Gemini API key** for AI-powered report generation.

You can enter the API key through the application's sidebar.

> 🔐 **Security:** Never commit your API key or other credentials to GitHub.

### 6. Run the Application

```bash
streamlit run streamlit_app.py
```

---

## 🧪 How to Use

### Step 1 — Upload Dataset

Upload a CSV or Excel dataset using the sidebar.

You can also use the included Titanic dataset for testing.

### Step 2 — Load Dataset

Click **`Load Dataset`**.

The application displays a preview and dataset overview.

### Step 3 — Run EDA

Click **`Run EDA Analysis`**.

The application performs:

* Missing-value analysis
* Duplicate detection
* Statistical analysis
* Outlier detection
* Correlation analysis

### Step 4 — Perform GroupBy Analysis

Select:

* Numeric metric columns
* Categorical grouping columns

Then click **`Run GroupBy Analysis`**.

### Step 5 — Create AI Input Summary

Click **`Create JSON Summary`**.

This creates a compact analytical summary used as input for the AI report-generation stage.

### Step 6 — Generate AI Report

Enter your Gemini API key and click **`Generate AI Report`**.

Gemini analyzes the prepared EDA summary and generates a structured professional report.

### Step 7 — Download Report

Click **`Download Report`** to download the generated Markdown report.

---

## 📑 Generated Report Structure

```text
# Dataset Overview

# Data Quality Assessment

# Statistical Insights

# Correlation Analysis

# Outlier Analysis

# GroupBy Insights

# Business Recommendations

# Suggested Visualizations

# Conclusion
```

---

## 💡 Example Use Cases

This tool can be useful for:

* 📊 Data Analysts
* 📈 Business Analysts
* 🎓 Students learning EDA
* 🧑‍💻 Data Science projects
* 🔎 Exploratory dataset investigation
* 📋 Automated analytical reporting
* 💼 Business insight generation

---

## 🎯 Project Objectives

1. Automate repetitive EDA tasks.
2. Reduce the time required for initial dataset investigation.
3. Identify important data-quality issues.
4. Discover statistical and correlation-based patterns.
5. Add business-oriented GroupBy analysis.
6. Use Generative AI to convert analytical results into a readable report.
7. Provide a simple interface for users who may not want to write EDA code manually.

---

## 🔮 Future Improvements

* [ ] Automatic visualization generation
* [ ] PDF report export
* [ ] PowerPoint report generation
* [ ] Advanced feature engineering suggestions
* [ ] Automated data-cleaning recommendations
* [ ] More AI model providers
* [ ] Interactive dashboards
* [ ] Natural-language dataset querying
* [ ] Automated chart recommendations
* [ ] Statistical hypothesis testing
* [ ] Machine-learning model suggestions
* [ ] Improved report customization

---

## ⚠️ Limitations

* AI-generated insights should be reviewed before being used for important business decisions.
* The quality of AI recommendations depends on the quality and structure of the dataset.
* A valid Gemini API key is required for AI report generation.
* Very large datasets may require additional optimization depending on available system resources.

---

## 🔐 Security

API keys should **never be hard-coded into the repository or committed to GitHub**.

For local development, use environment variables or enter the API key through the application's secure password input.

If an API key is accidentally exposed, revoke it and generate a new one.

---

## 🌐 Live Demo

### 🚀 [Launch AI-Powered EDA Report Generator](https://ai-powered-eda-report-generator-2ibmhfeuhulksiw6gvqemw.streamlit.app/)

Try the application directly in your browser.

---

## 📂 Source Code

### [View Project on GitHub](https://github.com/ay3944013-glitch/AI-Powered-EDA-Report-Generator)

---

## 📌 Project Highlights

> **Raw Dataset → Automated EDA → Business Analysis → AI Insights → Professional Report**

This project demonstrates practical skills in:

**Python • Pandas • Data Analysis • Exploratory Data Analysis • Data Visualization • Streamlit • Generative AI • Business Analytics • GitHub**

---

## 👨‍💻 Author

**Ayush**

Aspiring Data Analyst passionate about Data Analytics, Python, SQL, Business Intelligence, and AI-powered analytical solutions.

### GitHub

[@ay3944013-glitch](https://github.com/ay3944013-glitch)

---

## ⭐ Support

If you find this project useful, consider giving the repository a ⭐ on GitHub.

Your feedback and suggestions are welcome!

---

### 📄 License

This project is available for educational and portfolio purposes.
