# Eco-physiological data collected at Alice Holt Forest from July 2023

## Overview
- Dataset of photosynthesis and gas exchange measurements collected at Alice Holt Forest as part of a broader field campaign on forest structure and physiology.
- Timeframe: 18–20 July 2023; measurements taken during daylight hours only.
- Data format: all files provided as CSV.

## Data content and structure
- Photosynthetic parameters: a single CSV file.
- Gas exchange data: multiple CSV files named using the convention 2023_07_DD_XXX_PX_BX_CX.csv, with codes indicating Oak (tree) or Haz (understory) and platform, branch, and leaf-cluster identifiers.
- Sampling design: collected from a tower with six platforms (P1–P6) between two oak trees (T) with overhanging branches (B) and leaf clusters (C); hazel understory sampled similarly.

## Collection methods and instruments
- Setting: tower between two oak trees with overhanging branches; six platforms at 2 m intervals.
- Sampling targets: leaves from oak tree and hazel understory across branches and leaf clusters.
- Instruments: Handy PEA+ and LI-COR 6400 for measurements.

## Variables and key parameters

- Photosynthetic parameters (examples with units):
  - F0 (emission from PSII), Fm (maximum fluorescence), Fv_Fm (maximum quantum efficiency of PSII), P_Index (sample vitality), Tfm (time to maximum fluorescence), Intensity, P (tower platform), T (tree), B (branch), C (leaf cluster).

- Gas exchange parameters (examples with units):
  - HHMMSS (real-time clock), FTime (time since logging started), Photo (photosynthetic rate, μmol CO2 m^-2 s^-1), Cond (conductance to H2O, mol H2O m^-2 s^-1), Ci (intercellular CO2, μmol CO2 mol^-1), Trmmol (transpiration rate, mmol H2O m^-2 s^-1), VpdL (leaf-area-based vapor pressure deficit, kPa), Area (in-chamber leaf area, cm^2), StmRat (stomatal ratio), BLCond (boundary layer conductance, mol m^-2 s^-1), Tair (air temperature in sample cell, °C), Tleaf (leaf temperature, °C), TBlk (cooler block temperature, °C), CO2R/CO2S (reference/sample CO2, μmol CO2 mol^-1), H20R/H20S (reference/sample water content, mmol H2O mol^-1), RH_R/RH_S (relative humidity), Flow (flow rate to sample cell), PARi/PARo (in-chamber/external light, μmol m^-2 s^-1), Press (atmospheric pressure, kPa), CsMch (sample CO2 offset), StableF (stability status), Status (status string).

- Note: not all variables are present in every file; the dataset includes detailed field names and units as documented.

## Data quality and limitations
- Quality control: measurements were not taken for all branches or leaf clusters; some branches were removed by wind between labeling and measurement.
- Daylight-only data collection means no observations outside daylight hours.

## File naming conventions and metadata
- Photosynthetic data: a single CSV file.
- Gas exchange data: multiple CSV files named with 2023_07_DD_XXX_PX_BX_CX.csv; identifiers indicate tree type (Oak/Haz), platform, branch, and leaf cluster.
- Measurement logs include details such as observation codes (e.g., Oak_P2_B1_C1) and measurement type (A/Ci or LRC) with start times, documenting the measurement schedule across days.