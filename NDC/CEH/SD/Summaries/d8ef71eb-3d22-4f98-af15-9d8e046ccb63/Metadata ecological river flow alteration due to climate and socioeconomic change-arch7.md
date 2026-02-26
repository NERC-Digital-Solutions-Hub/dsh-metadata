This dataset is the first assessment of river ecological risk due to flow alteration: (i) to provide pan-European geographical coverage, (ii) to use a detailed (given the geographical extent) river network based on 33,368 cells with a 5' x 5' resolution, (iii) to consider explicitly a set of ecologically-relevant hydrological indicators (i.e. all facets of the flow regime), and (iv) to consider not just climate-induced change, but combined climate and socio-economic pressures.

## Overview
- Pan-European assessment of ecological risk from flow alteration using a fine-scale river network.
- Focus on ecologically relevant hydrological indicators across the full flow regime.
- Integrates climate change with socio-economic pressures.

## Spatial framework and data inputs
- 33,368 WaterGAP grid cells forming a pan-European river network; each cell represents an outlet of a basin or sub-basin (smallest basin ~63 km²).
- Spatial resolution: 5' x 5' grid (~6 x 9 km² in central Europe).
- Outputs include latitude/longitude coordinates for each cell.

## Climate data and socio-economic scenarios
- Observed climate: 1961–1990 from CRU (University of East Anglia).
- Future climate: 2040–2069 (2050s) from two GCMs:
  - IPSL-CM4 (IPCM4) under SRES A2 (warm and dry expected)
  - MIROC3.2 (MIMR) under SRES A2 (warm and wet expected)
- Four socio-economic narratives converted to quantitative scenarios via the SAS approach:
  - Economy First (EcF)
  - Fortress Europe (FoE)
  - Policy Rules (PoR)
  - Sustainability Eventually (SuE)

## Hydrological model and data generation
- WaterGAP (v3.1): semi-distributed global hydrological and water use model.
  - Simulates daily water balances per grid cell and routes runoff along modeled river networks.
  - Includes 590 European dams with management rules.
  - Calibrated/validated against GRDC measurements at 221 gauging stations.
- Baseline and future runs:
  - 11 monthly flow series total.
  - Baseline: naturalised flows for 1961–1990 (no water use) using CRU data.
  - Future: 10 runs (5 per GCM) including one naturaliser plus four socio-economic scenarios.
  - Period 2040–2069 (2050s) for all projections.

## ERFA methodology (ecological risk screening)
- Based on Range of Variability Approach (RVA) and Indicators of Hydrological Alteration (IHA).
- Uses a suite of monthly flow indicators to compare future flows against baseline naturalised flows.
- Aggregates results into a simple, map-friendly risk classification to avoid overload:
  - Blue: no risk
  - Green: low risk
  - Amber: medium risk
  - Red: high risk
- Classification is determined by how many indicators differ from baseline beyond defined thresholds.

## Monthly Flow Regime Indicators (MFRI)
- Derived from 16 indicators:
  - 7 medians and 7 IQRs describe magnitude and variability of hydrological variables.
  - 2 modes describe discrete timing for monthly flood and minimum flow timing (mode used due to discrete monthly values).
- Indicators cover:
  - Monthly flow magnitudes, timing of maximum flow, seasonal patterns, high/low flow frequencies, and sequences of low flows.

## Thresholds and ERFA classes
- Significance of departure from baseline:
  - Median/IQR indicators: >30% difference from baseline.
  - Mode indicators: >1 month difference.
- ERFA classification by site per scenario:
  - 0: blue/no risk
  - 1: green/low risk
  - 2: amber/medium risk
  - 3: red/high risk
- Output dataset includes 12 ERFA columns (one per combination of GCM and scenario) plus coordinates:
  - ERFA_IPCM4_Natural
  - ERFA_MIMR_Natural
  - ERFA_IPCM4_EcF
  - ERFA_MIMR_EcF
  - ERFA_IPCM4_FoE
  - ERFA_MIMR_FoE
  - ERFA_IPCM4_PoR
  - ERFA_MIMR_PoR
  - ERFA_IPCM4_SuE
  - ERFA_MIMR_SuE
  - X (Longitude)
  - Y (Latitude)

## Method testing and validation
- WaterGAP calibration/validation against GRDC data at 221 European gauging stations.
- MFRI/ERFA comparison with a daily-data RVA/IHA method for a subset of ~683 cells along major rivers; results largely concordant across time steps, supporting method suitability for this scale.

## GIS relevance and use
- Provides a harmonised, grid-based risk surface across Europe suitable for map-based visualisation and spatial analysis.
- Facilitates multi-scenario comparison and integration with other GIS layers (e.g., land use, dams, climate zones).
- Enables identification of hotspots where flow alteration poses ecologically meaningful risks under different climate and socio-economic futures.