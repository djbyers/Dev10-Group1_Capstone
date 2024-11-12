# Group1_Capstone

This was the final project as part of the Dev10 training course.


Broadly speaking, this project aims to use a variety of and financial factors to forecast different measures of economic and societal well-being. Our data, drawn primarily from the World Bank database, draws upon different measures of government debt, tax revenue, stock value within an economy, inflation, and GDP, among others, to predict values such as unemployment and wealth disparity.

Using an automated API call from the World Bank, we were able to collect data from every registered country from the years 1990-2020. There are two main goals of our analysis.
One is to be able to produce actionable results by building our models and visualizations to use the data from one country in one particular year to predict whichever dependent variable we choose for the following year in that country. For example, we will use GDP, tax revenue, and total value of stocks traded in the United States in 2000 to predict the unemployment rate in the United States in 2001. With this goal in mind, by the end of our process, we should be able to create predictions on a global scale for how these socioeconomic dependent variables will end up at the end of 2021 using the 2020 data. The other goals is to be able to use the economic and financial data within our predictive variables to be able to predict the gaps in data of our response variables. For example, our algorithm will take the predictive variables for country X in one year and predict the Gini Index from that year to help provide a better picture for how wealth inequality is changing in country X over time.

# Table of Contents
- DatabricksAndETL - This folder contains our Databricks Jupyter Notebooks and our ETL report.
- NapkinDrawingsAndFeedback - This folder contains our visualization and dashboard napkin drawings and the feedback we received about them.
- code - This folder contains the following sub-folders which all have code in them:
    - Preliminary Code - This code charts our early progress through the machine learning process. We did not directly use this code in the final implementation of our machine learning.
    -  Final Machine Learning - This code contains the Jupyer Notebooks we used to create our final machine learning models.
    -  Power BI Code - We used this code to create Power BI visualizations with Python.
- Project Specifications - This folder contains our initial exploratory questions, data platform diagrams, a glossary of our variables, and project management plan.
- FinalProjectDocuments - This folder contains our project executive summary and our presentation slides.

