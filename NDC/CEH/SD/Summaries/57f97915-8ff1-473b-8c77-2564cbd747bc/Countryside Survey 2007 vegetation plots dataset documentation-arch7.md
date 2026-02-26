# Countryside Survey 2007: vegetation plot data, Great Britain Dataset Documentation

## Overview
- Dataset documenting Countryside Survey vegetation plots in Great Britain (2007).
- Two CSV files: one with plot information, one with species lists.
- Designed to support GIS analyses and map-based visualisations of vegetation composition and cover.

## Data files and structure
- Vegetation Plot - Plot Information 2007.csv
  - KEY COLUMNS: YEAR, SQUARE_ID, PLOT_ID, PLOT_TYPE, COUNTRY, ENV_ZONE_2007, EZ_DESC_07
- Vegetation Plot - Species List 2007.csv
  - KEY COLUMNS: YEAR, SQUARE_ID, PLOT_ID, AMALG_PTYPE, BRC_NUMBER, BRC_NAMES, NEST_LEVEL, ZERO_COVER, FIRST_COVER, TOTAL_COVER
- Relationship: both files share YEAR, SQUARE_ID, and PLOT_ID for linking plot info with species data.

## Key fields and meanings
- Plot information
  - COUNTRY: England (ENG), Scotland (SCO), or Wales (WAL)
  - ENV_ZONE_2007 / EZ_DESC_07: environmental zone classification and description
- Species data
  - BRC_NUMBER: species identifier
  - BRC_NAMES: species name
  - NEST_LEVEL: order of first recording
  - ZERO_COVER / FIRST_COVER / TOTAL_COVER: percent cover measures
  - AMALG_PTYPE: plot type (amalgamated type, as defined in the dataset)
- Nomenclature
  - Species names follow Stace, C. (1997) New flora of the British Isles

## Nomenclature, methodology and references
- Field methodologies described in Countryside Survey Vegetation Plots Handbook (Maskell et al., 2008)
- Publications providing context and results:
  - Countryside Survey: UK Results from 2007 (Carey et al., 2008)
  - Countryside Survey Environmental Zones (metadata and zoning)
- Environmental zoning supports spatial analyses of habitat types across GB

## Using in GIS
- Join the two files on YEAR, SQUARE_ID, PLOT_ID to create a plot-level dataset with species composition.
- Map environmental zones using ENV_ZONE_2007 / EZ_DESC_07.
- Visualise species richness and cover using TOTAL_COVER, FIRST_COVER, ZERO_COVER with BRC_NAMES/BRC_NUMBER.

## Data quality, scope and constraints
- Scope: vegetation plots across England, Scotland, and Wales for the year 2007.
- Data compiled from field surveys; nomenclature and fields aligned to established Countryside Survey standards.
- Data quality depends on adherence to the Vegetation Plots Handbook methodologies and consistent data entry across plots.
- Data provided with explicit rights and acknowledgement requirements.

## Rights, acknowledgement and citations
- Data owned by NERC - Centre for Ecology & Hydrology; all rights reserved.
- Acknowledgement required on all copies, publications, presentations, and reports:
  - "Countryside Survey data owned by NERC - Centre for Ecology & Hydrology" and copyright notice.
- When citing or publishing analyses using this data, reference the Countryside Survey project documentation and related publications.

## Related publications and references
- Countryside Survey Website (general project overview and methodologies)
- Carey et al. (2008) Countryside Survey: UK Results from 2007
- Countryside Survey Environmental Zones (metadata and zoning)
- Maskell et al. (2008) Countryside Survey: Vegetation Plots Handbook
- Additional links to metadata hubs and documentation for environment zones and plots