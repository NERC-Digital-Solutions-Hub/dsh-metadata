# Countryside Survey 1990: vegetation plot data, Great Britain Dataset Documentation Version: 1: 28/2/2014

## Overview
- Two-file vegetation dataset from the Countryside Survey 1990 for Great Britain: plot information and species list.
- Data owned by NERC - Centre for Ecology & Hydrology (CEH); intended to support vegetation analyses and ecological reporting.
- Refer to Barr (1991) for detailed methodology and field handbook context.

## File structure and key variables
- Vegetation Plot - Plot Information 1990.csv
  - YEAR: Survey year
  - SQUARE_ID: Survey square identifier
  - PLOT_ID: Plot identifier
  - PLOT_TYPE: Type of plot
  - COUNTRY: England (ENG), Scotland (SCO), or Wales (WAL)
  - ENV_ZONE_2007: Environmental Zone number (2007 version)
  - EZ_DESC_07: Environmental Zone description (2007 version)
- Vegetation Plot - Species List 1990.csv
  - YEAR: Survey year
  - SQUARE_ID: Survey square identifier
  - PLOT_ID: Plot identifier
  - AMALG_PTYPE: Plot type (amalgamated)
  - BRC_NUMBER: Species identifier
  - BRC_NAMES: Species name (taxonomy follows Stace, 1997)
  - NEST_LEVEL: Nest species first recorded in
  - FIRST_COVER: Percent cover in first nest
  - TOTAL_COVER: Percent cover in whole plot

## Data usage and analytics opportunities
- Analyze relationships between vegetation composition and Environmental Zones (ENV_ZONE_2007 / EZ_DESC_07).
- Compute species richness, abundance, and cover metrics per plot/square.
- Map spatial distribution of species and community types across England, Scotland, and Wales.
- Cross-reference with other Countryside Survey datasets (e.g., 2007 UK results) for temporal comparisons and trend analyses.
- Prepare data for modeling vegetation-environment relationships; join the two CSVs on YEAR, SQUARE_ID, and PLOT_ID to create integrated datasets.
- Utilize Stace-based nomenclature for species-level analyses and comparisons with British Isles flora references.

## Data quality, scope, and limitations
- Single time point (1990) for Great Britain; limited temporal scope for trend analysis.
- Environmental zones use 2007 classification, which should be considered when integrating with other years.
- Potential data accessibility challenges noted in metadata context; administrative boundary details may be absent.
- Data may require harmonization across formats and sources; some details are referenced to Barr (1991) Field Handbook for methodology.
- Taxonomic references rely on Stace (1997), which may differ from other taxonomies in some datasets.

## Access, attribution, and provenance
- All Countryside Survey data usage must include acknowledgement:
  - "Countryside Survey data owned by NERC - Centre for Ecology & Hydrology"
  - "Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved."
- Data documentation and environmental zone metadata are available through the Countryside Survey website and linked resources, including Barr (1991) Field Handbook.

## References and further reading
- Countryside Survey: UK Results from 2007 (Carey et al., 2008)
- Countryside Survey Environmental Zones metadata and documentation
- Barr, C.J. 1991 (1990) Countryside Survey Field Handbook
- Countryside Survey website: http://www.countrysidesurvey.org.uk/