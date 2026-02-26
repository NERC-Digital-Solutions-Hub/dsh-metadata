# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Blelham Tarn 1945 to 2013

## Overview
- Long-term monitoring dataset from Blelham Tarn, Cumbria, England, covering surface temperature, surface oxygen, Secchi depth, water alkalinity, pH, and various nutrients and chlorophyll a.
- Sampling frequency ranges from weekly to fortnightly; active from 1945 to 2013 for various variables.
- Data originally collected by the Freshwater Biological Association; since 1989 collected by CEH and its predecessor.
- Variables available for download: TEMP (°C), OXYG (% air-saturation), SECC (m), ALKA (µg CaCO3 per L), PH; NH4N, NO3N, PO4P, TOTP, SIO2, TOCA (all µg per L). Water samples integrated from 0–5 m; measured from a boat at the deepest lake buoy, with shore samples (Flag 2) if buoy access was not possible.

## Content and Variables
- TEMP: surface temperature (°C)
- OXYG: surface oxygen saturation (% air-saturation)
- SECC: Secchi depth (m)
- ALKA: alkalinity (µg CaCO3 per L)
- PH: pH
- NH4N: ammonium (µg N per L)
- NO3N: nitrate (µg N per L)
- PO4P: soluble reactive phosphate (µg P per L)
- TOTP: total phosphorus (µg P per L)
- SIO2: dissolved reactive silicon (µg SiO2 per L)
- TOCA: phytoplankton chlorophyll a (µg per L)
- All values are from water samples collected 0–5 m; integrated when possible, otherwise sampling from shore (Flag 2)

## Data Quality and Documentation
- Raw data status: data are raw and not yet quality controlled or calibrated, with exceptions for double entries from 2005 onward.
- Visual checks have been performed.
- Notable data gaps: March–July 2001 missing due to foot-and-mouth disease restricting lake access.
- Data quality notes and detection limits are indicated via sign_if_LT_LOD (< sign for below detection limit) in the dataset.

## Data Structure and Access
- Format: comma-separated values (CSV).
- Columns include:
  - sdate: measurement date
  - variable: measurement type (e.g., TEMP, OXYG, SECC, ALKA, PH, NH4N, NO3N, PO4P, TOTP, SIO2, TOCA)
  - value: numeric measurement
  - sign_if_LT_LOD: indicator if value is below detection limit
  - flag: sampling location indicator (1 = buoy, 2 = shore)
- Sampling method and location details are embedded in the data (0–5 m integrated samples when possible; boat-based at buoy; shore samples when buoy inaccessible)

## Coverage and Scope
- Timeframe: April 1945 through the end of 2013.
- Coverage spans multiple related variables, with some variables available from 1945 onward; the dataset represents a cohesive, long-term record for surface water properties and phytoplankton chlorophyll a.

## Use and References
- The dataset has been used in several recent publications, illustrating its value for understanding long-term lake dynamics:
  - Modelling effects on phytoplankton communities with changing mixing depth and extinction coefficients
  - Spring phytoplankton phenology across lakes in a climatological region
  - Long-term oxygen depletion related to climate change and eutrophication
  - Catchment productivity controls on CO2 emissions from lakes
  - Lake surface temperatures and related climate context

## Governance and Stewardship Considerations
- Provenance: collected by longstanding organisations (FBA → CEH and predecessors), demonstrating robust historical data lineage.
- Metadata and discoverability: data are provided with clear variable definitions, units, integration depth, sampling location flags, and LOD indicators to support appropriate data use.
- Data quality management: currently raw with limited QC; future stewardship should prioritize formal QA/QC, calibration, and documentation of any adjustments.
- Access and sharing: dataset is available for download; stewardship should maintain clear records of data status, limitations (e.g., LOD, sampling gaps), and any updates or recalibrations.
- Data curation needs: continued attention to interoperability across variables, consistent metadata standards, and transparent handling of shore vs buoy sampling and any gaps in temporal coverage.