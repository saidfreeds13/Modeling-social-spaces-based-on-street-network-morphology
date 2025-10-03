# Socio-spatial-morphology assessment of an ex-industrial district

## Introduction ##
Former industrial cities of the 20th century today undergo changes in the properties and types of their spatial structures. These morphological changes can give rise to paradoxical forms of social organization or its absence. What forms of (paradoxical) relationships between the morphological configuration and social organization of the streets in a deindustrialized area can be identified? To what extent and with what reliability can the causality of morphology in the observed pattern of street use be revealed?Using the street network of the Narva quarter, which is part of St. Petersburg’s "Gray Belt," this research seeks answers to these questions. The theoretical foundation is the research trend known as "Spatial Cultures," which emerged under the influence of Émile Durkheim’s sociology and the Space Syntax theory of Hillier and Hanson.

## Repo's Coverage ##
This project provides a Python-based calculation and visualization of **Socio-spatial morphology analysis** of ex-industrial districts aimed at identification of relationships between street-network characetristics (integration, connectivity, choice) and the street-use pattern. The method measures the degree of each street's diversity of uses in such a way as to allow for a seamless joining with space-syntax measuremens of streets' morphology conducted either in QGIS or DepthmapX. Firstly, the code in '' estimates the intensity of each street's (segement's) uses by calculating Shannon-Wiener and Richness indecies. The section concludes with histograms of distribution. Secondly, the relationship between the uses and the morphological qualities is studied via the code in "SSM-Diversity Relationship.ipynb". It measures the spatial autocorrelation (global and local Moran's I) of each variable. Further, it runs the OLS regression with a dependant varible of streets' uses diversity and independent variables of streets' morphological characteristics. Initially, the method is created for ex-industrial context with s sensitivity to a non-linear (regression) relationship, but can be extended to other cases as well. 

Additionally, the folders in this repo contain the visualisations of key intermediate results.

---
## Installation

**Download the file ""** and open it in python 

## Data inputs needed
- **Polygons/POI of functional objects on a street:** Any geo-file with a **categorical column** (e.g., `type` for type/category of a fucntional object).
- **Study area:** Upload the area for boundary extraction.
- **Street-network:** Upload the linestring file, containing the streets in the area of interest.
---
## Code sections

**A. Street Uses** 
- **1. Libraries:** downloads all the necessary packages.
- **2. Diversity indexes:** Adds formulas for calculating diversity.
  - **Richness** number of unique cultural categories in each hexagon/buffer.
  - **Berger-Parker Dominance:** proportion of the most abundant category (values near 1 indicate dominance)
  - **Shannon-Wiener Diversity:** the uncertainty in predicting species identity of a random individual
- **3. Diversity of cultural cityscape:**
- **4. Results Visualisation:** 
- **5. Descriptive stats:** Creates and saves in png. boxplots and histograms for each diversity index

**B. Socio-spatial morphology and uses of streets in an ex-industrial neighborhood. Relationships.** 
- **1. Libraries:** downloads all the necessary packages.
- **2. Data import**
- **3. Spatial analysis** of morphological and diversity characteristics of streets
- **4. Regression analysis** of streets' morphological and diversity characteristics
---
