# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Esthwaite Water 2014 to 2018

## Overview
- Ongoing long-term fortnightly monitoring dataset from Esthwaite Water, Cumbria, England (2014–2018).
- Measured variables: surface temperature (TEMP), surface oxygen saturation (OXYG), Secchi depth (SECC), alkalinity (ALKA), pH, ammonium (NH4N), nitrate (NO3N), soluble reactive phosphate (PO4P), total phosphorus (TOTP), dissolved reactive silicon (SIO2), and phytoplankton chlorophyll a (TOCA).
- Purpose: support environmental health assessment and policy evaluation by providing temporal data on physical, chemical, and biological conditions.
- Sampling regime: integrated from 0–5 m, fortnightly; conducted from a boat at the deepest point buoy; when buoy access is unavailable, samples collected near the shore.
- Data availability: CSV format with detailed variable descriptions and metadata fields.

## Data Collected and Methods
- Variables and units:
  - TEMP: surface temperature in degrees Celsius
  - OXYG: surface oxygen saturation in % air-saturation
  - SECC: Secchi depth in metres
  - ALKA: alkalinity in µg CaCO3 per litre
  - pH
  - NH4N: ammonium in µg N per litre
  - NO3N: nitrate in µg N per litre
  - PO4P: soluble reactive phosphate in µg P per litre
  - TOTP: total phosphorus in µg P per litre
  - SIO2: dissolved reactive silicon in µg per litre
  - TOCA: phytoplankton chlorophyll a in µg per litre
- Data structure in CSV with columns:
  - Date, Description (variable), Value, Sign (if < LOD), Flag
- Measurement approach:
  - Water samples integrated from 0–5 m.
  - Flag 1 indicates sampling at the buoy location; Flag 2 indicates near-shore sampling when buoy access was not possible.
- Data notes:
  - Values below detection limit are marked with a < sign in Sign (if<LOD).
  - Data were collected from 2014-01 through 2018-12.

## Data Structure and Access
- Data format: comma-separated values (CSV) with explicit columns and descriptive metadata.
- Values are raw and have not yet undergone quality control or calibration (though double-entered and visually checked).
- Missing data explained by weather conditions or staff availability.

## Quality Control and Limitations
- Status: raw data not quality controlled or calibrated at the time of publication.
- Quality checks performed: double entry and visual verification.
- Limitations:
  - Some samples not integrated (Flag 2) when buoy sampling was not possible.
  - Missing data due to weather or staff constraints.
  - Requires subsequent QC calibration for formal policy-use readiness.

## Governance, Funding, and Use
- Funding: Natural Environment Research Council (NE/R016429/1) as part of the UK-SCaPE programme delivering National Capability.
- Scholarly use and references:
  - Pilotto et al. (2020) Nature Communications
  - Wang et al. (2016) Scientific Reports
  - Woolway et al. (2016) Bulletin of the American Meteorological Society
  - Overview reference: Maberly et al. (2017) Ecological Informatics

## Relevance to Monitoring Frameworks
- Provides a comprehensive suite of environmental health indicators (physical, chemical, and biological) suitable for evaluating policy outcomes and guiding future decisions.
- Supports long-term trend analysis and cross-variable integration (e.g., relationships between temperature, oxygen, nutrients, and chlorophyll a).
- Metadata and data handling practices align with the need for data provenance, openness (where applicable), and clear data descriptions to enable governance and accountability.
- Highlights practical governance considerations:
  - Handling raw data and planning for QC/calibration before formal reporting.
  - Importance of complete metadata (LOD, sampling location, depth) to enable data reuse and verification.
  - Operational challenges such as accessibility (buoy vs. shore sampling) and staffing affecting data continuity.