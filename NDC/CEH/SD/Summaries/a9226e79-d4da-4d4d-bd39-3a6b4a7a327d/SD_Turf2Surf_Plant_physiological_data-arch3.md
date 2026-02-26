# Details of data structure for the dataset Plant physiological measurements in North Wales and Northwest England (2013, 2014 and 2016) as detailed in the table Turf2Surf_Plant_physiological_data.csv

- This document supplements the supporting documentation for Turf2Surf data series (Turf2Surf_WP2_Supporting_documentation.rtf).
- Focuses on the plant physiological measurements dataset collected in 2013, 2014, and 2016 from North Wales and Northwest England.

## Data structure overview

- The datasets share a common set of first 9 columns describing site and sampling context.
- Datasets listed as sharing the first 9 columns:
  - Plant structural measurements in North Wales and Northwest England (2013 and 2014)
  - Plant aboveground and belowground standing biomass measurements in the Conwy catchment, North Wales (2013 and 2014)
  - Soil carbon data in the Conwy catchment, North Wales (2013 and 2014)
  - Soil physical, chemical and biological measurements in the Conwy catchment, North Wales (2013 and 2014)
  - Plant aboveground and belowground standing biomass measurements in the Conwy catchment, North Wales (2013 and 2014)
- Column A: unique Site Number
- Columns B–C: Habitat and Habitat Description
- Column D: Site name
- Column E: Ecosystem Component (Plant, Soil, or Roots)
- Column F: If Plant, plant species (otherwise NA)
- Columns G–H: Plot number and Replicate number
- Column I: Soil depth interval (for soil and roots)
- Missing values are indicated as NA (e.g., restricted depths, limited replicates, outliers)

## Data structure of the Plant physiological measurements dataset

- This dataset has 9 additional columns beyond the initial 9
- 96 rows in total

## Variables and measurements (columns J–R)

- J: Year of measurement
- K: Unit = µmol m^-2 s^-1; Description = Vcmax (Maximum rate of carboxylation at 25°C)
- L: Unit = µmol m^-2 s^-1; Description = Jmax (Electron transport capacity at 25°C)
- M: Unit = µmol m^-2 s^-1; Description = Asat (Photosynthetic rate at saturating irradiance and 400 ppm CO2 at 25°C)
- N: Unit = gm^-2; Description = Leaf mass area (Leaf mass per leaf area)
- O: Unit = %; Description = Foliar nitrogen content
- P: Unit = %; Description = Foliar phosphorus content
- Q: Unit = cm^2 g^-1; Description = Specific leaf area (SLA)
- R: Unit = none; Description = Comments

## Data quality and completeness

- NA entries indicate data not collected for certain sites or components.
- Some sites (5, 7, 14, 19) have leaves sampled in 2015 for re-analysis of foliar N and P content only.
- The dataset requires interpretation of columns and units when integrating with other monitoring data.

## Sampling and context

- Geographic scope: North Wales and Northwest England, with Conwy catchment focus for some datasets.
- Sampling context includes habitat type, plot-level replication, and soil depth considerations for soil and root components.
- Measurements capture key physiological and foliar traits relevant to plant function and nutrient status.

## Relevance for monitoring frameworks

- Provides structured, site-based metadata and a core set of functional plant traits and leaf chemistry measures for environmental health monitoring.
- Facilitates cross-dataset integration by using a consistent first-9-column schema (site, habitat, component, plot, replication, soil depth).
- Enables monitoring of photosynthetic capacity (Vcmax, Jmax, Asat), leaf traits (LMA, SLA), and foliar nutrients (N, P) across sites and years.
- Data governance considerations implied by the structure include:
  - Clear metadata needs (habitat description, site names, plot/replicate, soil depth) to ensure comparability.
  - Transparency about missing data (NA) and data provenance (originator metadata) for reproducibility.
  - Documentation of any data sharing or access constraints if applying these data within policy monitoring dashboards.

## Implications for policy evaluation and future decisions

- The dataset supports assessment of plant functional responses to environmental change across multiple sites and years.
- The standardized structure and key variables facilitate reporting, dashboards, and stakeholder communications in environmental health monitoring.
- When linking to governance processes, ensure data quality, open sharing where possible, and clear data provenance to enable transparent decision-making.