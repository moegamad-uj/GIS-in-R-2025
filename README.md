SpatialR
================
Moegamad Uzair Jack
2025-02-24

---
# What spatial patterns and potential biases can be identified in the global distribution of Nightjars (Caprimulgidae) based on GBIF occurrence records, and how do human observations influence these patterns?
---
## Mapping Nightjar Sightings with R 
---

## About  

This repository contains an **RMarkdown file** that maps the global distribution of **nightjars** (family *Caprimulgidae*). The occurrence data is retrieved from the **Global Biodiversity Information Facility (GBIF)** using the `rgbif` package on **R**.  

To ensure quality and relevance of data, the dataset is: 
- **Limited to 5,000 records**.  
- **Filtered to only include records with coordinates**.  
- **Restricted to human observations**.  

## Overview  

**SpatialR** is focused on visualising **Nightjar (family: Caprimulgidae) distributions** and this project generates both **static and interactive maps** to map species distribution patterns globally.  

## Workflow

Firstly, load in the necessary packages:
- `rgbif` 
- `sf`
- `ggplot2`
- `dplyr`
- `viridis`
- `leaflet`
- `rnaturalearth`

Then, retrieve data on the family Caprimulgidae using `rgbif` to access GBIF records. This occurrence data should be filtered to human observations, it must have coordinates and should be limited to 5000 records.
Thereafter, clean and prepare the data, removing rows with any NA values.
Convert to spatial data and then create a static map using `ggplot2`.

This static map should:
- have **species-specific colour markers** accompanied by a legend
- have **markers of variable size based on individual count** accompanied by a legend

Thereafter, do the necessary CRS corrections. However, in this case, no corrections are needed for the WGS84 projection. Once the CRS is corrected,  create an interactive map using `leaflet`.

The interactive map should:
- ensure individualCount is numeric and remove any NAs just in case
- create a color palette for species
- map with species-based color function
- have a popup with relevant information
- centre  map on Africa

The popup will have data on the species name, count, the country, data. The existence of the pop leave no need for varying marker sies or a legend.

The map will use the Esri.WorldPhysical basemap for a more user-friendly interface.

## Data Sources  

- **GBIF**: Global Biodiversity Information Facility ([https://www.gbif.org](https://www.gbif.org))  
- **Natural Earth**: Country boundaries ([https://www.naturalearthdata.com](https://www.naturalearthdata.com))  

## Repository Contents 

- **`Nightjar.Rmd`** – RMarkdown file containing the GIS analysis.  
- **`Nightjar.html`** – Rendered HTML output.  
- **`README.md`** – Project summary and details.  

## View the Project 

Click the link below to view the rendered HTML output:  
[Nightjar Spatial Analysis](https://htmlview.glitch.me/?https://github.com/moegamad-uj/GIS-in-R-2025/blob/main/Nightjar.html)  

---  

## License  

MIT License © 2025 Moegamad Uzair Jack  
