# This dataset is the first assessment of river ecological risk due to flow alteration: (i) to provide pan-European geographical coverage, (ii) to use a detailed (given the geographical extent) river network based on  33,368  cells with a 5' x 5' resolution, (iii) to consider explicitly a set of ecologically-relevant hydrological indicators (i.e. all facets of the flow regime), and (iv) to consider not just climate-induced change, but combined climate and socio-economic pressures.

## Overview
- First pan-European assessment of river ecological risk from flow alteration.
- Uses a detailed river network: 33,368 cells at 5' x 5' resolution (about 6 x 9 km2 per cell).
- Considers ecologically relevant hydrological indicators across the full flow regime.
- Integrates climate change with socio-economic pressures (not climate change alone).
- Produces monthly flow time series (baseline and future) fed into an ecological risk screening method (ERFA).

## Data inputs and geographical scope
- Climate data:
  - Observed historical: 1961-1990 from Climate Research Unit (CRU, UK).
  - Future projections (2040-2069, '2050s') from two GCMs: IPSL-CM4 (IPCM4) and MIROC3.2 (MIMR).
  - Emission scenario: IPCC SRES A2 (high population growth, heterogeneous world).
- Socio-economic scenarios (pan-European panel, PEP):
  - Economy First (EcF), Fortress Europe (FoE), Policy Rules (PoR), Sustainability Eventually (SuE).
  - Scenarios translate qualitative narratives into quantitative inputs via SAS (Story-And-Simulation) approach.
- Hydrological model:
  - WaterGAP v3.1 (Water - Global Assessment and Prognosis) on a 5' x 5' grid.
  - Global hydrological component + global water use component (domestic, electricity, manufacturing, irrigation, livestock).
  - Incorporates 590 European dams (ELDRED2) with management rules.
  - Calibration/validation against GRDC data at 221 gauging stations.

## Modelling framework and data pipeline
- Baseline (naturalised) runs: WaterGAP with hydrology only, using CRU climate; no water withdrawals.
- Future runs: 10 scenarios (5 per GCM) plus Natural baseline, covering EcF, FoE, PoR, SuE.
- Time horizon: 2040-2069 (the 2050s).
- Output: sets of monthly flow time series for each grid cell to feed ERFA.

## ERFA screening method (ecological risk due to flow alteration)
- Conceptual basis: Range of Variability Approach (RVA) using Indicators of Hydrological Alteration (IHA) to define ecologically meaningful limits.
- Core idea: departures from baseline flow conditions (beyond thresholds) indicate potential ecological risk.
- Indicators: Monthly Flow Regime Indicators (MFRI) capturing magnitude, timing, frequency, duration, and rate of change of flows.
- Data processing:
  - 16 indicators derived from 9 MFRI variables (medians, IQRs, and modes for monthly timing).
  - Baseline Indicators computed from 1961-1990 naturalised flows; future indicators computed for each scenario.
- Thresholds for departure from baseline:
  - Median or IQR indicators differ by more than 30%.
  - Mode indicators differ by more than 1 month.
- Classification and output:
  - Simple colour-coded risk aggregation by how many indicators depart from baseline:
    - 0 departures: blue (no risk)
    - 1-5 departures: green (low risk)
    - 6-10 departures: amber (medium risk)
    - 11-16 departures: red (high risk)
  - Internally stored as codes: 0 (blue), 1 (green), 2 (amber), 3 (red).
- Outputs: dataset with 12 columns including coordinates and ERFA classifications for each GCM and scenario combination (e.g., ERFA_IPCM4_Natural, ERFA_IPCM4_EcF, ERFA_MIMR_SuE, etc.).

## Indicators and data structure details
- Indicators summarize annual variables:
  - Magnitude: median and IQR of annual variables.
  - Timing/seasonality: modes for certain monthly timing variables.
- Derived indicators:
  - 16 indicators in total (7 medians, 7 IQRs, 2 modes) based on 9 MFRI variables.
- Dataset structure:
  - Includes X (latitude) and Y (longitude) of each WaterGAP cell centre (WGS 1984).
  - ERFA classifications for each GCM + scenario combination (Natural + EcF, FoE, PoR, SuE).

## Validation and method testing
- WaterGAP calibration/validation:
  - Independent validation against measured discharge from GRDC at 221 European stations.
- ERFA method testing:
  - Compared against a daily-data RVA/IHA method for a subset of 683 WaterGAP cells along major rivers.
  - Results largely consistent across time steps; MFRI/ERFA deemed suitable for the study’s scope.

## Implications for data governance and use
- Provides comprehensive, harmonised pan-European ecological risk data integrating climate and socio-economic dimensions.
- High-resolution spatial coverage enables targeted risk assessment and stakeholder co-ownership of data products.
- Clear documentation of methods, inputs, and scenarios supports reproducibility and cross-domain collaboration (water management, ecology, policy).
- Several sources and models (CRU, GCMs, WaterGAP, ELDRED2) introduce multiple layers of uncertainty; useful to consider scenario planning and uncertainty analysis in decision-making.
- Output dataset format and column structure enable integration with GIS and data visualization platforms for risk mapping and decision support.

## Key takeaways for Data Leaders
- This dataset demonstrates end-to-end data assembly: climate projections, socio-economic narratives, a global hydrological model, and an ecologically informed screening method, all mapped onto a consistent 5' x 5' European grid.
- The ERFA product translates complex multi-indicator hydrological changes into an intuitive risk classification, supporting fast interpretation and communication with policy and operational teams.
- Data governance considerations include provenance, versioning across GCMs and scenarios, and the alignment of outputs with user needs (e.g., policy colleagues, river basin managers).
- The approach can inform cross-sector data collaborations and the development of reusable data assets for monitoring ecological risk related to hydrological change.