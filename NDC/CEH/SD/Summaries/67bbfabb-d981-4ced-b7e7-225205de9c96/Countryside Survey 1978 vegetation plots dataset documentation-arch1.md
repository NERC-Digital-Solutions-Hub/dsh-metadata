# Countryside Survey 1978: vegetation plot data, Great Britain Dataset Documentation Version: 1: 28/2/2014

## Overview
- Dataset from Countryside Survey vegetation plots recorded in 1978 (and 1977), covering Great Britain (England, Scotland, Wales).
- Consists of two CSV files: one with plot information, one listing species found in each plot.
- Data are governed by acknowledgements and copyright to NERC - Centre for Ecology & Hydrology.

## Data files and structure
- Vegetation Plot - Plot Information 1978.csv
  - Columns: YEAR, SQUARE_ID, PLOT_ID, PLOT_TYPE, COUNTRY, ENV_ZONE_2007, EZ_DESC_07
- Vegetation Plot - Species List 1978.csv
  - Columns: YEAR, SQUARE_ID, PLOT_ID, AMALG_PTYPE, BRC_NUMBER, BRC_NAMES, TOTAL_COVER
- Plot-level and species-level data can be linked via SQUARE_ID and PLOT_ID.

## Key variables and nomenclature
- Plot information:
  - YEAR: survey year
  - SQUARE_ID: survey square identifier
  - PLOT_ID: plot identifier
  - PLOT_TYPE: type of plot
  - COUNTRY: ENG, SCO, or WAL
  - ENV_ZONE_2007: Environmental Zone number (2007 version)
  - EZ_DESC_07: Environmental Zone description (2007 version)
- Species data:
  - BRC_NUMBER: species identifier
  - BRC_NAMES: species name
  - AMALG_PTYPE: plot type
  - TOTAL_COVER: percent cover for the species in the whole plot
- Taxonomy: species names follow Stace, C. (1997) New flora of the British Isles.

## Usage and attribution
- All use of Countryside Survey data must be acknowledged.
- Required acknowledgement text:
  - "Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology"
  - "Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved."

## References and further information
- Countryside Survey Website: general overview and methodologies
- Countryside Survey Website: UK Results from 2007 ( Carey et al., 2008 )
- Field Handbook 1978 (Grange-over-Sands, NERC/Institute of Terrestrial Ecology)
- Countryside Survey: Environmental Zones (metadata and data documentation)
- Data-related links (examples listed in the document):
  - Field Handbook 1978: viewable via metadata portal
  - Countryside Survey Environmental Zones: metadata and data documentation

## Data provenance and rights
- Data owned by NERC - Centre for Ecology & Hydrology; all rights reserved.
- Clear line of credit and usage guidance provided for publications, presentations, and reports.