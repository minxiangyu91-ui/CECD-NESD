Repository Overview
This repository provides the Chinese Ecosystem Carbon Density Data and Associated Natural, Economic, and Social Drivers (CECD-NESD), integrated with complete R scripts for machine learning-based carbon density estimation. The data-code package supports reproducible modeling and driver contribution analysis across China's terrestrial ecosystems.

Repository Contents
File	Description
SOC Dataset.csv	Soil organic carbon density with 40+ natural-economic-social drivers
AGBC Dataset.csv	Above-ground biomass carbon density with matched driver variables
BGBC Dataset.csv	Below-ground biomass carbon density with matched driver variables
4 types of machine learning models.R	Implementation of RF, Cubist, SVM, and XGBoost algorithms
Accuracy.R	Model performance evaluation and Shapley value decomposition
Data Description
Each dataset contains carbon density values paired with 40+ predictor variables organized into four categories:
Carbon Density Target Variable: Carbon density (AGBC/SOC/BGBC, unit: Mg C/ha)

Topographic & Terrain Attributes: DEM, Slope, Aspect, Curvature Terrain Roughness Index, Topographic Wetness Index, Valley Bottom Flatness Index, Slope Length Factor

Soil Properties: Clay fraction, Silt fraction, Sand fraction, Bulk density, pH, Cation Exchange Capacity, Soil parent material, Total nitrogen

Climatic & Vegetation Factors: Annual mean temperature, Annual mean precipitation, Annual evapotranspiration, Surface solar radiation, Daytime/Nighttime land surface temperature

NDVI (Normalized Difference Vegetation Index), NPP (Net Primary Productivity)

Anthropogenic & Socio-Economic Drivers: Population density, GDP, Nighttime light index, Distance from railway, Distance from road, Land use type

Emissions: OC, NOx, NH3, CO, BC, CO2 emissions

Machine Learning Models
Four algorithms were implemented and compared for carbon density estimation:

Model	Description
Random Forest (RF)	Ensemble learning method based on regression trees
Cubist	Rule-based regression model with boosting capabilities
Support Vector Machine (SVM)	Kernel-based method for nonlinear regression
Extreme Gradient Boosting (XGBoost)	Gradient boosting framework with regularization
The modeling workflow includes hyperparameter tuning, cross-validation, and driver importance assessment.

Code Usage
Prerequisites
R (version ≥ 4.0)

Required packages:

r
install.packages(c("randomForest", "Cubist", "e1071", "xgboost", "caret", "shapviz", "tidyverse"))
Workflow
Load the desired dataset (e.g., SOC Dataset.csv)

Run 4 types of machine learning models.R for model training, comparison, and driver contribution analysis

Execute Accuracy.R for comprehensive performance metrics (R², RMSE, MAE) and Shapley value decomposition

Data Source
The original carbon density data were obtained from the National Ecosystem Science Data Center:
Xu, L., He, N. P., & Yu, G. R. (2020). 2010s中国陆地生态系统碳密度数据集 [2010s China's terrestrial ecosystem carbon density dataset] (Version 1) [Dataset]. National Ecosystem Science Data Center. https://doi.org/10.11922/sciencedb.603
Processed datasets integrating socio-economic drivers and all analytical code are publicly available in this repository.

Citation
If you use this data or code in your research, please cite:
Xu, L., He, N. P., & Yu, G. R. (2020). 2010s中国陆地生态系统碳密度数据集 [2010s China's terrestrial ecosystem carbon density dataset] (Version 1) [Dataset]. National Ecosystem Science Data Center. https://doi.org/10.11922/sciencedb.603
and
