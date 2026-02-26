# Countryside Survey 1998: vegetation plot data, Great Britain Dataset Documentation

## Overview
- Dataset documents Countryside Survey vegetation data collected in 1998 (and 1999), focusing on plot information and species lists.
- Consists of two CSV files: one with plot-level information and one with species recorded per plot.
- Data are owned by NERC – Centre for Ecology & Hydrology (CEH); acknowledgement and copyright restrictions apply.
- Intended for integration into GIS-style analyses and map-based visualisations of vegetation across Great Britain.

## Data files and key fields

- Vegetation Plot - Plot Information 1998.csv
  - YEAR: Survey year
  - SQUARE_ID: Survey square identifier
  - PLOT_ID: Plot identifier
  - PLOT_TYPE: Type of plot
  - COUNTRY: England (ENG), Scotland (SCO), or Wales (WAL)
  - ENV_ZONE_2007: Environmental Zone number (2007 version)
  - EZ_DESC_07: Environmental Zone description (2007 version)

- Vegetation Plot - Species List 1998.csv
  - YEAR: Survey year
  - SQUARE_ID: Survey square identifier
  - PLOT_ID: Plot identifier
  - AMALG_PTYPE: Plot type (amalgamated)
  - BRC_NUMBER: Species identifier
  - BRC_NAMES: Species name
  - NEST_LEVEL: Nest species first recorded level
  - FIRST_COVER: Percent cover in first nest
  - TOTAL_COVER: Percent cover in the whole plot

- Nomenclature: Species names follow Stace, C. (1997) New flora of the British Isles.

## How to use in GIS

- Link the two files on YEAR, SQUARE_ID, and PLOT_ID to associate plot-level attributes with species data.
- Map applications:
  - Create per-plot vegetation composition and species richness.
  - Visualise cover metrics (FIRST_COVER, TOTAL_COVER) by plot.
  - Explore spatial patterns across countries (ENG/SCO/WAL) and Environmental Zones (ENV_ZONE_2007 / EZ_DESC_07).
  - Integrate with other GIS layers to assess habitat associations and landscape context.
- Data fusion considerations:
  - Different data resolutions may require harmonisation.
  - Cleaning and standardising data prior to analysis is recommended, given the dataset's multi-source origin.

## Data standards, quality, and practices

- Data were collected as part of the Countryside Survey project; users should be aware of potential variability in data collection and formatting across plots.
- The documentation notes that data are part of a broader suite of Countryside Survey materials; standardisation and clean-up may be needed for integration with other datasets.
- Explicit data quality metrics are not provided in this document; attention to consistency in field values (e.g., cover percentages, plot types) is advised.

## Usage, citations, and references

- All uses of Countryside Survey data must include the formal acknowledgement:
  - Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology
  - Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.
- Key references and resources:
  - Countryside Survey Website: general project overview and methodologies
  - Carey et al. (2008): Countryside Survey: UK Results from 2007
  - Barr (1998): Countryside Survey 2000 Field Handbook (reference for field methodology)
  - Countryside Survey Environmental Zones documentation and metadata
- Useful links in the references section accompany the dataset documentation for deeper methodological context.