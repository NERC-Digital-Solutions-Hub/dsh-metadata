# Predicting spatially heterogeneous invasive spread: Pyracantha angustifolia invading a dry Andean valley in northern Argentina

## Overview
- Freely available dataset associated with a study on predicting spatially heterogeneous invasive spread.
- Data last modified and submitted on 09/12/2020; primary contact is Fiona Plenderleith, University of Aberdeen.
- Field data collected in May 2019 from ten sites, focusing on Pyracantha angusta- (Pyracantha angustifolia) in a dry Andean valley of northern Argentina.
- Contains multiple CSV data files detailing fecundity, fruit counts, dendrochronology, and diameters.

## Study area, design, and scope
- Location: Tafi Del Valle, Tucuman, Argentina.
- Sampling: ten sites with random middle-point selection for three circular plots (20 m diameter), 30 plots in total (area ~9,426 m2).
- Objectives related to invasion dynamics and reproductive output across habitats.
- Habitat categories recorded: grassland, shrubland, rocky (seasonally dry stream beds and boulder fields).

## Data collection and measurements
- Geospatial and environmental data:
  - Coordinates (GPS: Garmin eTrex Touch 35) and elevation recorded at plot centers.
  - Habitat type assigned per plot.
- Plant-level measurements:
  - Sapling counts and reproductive adult counts per plot.
  - For reproductive adults: basal stem diameter, plant height, canopy diameter (four cardinal directions), and evidence of grazing.
  - Fruit sampling: sampled segments representing one-eighth of projected canopy area; total fruit per plant estimated by scaling, with 8x multiplier.
  - Seed counts: seeds per fruit determined by analyzing 30 fruits from 10 shrubs; consistently 5 seeds per fruit observed.
- Age estimation:
  - Harvested 32 shrubs; cylindrical stem blocks extracted for basal ring counts.
  - Growth rings counted by four observers; mean used for age estimates.
- Data collection notes:
  - Field work conducted May 2019; data integrity supported by multiple observers for dendrochronology.

## Data files and schemas
- RawFecundityData.csv
  - Keys: Date, Site, Plot, latitude, longitude, Elevation, Habitat_type, Cotoneaster_presence, Cotoneaster_count, Cattle_dung, Horse_dung, Grazing, Sapling_count, Adult_count, Plant_number, Plant_grazed, Basal_stem_circumference, Basal_stem_diameter, Rosette_Diameter_1-4, Average_Rosette_Diameter, Height, Number_of_Fruits, Proportion_counted, Total_fruit, Total_seeds.
  - Describes fecundity (fruit counts), shrub size, and environmental conditions within plots.
- FruitCounts.csv
  - Keys: Sample_ID, Seed_count.
  - Seed counts per fruit.
- DendrochronologyPyrcantha.csv
  - Keys: Sample_ID, circumference, count1, count2, count3, count4, mean_count.
  - Ring counts from four observers used to derive mean growth-ring count per sample.
- diameter
  - File name indicates diameter-related measurements; details not provided in the excerpt.
- Notes:
  - Additional columns include management/interaction indicators (Cotoneaster presence, grazing indicators, dung presence).

## Data access, contact, and governance
- Accessibility: Freely available data.
- Submission and modification timestamps: 09/12/2020 (submission and last modification).
- Primary contact: Fiona Plenderleith (University of Aberdeen); emails provided for correspondence.
- Documentation quality: Explicit field definitions and column descriptions for major datasets; cross-file linkage via Sample_ID/Plant_number to enable data integration.

## Data quality and interoperability considerations
- Multi-file data integration required (RawFecundityData.csv, FruitCounts.csv, DendrochronologyPyrcantha.csv, diameter).
- Inter-observer variability addressed in age estimation (four observers; mean counts used).
- Metadata includes explicit habitat categorization and environmental indicators (grazing, dung presence, Cotoneaster presence), enabling context-aware analyses.
- Potential challenge for stewardship:
  - Ensuring consistent metadata standards across files (naming, units, and definition harmonization).
  - Integrating data across plots and observers for reproducible analyses, given multiple data types (fecundity, morphology, age).

## Usage, applications, and stewardship notes
- Suitable for invasive species spread modeling, spatial analysis of fecundity, and habitat-specific reproductive output.
- Data governance opportunities:
  - Maintain consistent metadata schemas, controlled vocabularies for habitat_type, and documentation of measurement protocols.
  - Provide clear licensing and citation guidance; outline update mechanisms for new field data.
  - Consider consolidating the diameter-related file into a complete, documented dataset with explicit units and methods.
- Overall aim aligns with data stewardship goals: standardized storage, clear metadata, and accessible datasets to support discovery and reuse by researchers and practitioners.