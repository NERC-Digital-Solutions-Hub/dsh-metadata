# Predicting spatially heterogeneous invasive spread: Pyracantha angustifolia invading a dry Andean valley in northern Argentina

## Overview
- A freely available data package from a study on the spatial spread of Pyracantha angustifolia in a dry Andean valley in northern Argentina.
- Fieldwork conducted in May 2019 at 10 sites, focusing on spatially explicit measurements to support invasion modeling.
- Data collected include georeferenced plot-level measurements, plant demography, fecundity, seed counts, and dendrochronology.

## Field Sampling Design
- Ten sites with three circular plots per site, each 20 meters in diameter, totaling 30 plots over ~9,426 m².
- For each plot, central point coordinates and elevation recorded with a GPS device.
- Habitat types recorded as grassland, shrubland, or rocky.
- Sampling aimed to capture Pyracantha demography and reproductive status across habitats and conditions.

## Measurements and Observations
- Species and structure: number of Pyracantha saplings and reproductive adults per plot; for each reproductive adult, basal stem diameter, plant height, and canopy diameter (cardinal directions).
- Grazing and disturbance: notes on grazer damage and presence of cattle/horse dung.
- Fecundity: sampling of fruit production by segmenting a random canopy segment and extrapolating to total fruits per plant.
- Seed counts: seeds counted from fruits (30 fruits from 10 shrubs) to estimate average seeds per fruit and per plant.
- Age estimation: growth rings counted from 32 shrubs via a cylindrical stem block, with four observers to determine annual ring counts.
- Data scale: direct measurements tied to plot centers, enabling linkage to location-based analyses in GIS.

## Data Files and Contents
- RawFecundityData.csv
  - Columns include: Date, Site, Plot, latitude, longitude, Elevation, Habitat_type, Cotoneaster_presence, Cotoneaster_count, Cattle_dung, Horse_dung, Grazing, Sapling_count, Adult_count, Plant_number, Plant_grazed, Basal_stem_circumference, Basal_stem_diameter, Rosette_Diameter_1–4, Average_Rosette_Diameter, Height, Number_of_Fruits, Proportion_counted, Total_fruit, Total_seeds.
  - Describes fecundity and plant-descriptor data at the plot/plant level.
- FruitCounts.csv
  - Columns: Sample_ID, Seed_count.
  - Seed counts per sampled fruit.
- DendrochronologyPyrcantha.csv
  - Columns: Sample_ID, circumference, count1, count2, count3, count4, mean_count.
  - Four observers’ growth ring counts with an average.
- diameter
  - File name indicates plant diameter data; specific fields not listed in the provided text.
- Notes: Data last modified and submitted on 09/12/2020; data are freely available; contact provided for metadata and usage.

## Data Access and Metadata
- Data freely available; contact: Fiona Plenderleith, University of Aberdeen (f.plenderleith.19@abdn.ac.uk; permanent: fiona.plenderleith@outlook.com).
- Data collected in May 2019; field coordinates include latitude/longitude and plot-level environmental attributes.

## GIS Relevance and Potential Uses
- Enables spatial analysis of invasive spread patterns with exact plot-level coordinates and elevation.
- Rich predictor variables for GIS-based modeling: habitat type, presence of other plant species (Cotoneaster), grazing pressure, dung, and disturbance indicators.
- Facilitates the construction of map-based data products (e.g., distribution maps, fecundity surfaces, age structure maps) for policy colleagues, clients, or the public.
- Data can be integrated with other spatial layers (topography, land use, vegetation) to explore drivers of spread and patch dynamics.
- Supports multi-resolution analysis by linking plot- and plant-level data to broader landscape context.