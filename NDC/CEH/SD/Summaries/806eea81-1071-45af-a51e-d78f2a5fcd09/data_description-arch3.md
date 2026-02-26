# Predicting spatially heterogeneous invasive spread: Pyracantha angustifolia invading a dry Andean valley in northern Argentina

## Overview
- Study documenting field data collected to understand spatially variable invasion dynamics of Pyracantha angustifolia in a dry Andean valley (northern Argentina).
- Freely available dataset compiled from field surveys conducted in May 2019 at 10 sites (30 plots total) to quantify plant abundance, age structure, fecundity, and potential grazing impacts.
- Data intended to inform monitoring frameworks by linking environmental conditions to invasion indicators and enabling future policy evaluation and decision-making.

## Study design and data collection
- Site and plot layout:
  - 10 sites with randomly selected middle points for three circular plots per site (20 m diameter each), separated by at least 20 m.
  - Total sampled area: 9,426 m2.
- Measurements at each plot:
  - Geographic coordinates (latitude, longitude) and elevation (GPS).
  - Habitat type categorized as grassland, shrubland, or rocky.
  - Presence and counts of Pyracantha saplings (>10 cm, non-reproductive) and reproductive adults.
  - For each reproductive plant: basal stem diameter, plant height, canopy diameter (cardinal directions), and signs of grazing damage.
  - Fruit sampling: fruit counts on a segment corresponding to one-eighth of the canopy, with total fruit per plant extrapolated by factor eight; seeds counted per fruit were determined via sampling (five seeds per fruit found).
- Age estimation:
  - 32 shrubs sampled to extract a stem block at the base.
  - Growth rings counted on cross-sections by four observers to estimate age (latewood bands used as annual growth indicators).

## Measurements and variables collected
- Fecundity and seed production:
  - RawFecundityData.csv includes date, site, plot, location, habitat, grazing indicators, and plant-level metrics (sapling/adult counts, growth measurements, grazing evidence).
  - Derived fields estimate total fruits per plant and total seeds per plant.
  - FruitCounts.csv provides seed counts per sampled fruit.
- Growth and age:
  - DendrochronologyPyrcantha.csv contains stem circumference and growth-ring counts from four observers, with a mean count for age estimation.
- Size metrics:
  - Diameter-related data (file named diameter) accompanies growth measurements such as basal circumference/diameter and rosette/canopy dimensions.
- Metadata and definitions:
  - Data fields are explicitly labeled (e.g., Date, Site, Plot, latitude, longitude, Elevation, Habitat_type, Grazing, Plant_grazed, Basal_stem_circumference, Height, Number_of_Fruits, Proportion_counted, Total_fruit, Total_seeds, Sample_ID, Seed_count, mean_count, etc.).

## Data files and access
- RawFecundityData.csv: includes plant-level fecundity and environmental context per plot.
- FruitCounts.csv: seed counts per sampled fruit.
- DendrochronologyPyrcantha.csv: ring counts from multiple observers with an average (mean_count).
- diameter (additional data file for size metrics).
- Data last modified: 09/12/2020; Data submission: 09/12/2020.
- Contact: Fiona Plenderleith, University of Aberdeen (f.plenderleith.19@abdn.ac.uk; permanent: fiona.plenderleith@outlook.com).
- Access status: Freely available data.

## Data quality, governance, and usability considerations
- Multiple observers (four) used for dendrochronology to improve reliability of age estimates.
- Comprehensive metadata for key variables (location, habitat, grazing indicators, plant metrics) facilitates reproducibility and cross-study comparisons.
- Metadata and explicit column explanations accompany each file, supporting data interpretation and reuse.
- Potential data-handling considerations for monitoring use:
  - Derived metrics require transparent computation (e.g., Total_fruit, Total_seeds).
  - Spatial analyses may require harmonization of plot-level coordinates and environmental covariates.
  - Data transformation may be needed to align with standard monitoring indicators (abundance, age structure, fecundity).

## Implications for monitoring frameworks and policy
- Demonstrates a structured approach to measuring invasion dynamics across spatially heterogeneous landscapes.
- Combines direct field measurements (abundance, age, growth) with reproductive output (fruit/seed production) to inform monitoring indicators of invasion pressure.
- Supports data governance by openly sharing datasets and providing detailed metadata, enabling policy-makers to assess data quality, timeliness, and applicability for decision-making.
- Highlights the importance of:
  - Clear documentation of sampling design and measurement protocols.
  - Open data sharing and provenance to reduce barriers in using existing datasets.
  - Managing data interpretation challenges, such as transforming raw counts into policy-relevant metrics.