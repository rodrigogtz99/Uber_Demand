# Uber Demand Prediction Project

This repository contains the code and data for my data analytics project aimed at predicting Uber demand for each day of the year, and proposing an optimal number of drivers needed to meet that equilibrium. The primary dataset used in this project is the [Uber Fares Dataset from Kaggle](https://www.kaggle.com/datasets/yasserh/uber-fares-dataset), which encompasses data spanning from 2009 to 2015, comprising approximately 200,000 rows.

## Data Preprocessing

To ensure effective analysis, the dataset was transformed into a consistent 52-week format to facilitate the visualization of weekly trends. This transformation primarily focuses on two key factors: the week number and the day of the week (e.g., Monday, Tuesday, etc.). The daily average of Uber pickups per neighborhood across the years was calculated, with outliers removed, resulting in a unique estimate of pickups for the year "X."

To project this estimate into the present day, a multiplier was determined by comparing the number of estimated Uber rides in 2023 to the total rides recorded in the dataset. This assumes that the underlying trends remain unchanged.

## Geospatial Analysis

Geospatial analysis was performed using a GeoJSON file obtained from the NYC government, which contains coordinates for all neighborhoods and boroughs within the city. This data was used to assign each ride to a specific neighborhood, enabling the identification of "hot spots" with high demand.

## Data Analysis

After cleaning, exploring, and manipulating the data, I proceeded to analyze neighborhoods with the highest demand and estimated the number of drivers needed to serve them. The assumption here is that the average Uber driver conducts 10.9 rides per day, according to NYC.gov statistics.

## Machine Learning Model

To enhance the predictive capabilities of the project, a machine learning model was trained using H2O. This model takes into account the day of the week, week number, and neighborhood to forecast the demand for each day of the year and the corresponding number of drivers required to meet that demand for every neighborhood in New York City.

## Project Visualization

To explore the results of this project, you can view the visualizations created in Tableau by following this [link](#(https://public.tableau.com/app/profile/rodrigo.gutierrez.garcia/viz/UberDemandModelNYC/Story1?publish=yes)). These visualizations provide insights into the predicted demand, driver requirements, and hot spots across NYC neighborhoods.

Feel free to explore the code, datasets, and visualizations provided in this repository to gain a deeper understanding of the project and its findings. If you have any questions or feedback, please don't hesitate to reach out. Your input is highly appreciated.
