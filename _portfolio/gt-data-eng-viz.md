---
title: "Advanced Data Engineering & Visualization Projects (GT)"
order: 3
collection: portfolio
excerpt: "Modeling urbanization's impact on coastal ecosystems (XGBoost, SHAP, D3.js dashboard) and advanced data engineering projects covering TMDB API, SQLite, Flask, Tableau, D3.js (graphs, interactivity, maps), Azure ML, Spark/Scala on DataBricks, PageRank, Random Forest from scratch, Scikit-Learn, and LLM API integration."
#date: 2025-04-28 
tags: [Data Engineering, Big Data, Spark, Azure, Docker, D3.js, Tableau, Machine Learning, Visualization, Python, Flask]
technologies: "Python, D3.js, Tableau, SQLite, Flask, Spark (Scala), Azure ML, DataBricks, Scikit-Learn, XGBoost, SHAP, PageRank, Random Forest, LLM APIs"
#github_url: "[Link to primary GitHub repo or a summary page for these projects]"
# live_demo_url: "[Link to a key demo if applicable]"
# image_path: "/images/portfolio/gt-data-viz-teaser.png"
---

 ## Project 1
* **Objective:**
To evaluate the impacts of district-level urban development on Guangdong Province's coastal water quality, specifically examining the transmission of these impacts through the river-sea interface to nearshore zones, and to identify key urban drivers. 

* **Role & Contributions:**
    * Handled the visualization part of the project where I designed and implemented the interactive dashboard with charts and choropleth maps using D3.js to visualize regional and district level spatial patterns of urban development, water quality station data, and linked time-series charts for selected locations and indicators, allowing users to explore spatial and temporal relationships between urban development and water quality.
    * Contributed to the evaluation of forecasting performance against baseline models and the analysis of propagation pathways.
    * Co-authored the final project report summarizing the methodology, findings, and conclusions.
* **Technologies Used:** XGBoost, SHAP, AR(1) models (potentially R with `fable` or Python equivalents), Python (for ML and data analysis), D3.js (for interactive dashboard), GeoJSON, Haversine distance calculation.
* **Key Outcomes & Learnings:**
    * Developed an interactive D3.js dashboard allowing users to explore spatial and temporal relationships between urban development and water quality.
    * Gained significant experience in a multi-stage modeling approach, time series analysis, spatial data handling, interpretable machine learning, and advanced data visualization.
* **Artifacts:**
    * **Final Project Report:**  
    * **Interactive Dashboard Demo:**  
    * **GitHub Repository (if applicable):** 

## Project 2
* **HW1: End-to-End Data Wrangling & Web Application Basics**
    * **Data Acquisition & Graph Construction:** Extracted data from The Movie Database (TMDB) API using Python's standard library (`urllib`) to build a co-actor network graph.
    * **Database Management:** Designed and populated an SQLite database with movie and cast information; performed vertical partitioning and created indexes for query optimization. Executed complex SQL queries for data analysis and retrieval.
    * **Data Cleaning:** Utilized OpenRefine and GREL (General Refine Expression Language) to clean and transform messy datasets.
    * **Basic Web Development:** Developed a simple single-page web application using Python Flask to display tabular data.
    * **Introductory Visualization:** D3.js (v5) warm-up creating a bar plot of movie release trends.
    * *Key Technologies: Python (std lib), SQLite, SQL, D3.js (v5 basics), OpenRefine, GREL, Flask.*

## Project 3
* **Advanced Data Visualization**
    * **Business Intelligence Tools:** Designed tables, grouped bar charts, and stacked bar charts with interactive filters using Tableau.
    * **Interactive Network Graphs:** Created interactive force-directed graph layouts in D3.js (v5), implementing features such as node labeling, dynamic edge styling based on data attributes, node scaling by degree, and interactive node pinning/unpinning.
    * **Time-Series Visualization:** Developed D3.js line charts to visualize temporal patterns in board game ratings, including adding symbols for rankings and comparing the effects of different y-axis scales (linear, square root, log).
    * **Complex Interactive Dashboards:** Built an interactive D3.js line chart that, upon mouseover of data points, dynamically generated a sub-bar chart displaying related top-N data.
    * **Geospatial Visualization:** Created interactive choropleth maps in D3.js using GeoJSON to display board game ratings by country, incorporating dropdown selectors for game selection, quantile color scales, dynamic legends, and tooltips (d3-tip).
    * *Key Technologies: Tableau, D3.js (v5 advanced: force layouts, line charts, interactivity, scales, choropleth maps, GeoJSON, d3-tip).*

## Project 4
* **Cloud Machine Learning & Big Data Processing**
    * **Cloud ML Platforms:** Utilized Microsoft Azure Machine Learning Studio to build and evaluate a regression model for automobile price prediction, including data splitting and k-fold cross-validation.
    * **Big Data with Spark:** Analyzed large datasets (NYC trip data) using Apache Spark with Scala on the DataBricks platform. Performed complex DataFrame operations (joins, aggregations, filtering, sorting, window functions implicitly) to derive insights on popular locations, borough activity, and temporal pickup patterns.
    * *Key Technologies: Microsoft Azure Machine Learning Studio, Apache Spark (Scala API, DataFrames), DataBricks.*

## Project 5
* **Algorithm Implementation & Advanced Machine Learning**
    * **Graph Algorithms:** Implemented the PageRank algorithm from scratch in Python to rank nodes in a large network graph.
    * **Machine Learning from Scratch:** Implemented a Random Forest classifier from scratch in Python (Jupyter Notebook), including functions for entropy, information gain, bootstrapping, and Out-of-Bag (OOB) error estimation.
    * **Applied Machine Learning with Scikit-Learn:** Utilized Scikit-Learn in Python to train, tune (GridSearchCV), and evaluate various classifiers (Linear Regression, Random Forest, Support Vector Machines with StandardScaler preprocessing) on the Pima Indians diabetes dataset. Performed Principal Component Analysis (PCA) for dimensionality reduction.
    * **LLM API Integration:** Developed a Python program to simulate a moderated academic discussion using the DeepSeek API (OpenAI-compatible), featuring customizable participants, discussion rounds, real-time streaming responses, and automated summary generation.
    * *Key Technologies: Python, PageRank, Random Forest (implementation), Scikit-Learn (Linear Regression, RF, SVM, PCA, GridSearchCV, StandardScaler), LLM APIs (DeepSeek/OpenAI).*
