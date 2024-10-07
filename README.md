# County-Specific Wildfire Prediction Using Machine Learning: A Southern California Case Study

## Overview

This project explores the use of machine learning models to predict wildfire occurrences in Southern California's high-risk counties: Los Angeles, Riverside, San Diego, and San Bernardino. The project utilized various machine learning techniques, including Random Forests, Decision Trees, k-Nearest Neighbors (KNN), and Support Vector Machines (SVM), to identify county-specific factors influencing wildfire risk. By evaluating these models using a dataset spanning from 2016 to 2020, this study aims to provide a more accurate, localized approach to wildfire prediction, which can support effective wildfire management strategies in California.

## Key Features
- **Data Preprocessing**: Feature engineering, data balancing using SMOTE, and grid-based spatial data organization.
- **Machine Learning Models**: Implementation of four different models to identify the most suitable method for each county.
- **Feature Importance Analysis**: Identification of the most significant variables influencing wildfire occurrence.
- **Localized Insights**: County-specific analysis highlighting the importance of tailored models for regional wildfire risk assessment.

## Project Structure

- **`data/`**: Contains raw and processed datasets used in the analysis.
- **`notebooks/`**: R Markdown notebooks detailing data preprocessing, exploratory data analysis (EDA), and model training.
- **`scripts/`**: R scripts used for data cleaning, feature engineering, and model evaluation.
- **`results/`**: Performance metrics and results of the trained models.
- **`visualizations/`**: Plots and images generated during the analysis (e.g., county maps, feature importance plots).
- **`thesis_summary.pdf`**: PDF version of the project thesis report.
- **`README.md`**: Overview of the project, including objectives, methodology, and findings.

## Research Objectives

1. **Determine High-Risk Counties**: Identify Southern California counties with the highest wildfire risk based on historical fire occurrence and radiative power data.
2. **Compare Machine Learning Models**: Evaluate the effectiveness of different machine learning techniques (Random Forests, Decision Trees, KNN, and SVM) in predicting wildfire occurrences.
3. **Identify Key Predictors of Wildfire Risk**: Determine county-specific factors (e.g., NDVI, average temperature, wind speed) that significantly impact wildfire occurrence.
4. **Provide Recommendations**: Offer data-driven recommendations for improving wildfire management strategies based on model insights.

## Data Overview

- **Counties Analyzed**: Los Angeles, Riverside, San Diego, San Bernardino
- **Time Period**: 2016 - 2020
- **Variables**: 
  - `longitude`, `latitude`: Geographic coordinates of fire occurrences
  - `year`, `month`, `day`: Date of fire occurrences
  - `frp`: Fire radiative power
  - Meteorological variables: `AWND` (average wind speed), `PRCP` (precipitation), `TAVG` (average temperature)
  - Vegetation index: NDVI (Normalized Difference Vegetation Index)

## Methodology

1. **Data Collection**:
   - Fire occurrence data from NASA MODIS and VIIRS satellite observations.
   - Meteorological data (average temperature, precipitation, wind speed) from NOAA.
   - Vegetation indices (NDVI) from NASA Landsat 8 satellite imagery.
  
2. **Data Preprocessing**:
   - Spatial data organization using grid tiles for each county.
   - Handling missing data through interpolation and the Last Observation Carried Forward (LOCF) method.
   - Addressing data imbalances using the Synthetic Minority Over-sampling Technique (SMOTE).

3. **Model Training**:
   - Models were trained and tested on separate datasets for Los Angeles and Riverside counties.
   - Evaluation metrics included precision, recall, F1 score, and AUCROC.

4. **Feature Importance**:
   - Variable importance was measured using Mean Decrease in Accuracy (MDA) in Random Forest models.

## Results

1. **Best Performing Model**:
   - The Random Forest model achieved the highest performance for both Los Angeles and Riverside counties, with F1 scores of 0.964 and 0.911, respectively.
   
2. **Significant Predictors**:
   - NDVI and average temperature were identified as the most significant variables affecting wildfire risk.
   - The models revealed that higher NDVI values (indicating dense vegetation) and elevated average temperatures were strongly associated with increased fire occurrences.

3. **Regional Insights**:
   - The study confirmed the need for localized models, as factors influencing wildfire risk varied significantly between counties.

## Visualizations

### Wildfire Locations in Los Angeles County
![Wildfire Locations in Los Angeles County](visualizations/la_county_map.png)

### Wildfire Risk Comparison by County
![Wildfire Risk Comparison by County](visualizations/wildfire_risk_comparison.png)

## Conclusion

This project demonstrates the potential of using localized machine learning models to predict wildfire occurrences in Southern California. By focusing on county-specific data, the study highlights the importance of regionally tailored models in accurately capturing the factors that drive wildfire risk. The findings provide valuable insights for policymakers, fire response teams, and environmental scientists aiming to develop more effective wildfire management strategies.

## Future Directions
- Expand Analysis to Additional Counties: Include more counties in Southern California to create a more comprehensive regional model.
- Incorporate Additional Variables: Use variables such as soil moisture, wind direction, and ozone ratio to improve prediction accuracy.
- Explore Advanced Techniques: Implement deep learning models for image analysis and incorporate real-time data for dynamic predictions.

