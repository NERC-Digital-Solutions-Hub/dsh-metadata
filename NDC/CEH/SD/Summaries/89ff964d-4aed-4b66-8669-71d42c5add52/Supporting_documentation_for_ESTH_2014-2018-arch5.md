# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Esthwaite Water 2014 to 2018. Feuchtmayr, H., Clarke, M.A., De Ville, M.M., Dodd, B.A., Fletcher, J.M., James, J.B., Mackay, E.B., Pereira, M.G., Rhodes, G., Thackeray, S.J., Maberly, S.C. (2021)

## Overview
- Long-term, fortnightly monitoring dataset from Esthwaite Water, Cumbria, England.
- Covers surface temperature (TEMP), surface oxygen saturation (OXYG), Secchi depth (SECC), alkalinity (ALKA), pH, ammonium (NH4N), nitrate (NO3N), soluble reactive phosphate (PO4P), total phosphorus (TOTP), dissolved reactive silicon (SIO2) and phytoplankton chlorophyll a (TOCA).
- Sampling targets the 0–5 m water layer; measurements taken from a boat at the deepest part (buoy) with shore-based sampling when buoy access is not possible.
- Data span: January 2014 to end of 2018.

## Sampling regime and collection methods
- Fortnightly sampling with measurements of multiple physical, chemical and biological variables.
- Water samples typically integrated from 0 to 5 m; when buoy sampling was not possible, samples were taken near the shore and noted.
- Data are provided as raw measurements (not yet quality controlled or calibrated).
- Missing data mainly due to weather conditions or staff shortages.
- Data entries were double-entered and visually checked for accuracy.

## Data quality and governance
- Status: raw data not yet quality controlled or calibrated.
- Quality assurance steps performed: double data entry and visual checks.
- Metadata and unit definitions are explicit (units for each variable are specified; detection limits are indicated with a “<” in the data column).
- Data provenance and collection methods are documented (sampling location, depth, and conditions).
- Data availability implied by “data available to download”; suitable for discovery and reuse, with references in recent publications.

## Data structure and metadata
- Stored as comma-separated values (CSV) with explicit columns:
  - Date: measurement date.
  - Variable, Description: name and units for each parameter (e.g., TEMP in °C, OXYG in % air-saturation, SECC in metres, ALKA in µg CaCO3 L−1, pH, NH4N, NO3N, PO4P, TOTP, SIO2, TOCA).
  - Value, Description: numerical values for each variable.
  - Sign (if<LOD), Description: indicates values below detection limit with a < sign.
  - Flag, Description: 1 = sample collected at buoy location; 2 = sample collected near shore when buoy sampling was not possible.
- Clear interpretation of data limits, measurement conditions, and data completeness.

## Data availability, usage, and impact
- Data are suitable for long-term trend analyses and cross-variable studies due to multi-parameter time series.
- Recent example publications demonstrate dataset usage:
  - Pilotto et al. (2020) – meta-analysis in Nature Communications.
  - Wang et al. (2016) – ecological and geochemical cycle studies.
  - Woolway et al. (2016) – lake surface temperatures (state of the climate context).
  - Overview reference: Maberly et al. (2017) on long-term ecological informatics in the English Lake District.
- Funding: NERC award NE/R016429/1 as part of the UK-SCaPE programme delivering National Capability.

## Provisions for data stewardship and future updates
- Documentation provides essential metadata, sampling regime, units, detection limits, and data structure to support discoverability and reuse.
- To maintain governance quality, consider:
  - Completing quality control/calibration to readiness for broader sharing.
  - Updating dataset with post-2018 data, if available, to extend the time series.
  - Maintaining clear provenance, versioning, and changelog for any future updates.
  - Ensuring ongoing metadata alignment with user needs (e.g., data user guides, variable definitions, and planetary units).