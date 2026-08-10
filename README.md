# SpaceX Falcon 9 First-Stage Landing Prediction

An end-to-end data science and machine learning project analyzing SpaceX Falcon 9 launch data to investigate the factors associated with successful first-stage landings and develop a predictive model for landing outcomes.

This project was completed as the final project for the **IBM Data Science Professional Certificate – Applied Data Science Capstone**.

---

## Project Overview

The cost of launching rockets is strongly influenced by whether the first stage can be recovered and reused. This project analyzes historical Falcon 9 launch data to understand launch and landing patterns and to develop a machine learning model capable of predicting first-stage landing outcomes.

The project follows a complete data science workflow:

**Data Collection → Data Wrangling → Exploratory Data Analysis → SQL Analysis → Interactive Visualization → Machine Learning → Dashboard**

The repository contains the executed notebooks, supporting datasets, SQL database, interactive dashboard application, and final project presentation.

---

## Business Problem

SpaceX's ability to recover and reuse Falcon 9 first stages is an important component of its launch economics.

The objective of this project is to use historical launch data to:

* Analyze launch and landing patterns.
* Identify variables associated with successful first-stage landings.
* Explore the relationship between launch characteristics and landing outcomes.
* Build a machine learning model to predict whether a Falcon 9 first stage will successfully land.

---

## Objective

The primary objective is to develop a data-driven understanding of Falcon 9 first-stage landing success and use machine learning to predict landing outcomes.

The project combines:

* Data collection through APIs and web scraping.
* Data cleaning and transformation.
* Exploratory data analysis.
* SQL-based analysis.
* Interactive visual analytics.
* Geospatial analysis using Folium.
* Machine learning classification.
* An interactive Plotly Dash dashboard.

---

## Dataset

The analysis uses SpaceX Falcon 9 launch data collected and processed during the project.

The repository includes:

* API-collected launch data.
* Web-scraped launch information.
* Processed CSV datasets used by the dashboard and geospatial analysis.
* A SQLite database used for SQL-based exploratory analysis.

Supporting data files currently included in the repository are:

* `spacex_launch_dash.csv`
* `spacex_launch_geo.csv`
* `my_data1.db`

---

# Data Science Workflow

## 1. Data Collection

Launch data was collected using two complementary approaches:

### SpaceX API

The project uses API-based data collection to retrieve structured launch information.

Notebook:

`Data-Collection-API.ipynb`

### Web Scraping

Additional launch information was collected through web scraping.

Notebook:

`Data-Collection-with-Web-Scrapping.ipynb`

---

## 2. Data Wrangling

The collected data was cleaned and transformed into a format suitable for exploratory analysis and machine learning.

The data-wrangling stage prepares the launch records for:

* Exploratory data analysis.
* SQL analysis.
* Visualization.
* Machine learning.

Notebook:

`Data-Wrangling.ipynb`

---

## 3. Exploratory Data Analysis

Exploratory analysis was performed to investigate relationships between launch characteristics and first-stage landing outcomes.

The project uses visual analysis to examine launch patterns and relationships among relevant variables.

Notebook:

`Complete-the-EDA-with-Visualization.ipynb`

---

## 4. SQL Analysis

SQL was used to query the launch dataset and investigate relationships and patterns using a relational database.

The analysis demonstrates practical use of:

* SQL queries.
* Filtering.
* Aggregation.
* Grouping.
* Ordering.
* Relational data analysis.

Notebook:

`Complete-the-EDA-with-SQL.ipynb`

Database:

`my_data1.db`

---

## 5. Interactive Visualization

Interactive visual analytics were used to explore the geographic and operational characteristics of Falcon 9 launches.

### Folium

Folium was used for geospatial analysis and visualization of launch sites and related launch information.

Notebook:

`Interactive-Visual-Analytics-with-Folium.ipynb`

---

## 6. Machine Learning

Machine learning was used to predict Falcon 9 first-stage landing outcomes.

The workflow includes:

1. Preparing the machine learning dataset.
2. Defining the prediction target.
3. Splitting the data into training and testing sets.
4. Training classification models.
5. Evaluating model performance.
6. Comparing model results.
7. Selecting the best-performing model.

Notebook:

`Complete-the-Machine-Learning-Prediction.ipynb`

### Machine Learning Results

