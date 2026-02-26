# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Windermere North Basin, UK, 2021 -2022. Feuchtmayr, H., Carter, H.T., Clarke, M.A., Dodd, B.A., James, J.B., Keenan, P.O., Kelsall, M., Mackay, E.B., McShane, G., Rankin, G., Rhodes, G., Thackeray, S.J., Maberly, S.C. (2025)

## Overview
- Part of an ongoing fortnightly monitoring dataset for Windermere North Basin, Cumbria, England.
- Variables collected: surface temperature (TEMP), surface oxygen saturation (OXYG), Secchi depth (SECC), alkalinity (ALKA), pH, ammonium (NH4N), nitrate (NO3N), soluble reactive phosphate (PO4P), total phosphorus (TOTP), dissolved reactive silicon (SIO2), phytoplankton chlorophyll a (TOCA).
- Timeframe: January 2021 – end of 2022.
- Sampling location and method: collected from a boat at a buoy in the deepest part of the lake; integrated water sample from 0–7 m.

## Data Collected and Regime
- Data units:
  - TEMP: degrees Celsius
  - OXYG: % air-saturation
  - SECC: metres
  - ALKA: µg CaCO3 per litre
  - pH: unitless
  - NH4N, NO3N, PO4P, TOTP, SIO2, TOCA: µg per litre (as indicated)
- Data format: CSV file with columns:
  - Date (measurement date)
  - Variable, Description (name and meaning of each variable)
  - Value, Description (measurement values)
  - Sign(if<LOD) (indicator for values below detection limit)
- Data are raw and not yet quality controlled; double-entered and visually checked.
- Missing data occurrences linked to weather, COVID-19 restrictions, or staff shortages.

## Data Structure and Format
- CSV structure with:
  - Date
  - Variable (and description)
  - Value (and description)
  - Sign(if<LOD) (indicator for below detection limit)

## Quality Control and Limitations
- Current status: raw data not quality controlled or calibrated.
- Quality practices in place: double data entry and visual checks.
- Limitations: incomplete data capture due to weather, health restrictions, and staff availability.
- Detection limits: values below detection limit flagged with a “<” sign.

## Data Provenance and Funding
- Data collection supported by Natural Environment Research Council (NERC) award NE/R016429/1 (UK-SCaPE National Capability).
- Data validation supported by NERC award NE/Y006208/1 (ACCESS-UK National Capability).

## Data Sharing and Governance Considerations
- Data are available to download as a dataset.
- Emphasizes standard metadata and transparent provenance to support discoverability and reuse.
- As raw data, plan for QC, calibration, metadata enrichment, and documentation of processing steps before broader sharing or reuse.

## Key Takeaways for Data Stewards
- Treat this as a raw, archival dataset requiring formal QC/validation before deployment in analyses or decision-making.
- Maintain and expand metadata: sampling protocol, exact buoy location, instrumentation details, and any data processing steps.
- Ensure consistent units and variable naming across updates; document any transformations.
- Plan for routine updates and a clear data release schedule, including versioning and changelog.
- Confirm data access rights, licensing, and embargoStatus if applicable, to support appropriate reuse.