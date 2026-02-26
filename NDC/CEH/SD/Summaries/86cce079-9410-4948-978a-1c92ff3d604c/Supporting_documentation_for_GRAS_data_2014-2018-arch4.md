# Supporting Document
Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Grasmere 2014 to 2018. Feuchtmayr, H., Clarke, M.A., De Ville, M.M., Dodd, B.A., Fletcher, J.M., Guyatt, H., James, J.B., Mackay, E.B., Pereira, M.G., Rhodes, G., Thackeray, S.J., Maberly, S.C. (2021)

## Overview
- Long-term monitoring dataset from Grasmere (Cumbria, England) with fortnightly sampling from 2014 to 2018.
- Variables collected: surface temperature (TEMP), surface oxygen saturation (OXYG), Secchi depth (SECC), alkalinity (ALKA), pH, ammonium (NH4N), nitrate (NO3N), soluble reactive phosphate (PO4P), total phosphorus (TOTP), dissolved reactive silicon (SIO2), and phytoplankton chlorophyll a (TOCA).
- Measurements typically taken from a boat at the deepest part of the lake (buoy); when inaccessible, samples taken from the shore.

## Data Collected and Measurements
- TEMP: degrees Celsius
- OXYG: % air-saturation
- SECC: metres
- ALKA: µg CaCO3 per litre
- pH: standard pH units
- NH4N: µg N per litre
- NO3N: µg N per litre
- PO4P: µg P per litre
- TOTP: µg P per litre
- SIO2: µg per litre
- TOCA: µg per litre

## Sampling Regime and Data Collection Methods
- Integrated water samples from 0 to 5 m depth.
- Location: buoy at the deepest part of the lake; if buoy visit not possible, shore samples collected.
- Temporal coverage: January 2014 to end of March 2018.
- Monitoring ended in March 2018 due to funding shortages.

## Data Quality and Limitations
- Data are raw and have not yet been quality controlled or calibrated.
- Double entered and visually checked; some missing data due to weather or staff shortages.
- Some measurements are below detection limits, indicated by a < sign in the Sign (if<LOD) field.

## Data Structure and Access
- Format: comma-separated values (CSV).
- Columns include:
  - Date: measurement date
  - Variable, Description: the measured parameter (e.g., TEMP, OXYG) and its description
  - Value, Description: measured value
  - Sign (if<LOD), Description: indicates below detection limit
  - Flag, Description: 1 = sample taken at buoy; 2 = shore sample when buoy visit was not possible
- Data dictionary embedded in the dataset for interpretation.

## Provenance, Context, and Usage
- Part of a long-term ecological monitoring effort; data have been used in published work (e.g., studies on carbon-silicon cycles in aquatic systems and Lake District ecological knowledge).
- Example publications listed for context:
  - Wang et al. (2016) Scientific Reports
  - Woolway et al. (2016) Bulletin of the American Meteorological Society
  - Maberly et al. (2017) Ecological Informatics overview

## Implications for Data Leaders
- Data governance: raw data shared with minimal processing; need for documented quality control and calibration procedures for downstream use.
- Metadata and discoverability: clear data dictionary and sampling protocol support data discovery and reuse; flags and LOD indications enhance interpretability.
- Data quality and standards: presence of detection limits and method notes highlights importance of standardizing QC, calibration, and metadata across datasets.
- Data accessibility and sustainment: monitoring ended due to funding; underscores need for long-term data stewardship, sustainability planning, and potential data archival strategies.
- Strategic actions: implement formal QC workflows, maintain comprehensive metadata (sampling location, depth, method), and ensure regular updates or clear end-of-life statements; promote cross-project data standardization to reduce fragmentation and facilitate cross-network data integration.