The machine learning analysis compares multiple classification approaches and evaluates their ability to predict first-stage landing success.

Recommended results to display:

| Metric                |                             Result |
| --------------------- | ---------------------------------: |
| Best-performing model |                      Decision Tree |
| Test accuracy         |                              94.4% |
| Precision             |                              92.3% |
| Recall                |                               100% |
| F1 score              |                                96% |

---

## 7. Dashboard

An interactive dashboard was developed using **Plotly Dash** to allow users to explore Falcon 9 launch data interactively.

The dashboard provides interactive visual analysis of launch characteristics and landing outcomes.

Application:

`Build-an-Interactive-Dashboard-with-Plotly-Dash.py`

---

# Key Findings

The analysis investigates several aspects of Falcon 9 launch and landing performance, including:

* Launch history and temporal patterns.
* Launch-site characteristics.
* Payload and mission characteristics.
* Relationships between launch variables and landing outcomes.
* Geographic characteristics of launch sites.
* Machine learning predictions of first-stage landing success.

---

# Technologies

The project uses the following technologies and tools:

### Programming

* Python
* SQL

### Data Collection

* REST API
* Web Scraping

### Data Analysis

* Pandas
* NumPy
* SQL / SQLite

### Visualization

* Matplotlib
* Seaborn
* Plotly
* Folium

### Machine Learning

* Scikit-learn

### Dashboard

* Plotly Dash

### Development Environment

* Jupyter Notebook
* Git
* GitHub

---

# Repository Structure

```text
applied-data-science-capstone/
│
├── README.md
│
├── data/
│   ├── DATABASE/
│   │   └── my_data1.db
│   │
│   └── processed/
│       ├── spacex_launch_dash.csv
│       └── spacex_launch_geo.csv
│
├── notebooks/
│   ├── 01-data-collection-api.ipynb
│   ├── 02-data-collection-web-scraping.ipynb
│   ├── 03-data-wrangling.ipynb
│   ├── 04-eda-sql.ipynb
│   ├── 05-eda-visualization.ipynb
│   ├── 06-folium-geospatial-analysis.ipynb
│   └── 07-machine-learning-prediction.ipynb
│
├── dashboard/
│   ├── app.py
│   └── README.md
│
├── reports/
│   └── presentation/
│       └── capstone-presentation.pdf

```

---

# How to Run

## 1. Clone the repository

```bash
git clone https://github.com/farturo93/applied-data-science-capstone.git
cd applied-data-science-capstone
```

## 2. Create a Python environment

```bash
python -m venv .venv
```

Activate the environment:

### Windows

```bash
.venv\Scripts\activate
```

### macOS / Linux

```bash
source .venv/bin/activate
```

## 3. Install dependencies

```bash
pip install pandas numpy matplotlib seaborn plotly folium scikit-learn requests beautifulsoup4 dash jupyter
```

## 4. Launch Jupyter Notebook

```bash
jupyter notebook
```

Execute the notebooks in the following order:

```text
01. Data Collection - API
02. Data Collection - Web Scraping
03. Data Wrangling
04. EDA with SQL
05. EDA with Visualization
06. Interactive Visual Analytics with Folium
07. Machine Learning Prediction
```

## 5. Run the dashboard

```bash
python Build-an-Interactive-Dashboard-with-Plotly-Dash.py
```

The dashboard requires the supporting CSV data included in the repository.

---

# Results / Presentation

The complete project presentation is available in:

**`Applied Data Science Capstone.pdf`**

The presentation summarizes the project methodology, exploratory analysis, interactive visualizations, machine learning workflow, results, and conclusions.

---

# Future Improvements

This project can be extended beyond the original Coursera capstone into a more production-oriented machine learning system.

Potential improvements include:

* Refactoring reusable analysis code into Python modules.
* Adding automated tests.
* Improving feature engineering.
* Performing more systematic hyperparameter optimization.
* Packaging the machine learning model as a REST API.
* Containerizing the application with Docker.
* Deploying the model and dashboard to the cloud.
* Adding CI/CD.
* Adding model monitoring and reproducibility tooling.

These improvements would extend the project from a data-science capstone into an end-to-end machine learning engineering project.

---

## Author

**Fernando Arturo Araiza Sixtos, PhD**

Data Science • Machine Learning • AI • Computer Vision

[GitHub](https://github.com/farturo93)
