# Former industrial neighborhoods of St. Petersburg: assessing relationship between street-network morphology and social organization of space. 
# The part of the *"Life to Streets"* project.
*Developed by Bereiya Said, 2nd year master student of IDU ITMO*
## Introduction ##
More often than not former industrial districts of USA and Europe today experience the consequences of being "left-behind". "Left-behindness" entails a variety of socio-spatial externalities such as physical deterioration of infrastructure, an increased social tension among its residents, stigmatization of space. These are what an american geographer Ed Soja called "metropolarities", and they give rise to all kinds of social and spatial paradoxes. To initiate a more evidence-based policy for these areas, a deep understanding of the exisitng space-society relationships is required. It is thus in the scope of this thesis to identify and characterise the forms of (paradoxical) relationships between the morphological configuration and social organization of space in the deindustrialized areas. The street-network, and a street as its element, is taken as an object, allowing for a microlevel analysis. The city of interest is St. Petersburg (Russia) which has an immense territory of previous industrial use now referred to as "Gray Belt" .The theoretical foundation is the research movement dubbed "Spatial Cultures," which emerged under the influence of Émile Durkheim’s sociology and the Space Syntax theory of Hillier and Hanson.

## Repo's Coverage ##
This project provides a Python-based calculation, analysis, visualization and modeling of the (spatial) relationships between street-nework morphology and social organization of space in the context of former industrial neighborhoods of Saint Petersburg. Street-network morphology is understood under the framework of Space Syntax and its key measures of Integration and Choice. Whereas, the social organization is uderstood as a pattern of streets' functionality across the neighborhood. The operationalization for the social organization is done via a diveristy metric, showing how diverse and dense the functional uses of each street's segment.  

The method functions across 3 notebooks: 
1. 'Street_use_diversity.ipynb': the code estimates the intensity of each street's (segement's) use and provides an evidence of a street's social role in the neighborhood by calculating Shannon-Wiener index as a key metric, as well as two additional ones (Richness Berger-Parker indecies). The section concludes with histograms of distributions for each variable. 
2. "SSM-Diversity Relationship.ipynb": the relationship between the urban functions and the morphological qualities is studied. It measures the spatial autocorrelation (global and local Moran's I) of each variable. Also, it runs the OLS regression with a dependant varible of streets' uses diversity and independent variables of streets' morphological characteristics. The results of this code are delivered in choropleths and ols-tables.  
3. "Rebalancing Social Life" (IN DEVELOPMENT): provides a flexible analytical tool to rebalance the instensity of social life (as proxied with diversity) across the neighborhood according to the morphological qualities of a street. 

The method may be adopted more broadly in the analysis of other cities and other type of districts. Yet, the initial hypotheses as to what type of relationships are more likely to take place in the area of study is a helpful prerequisite to the analysis and modeling. 


<p align="center">
  <img width="645" height="1002" alt="BS_methodology drawio" src="https://github.com/user-attachments/assets/3411a3d7-996a-4321-badd-f8f31f8f8af8">
</p>
<p align= "center"> *The block-scheme of the method, author: Bereiya Said 2nd year master student of IDU ITMO* </p>

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
- **3. Diversity of social life:**
- **4. Results Visualisation:** 
- **5. Descriptive stats:** Creates and saves in png. boxplots and histograms for each diversity index

**B. Socio-spatial morphology and uses of streets in an ex-industrial neighborhood. Relationships.** 
- **1. Libraries:** downloads all the necessary packages.
- **2. Data import**
- **3. Spatial analysis** of morphological and diversity characteristics of streets
- **4. Regression analysis** of streets' morphological and diversity characteristics
---
