# UK estuary greenhouse gas and nutrients data set

## Overview
- A multi-estuary, multi-campaign dataset detailing greenhouse gas concentrations and water chemistry across salinity gradients in seven UK estuaries (Clyde, Clywyd/Clwyd, Conwy, Forth, Tay, Dart, Tamar) collected during four campaigns (July 2017, October 2017, January 2018, April 2018).
- Aims to enable analysis of estuarine processing of greenhouse gases and nutrients, with data intended for self-service use and further product development.

## Scope and Sampling Design
- Estuaries: Clyde, Clywd/Clwyd, Conwy, Forth, Tay (central Scotland and northern Wales); Dart, Tamar (southwest England).
- Four sampling campaigns spanning mid-2017 to early 2018.
- Sampling sites chosen to span the salinity gradient; target salinities: 1, 2, 5, 10, 15, >25 ppt (not always achieved).
- Sampling points varied by salinity and were conducted from rigid inflatable boats or fixed points (bridges).
- Depth of in situ measurements: ~10 cm below surface; surface water samples collected at target salinities for various analyses.
- Two methods for greenhouse gases: headspace equilibration (Clyde, Clywyd/Clwyd, Conwy, Forth, Tay) and bottle equilibration (Tamar, Dart).

## Field and Laboratory Methods

- In situ measurements:
  - Physico-chemical parameters: temperature and salinity measured with a sensor ~10 cm below surface.
  - Salinity and temperature used to compute gas solubility adjustments (Henry’s Law, Bunsen solubility adjustments for temperature/salinity).

- Greenhouse gas sampling and analysis:
  - Clyde, Clywyd/Clwyd, Conwy, Forth, Tay: headspace method with exact volumes, duplicate sampling, and GC analysis (CH4 and CO2 by FID; N2O by μECD); includes ambient air samples; detection limits: CH4 40 ppb, CO2 5000 ppb, N2O 5 ppb.
  - Tamar and Dart: 500 mL bottles, single-phase equilibration GC with FID (CH4) and EC (N2O); calibrations against three certified standards traceable to NOAA; CH4 and N2O solubility adjusted to ~25°C.

- Water chemistry analyses:
  - Dissolved organic carbon (DOC) and total dissolved carbon (TDC) measured at UKCEH Lancaster using TOC-L; freshwater TDC includes inorganic carbon.
  - Freshwater nutrients (Position 1): nitrate + nitrite, ammonium, total nitrogen (TN), total phosphorus (TP), soluble reactive phosphorus (PO4-P) measured with specified instruments and methods (ion chromatography, colorimetric analyses, moisture-specific calibration/LoD rules). LOQs and calibration ranges provided; QC samples used regularly.
  - Saline nutrients (Positions 2–6): analyzed at Plymouth Marine Laboratory using SEAL Analytical AAIII autoanalyser; established methods for nitrate, nitrite, ammonium, phosphate, silicate; GO-SHIP protocols; LoD values specified; ranges cover detected concentrations.

- Units and data recording:
  - Data are reported to two decimal places.
  - Units and column definitions are detailed in Table 1 (e.g., NO3-N, NH4-N, PO4-P, PO4-P, TDC, TN, TP, CH4, CO2, N2O, and gas saturations).
  - Missing values are marked with an asterisk; freshwater and saline data may have many missing values in different columns due to laboratory separation.

## Data Structure and Content

- Columns and metadata:
  - Estuary name; Position (1 = furthest upstream, 6 = furthest downstream); Lat/Long; Day/Month/Year.
  - Salinity and Temperature (surface water).
  - Gas concentrations: CH4, CO2, N2O; N2O sat, CH4 sat, CO2 sat (saturation percentages where reported).
  - Nutrients and carbon measures: NO3-N, NO2-N, NH4-N, PO4-P, PO4-P, Silicate, TN, TP, DOC, TDC, N2O, CH4, CO2, with specified units (μM/L, mg/L, etc).
- Data handling notes:
  - Saline and freshwater samples analyzed at different laboratories, leading to systematic missing values across certain columns; columns referencing the other matrix may contain relevant data (as noted in dataset documentation).
  - Data are structured to support cross-parameter comparisons along the salinity gradient and across estuaries.

## Data Quality, Limitations, and Notes

- QA and calibration:
  - GHG analyses calibrated with standard reference materials; detection limits defined for each gas and methodology.
  - Nutrient analyses followed established methods (GO-SHIP protocols where applicable) with QC samples, certified references, and method-specific calibration ranges.
- Potential data limitations:
  - Not all sampling points achieved the full intended salinity gradient; some target salinities were missed.
  - Cross-lab data integration required due to separate freshwater and saline laboratories; notable missing data in certain parameter columns.
  - Data may contain missing values (*) and require careful handling for complete multi-parameter analyses.

## Data Products and Usability

- Designed for end-user self-service exploration (e.g., dashboards, pivot tables, and other data products) to enable analysis of estuarine GHG and nutrient dynamics.
- Dataset supports comparative analyses across estuaries, campaigns, and salinity gradients.
- Table 1 provides column-by-column definitions and units to aid interpretation and integration with user analyses.

## References

- Becker et al. GOSHIP Repeat Hydrography Nutrient Manual (2020)
- BreweR & Riley (1965)
- García-Martín et al. 2021 (estuarine dissolved organic matter and related processing)
- Grasshoff (1976)
- Kirkwood (1989)
- Mantoura & Woodward (1983)
- Upstill-Goddard et al. (1996)
- Weiss & Price (1980)
- Wiesenburg & Guinasso (1979)