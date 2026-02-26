# Headwater stream invertebrate data 1990 [Countryside Survey] Data Table Descriptions

## Overview
- Documents data table descriptions for headwater stream invertebrate data collected in 1990 as part of the Countryside Survey (NERC - Centre for Ecology & Hydrology).
- Data collection followed standard Countryside Survey freshwater protocols; related manuals and reports cited for context and methodology.

## Data Tables Included
- STREAM_INV_SITE_90.csv
  - Brief Description: Freshwater Stream - invertebrate sampling site data, 1990
  - Key fields include: YEAR, SQUARE (1km square code), SITE_ID, SAMPLE_DATE, WATER_WIDTH, DEPTH1/2/3, SURF_VEL_CAT, CLARITY, SAMPLING_TIME, METHOD, substrate cover (ROCK_PAVEMT, BOULDER_COBBLE, PEBBLE_GRAVEL, SAND, SILT_CLAY), DOM_PART_SIZE, MACROPHYTE_COVER, LC07, LC07_NUM, EZ_DESC_07, COUNTRY, COUNTY07.
- STREAM_INV_SP_90.csv
  - Brief Description: Freshwater Stream invertebrate species data, 1990
  - Key fields include: YEAR, SQUARE, SITE_ID, SAMPLE_DATE, SPECIES_CODE, NAME, LC07, LC07_NUM, EZ_DESC_07, COUNTRY, COUNTY07.

## Methods and Harmonisation
- Sampling protocol
  - Macroinvertebrates sampled using standard 1990 (and later) Countryside Survey methods.
  - Sample area: 5–15 m of stream, within a 3-minute active sampling plus 1 minute of hand search.
  - Net: standard 1 mm mesh pond net; samples returned to CEH for sorting/identification.
  - Supplemental measurements collected: width, depth, substrate to support RIVPACS analyses.
- Taxonomy and abundance harmonisation
  - Taxonomic resolution and counting changed over time (1990: presence/absences; 1998: presence/absence for species; abundance classes for families; 2007: actual abundances for species).
  - To enable comparability, species data harmonised to a common modern taxonomy; standardisation produced a mutually exclusive taxon list for species richness.
- Data handling
  - Field and laboratory data entry process: paper sheets -> database; cross-checking against original lab sheets; corrections of data-entry errors.
  - Data is associated with specific file tables (STREAM_INV_SITE_90.csv and STREAM_INV_SP_90.csv) as described.

## Data Quality, Access, and Governance
- Metadata and data quality
  - Acknowledgement of taxonomy changes and standardisation efforts to ensure consistent interpretation.
  - Metadata completeness and standardised fields documented to aid verification and reuse.
- Data sharing and governance
  - Data usage subject to acknowledgement requirements.
  - Data must be shared in accordance with Countryside Survey copyright and database rights.
- Barriers and considerations for monitoring frameworks
  - Emphasis on ensuring data quality, openness, and governance for reuse in policy evaluation and decision-making.
  - Acknowledgement that data may involve limitations in metadata completeness or historical harmonisation aspects.

## Usage, Acknowledgement, and Related Documents
- Acknowledgement requirement
  - All Countryside Survey data must be acknowledged: “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology.”
  - Countryside Survey © database rights, with all rights reserved.
- Related literature and resources
  - Murphy, John; Weatherby, Anita. 2008. Countryside Survey. Freshwater Manual.
  - Dunbar, M. et al. 2010. Countryside Survey: Headwater Streams Report from 2007.
  - Bunce, R.G.H. et al. 2007. ITE Land Classification of Great Britain 2007. (LC07 references)
  - These references provide methodological details and context for the 1990 headwater invertebrate data and its analyses (e.g., RIVPACS).

## Related Considerations for Monitoring Framework Authors
- Highlights the need to:
  - Define clear, comparable measurement units across time (taxonomic harmonisation).
  - Document data provenance, sampling methods, and any transformations or standardisations.
  - Anticipate barriers such as metadata gaps, data access, and governance requirements when sharing data publicly.
  - Ensure data are accompanied by robust metadata and clear acknowledgement statements to enable policy-relevant analysis and transparent decision-making.