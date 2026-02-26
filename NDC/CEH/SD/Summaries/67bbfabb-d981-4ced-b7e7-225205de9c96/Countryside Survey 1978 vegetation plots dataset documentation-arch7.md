# Countryside Survey 1978: vegetation plot data, Great Britain Dataset Documentation Version: 1: 28/2/2014 Countryside Survey data © NERC - Centre for Ecology & Hydrology

## Overview
- Dataset from Countryside Survey vegetation plots in 1978 (and 1977), focusing on vegetation species.
- Comprises two CSV files: 
  - Vegetation Plot - Plot Information 1978.csv
  - Vegetation Plot - Species List 1978.csv
- Data are owned by NERC - Centre for Ecology & Hydrology; all uses must acknowledge the source.

## Data files and schema
- Vegetation Plot - Plot Information 1978.csv
  - YEAR (number) – Year of Survey
  - SQUARE_ID (text) – Survey square identifier
  - PLOT_ID (text) – Plot identifier
  - PLOT_TYPE (text) – Plot type
  - COUNTRY (text) – England (ENG), Scotland (SCO) or Wales (WAL)
  - ENV_ZONE_2007 (number) – Environmental Zone number (2007 version)
  - EZ_DESC_07 (text) – Environmental Zone description (2007 version)

- Vegetation Plot - Species List 1978.csv
  - YEAR (number) – Survey Year
  - SQUARE_ID (text) – Survey square identifier
  - PLOT_ID (text) – Plot identifier
  - AMALG_PTYPE (text) – Plot type (amalgamated)
  - BRC_NUMBER (number) – Species identifier
  - BRC_NAMES (text) – Species name
  - TOTAL_COVER (number) – Percent cover in whole plot

- Taxonomy note
  - Species nomenclature follows Stace, C. (1997). New flora of the British Isles.

- Data usage note
  - All use of Countryside Survey data must be acknowledged.

## GIS-friendly considerations
- Join keys for linking datasets: YEAR, SQUARE_ID, PLOT_ID (across the two files).
- Spatial context: ENV_ZONE_2007 and EZ_DESC_07 provide environmental zoning for mapping at the GB level.
- Attributes for mapping:
  - Plot-level: PLOT_TYPE, COUNTRY, YEAR, environmental zone
  - Species-level within plots: BRC_NUMBER, BRC_NAMES, TOTAL_COVER
- Potential GIS outputs:
  - Spatial distribution of plots by country and environmental zone
  - Species distribution and total cover per plot
  - Aggregated cover statistics across plots or zones
- Data provenance and interoperability: nomenclature aligned to 1997 flora reference; consistent year-based joins facilitate temporal analyses if other years are available.

## Data quality and usage notes
- Data are provided at plot and species-list levels; careful joining is required to integrate plot attributes with species data.
- Environmental zoning uses 2007 version metadata; verify compatibility with your analysis period.
- Acknowledgement and rights statements must accompany all outputs, including maps and publications.

## Attribution and licensing
- Acknowledgement text (to be used on copies, publications, and presentations):
  - "Countryside Survey data owned by NERC - Centre for Ecology & Hydrology"
- Copyright: Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.

## References and access
- Countryside Survey Website (general overview and methodologies)
  - Link: http://www.countrysidesurvey.org.uk/ (as provided)
- Carey et al. (2008) Countryside Survey: UK Results from 2007
  - Link: (as provided in the document)
- Countryside Survey Environmental Zones
  - Metadata and data documentation links:
    - http://eidchub.ceh.ac.uk/metadata/0cfd454a-d035-416c-80dc-803c65470ea2/view
    - http://eidchub.ceh.ac.uk/metadata/0cfd454a-d035-416c-80dc-803c65470ea2/data_documentation_envzones/view
- Field Handbook 1978 (Grange-over-Sands, UK)
  - Link: http://eidchub.ceh.ac.uk/metadata/67bbfabb-d981-4ced-b7e7-225205de9c96/field-handbook-1978/view

## End-user guidance
- Plan data preparation steps:
  - Extract and harmonize fields from both CSVs
  - Join on YEAR, SQUARE_ID, PLOT_ID
  - Map plot-level attributes (country, environmental zone) and visualize species cover
- Ensure proper data acknowledgement in all outputs; maintain traceability to the Countryside Survey source.