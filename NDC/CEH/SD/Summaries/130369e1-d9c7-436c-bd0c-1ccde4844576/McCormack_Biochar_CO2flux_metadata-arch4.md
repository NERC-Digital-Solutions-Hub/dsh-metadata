# Pot_number  Unique identifier for each individual mesocosm

## Overview
- Describes a mesocosm dataset from a fully factorial experiment examining CO2 flux under different conditions.
- Treatment factors include presence of 2% biochar in soil, crop type (Barley, Ryegrass, Unvegetated), and soil texture (SC, SZL, CL).
- Sampling spans multiple months and years, with detailed temporal data (Month, Year, Day_of_year).
- Experimental design includes four spatial blocks to represent replicates across space.

## Key variables and data structure
- Pot_number: unique identifier for each mesocosm individual.
- Block (biochar): indicates the presence (+) or absence of 2% biochar in soil.
- Crop_type: treatment type - Barley (Hordeum vulgare L.), Ryegrass (Lolium perenne), or Unvegetated.
- Soil_texture: soil texture category - SC (sandy clay), SZL (sandy silt loam), or CL (clay loam).
- Month, Year, Day_of_year: timestamp data for sampling (Day_of_year uses 1–365).
- Block (spatial): spatial block within the enclosure; in the fully factorial design, each treatment combination is represented in four spatial blocks.
- Light_flux: CO2 flux rate during light exposure (g CO2 m-2 h-1); positive = net efflux, negative = net uptake; measured with IRGA.
- Dark_flux: CO2 flux rate during light exclusion (g CO2 m-2 h-1); same sign convention as light_flux; measured with IRGA.
- Photosynthes: derived as Light_flux minus Dark_flux (g CO2 m-2 h-1).
- Note: '.' indicates no sample taken for a given record.

## Data collection and interpretation
- Measurements performed with an infrared gas analyzer (IRGA).
- Positive values indicate CO2 efflux from the system; negative values indicate CO2 uptake.
- Photosynthesis value computed from the difference between light and dark flux readings.
- Missing samples are indicated by a dot (.) in the dataset.

## Data quality and governance considerations for Data Leaders
- Metadata clarity: ensure clear definitions for each column, especially dual usage of Block (biochar presence vs. spatial block).
- Data integrity: units are specified (g CO2 m-2 h-1); verify consistency across the dataset.
- Handling missing data: '.' indicates no sample; establish rules for imputation or exclusion in analyses.
- Data discoverability: maintain complete metadata (treatments, temporal coverage, spatial design) to enable reuse across projects.
- Provenance and versioning: track experimental conditions, measurement methods (IRGA protocol), and any data corrections or recalculations (e.g., Photosynthes).
- Data standards: align with broader data standards for ecological/soil CO2 flux datasets to facilitate cross-study comparability.
- User needs and iteration: support analyses for policy colleagues or partner networks by providing clear, reproducible calculations (e.g., net ecosystem CO2 exchange from light and dark flux).

## Practical implications for use and decision-making
- Enables comparison of CO2 flux across biochar presence, crop types, and soil textures, with temporal resolution.
- Supports assessment of biochar effects on soil CO2 dynamics and the influence of cropping on gas exchange.
- Can inform scaling decisions, soil amendment strategies, and sensor/measurement approaches in similar ecosystems.
- Facilitates collaboration and data sharing within a wider data community by providing a well-documented data schema and derived variables (Photosynthes).