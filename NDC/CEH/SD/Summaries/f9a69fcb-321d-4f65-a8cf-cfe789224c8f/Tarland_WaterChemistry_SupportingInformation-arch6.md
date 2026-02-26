# Tarland catchment water quality and discharge data (Tarland Burn), 2000-2010

## Overview
- Part of a long-running Scottish Government-funded study focused on water quality, habitat, diffuse pollution, and flood mitigation in the Tarland Burn, the upper tributary of the River Dee (NE Scotland) under intensive land management.

## Data scope and variables
- Mean daily flow (m3/s) and water chemistry data collected from Tarland Burn (Coull site near catchment outlet), 2000-2010.
- Water chemistry determinands (units mg/L):
  - Total dissolved phosphorus (TDP)
  - Soluble reactive phosphorus (SRP)
  - Total phosphorus (TP)
  - Particulate phosphorus (PP)
  - Nitrate-nitrogen (NO3-N)
  - Ammonium-nitrogen (NH4-N)
  - Suspended solids (SS)
- Derived variables:
  - Dissolved organic N (DON) = TDN - (NO3-N + NH4-N)
  - Dissolved organic P (DOP) = TDP - MRP
  - Particulate N (PN) = TN - TDN
  - Particulate P (PP) derived from digest data

## Site location
- Sampling site: Coull, Tarland Burn, near the catchment outlet
- Coordinates: 57.111, -2.810 (WGS84)

## Sampling regime
- 2000-2003: weekly grab samples; some daily sampling during rainfall events
- Feb–Mar 2004: daily samples using autosampler (Isco 3700)
- Apr 2004–May 2005: daily samples with increased 4-hour sampling during storm events
- Post-Jun 2005: sampling became more infrequent and irregular

## Sample analysis and data processing
- Lab procedures:
  - 0.45 µm filter for SS; gravimetric determination
  - Colorimetric analysis for NO3-N, NH4-N, and MRP
  - Automated persulphate/UV digestion for TDN, TDP, DOC
  - Unfiltered sample digestion for NO-N and MRP (to obtain TN, NO-N, MRP)
- Derived calculations:
  - DON, DOP from digested vs. filtered results
  - PN and PP from differences between TN and TDN (and other digest values)
- Data handling:
  - Samples transported in cool conditions; analysis within specified QA windows
  - Discharge data calibrated against velocity-area profiles; stage height integrated across channel at 60% depth

## Discharge measurement details
- Stage height calibrated to discharge using velocity-area profiling
- Velocities measured with a propeller device (Valeport)
- Stage heights logged as 1-minute data; daily flow calculated with a 9:00–8:45 window to align with Met Office rainfall data

## Data quality and considerations
- Uses standard laboratory procedures and established calculation methods
- Temporal coverage includes both routine and storm-event focused sampling; irregular post-2005 sampling may affect continuity
- Derived variables enable assessment of dissolved vs. particulate phosphorus/N forms and potential organic components

## Potential data products for end users
- Self-serve time-series dashboards of daily flow, nutrient concentrations (TDP, SRP, TP, PP, NO3-N, NH4-N, SS)
- Temporal trend analyses and seasonal profiles for Tarland Burn
- Load calculations by integrating concentration with discharge
- Visualizations of DON, DOP, PN, PP trends and their relation to hydrological events
- Data quality notes and metadata to support cross-catchment comparisons