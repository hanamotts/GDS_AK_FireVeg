# Predicting wildfire occurrence in Alaska

## Hana Matsumoto

_____

## Project overview

This project will investigate wildfire occurrence in Alaska using predictors such as the underlying vegetation and permafrost type using machine learning.

### **Objectives**

1. Define wildfire incidents, vegetation and permafrost for Alaska
	1. Severity: low, moderate, high
	2. Vegetation: forest type
	3. Permafrost: continuous, discontinuous, sporadic, seasonal
2. Create a basic machine learning model to predict based on vegetation and permafrost type

### **Datasets**

1. Fire
	1. Perimeters
		1. [Global Wildfire Information System (GWIS)](https://gwis.jrc.ec.europa.eu/apps/country.profile/downloads)
		2. [FIREDpy](https://github.com/earthlab/firedpy)
			1. More information from [this](https://www.nature.com/articles/s41597-022-01572-3#Sec3) paper
	2. Imagery
		1. [USGS Earth Explorer](https://earthexplorer.usgs.gov/) 
	3. Fire severity resources
		1. [dNBR](https://www.researchgate.net/publication/358213336_Classification_of_Fire_Damage_to_Boreal_Forests_of_Siberia_in_2021_Based_on_the_dNBR_Index) paper
2. Vegetation
	1. Bioclimate zone vegetation types shapefile (previously provided)
3. Permafrost zones
	1. Existing shapefile (previously provided)
	
### **Python packages**

1. geopandas
2. pandaa
3. numpy
4. rasterio
5. matplotlib.pyplot
6. sklearn.preprocessing
	1. StandardScaler
7. sklearn.model_selection
	1. train_test_split
8. sklearn.linear_model
	1. LinearRegression
9. sklearn.ensemble
	1. RandomForest
10. sklearn.metrics
	1. mean_squared_error
	
### **Methods**

1. Create (or find) shapefile of fire severity classes based off satellite imagery for 2022
	1. GEE or ArcGIS Pro
	2. Differenced normalized burn ratio (dNBR)
2. Import fire, vegetation and permafrost shapefiles into Jupyter Notebook for analyzing
	1. Clean datasets (if needed)
	2. Determine how to correlate fire severity class to underlying vegetation and permafrost
	3. Run linear regression and random forest model to see how accurately the models can predict fire severity based on permafrost and vegetation alone

### **Expected outcomes**

I expect there to be relatively high correlation values with fire severity and vegetation. The vegetation classes are closely tied to climatic zones and therefore likely good predictors for fire severity.

Permafrost may also be a predictor of fire severity because permafrost zones are also controlled by climate and have close relations to vegetation type.