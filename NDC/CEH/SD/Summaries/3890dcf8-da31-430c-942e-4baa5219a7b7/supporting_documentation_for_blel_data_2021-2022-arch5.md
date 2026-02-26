# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Blelham Tarn 2021 to 2022

## Scope and purpose
- Long-term monitoring dataset from Blelham Tarn, Cumbria, England, comprising fortnightly measurements from Jan 2021 to end of 2022.
- Variables include surface temperature, surface oxygen saturation, Secchi depth, water chemistry, and phytoplankton chlorophyll a.

## Sampling regime and collection methods
- Water samples collected from 0 to 5 m depth; measurements taken from a boat at the deepest part of the lake (buoy).
- When buoy sampling was not possible, samples collected from the shore.
- Sampling frequency: fortnightly.
- Data available for download include:
  - TEMP: surface temperature (°C)
  - OXYG: surface oxygen saturation (% air-saturation)
  - SECC: Secchi depth (m)
  - ALKA: alkalinity (µg CaCO3 L⁻¹)
  - pH
  - NH4N: ammonium (µg N L⁻¹)
  - NO3N: nitrate (µg N L⁻¹)
  - PO4P: soluble reactive phosphate (µg P L⁻¹)
  - TOTP: total phosphorus (µg P L⁻¹)
  - SIO2: dissolved reactive silicon (µg SiO₂ L⁻¹)
  - TOCA: phytoplankton chlorophyll a (µg L⁻¹)

## Data quality and QC status
- Raw data are presented and have not yet undergone full quality control or calibration.
- Data have been double-entered and visually checked.
- Missing data attributed to weather conditions, COVID-19 restrictions, or staff shortages.

## Data structure and metadata
- Data provided as a comma-separated values (CSV) file with columns:
  - Date: measurement date
  - Variable, Description: name and description of each variable (as listed above)
  - Value, Description: measured values
  - Sign(if<LOD), Description: indicates if a value is below detection limit with a < sign
  - Flag, Description: 1 = sample taken at buoy location; 2 = sample taken from shore when buoy sampling was not possible

## Coverage and provenance
- Location: Blelham Tarn, Cumbria, England.
- Time coverage: January 2021 to end of 2022.
- Sampling integrated depth: 0–5 m; measurements based on a specific buoy site, with shore sampling as needed.
- Part of a long-term monitoring program under UK-SCaPE and ACCESS-UK frameworks.

## Access, sharing, and updates
- Data are available to download; provisions exist for updates and adherence to data-sharing limitations.
- Governance emphasizes appropriate data stewardship, including provenance and alignment with user needs.

## Limitations and cautions for users
- Data are raw and require quality control and calibration before certain analyses or public release.
- Some values may be below detection limits (indicated by signs in the dataset).
- Sampling gaps may occur due to weather, restrictions, or staffing, which should be considered in analyses.

## Funding and acknowledgements
- Data collection supported by Natural Environment Research Council (NERC) award NE/R016429/1 (UK-SCaPE National Capability).
- Data validation supported by NERC award NE/Y006208/1 (ACCESS-UK National Capability).