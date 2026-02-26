# Countryside Survey 1978: vegetation plot data, Great Britain Dataset Documentation Version: 1: 28/2/2014

## Overview
- Documentation for Countryside Survey vegetation plot data from 1978 (and 1977), held as two CSV files: one with plot information and one with species lists.
- Data are owned by NERC - Centre for Ecology & Hydrology; all uses must acknowledge the dataset.

## Data files and structure
- Vegetation Plot - Plot Information 1978.csv
  - YEAR: Survey year
  - SQUARE_ID: Survey square identifier
  - PLOT_ID: Plot identifier
  - PLOT_TYPE: Type of plot
  - COUNTRY: England (ENG), Scotland (SCO), or Wales (WAL)
  - ENV_ZONE_2007: Environmental Zone number (2007 version)
  - EZ_DESC_07: Environmental Zone description (2007 version)
- Vegetation Plot - Species List 1978.csv
  - YEAR: Survey year
  - SQUARE_ID: Survey square identifier
  - PLOT_ID: Plot identifier
  - AMALG_PTYPE: Plot type
  - BRC_NUMBER: Species identifier
  - BRC_NAMES: Species name
  - TOTAL_COVER: Percent cover in whole plot

## Nomenclature and data standards
- Species names follow Stace, C. (1997) New flora of the British Isles.

## Usage, acknowledgment, and rights
- All uses of Countryside Survey data must be acknowledged.
- Required acknowledgement text (to be used on copies, publications, reports, and presentations):
  - Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology
  - Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.

## Related publications and references
- Countryside Survey Website: general overview and methodologies
- Carey et al. (2008): Countryside Survey: UK Results from 2007
- Countryside Survey Environmental Zones (GB-wide zoned areas)
- Field Handbook 1978 (Grange-over-Sands, UK) – Field survey handbook
- Links and data documentation can be found via the Countryside Survey portal and CEH metadata pages

## How to use the data (data support guidance)
- Join plots and species data via PLOT_ID and SQUARE_ID to analyze vegetation composition by plot.
- Use YEAR and COUNTRY to compare across years and regions (England, Scotland, Wales).
- TOTAL_COVER provides within-plot species abundance; BRC_NUMBER and BRC_NAMES identify species for analysis.
- Environmental Zone metadata (ENV_ZONE_2007, EZ_DESC_07) supports spatial analyses aligned with 2007 environmental classifications.
- When preparing outputs, ensure proper data provenance and the required Countryside Survey acknowledgment.

## Data provenance and access
- Data are sourced from Countryside Survey datasets and related publications; see referenced reports and the Countryside Survey website for methodologies and supplementary documents.