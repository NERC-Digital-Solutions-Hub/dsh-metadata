# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Esthwaite Water, UK, 2023

## Overview
- Long-term, fortnightly monitoring dataset from Esthwaite Tarn, Cumbria, England (January–December 2023).
- Parameters collected: surface temperature (TEMP, °C), surface oxygen saturation (OXYG, % air-saturation), Secchi depth (SECC, m), alkalinity (ALKA, µg CaCO3 per L), pH, ammoniacal and oxidised nitrogen (NH4N, TON, µg N per L), soluble reactive phosphate (PO4P, µg P per L), total phosphorus (TOTP, µg P per L), dissolved reactive silicon (SIO2, µg per L), phytoplankton chlorophyll a (TOCA, µg per L).
- Sampling integrates 0–5 m water column; collected from the lake buoy at the deepest part or, when unavailable, from the shore.
- Data are raw (not fully quality controlled) but some variables have manual double-entry validation.

## Data scope and variables
- Temporal coverage: January 2023 to December 2023.
- Data granularity: fortnightly measurements; not all parameters are measured every sampling event.
- Variables and units:
  - TEMP: surface temperature, °C
  - OXYG: surface oxygen saturation, % air-saturation
  - SECC: Secchi depth, m
  - ALKA: alkalinity, µg CaCO3 per L
  - pH: pH
  - NH4N: total ammoniacal nitrogen, µg N per L
  - TON: total oxidised nitrogen, µg N per L
  - PO4P: soluble reactive phosphate, µg P per L
  - TOTP: total phosphorus, µg P per L
  - SIO2: dissolved reactive silicon, µg per L
  - TOCA: phytoplankton chlorophyll a, µg per L
- Data are provided in a CSV with: sdate, variable/description, value, sign(if<LOD), and flag (1 or 2).

## Sampling regime and collection details
- Fortnightly sampling regime as part of a long-term programme.
- Sample types:
  - Integrated water sample from 0–5 m for chemistry parameters.
  - Measurements taken in situ for TEMP and OXYG.
- Location:
  - Primary buoy (deep-water site) for lake-wide sampling.
  - Shore sampling when buoy access was not possible.
- Documentation notes:
  - Values below detection limits indicated with a < sign in the sign(if<LOD) column.
  - Flag 2 indicates shore-based sampling without buoy visit.

## Data structure and access
- File format: comma-separated values (CSV).
- Columns:
  - sdate: measurement date
  - Description: variable name
  - value: measurement value
  - sign(if<LOD): indicates values below detection limit
  - flag: 1 = buoy-based sample; 2 = shore-based sample
- Data are raw and require cleaning/quality control for GIS applications; some variables have been double-entered and validated, but not all have undergone full QC.

## Quality control and limitations
- Raw data are presented without full quality control or calibration yet.
- Some variables (TEMP, OXYG, SECC, ALKA, pH, PO4P, TOCA) have been double-entered and visually checked by a database manager.
- Missing data caused by weather, equipment limitations, or staff shortages.
- Calibration and validation details are provided for measurement methods and are UKAS-accredited for several analyses (NH4N, TON) where applicable.
- Users should perform additional QC/validation and consider detection limits when mapping or analyzing trends.

## Measurement methods (highlights)
- TEMP and OXYG: measured with YSI ProODO; oxygen % calibrated daily; DO% calibration checks biweekly and bimonthly.
- SECC: Secchi depth measured with a marked rope.
- Alkalinity and pH: integrated water sample; Gran titration with a combination electrode; calibration before each run.
- NH4N and TON: colorimetric analysis using SEAL AQ2; filtration through GF/C; standard digestion and calibration with UKAS-accredited protocols.
- TP: digestion with potassium persulphate, molybdenum blue colorimetric analysis; UV-Vis measurement; standards validated with reference materials.
- SIO2: colorimetric silica method with ammonium molybdate and ascorbic acid; measurement at 880 nm; QC checks with known concentrations.
- TOCA: filtration, methanol extraction, spectrophotometric analysis following established procedures.

## GIS relevance and usage notes
- Suitable for map-based visualization of lake water quality over 2023, and for integration with other spatial datasets (e.g., catchment data, hydrology, land use).
- Use caution due to raw data status; require cleaning, unit harmonization, and handling of detection-limit indicators.
- Data primarily describe a single lake site with buoy-based sampling; consider spatial representativeness when comparing to other lakes or broader scales.
- Join with temporal data (dates) for time-series maps and dashboards.

## Metadata, provenance, and references
- Funding: Natural Environment Research Council (NERC) award NE/R016429/1 (UK-SCaPE programme) and UKCEH support NE/Y006208/1 for data validation.
- References for methods:
  - Mackereth et al. (1978): Water Analysis methods
  - Mortimer (1981): Oxygen content in air-saturated water
  - Talling (1974): Methods for measuring primary production in aquatic ecosystems
- Documented in the Supporting Document for Esthwaite Water data (2025 publication), with 2023 dataset details.

## Access and citations
- Data described as downloadable CSV files containing the Fortnightly measurements for 2023.
- Users should cite the Esthwaite Water dataset and the associated 2025 publication when utilizing the data.