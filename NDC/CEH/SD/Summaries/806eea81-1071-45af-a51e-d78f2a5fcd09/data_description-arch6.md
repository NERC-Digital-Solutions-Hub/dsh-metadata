# Predicting spatially heterogeneous invasive spread: Pyracantha angustifolia invading a dry Andean valley in northern Argentina

## Overview
- Field data collected in May 2019 at 10 sites in Tafi Del Valle, Tucuman, Argentina to study spatially heterogeneous invasion by Pyracantha angustifolia.
- Aimed to quantify plant demographics, fecundity, growth, and habitat associations to enable prediction of invasion spread.

## Study design and data collection
- Plot design: 30 circular plots (20 m diameter) across 10 sites, with plots selected at random midpoints and separated by at least 20 m.
- Habitat types: grassland, shrubland, rocky.
- Within plots:
  - Recorded coordinates, elevation, and habitat type.
  - For Pyracantha: counted saplings (>10 cm, non-reproductive) and reproductive adults; measured basal stem diameter, plant height, and canopy diameter (cardinal directions).
  - Assessed grazing impact: visible damage by grazers; noted presence of cattle/horse dung; overall grazing status.
  - Fruit sampling: counted fruit on one-eighth canopy area segment with random compass bearing; estimated total fruits per plant by scaling to whole canopy; counted seeds in 30 fruits from 10 shrubs (found five seeds per fruit on average).
- Age estimation: harvested 32 shrubs at ground level, extracted a stem block from the base, prepared cross-sections, and counted growth rings (four observers) to infer age.
- Total plants and samples: 309 reproductive adults of known size were incorporated into fruit production estimates.

## Data files and key variables
- RawFecundityData.csv
  - Core measurements and context: Date, Site, Plot, latitude, longitude, Elevation, Habitat_type.
  - Habitat/biotic context: Cotoneaster_presence, Cotoneaster_count, Cattle_dung, Horse_dung, Grazing.
  - Plant-level measures: Sapling_count, Adult_count, Plant_number, Plant_grazed, Basal_stem_circumference, Basal_stem_diameter, Rosette_Diameter_1–4, Average_Rosette_Diameter, Height.
  - Fecundity metrics: Number_of_Fruits, Proportion_counted, Total_fruit, Total_seeds.
- FruitCounts.csv
  - Sample_ID, Seed_count (counts per fruit).
- DendrochronologyPyrcantha.csv
  - Sample_ID, circumference, count1–count4 (growth rings counted by four observers), mean_count.
- diameter
  - Data file indicated as containing diameter-related measurements (specific columns not detailed in the provided content).

## Data collection methods details
- GPS and elevation recorded at plot centers.
- Plant measurements included morphology (basal diameter, height, canopy spread) and signs of grazing damage.
- Fecundity estimation involved sampling fraction of the canopy and extrapolating to total fruit production.
- Seed production estimated from fruit counts and average seed per fruit.
- Dendrochronology used cross-sections from shrubs with multi-observer ring counts to derive mean age markers.

## Potential uses and data products (Data Support perspective)
- Create dashboards and self-serve analyses linking spatial location with fecundity, age, and habitat type.
- Map-based exploration of invasion potential across different habitats (grassland, shrubland, rocky).
- Comparisons of fecundity and age structure across sites to identify drivers of spread.
- Derived products: per-plant metrics (total fruits, total seeds, age proxy), plot-level summaries, and site-level aggregates.
- Data harmonization opportunities: combine RawFecundityData with Dendrochronology and diameter data for age-structure and growth analyses.
- Cross-disciplinary utility: informs management decisions in similar habitats and supports policy or outreach about invasive spread risks.

## Accessibility and contact
- Freely available data; methods and variables clearly described.
- Data last modified: 09/12/2020; Field data collected May 2019.
- Primary contact: Fiona Plenderleith, University of Aberdeen (f.plenderleith.19@abdn.ac.uk; fiona.plenderleith@outlook.com).