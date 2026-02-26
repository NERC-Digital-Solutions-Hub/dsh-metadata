# Eco-physiological data collected at Alice Holt Forest from July 2023

## Overview
- Dataset on photosynthesis and gas exchange collected within the Alice Holt Forest as part of a wider field campaign examining photosynthesis and forest structure.
- Sampling occurred July 18–20, 2023; measurements were taken from each leaf only during the day.

## Data and format
- All files provided as CSV (.csv).
- Two main data components:
  - Photosynthetic parameters (one CSV file).
  - Gas exchange files named using the convention: 2023_07_DD_XXX_PX_BX_CX.csv, with codes indicating Oak or Haz (understory), and platform (P), branch (B), and leaf cluster (C).

## Collection methods
- Data collected from a tower with six platforms (P) at 2 m intervals.
- Tower positioned between two oak trees (T) with several overhanging branches (B); each branch subdivided into leaf clusters (C). Hazel understory sampled similarly.
- Instruments used: Handy PEA+ and LI-COR 6400.

## Naming conventions
- Photosynthetic parameters: single CSV file.
- Gas exchange: files follow the 2023_07_DD_XXX_PX_BX_CX.csv format, with Oak or Haz indicators and platform/branch/leaf-cluster identifiers.

## Quality control
- Not all branches or leaf-clusters were measured; some branches were taken down by wind between labeling and measurement.

## Photosynthetic parameters (variables)
- F0: Emission from PSII (unitless).
- Fm: Maximum fluorescence (unitless).
- Fv_Fm: Maximum quantum efficiency of PSII (unitless).
- P_Index: Performance index (indicator of sample vitality) (unitless).
- Tfm: Time to maximum fluorescence (ms).
- Intensity: In-chamber light intensity (μM).
- P, T, B, C: Tower platform, Tree, Branch, Leaf cluster identifiers.

## Gas exchange parameters (variables)
- HHMMSS: Real-time clock.
- FTime: Time since logging started (s).
- Photo: Photosynthetic rate (μmol CO2 m^-2 s^-1).
- Cond: Conductance to H2O (mol H2O m^-2 s^-1).
- Ci: Intercellular CO2 concentration (μmol CO2 mol^-1).
- Trmmol: Transpiration rate (mmol H2O m^-2 s^-1).
- VpdL: Leaf temperature-based vapor pressure deficit (kPa).
- Area: In-chamber leaf area (cm^-2).
- StmRat: Stomatal ratio estimate.
- BLCond: Total boundary layer conductance (mol m^-2 s^-1).
- Tair: Temperature in the sample cell (°C).
- Tleaf: Temperature of leaf thermocouple (°C).
- TBlk: Temperature of cooler block (°C).
- CO2R: Reference cell CO2 (μmol CO2 mol^-1).
- CO2S: Sample cell CO2 (μmol CO2 mol^-1).
- H20R: Reference cell H2O (mmol H2O mol^-1).
- H20S: Sample cell H2O (mmol H2O mol^-1).
- RH_R: Reference relative humidity (%).
- RH_S: Sample cell relative humidity (%).
- Flow: Flow rate to the sample cell (μmol s^-1).
- PARi: In-chamber PAR (μmol m^-2 s^-1).
- PARo: External PAR (μmol m^-2 s^-1).
- Press: Atmospheric pressure (kPa).
- CsMch: Sample CO2 offset (μmol mol^-1).
- StableF: Stability status (decimal value).
- Status: Status as string (e.g., '1101').

## Details of Licor measurements
- Measurements captured under various conditions and types (e.g., A/Ci for photosynthetic vs. leaf/branch conditions; LRC for certain measurement runs).
- Time stamps and codes indicate specific leaf samples and locations (e.g., Oak_P2_B1_C1, Oak_P5_B1_C1, Haz1).
- Measurement periods documented: Tue 18 Jul 2023 (multiple A/Ci measurements), Wed 19 Jul 2023 (Oak_P2_B1_C1, Oak_P2_B3_C1, Oak_P2_B1_C2, Oak_P5_B1_C1, Oak_P5_B1_C2, Oak_P5_B1_C3), Thu 20 Jul 2023 (LRC measurements for various oak and hazel samples).

## Access and potential uses
- Dataset enables analysis of leaf-level photosynthesis and gas exchange across different tree types (Oak vs. Hazen understory) and locations on the tower.
- Suitable for creating self-serve data products (e.g., dashboards) to explore relationships between photosynthetic parameters and gas exchange metrics.
- Useful for cross-dataset integration aimed at understanding canopy structure, leaf physiology, and environmental responses in the Alice Holt site.
- Note: Some data gaps due to wind-related branch loss should be considered during analysis.