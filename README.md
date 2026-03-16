# STA 141B Final Project: Factors Driving Success on Steam: A Data-Driven Analysis

## Project Overview
This repository contains the code and data for the STA 141B final project in Winter 2026 UCdavis. The study focuses on analyzing Steam store data to explore the underlying relationships between game metadata, user review sentiments, discount behavior, and commercial performance (e.g., game sales or ownership). Advanced machine learning algorithms and natural language processing techniques are applied to extract features and construct predictive models.

## Repository Structure
The repository is organized into several modules, separating data preprocessing, exploratory data analysis (EDA), and final model training:

* **`sample data/`**: Code for fetching initial sample data (`sample data.ipynb`) and sample data of Cyberpunk 2077 
(`sample_app_data.json`), use for generating project ideas.

* Data used in this project:

  * `1000games.ipynb`: Notebook for fetching, filtering, cleaning a specific subset of 1000 representative games.
  * `steam_1000.jsonl`: The cleaned dataset comprising the subset of 1000 games.

* **`part1/`**: Files using in part 1
  * `part1.ipynb`: all coding, containging feching data from SteamSpy, data preprocessing, model training and virtualization
  * `steam_with_owners.jsonl`: dataset used in this part, integrating data from `steam_1000.jsonl` and game owner range data from SteamSpy

* **`Q2.ipynb` & `Question 3.ipynb`**: Modular Jupyter Notebooks addressing specific research questions (Question 2 and Question 3) defined in the project scope.

## Methodology
1.  **Data Collection & Engineering**: Data extraction leveraging Steam App IDs, and scraping owner range data from SteamSpy, followed by data cleaning and missing value imputation.
2.  **Natural Language Processing (NLP)**: Implementation of Term Frequency-Inverse Document Frequency (TF-IDF) via `scikit-learn`. This step vectorizes textual review data while applying threshold filters (e.g., maximum document frequency) to prevent overfitting and optimize computational efficiency.
3.  **Predictive Modeling**: Utilization of eXtreme Gradient Boosting (XGBoost) to construct an ensemble learning model. The algorithm is trained to minimize the regularized objective function, capturing complex nonlinear relationships within the features.

## Usage and Replication
To reproduce the analysis, execute the notebooks in the following sequence:
1.  Execute `1000games.ipynb` to generate the core dataset (`steam_1000.jsonl`).
2.  Navigate to the `part1/` directory and run `part1.ipynb` for data preprocessing and model building in part 1
3.  Run `Q2.ipynb` and `Question 3.ipynb` to review the specific statistical testing and feature engineering steps.
If you would like to know data structure of Steam API, run `sample data.ipynb` and check `sample_app_data.json` in `sample data\`

## Dependencies
Ensure a standard scientific Python environment is configured with the following key libraries:
* `pandas`
* `numpy`
* `request`
* `xgboost `
* `josn`
* `sklearn`
* `matplotlib`
* `seaborn`
* `json`
* `matplotlib`


* `saeborn`
* `sklearn`
* `xgboost`
