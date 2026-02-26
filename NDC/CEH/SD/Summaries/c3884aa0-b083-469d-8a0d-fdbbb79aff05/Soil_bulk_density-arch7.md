# DATA HEADER INFORMATION for Soil_bulk_density.csv

## Overview
- Records soil bulk density.
- Soil samples collected in cylinders, oven-dried 24 hours at 105°C.
- Coarse fraction (rocks/roots/biomass) removed by passing through a 2 mm sieve.
- Bulk density values adjusted using the proportion of coarse fraction.

## Data provenance and references
- Related manuals: Manual_1_ Classical_Survey; Manual_3_Laboratory_Works.
- DOIs/links: https://doi.org/10.5285/c3884aa0-b083-469d-8a0d-fdbbb79aff05
- Programme: ESPA; Project: P4GES.
- Acknowledgement required for products derived from these data: Laboratoire des Radio Isotopes, Université d'Antananarivo.

## Data fields (structure)
- site_id
  - Information: P4GES site code
  - Variable Type: Text String
  - Unit: .
- subplot
  - Information: subplot where sampling was done
  - Variable Type: Categorical
  - Unit: S1 / S2 / S3 / S4
- Bulk_density
  - Information: Soil bulk density value
  - Variable Type: Numeric
  - Unit: Grams per cubic centimeter (g.cm-3)
- depth
  - Information: depth of the sampled soil layer (from 10 to 100 cm)
  - Variable Type: Numeric
  - Unit: Centimeter (cm)

## Sampling details and data quality
- Bulk density is adjusted by the proportion of the coarse fraction.
- Depth range indicates sampling across 10–100 cm soil profile.
- Data types: site_id (text), subplot (categorical), bulk_density (numeric), depth (numeric).

## GIS usage notes
- Use site_id as the unique identifier; join with spatial layers of P4GES sites.
- Subplot provides stratification (S1–S4) for thematic analyses.
- Depth serves as a vertical attribute for soil-profile mapping.
- Bulk_density is suitable for thematic mapping (ensure unit consistency: g/cm3).
- Plan for data cleaning/transformations when integrating with other datasets.

## Acknowledgments
- Acknowledgement required for Laboratoire des Radio Isotopes, Université d'Antananarivo for products derived from these data.