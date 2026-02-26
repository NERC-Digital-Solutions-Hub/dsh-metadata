# Eco-physiological data collected at Alice Holt Forest from July 2023

## Overview
- Dataset of photosynthesis and gas exchange collected at the Alice Holt Forest as part of a broader field campaign on forest structure and photosynthesis.
- Timeframe: 18–20 July 2023; measurements were taken only during daylight.

## Study site and sampling design
- Location: Alice Holt Forest.
- Experimental setup: A tower with six platforms (P), spaced at two-metre intervals. The tower sits between two oak trees (T) with overhanging branches (B).
- Sampling units: Leaves collected from leaf clusters (C) on branches, plus inclined sampling of the hazel understory (Haz).
- Instruments: Handy PEA+ and LI-COR 6400.

## Data files and naming conventions
- File format: All data provided as CSV (.csv).
- Photosynthetic parameters: Contained in a single CSV file.
- Gas exchange: Individual files named using the convention 2023_07_DD_XXX_PX_BX_CX.csv, where Oak/Haz indicates tree or understory, and P/ B/ C denote platform, branch, and leaf-cluster identifiers.
- Observations and sampling details are encoded in file headers and in the Licor measurement details.

## Measured parameters

### Photosynthetic parameters
- F0: Emission from PSII (unitless).
- Fm: Maximum fluorescence (unitless).
- Fv/Fm: Maximum quantum efficiency of PSII (unitless).
- P_Index: Performance index (indicator of sample vitality) (unitless).
- Tfm: Time at which maximum fluorescence was reached (ms).
- Intensity: Intensity (unit unclear in description; listed as μM in table).
- P, T, B, C: Categorical identifiers for Platform, Tree, Branch, Leaf cluster (unitless/[categorical]).

### Gas exchange parameters
- HHMMSS: Real-time clock (format HHMMSS; unitless).
- FTime: Time since logging started (s).
- Photo: Photosynthetic rate (μmol CO2 m^-2 s^-1).
- Cond: Conductance to H2O (mol H2O m^-2 s^-1).
- Ci: Intercellular CO2 concentration (μmol CO2 mol^-1).
- Trmmol: Transpiration rate (mmol H2O m^-2 s^-1).
- VpdL: Leaf temperature-based vapor pressure deficit (kPa).
- Area: In-chamber leaf area (cm^2).
- StmRat: Stomatal ratio estimate (dimensionless).
- BLCond: Total boundary layer conductance for the leaf (mol m^-2 s^-1).
- Tair: Air temperature in sample cell (°C).
- Tleaf: Leaf temperature (°C).
- TBlk: Cooler block temperature (°C).
- CO2R: Reference cell CO2 (μmol CO2 mol^-1).
- CO2S: Sample cell CO2 (μmol CO2 mol^-1).
- H20R: Reference cell H2O (mmol H2O mol^-1).
- H20S: Sample cell H2O (mmol H2O mol^-1).
- RH_R: Reference relative humidity (%).
- RH_S: Sample cell relative humidity (%).
- Flow: Flow rate to the sample cell (μmol s^-1).
- PARi: In-chamber photosynthetically active radiation (μmol m^-2 s^-1).
- PARo: External PAR (μmol m^-2 s^-1).
- Press: Atmospheric pressure (kPa).
- CsMch: Sample CO2 offset (μmol mol^-1).
- StableF: Stability status as a decimal value.
- Status: Status as string (e.g., '1101').

## Sampling protocol and Licor measurements
- Licor measurement sessions occurred on multiple days with records including:
  - A/Ci measurements (photosynthetic CO2 response curves) on 18–19 July.
  - LRC measurements (linked to leaf/branch conditions) on 20 July for selected observations (Oak and Haz observations across multiple platforms, branches, and leaf clusters).
- Detailed time stamps and observation codes accompany each measurement, indicating the exact platform, tree/understory, branch, and leaf-cluster being sampled.

## Quality control and limitations
- Not all branches or leaf-clusters were measured; wind caused some branches to be removed between labeling and measurement.
- Data quality relies on standardised collection methods, with clear naming conventions to support traceability and reproducibility.

## Relevance for environmental monitoring
- Provides standardized, day-time-only eco-physiological data (photosynthesis and gas exchange) aligned with monitoring aims to assess environmental health and forest function.
- Data are clearly structured for integration with other environmental datasets, enabling cross-linking and time-series analysis.
- Documentation includes explicit variable definitions, collection methods, and file naming conventions to facilitate verification, quality assurance, and data sharing through portals.