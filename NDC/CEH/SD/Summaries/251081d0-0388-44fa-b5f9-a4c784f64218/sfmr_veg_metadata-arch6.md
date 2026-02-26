# Vegetation data from the South Fork McKenzie River in Oregon, USA.

## Overview
- Purpose: Monitor vegetation response to wildfire across restored-burned, unrestored-burned, and unrestored-unburned sites (reference at Horse Creek, east of the study area).
- Spatial scope: South Fork McKenzie River, Oregon; sampling via transects and quadrats with latitude/longitude coordinates.
- Temporal scope: Data collected in June 2021.

## Datasets and structure
- Four separate CSV files:
  - SFMR_Veg_Coordinates
  - SFMR_Veg_Species
  - SFMR_Veg_Ground
  - SFMR_Veg_Canopy

- SFMR_Veg_Coordinates columns:
  - Transect, Quad, Lat, Long

- SFMR_Veg_Species columns:
  - Transect, Site, Quad, Treatment, Initials, Species.name, Cover.Class, Cover.2, Comments, Category, Family, Duration, Growth_Habit, Native_Status
  - Notes:
    - Treatment values: restored.burned, unrestored.burned, unrestored.unburned
    - Species.name: taxon identified
    - Cover.Class uses Braun-Blanquet scale (0.1–5)
    - Cover.Class.pct provides a percent cover conversion
    - Category: vegetation type (e.g., dicot, monocot, gymnosperm)
    - Duration: perennial/annual/both; Growth_Habit: growth form; Native_Status: native vs introduced

- SFMR_Veg_Ground columns:
  - Transect, Quad, Type, Cover_Class, Cover_class_pct
  - Type: ground vegetation cover category (e.g., leaf litter, bare ground, moss, log)
  - Cover_Class: Braun-Blanquet scale (0.1–5)
  - Cover_class_pct: percent cover conversion

- SFMR_Veg_Canopy columns:
  - Transect, Quad, Measurement, Densiom
  - Measurement: cardinal direction (North=1, East=2, South=3, West=4; decimals for non-cardinal)
  - Densiom: canopy unoccupied by vegetation (%)

## Sampling design and collection
- Methodology: Braun-Blanquet estimated abundance (% cover) across 20 quadrats (1 m x 1 m).
- Quadrats per treatment:
  - Restored/burned: 8 quadrats along Transects 1 and 2
  - Unrestored/burned: 4 quadrats paired with soil data
  - Unrestored/unburned (reference): 4 quadrats paired with soils sampling
  - Additional: 3 quadrats in an additional unburned/non-degraded treatment
- Collection dates: June 2021
- Data provenance: Collected by Andrès Holz, Krista Farris, Bobette Jones, Upekala Wijayratne; data interpreted by all authors
- Data quality: Standardised procedures; field data digitised from field sheets and double-checked prior to upload

## Taxonomy, classification, and metadata
- Taxonomic resolution: Identified to genus/unclear (40 taxa) and to species (29 taxa); total taxonomic units = 69
- Additional attributes per record: Growth_Habit, Duration, Native_Status, Family, and descriptive Comments
- Outputs include a structured linkage between coordinates, species composition, ground cover, and canopy measurements

## Quality control and provenance
- Data collected using standardised procedures by trained fieldworkers
- Digitisation and double-checking performed prior to data upload
- Dataset compiled with clear links between quadrats, transects, treatments, and measurements

## Potential data products and analyses (Data Support perspective)
- Self-serve dashboards or reports comparing vegetation composition and cover across treatments and transects
- Species richness and community composition analyses by treatment (restored vs unrestored; burned vs unburned)
- Quantitative summaries of canopy cover (Densiom) and ground cover types by quadrat and treatment
- Conversion-ready inputs: percent cover (from Braun-Blanquet) for integration with other datasets
- Spatial mapping: quadrat-level coordinates to visualize treatment areas and canopy/ground cover gradients
- Data harmonization: linking coordinates with species, ground, and canopy data for multi-layer analyses

## Access and attribution
- Dataset created by Andrès Holz, Krista Farris, Bobette Jones, Upekala Wijayratne
- Interpreted by all authors
- File names and structure designed to support cross-dataset analyses and data product development