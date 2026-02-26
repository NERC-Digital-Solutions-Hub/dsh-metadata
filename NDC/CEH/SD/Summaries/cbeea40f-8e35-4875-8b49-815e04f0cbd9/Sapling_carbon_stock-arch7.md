# DATA HEADER information for Sapling_carbon_stock.csv

## Overview
- Records the carbon stock of regenerating tree clusters.
- Data intended for GIS-enabled map-based visualisations and spatial analysis.
- Spatial context: counts and weights calculated within a 2-meter radius circle around each site.

## Provenance and acknowledgements
- Programme: ESPA; Project: P4GES.
- DOI: https://doi.org/10.5285/cbeea40f-8e35-4875-8b49-815e04f0cbd9
- Acknowledgement required for products derived from these data: Laboratoire des Radio Isotopes, Université d'Antananarivo.

## Key fields and data types
- site_ID
  - Information = P4GES site code
  - Variable type = Text String
  - Unit = (not specified)
- Number_saplings
  - Information = number of trees with diameter < 5 cm and height > 1.3 m counted in a 2 m radius circle
  - Variable type = Numeric
  - Unit = (not specified)
- Number_collected_saplings
  - Information = number of sapling trees collected among the population inside the 2 m radius circle
  - Variable type = Numeric
  - Unit = (not specified)
- Fresh_weight_total
  - Information = weight of all the collected saplings
  - Variable type = Numeric
  - Unit = grams
- Fresh_weight_sample
  - Information = weight of the sample among the collected saplings (some samples collected for biomass analysis weighed in the field)
  - Variable type = Numeric
  - Unit = grams
- Dry_weight_sample
  - Information = weight of subsample after oven drying (stabilized dry weight)
  - Variable type = Numeric
  - Unit = grams
- Dry_weight_collected_saplings
  - Information = weight of all collected saplings after oven drying (stabilized dry weight)
  - Variable type = Numeric
  - Unit = grams
- Biomass
  - Information = Biomass stock of sapling
  - Variable type = Numeric
  - Unit = milligrams per hectare (Mg.ha-1)
- Stock_C
  - Information = Carbon stock of sapling
  - Variable type = Numeric
  - Unit = milligrams per hectare (Mg.ha-1)

## Notes on data handling
- Notes: "Notes" indicates missing data (means no data available for that entry).
- Some fields show blank metadata under Field and materials resources; emphasis on numeric values with specified units where provided.

## Data usage considerations for GIS
- Ensure consistent handling of units (mg.ha-1) across datasets when aggregating carbon and biomass.
- Maintain the 2-meter radius spatial context for all calculations and visualisations.
- Record and display site_ID as the primary spatial identifier for linking with other GIS layers.
- Be aware of potential data gaps indicated by notes for proper gap-filling or exclusion in analyses.