# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Esthwaite Water 2014 to 2018.

## Overview
- Long-term, fortnightly monitoring dataset from Esthwaite Water, Cumbria, England (2014–2018).
- Variables collected: surface temperature (TEMP), surface oxygen saturation (OXYG), Secchi depth (SECC), alkalinity (ALKA), pH, ammonium (NH4N), nitrate (NO3N), soluble reactive phosphate (PO4P), total phosphorus (TOTP), dissolved reactive silicon (SIO2), and phytoplankton chlorophyll a (TOCA).
- Integrated water sample from 0–5 m when possible; otherwise shore-based samples alongside surface measurements.
- Data intended for download as a CSV with detailed field descriptions and flags.

## Sampling regime and collection methods
- Measurements taken fortnightly as part of ongoing monitoring.
- Primary sampling point is a buoy at the deepest part of Esthwaite Water; if inaccessible, samples collected near the shore.
- Water chemistry values reflect the 0–5 m integrated sample; not always possible to integrate.

## Quality control and data quality
- Data are raw and have not yet been quality controlled or calibrated.
- Data have been double-entered and visually checked.
- Missing data arise from weather conditions or staff shortages.

## Data structure and fields
- CSV structure includes:
  - Date: measurement date.
  - Variable: the parameter (TEMP, OXYG, SECC, ALKA, pH, NH4N, NO3N, PO4P, TOTP, SIO2, TOCA).
  - Value: measured value (with units as specified).
  - Sign (if<LOD): indicates values below detection limit with a < sign.
  - Flag: 1 = sample collected at buoy location; 2 = sample collected near shore when buoy sampling not possible.

## Availability, access, and documentation
- Data provided as downloadable CSV with explicit variable descriptions, units, and detection-limit indicators.
- Clear documentation of sampling context, measurement method, and data limitations to guide use.

## Funding and provenance
- Collected with support from Natural Environment Research Council (award NE/R016429/1) as part of the UK-SCaPE programme delivering National Capability.

## Related publications and use
- Recent uses include studies on multidecadal biodiversity trends, carbon and silicon cycles in aquatic systems, and state-of-the-climate summaries.
- Example references illustrating dataset applicability to ecological and biogeochemical research.

## Implications for data leadership and governance
- Emphasizes the need for formal QA/QC and calibration pipelines to convert raw data into production-ready datasets.
- Highlights importance of comprehensive metadata (sampling regime, units, detection limits, flags) to ensure discoverability and reusability.
- Underlines data governance needs: clear data structure, versioning, and documentation to support collaboration and cross-system analyses.
- Suggests establishing processes for data validation, standardization across datasets, and stakeholder engagement to maintain data usability over time.