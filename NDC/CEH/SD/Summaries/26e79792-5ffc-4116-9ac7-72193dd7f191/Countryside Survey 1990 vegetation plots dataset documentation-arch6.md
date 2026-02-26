# Countryside Survey 1990: vegetation plot data, Great Britain Dataset Documentation

## Overview
- Dataset documenting Countryside Survey vegetation plots and species for Great Britain from 1990.
- Consists of two CSV files: one with plot information, one with species lists.
- Data use requires specific acknowledgement to NERC - Centre for Ecology & Hydrology.

## Data Files and Structure
- Vegetation Plot - Plot Information 1990.csv
  - Columns: YEAR, SQUARE_ID, PLOT_ID, PLOT_TYPE, COUNTRY (ENG/SCO/WAL), ENV_ZONE_2007 (Environmental Zone number), EZ_DESC_07 (Environmental Zone description, 2007 version)
- Vegetation Plot - Species List 1990.csv
  - Columns: YEAR, SQUARE_ID, PLOT_ID, AMALG_PTYPE, BRC_NUMBER (species identifier), BRC_NAMES (species name), NEST_LEVEL (nesting level), FIRST_COVER (percent cover in first nest), TOTAL_COVER (percent cover in whole plot)
- Linking: Both files share YEAR, SQUARE_ID, and PLOT_ID to join plot-level context with species observations.
- Species nomenclature follows Stace (1997): New flora of the British Isles.

## Key Variables and Format
- Plot information: year of survey, geographic unit (country), plot type, and environmental zoning data (ENV_ZONE_2007 and EZ_DESC_07).
- Species data: species identifier (BRC_NUMBER), species name (BRC_NAMES), abundance metrics (FIRST_COVER, TOTAL_COVER), and nest-level context (NEST_LEVEL).

## Nomenclature, Provenance and Acknowledgement
- All uses must acknowledge Countryside Survey data owned by NERC - Centre for Ecology & Hydrology.
- Acknowledgement statements recommended for copies, publications, and presentations.
- References for methodology and context include Barr (1991) Countryside Survey Field Handbook and Carey et al. (2008) UK Results from 2007, among others.
- Environmental Zones metadata and related resources are linked (Guidance and data documentation).

## How to Use
- Potential analyses:
  - Compute plot-level metrics: species richness, overall and per-nest cover (FIRST_COVER, TOTAL_COVER).
  - Compare vegetation across countries (ENG, SCO, WAL) and across Environmental Zones (ENV_ZONE_2007 / EZ_DESC_07).
  - Analyze species distribution via BRC numbers and names; track changes using the year dimension if combined with other years.
  - Create self-serve data products (dashboards, pivot tables) for researchers or policymakers; produce maps by SQUARE_ID and PLOT_ID.
- Data integration tips:
  - Join the two files on YEAR, SQUARE_ID, PLOT_ID to associate plot metadata with species observations.
  - Use the Stace nomenclature as the authoritative species taxonomy baseline for consistency with other Countryside Survey outputs.
  - Use environmental zone descriptors to contextualize results geographically.

## Related Publications and References
- Countryside Survey website (general overview and methodologies): http://www.countrysidesurvey.org.uk/
- Barr, C.J. 1991 (1990) Countryside Survey Field Handbook.
- Carey, P.D. et al. 2008, Countryside Survey: UK Results from 2007.
- Environmental Zones metadata and data documentation:
  - http://eidchub.ceh.ac.uk/metadata/0cfd454a-d035-416c-80dc-803c65470ea2
- Other references listed for background and methodology.