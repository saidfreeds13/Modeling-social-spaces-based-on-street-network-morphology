# socio-spatial-morphology of an ex-industrial district

This project provides a Python-based calculation and visualization of **Socio-spatial morphology analysis** of ex-industrial districts aimed at identification of relationships between street-network characetristics (integration, connectivity, choice) and the street-use pattern. The method measures the degree of each street's diversity of uses in such a way as to allow for a seamless joining with space-syntax measuremens of streets' morphology conducted either in QGIS or DepthmapX. Firstly, the code in '' estimates the intensity of each street's (segement's) uses by calculating Shannon-Wiener and Richness indecies. The section concludes with histograms of distribution. Secondly, the relationship between the uses and the morphological qualities is studied via the code in "". It measures the spatial autocorrelation (global and local Moran's I) of each variable. Further, it runs the OLS regression with a dependant varible of diversity of streets' uses and independent variables of streets' morphological characteristics. Initially, the method is created for ex-industrial context with s sensitivity to a non-linear (regression) relationship, but can be partly used for other cases. 

---
## Installation

**Download the file ""** and open it in python 

## Data inputs needed
- **Polygons/POI of functional objects on a street:** Any geo-file with a **categorical column** (e.g., `type` for type/category of a fucntional object).
- **Study area:** Define the area (`" "`) for boundary extraction.
---
## Code sections

**A. Street Uses** 
- **1. Libraries:** downloads all the necessary packages.
- **2. Diversity indexes:** Adds formulas for calculating diversity.
  - **Richness** number of unique cultural categories in each hexagon/buffer.
  - **Berger-Parker Dominance:** proportion of the most abundant category (values near 1 indicate dominance)
  - **Shannon-Wiener Diversity:** the uncertainty in predicting species identity of a random individual
- **5. Diversity of cultural cityscape. :**
- **6. Results Visualisation:** 
- **7. Descriptive stats:** Creates and saves in png. boxplots and histograms for each diversity index

**B. Socio-spatial morphology and uses of streets in an ex-industrial neighborhood. Relationships.** 
- **1. Libraries:** downloads all the necessary packages.

---

## Adaptation for a user's input 

- **Category column:** Change `type` to match your dataset structure.
- **Area of interest:** Use any polygon of a city or a district.
---
