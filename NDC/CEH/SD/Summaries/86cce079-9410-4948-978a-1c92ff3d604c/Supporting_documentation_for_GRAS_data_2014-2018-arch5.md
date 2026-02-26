# Supporting Document
Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Grasmere 2014 to 2018. Feuchtmayr, H., Clarke, M.A., De Ville, M.M., Dodd, B.A., Fletcher, J.M., Guyatt, H., James, J.B., Mackay, E.B., Pereira, M.G., Rhodes, G., Thackeray, S.J., Maberly, S.C. (2021)

## Overview
- Long-term monitoring dataset from Grasmere, Cumbria, England, with fortnightly sampling from January 2014 to March 2018.
- Measured variables and units:
  - Surface temperature (TEMP) in °C
  - Surface oxygen saturation (OXYG) in % air-saturation
  - Secchi depth (SECC) in metres
  - Alkalinity (ALKA) in µg CaCO3 per L
  - pH
  - Ammonium (NH4N) in µg N per L
  - Nitrate (NO3N) in µg N per L
  - Soluble reactive phosphate (PO4P) in µg P per L
  - Total phosphorus (TOTP) in µg P per L
  - Dissolved reactive silicon (SIO2) in µg per L
  - Phytoplankton chlorophyll a (TOCA) in µg per L
- Water samples generally from 0–5 m integrated depth; measurements taken from a boat at the deepest lake location (buoy). If the buoy was inaccessible, shore sampling was used (Flag 2).
- End of long-term monitoring due to funding constraints in March 2018.
- Data availability: dataset intended for download; part of ongoing long-term monitoring and accessible for reuse with proper attribution.

## Data Content and Structure
- Data file format: CSV with the following columns and descriptions:
  - Date: date of measurement
  - Variable, Description: name and meaning of each measured variable (TEMP, OXYG, SECC, ALKA, pH, NH4N, NO3N, PO4P, TOTP, SIO2, TOCA)
  - Value, Description: measured value for each variable
  - Sign (if<LOD), Description: indicates if values are below detection limit with a < sign
  - Flag, Description: 1 = sample taken at buoy location; 2 = sample taken from shore
- Example use cases in literature are provided to illustrate dataset applicability (e.g., studies on carbon-silicon cycles and Lake surface temperatures).

## Data Quality, Provenance, and Limitations
- Quality control status: raw data not yet quality controlled or calibrated; however, data have been double-entered and visually checked.
- Missing data: attributable to weather conditions or staff shortages.
- Data provenance: explicitly documents collection methods, sampling regimes, and measurement context to support data lineage and reproducibility.
- Notable notes:
  - Some samples not integrated (shore samples) are flagged accordingly (Flag 2).
  - End date of data collection is March 2018 due to funding shortfalls.

## Governance, Sharing, and Use Considerations for Data Stewards
- Data governance:
  - Clearly documented metadata within the dataset (variable definitions, units, data collection context, and flag meanings) supports discoverability and correct interpretation.
  - Transparency about QC status and data limitations aids appropriate reuse and prevents misapplication.
- Data availability and updates:
  - Although ongoing monitoring existed, current data end date is March 2018; consider governance processes if new funding enables continued data collection and subsequent integration.
  - The dataset is suitable for integration with other long-term monitoring data, provided standardization of units and column definitions is maintained.
- Data sharing and citation:
  - Include explicit references to example publications and overview papers to support proper citation and traceability of data usage.
  - When uploading to data portals or catalogues, preserve the described column semantics (Date, Variable/Description, Value/Description, Sign, Flag) to maintain interoperability.
- Metadata and standardization:
  - Maintain consistent units (e.g., °C, % air-saturation, mg/L equivalents) and clearly document any deviations or special cases (e.g., shore samples, LOD indicators).
  - Ensure future datasets align with the same structure or provide mapping guidelines to facilitate cross-dataset interoperability.

## Publications and References (Context for Reuse)
- Example publications where this dataset has been used:
  - Wang, B., Liu, C.-Q., Maberly, S.C., Wang, F. & Hartmann, J. (2016). Coupling of carbon and silicon geochemical cycles in rivers and lakes. Scientific Reports 6, 35832.
  - Woolway, R.I., et al. (2016). Lake surface temperatures. Bulletin of the American Meteorological Society 97(8), S17-S18.
- Overview reference:
  - Maberly, S.C., et al. (2017). From Ecological Informatics to the Generation of Ecological Knowledge: Long-Term Research in the English Lake District. In Ecological Informatics, 455-482.