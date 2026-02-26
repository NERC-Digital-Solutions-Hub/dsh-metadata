# Countryside Survey 2007: vegetation plot data, Great Britain Dataset Documentation

## Overview
- Datasets from Countryside Survey covering vegetation data collected in 2007 across Great Britain.
- Comprises two CSV files: one with plot-level information and one with species lists per plot.
- Data are owned by NERC - Centre for Ecology & Hydrology (CEH).

## Data files and structure
- Vegetation Plot - Plot Information 2007.csv
  - YEAR: Year of Survey
  - SQUARE_ID: Square identifier
  - PLOT_ID: Plot identifier
  - PLOT_TYPE: Type of plot
  - COUNTRY: England (ENG), Scotland (SCO) or Wales (WAL)
  - ENV_ZONE_2007: Environmental Zone number
  - EZ_DESC_07: Environmental Zone description
- Vegetation Plot - Species List 2007.csv
  - YEAR: Survey Year
  - SQUARE_ID: Survey square identifier
  - PLOT_ID: Plot identifier
  - AMALG_PTYPE: Plot type
  - BRC_NUMBER: Species identifier
  - BRC_NAMES: Species name
  - NEST_LEVEL: Nest species first recorded in
  - ZERO_COVER: Percent cover in zero nest
  - FIRST_COVER: Percent cover in first nest
  - TOTAL_COVER: Percent cover in whole plot

## Nomenclature and standards
- Species nomenclature follows Stace, C. (1997) New flora of the British Isles.
- Data are organized to support consistent interpretation of plot and species information.

## Provenance, rights and acknowledgements
- Countryside Survey data are owned by NERC - Centre for Ecology & Hydrology; all rights reserved.
- All uses of Countryside Survey data must be acknowledged.
- Required acknowledgement language:
  - "Countryside Survey data owned by NERC - Centre for Ecology & Hydrology"
  - "Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved."

## Related publications and access
- Maskell et al., 2008. Countryside Survey: Vegetation Plots Handbook (field methodology).
- Carey et al., 2008. Countryside Survey: UK Results from 2007.
- Countryside Survey website and environmental zones metadata are provided as references and further reading.
- Links referenced include the Countryside Survey website and environmental zones metadata pages.

## Data management and stewardship considerations
- Clear mapping between plot information and species lists is required for proper interpretation (PLOT_ID and SQUARE_ID used across files).
- Metadata includes environmental zone definitions and descriptions to aid contextual data use.
- Alignment with referenced handbooks and UK Results reports is recommended to ensure methodological compatibility.
- Data may require ongoing governance for updates or corrections, with consistent acknowledgment in any dissemination.