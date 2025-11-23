# Former industrial neighborhoods of St. Petersburg: modeling social spaces based on street-network morphology. 
# The part of the *"Life to Streets"* project.
*Developed by Bereiya Said, 2nd year master student of IDU ITMO*
## Introduction ##
More often than not former industrial districts of USA and Europe today experience the consequences of being "left-behind". "Left-behindness" entails a variety of socio-spatial externalities such as physical deterioration of infrastructure, an increased social tension among its residents, stigmatization of space. These are what american geographer called "metropolarities", and they give rise to all kinds of social and spatial paradoxes. To initiate a more evidence-based policy for these areas, a deep understanding of the exisitng space-society relationships is required. It is thus in the scope of this thesis to identify and characterise the forms of (paradoxical) relationships between the morphological configuration and social organization of space in the deindustrialized areas. The street-network, and a street as its element, is taken as an object, allowing for a microlevel analysis. The city of interest is St. Petersburg (Russia) which has an immense territory of previous industrial use now referred to as "Gray Belt" .The theoretical foundation is the research movement dubbed "Spatial Cultures," which emerged under the influence of Émile Durkheim’s sociology and the Space Syntax theory of Hillier and Hanson.

## Repo's Coverage ##
This project provides a Python-based calculation and visualization of **Socio-spatial morphology analysis** of ex-industrial districts aimed at identification of relationships between street-network characetristics (integration, connectivity, choice) and the street-use pattern. The method measures the degree of each street's diversity of uses in such a way as to allow for a seamless joining with space-syntax measuremens of streets' morphology conducted either in QGIS or DepthmapX. Firstly, the code in 'Street_use_diversity.ipynb' estimates the intensity of each street's (segement's) uses by calculating Shannon-Wiener and Richness indecies. The section concludes with histograms of distribution. Secondly, the relationship between the uses and the morphological qualities is studied via the code in "SSM-Diversity Relationship.ipynb". It measures the spatial autocorrelation (global and local Moran's I) of each variable. Further, it runs the OLS regression with a dependant varible of streets' uses diversity and independent variables of streets' morphological characteristics. Initially, the method is created for ex-industrial context with s sensitivity to a non-linear (regression) relationship, but can be extended to other cases as well. 

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
