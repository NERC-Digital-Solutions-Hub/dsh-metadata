# Predicting spatially heterogeneous invasive spread: Pyracantha angustifolia invading a dry Andean valley in northern Argentina

## Overview
- Study of the invasive spread of Pyracantha angustifolia in a dry Andean valley, northern Argentina.
- Fieldwork conducted in May 2019 across 10 sites with 30 circular plots (20 m diameter) to assess plant demography and fecundity.
- Data collected include geolocation, habitat type, plant size metrics, grazing indicators, fruit production, seed counts, and tree age via dendrochronology.
- Freely available dataset with multiple data files supporting standardized analysis and monitoring of invasion dynamics.

## Field sampling design
- Ten sites with three circular plots per site, randomly selecting the middle point for each plot.
- Plots are separated by at least 20 m, forming a total sampling area of 9,426 m2.
- GPS coordinates and elevation recorded at plot centers.
- Habitat types categorized as grassland, shrubland, or rocky.

## Measurements and variables
- Taxa and counts:
  - Saplings (>10 cm tall, non-reproductive) and reproductive adults counted per plot.
- Individual plant measurements (for each reproductive adult):
  - Basal stem diameter, plant height, canopy diameter (measured in four cardinal directions).
  - Evidence of damage by grazers.
- Reproductive output:
  - Fruit sampling by counting one-eighth of the canopy area on a random segment; total fruit per plant estimated by multiplying by eight.
  - Seeds per fruit determined from 30 fruits across 10 shrubs, consistently averaging five seeds per fruit.
- Age estimation:
  - Ground-level harvesting of 32 shrubs; stem blocks extracted from the base.
  - Growth rings counted on cross-sections by four observers to estimate age.

## Data files and contents
- RawFecundityData.csv
  - Columns include Date, Site, Plot, latitude, longitude, Elevation, Habitat_type, Cotoneaster_presence, Cotoneaster_count, Cattle_dung, Horse_dung, Grazing, Sapling_count, Adult_count, Plant_number, Plant_grazed, Basal_stem_circumference, Basal_stem_diameter, Rosette_Diameter_1–4, Average_Rosette_Diameter, Height, Number_of_Fruits, Proportion_counted, Total_fruit, Total_seeds.
- FruitCounts.csv
  - Sample_ID, Seed_count (seed counts per fruit).
- DendrochronologyPyrcantha.csv
  - Sample_ID, circumference, count1, count2, count3, count4, mean_count.
- diameter
  - (File name indicated; content not detailed in provided text.)
- Data last modified and submitted: 09/12/2020.
- Contact: Fiona Plenderleith, University of Aberdeen (emails provided).

## Data availability and accessibility
- Freely available data; contact for access and use details.
- Data originates from an under-review study reporting standardized field and laboratory measurements.

## Relevance for environmental monitoring
- Provides georeferenced, habitat-specific data on invasive plant demography and fecundity, enabling spatial monitoring of invasion potential.
- Standardized metrics (e.g., fruit production, seed counts, growth rings) support cross-site comparisons and temporal trend analyses.
- Outputs suitable for visualization (maps, charts, reports) and integration into broader environmental health assessments.

## Potential data use and integration
- Combine with land-use, grazing, and biodiversity datasets to model drivers of invasion and assess policy effectiveness.
- Use as a baseline for longitudinal monitoring of Pyracantha angustifolia spread and reproductive success across different habitats.
- Ensure data storage in centralized portals and provide underlying data access to support transparency and reuse.

## Key considerations for analysts
- Sampling scope is 10 sites with 30 plots; consider spatial coverage and potential extrapolation limitations.
- Dendrochronology involves multiple observers; consider inter-observer variability in age estimates.
- Data richness (demography, fecundity, age) enables multifactor analyses linking habitat type, grazing, and invasive potential.