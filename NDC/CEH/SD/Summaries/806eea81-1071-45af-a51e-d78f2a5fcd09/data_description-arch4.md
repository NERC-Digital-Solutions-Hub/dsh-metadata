# Predicting spatially heterogeneous invasive spread: Pyracantha angustifolia invading a dry Andean valley in northern Argentina. Under review

## Overview
- Freely available field data from a study on Pyracantha angustifolia invasion in northern Argentina, with methods, dataset descriptions, and sample metadata.
- Data collected May 2019 at 10 sites; includes spatial, habitat, plant morphology, fecundity, and dendrochronology metrics; multiple observers for some measures to support reliability.
- Data last modified and submission date: 09/12/2020. Contacts: Fiona Plenderleith.

## Datasets Included
- RawFecundityData.csv
  - Variables span date, site/plot, location (latitude, longitude, elevation), habitat_type, presence/count of Cotoneaster and dung, grazing indicators, sapling/adult counts, plant IDs, grazing evidence, basal circumference/diameter, rosette diameters, height, fruit counts, sampling proportions, total fruits and seeds per plant.
- FruitCounts.csv
  - Sample_ID and Seed_count (seeds per fruit) data.
- DendrochronologyPyrcantha.csv
  - Sample_ID, circumference, and ring counts from four observers (count1–count4) plus mean_count.
- diameter (incomplete/file name present; additional diameter-related data likely in this or related file).

## Study Design and Key Variables
- Field design
  - Ten sites in Tafi Del Valle, Tucuman, May 2019.
  - At each site: three circular plots (20 m diameter) centered at randomly selected midpoints; plots separated by at least 20 m (total: 30 plots; ~9,426 m2).
  - For each plot: coordinates and elevation recorded; habitat type categorized as grassland, shrubland, or rocky.
- Plant and habitat measurements
  - Counts of Pyracantha saplings (>10 cm, non-reproductive) and reproductive adults per plot.
  - For reproductive adults: basal stem diameter, plant height, canopy diameter in four directions; grazing signs noted.
  - Fruit sampling: fruits counted on one-eighth of canopy area, with segment selection via random compass bearing; total fruits per plant estimated by scaling by eight.
  - Seeds per fruit determined by sampling 30 fruits from 10 shrubs; five seeds per fruit observed.
- Age estimation
  - Ground-level shrubs (n=32) used to harvest stem blocks; growth rings counted by four observers to estimate age.

## Data Processing and Calculations
- Fecundity estimates
  - Total_fruit per plant = Number_of_Fruits × Proportion_counted.
  - Total_seeds per plant = Total_fruit × Seed_count.
- Ring chronology
  - Growth-ring counts obtained from cross-sections; four observers provide counts to derive mean_count.
- Notable metadata fields
  - Date, site ID, plot ID, latitude, longitude, elevation, habitat_type, grazing indicators, plant morphometrics, and sampling details (e.g., Proportion_counted).

## Metadata, Access, and Provenance
- Descriptions provided for each data file’s columns (definitions and units where applicable).
- Data submission and modification date: 09/12/2020.
- Freely available data with explicit contact for data inquiries (Fiona Plenderleith; University of Aberdeen).
- Data organization supports linking across datasets via common identifiers (Site, Plot, Sample_ID, Plant_number).

## Data Quality and Validation
- Use of multiple observers for dendrochronology increases reliability of age estimates.
- Direct measurement protocols for plant metrics and fecundity; explicit calculation rules for derived fields (Total_fruit, Total_seeds).
- Habitat categorization and spatial coordinates enable reproducibility and cross-site comparisons.

## Considerations for Data Leaders
- The dataset exemplifies an end-to-end data lifecycle: field collection, processing rules, derived metrics, and rich metadata suitable for open data sharing.
- Strengths
  - Spatially explicit data with GPS coordinates and elevations.
  - Comprehensive plant metrics tied to ecological questions (fecundity, age structure, grazing impact).
  - Derived fields and clear calculation methods documented alongside raw counts.
  - Multiple observers for critical measurements (growth rings) to improve reliability.
  - Open-access sharing with clear data descriptions and contact points.
- Potential gaps or considerations
  - The presence of an incomplete or misnamed file (diameter) suggests verification of dataset completeness and naming consistency for discoverability.
  - Some fields (e.g., Cotoneaster_presence, Cotoneaster_count, habitat categories) may require standardization if integrated with broader datasets.
  - Metadata could be expanded with data licensing details and data quality flags beyond the current descriptions.
- Practical application
  - Data can support spatial modeling of invasive spread, fecundity-based risk assessments, and age-structure analyses.
  - Suitable for integration into broader data networks examining plant invasions, provided consistent standards and linking keys are maintained.

## Endnotes
- The document provides a robust, well-structured data suite with explicit field definitions and processing steps, appropriate for data-driven analysis by data leaders seeking to implement or benchmark effective data strategies in ecological surveillance and invasion biology.