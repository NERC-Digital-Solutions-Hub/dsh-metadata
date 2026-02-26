# This dataset is the first assessment of river ecological risk due to flow alteration

## Overview
- Pan-European assessment of river ecological risk from flow alteration.
- Detailed river network: 33,368 cells at 5' x 5' resolution.
- Considers ecologically relevant hydrological indicators covering all facets of the flow regime.
- Accounts for both climate change and combined climate–socio-economic pressures.

## Geographic coverage and network
- 33,368 WaterGAP grid cells used as outlets of major European basins and nested sub-basins.
- Spatial resolution ~6 x 9 km2 in central Europe.
- Smallest represented basin: 63 km2.

## Data sources and climate data
- Historical climate: observed 1961–1990 from Climate Research Unit (CRU, UK).
- Future climate: 2040–2069 ('2050s') from two GCMs (IPSL-CM4 and MIROC3.2) under IPCC SRES A2.
- GCMs chosen to reflect inter-model variability; scenarios selected by a pan-European expert panel (PEP) using the SAS approach.

## Socio-economic scenarios
- Four pan-European freshwater visions (narratives turned into quantitative scenarios):
  - Economy First (EcF)
  - Fortress Europe (FoE)
  - Policy Rules (PoR)
  - Sustainability Eventually (SuE)

## WaterGAP model
- Global, semi-distributed hydrological and water-use model.
- Simulates terrestrial water cycle and withdrawals/consumption across five sectors (domestic, electricity, manufacturing, irrigation, livestock).
- Version 3.1 used on a 5' x 5' grid; includes 590 European dams with management rules.
- Outputs daily balances; routing to river discharge; calibration/validation at 221 GRDC gauging stations.

## Model runs and baseline
- 11 modelled monthly flow series total.
- Baseline: naturalised flows (1961–1990) with hydrology only (no water use).
- Future runs (2040–2069) include 10 scenarios:
  - For each GCM (IPCM4, MIMR): Natural plus EcF, FoE, PoR, SuE (5 runs each).

## ERFA screening method
- Based on Range of Variability Approach (RVA) using Indicators of Hydrological Alteration (IHA).
- Compares future flows against baseline across multiple indicators to assess ecological risk from flow alteration.
- Aggregates indicator departures into a simple colour-coded risk classification for each cell.

## Monthly Flow Regime Indicators (MFRI)
- Derived from 16 indicators (7 medians, 7 IQRs, 2 modes) across nine MFRI variables.
- Examples include:
  - Number of months above/below high/low thresholds
  - Month of maximum/minimum flow
  - Seasonal mean flows (January, April, July, October)
  - Frequency, magnitude, timing, and duration characteristics
- Thresholds used to identify departures from baseline (e.g., median/IQR differences >30%; mode differences >1 month).

## ERFA classification and data encoding
- Risk classes based on number of departing indicators:
  - 0 departures → blue (no risk)
  - 1–5 departures → green (low risk)
  - 6–10 departures → amber (medium risk)
  - 11–16 departures → red (high risk)
- Coding in dataset:
  - X, Y: cell centre coordinates (WGS84)
  - ERFA_IPCM4_Natural, ERFA_MIMR_Natural: risk codes for IPCM4/MIMR under Natural scenario
  - ERFA_IPCM4_EcF, ERFA_MIMR_EcF: IPCM4/MIMR under EcF
  - ERFA_IPCM4_FoE, ERFA_MIMR_FoE: IPCM4/MIMR under FoE
  - ERFA_IPCM4_PoR, ERFA_MIMR_PoR: IPCM4/MIMR under PoR
  - ERFA_IPCM4_SuE, ERFA_MIMR_SuE: IPCM4/MIMR under SuE

## Validation and method testing
- WaterGAP calibration/validation against measured annual discharge at 221 GRDC stations across Europe.
- MFRI/ERFA results compared with RVA/IHA (daily-data method) for a subset of ~683 cells along major rivers.
- In most cases, results were consistent across time steps; MFRI/ERFA deemed suitable for the study scope.