# Countryside Survey 1998: vegetation plot data, Great Britain Dataset Documentation

- The Countryside Survey dataset provides vegetation plot data from Great Britain (England, Scotland, and Wales) collected in 1998 (and 1999). It consists of two CSV files: one with plot information and one listing the species found in each plot.
- Source and rights: data owned by NERC - Centre for Ecology & Hydrology; all uses must acknowledge Countryside Survey data and include the specified acknowledgement. © NERC-CEH.

## Dataset structure

- Vegetation Plot - Plot Information 1998.csv
  - YEAR: survey year
  - SQUARE_ID: survey square identifier
  - PLOT_ID: plot identifier
  - PLOT_TYPE: plot type
  - COUNTRY: England (ENG), Scotland (SCO), or Wales (WAL)
  - ENV_ZONE_2007: Environmental Zone number (2007 version)
  - EZ_DESC_07: Environmental Zone description (2007 version)

- Vegetation Plot - Species List 1998.csv
  - YEAR: survey year
  - SQUARE_ID: survey square identifier
  - PLOT_ID: plot identifier
  - AMALG_PTYPE: plot type
  - BRC_NUMBER: species identifier
  - BRC_NAMES: species name
  - NEST_LEVEL: nest species first recorded in
  - FIRST_COVER: percent cover in first nest
  - TOTAL_COVER: percent cover in the whole plot

## Field nomenclature and references

- Species names follow Stace, C. (1997) New flora of the British Isles.
- Cross-references: Barr, 1998 for field handbook details; Carey et al. (2008) UK results from 2007; Countryside Survey Environmental Zones metadata available online.

## Geographic scope and environmental context

- Country coverage: England, Scotland, Wales.
- Environmental zones: data include ENV_ZONE_2007 and descriptions (2007 version) to contextualize plots within environmental characteristics.

## Usage, attribution, and references

- All uses of Countryside Survey data must be acknowledged using the provided acknowledgements.
- Relevant publications and resources:
  - Countryside Survey website (general overview and methodologies)
  - Carey et al. (2008) Countryside Survey: UK Results from 2007
  - Countryside Survey Environmental Zones (metadata and zoning)

## Additional notes for analysts

- Data pertains to 1998 (and 1999) plot records; cross-year analyses would require additional datasets beyond this documentation.
- Plot-level and species-level data can be joined via SQUARE_ID and PLOT_ID to analyze vegetation composition, species richness, and cover patterns by environmental zone or country.
- Data quality considerations include consistent nomenclature (Stace 1997), and potential limitations around missing details or scale when integrating with other datasets.