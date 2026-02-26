# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Blelham Tarn 2014 to 2018. Feuchtmayr, H., Clarke, M.A., De Ville, M.M., Dodd, B.A., Fletcher, J.M., Guyatt, H., Hunt, A.G., James, J.B., Mackay, E.B., Rhodes, G., Thackeray, S.J., Maberly, S.C. (2021)

## Overview
- Long-term, ongoing monitoring dataset from Blelham Tarn, Cumbria, England.
- Fortnightly sampling from January 2014 to end of 2018.
- Measured variables: surface temperature, surface oxygen saturation, Secchi depth, alkalinity, pH, ammonium, nitrate, soluble reactive phosphate, total phosphorus, dissolved reactive silicon, and phytoplankton chlorophyll a.

## Sampling regime and collection methods
- Water samples integrated from 0 to 5 m; measurements taken from a boat at the deepest part of the lake (buoy).
- If the buoy could not be visited, samples were taken from shore along with surface temperature and oxygen measurements.
- Location-specific sampling at the marked buoy, with occasional shore sampling when access was restricted.

## Variables and units
- Temperature (TEMP): degrees Celsius.
- Surface oxygen saturation (OXYG): percent air-saturation.
- Secchi depth (SECC): metres.
- Alkalinity (ALKA): micrograms CaCO3 per litre.
- pH: (no units specified in document).
- Ammonium (NH4N): micrograms N per litre.
- Nitrate (NO3N): micrograms N per litre.
- Soluble reactive phosphate (PO4P): micrograms P per litre.
- Total phosphorus (TOTP): micrograms P per litre.
- Dissolved reactive silicon (SIO2): micrograms per litre.
- Phytoplankton chlorophyll a (TOCA): micrograms per litre.

## Data quality and quality control
- Data are raw and have not yet been quality controlled or calibrated.
- Data have been double-entered and visually checked.
- Missing data attributed to weather conditions or staff shortages.

## Data structure and file format
- Data provided as a comma-separated values (CSV) file.
- Columns include:
  - Date: date of measurement.
  - Description = Variable description.
  - Variable: variable name (e.g., TEMP, OXYG, SECC, etc.).
  - Description = Units for each variable.
  - Value: measured value for each variable.
  - Sign (if<LOD): indicator if value is below detection limit (a < sign).
  - Flag: sampling context (Flag = 1 = buoy location; Flag = 2 = shore sampling when buoy unavailable).

## Data governance, provenance, and funding
- Funding: Natural Environment Research Council award NE/R016429/1 as part of the UK-SCaPE programme delivering National Capability.
- Dataset referenced in multiple publications, illustrating reuse and impact (examples listed in document).

## Access, reuse, and metadata
- Data are available to download; currently raw data with noted QC status.
- Provides context on sampling regime, methods, and data structure to support reuse.

## Recommendations for data stewards
- Implement a formal quality control and calibration workflow; document QC steps and outcomes.
- Capture and publish metadata on detection limits, data transformations, and any data corrections.
- Maintain clear data provenance and versioning; update dataset status as QC is completed.
- Ensure interoperability by aligning variable names, units, and formats with related datasets; provide guidance on handling <LOD values.
- Facilitate timely data updates and establish a clear data sharing plan through appropriate portals or catalogues.