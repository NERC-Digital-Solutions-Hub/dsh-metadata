Half-hourly water level and temperature measurements from seven wetland sites in the Pastaza-Marañón Basin, Amazonian Peru, 2018-2020

## Overview
- A dataset of automated, half-hourly measurements of water level and temperature across seven wetland sites in the Pastaza-Marañón Basin, Peru.
- Data collected during parts of 2018, 2019, and 2020 using Solinst Leveloggers in perforated dipwells.
- Corrected for barometric pressure variations; analysis and publication of findings appear in Flores Llampazo et al. (2022) Hydrological Processes.

## Data Collection and Quality Assurance
- Equipment: Solinst Leveloggers installed in perforated plastic tube dipwells.
- Correction: Barometric pressure variations adjusted using nearby barologgers and Levelogger software.
- Quality control: Field-level checks for logical values and atmospheric-pressure corrections applied to ensure data reliability.
- Data file: CSAP_2.1_Dipwell_loggers.csv (UTF-8, CSV).

## Data Structure and Variables
- File: CSAP_2.1_Dipwell_loggers.csv
- Columns:
  - Plot_code: Unique site identifier
  - Date: dd/mm/yyyy
  - Time: Decimal fraction of the day
  - Level: Water level in metres relative to the dipwell datum (positive = rising water)
  - Temperature: Water temperature in degrees Celsius
- Missing data: NA indicates no data recorded
- Geographical scope: Latitude -4.07 to -5.88; Longitude -73.27 to -74.83
- Units and interpretation provided in the metadata, with Level values relative to each site datum

## Geographical and Temporal Coverage
- Location: Seven wetlands in the Pastaza-Marañón Basin, Amazonian Peru
- Spanning years: 2018–2020 (with measurements taken at half-hour intervals within this period)

## Provenance, Publication, and Access
- Project and funding: Funded by UKRI-NERC, grant NE/R000751/1
- Principal investigator: Dr Ian Lawson (itl2@st-andrews.ac.uk)
- Publication: Data analyzed and published by Flores Llampazo et al. (2022) in Hydrological Processes
- Data availability: Described and provided as a structured CSV with detailed metadata; dataset accompanies the publication and includes explicit data structure and QA notes

## Relevance for Monitoring Frameworks and Policy
- Provides high-resolution hydrological and thermal observations essential for environmental health monitoring and wetland management.
- enables tracking of hydrological responses to climatic variability, informing water management, flood risk assessment, and conservation planning.
- Supports development of indicators based on water level dynamics and temperature regimes in wetland ecosystems.
- Metadata-rich dataset aligns with data governance needs: provenance, data quality checks, correction procedures, and transparency about data origin and structure.
- Considerations for governance and data sharing: dataset includes QA steps and sharing of underlying data, illustrating processes and barriers often encountered in monitoring frameworks (e.g., metadata completeness, data standardization, timeliness).