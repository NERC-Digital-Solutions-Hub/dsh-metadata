# This dataset is the first assessment of river ecological risk due to flow alteration

## Overview
- Pan-European geographic coverage using a high-resolution river network (33,368 cells at 5' x 5' resolution).
- Focus on ecologically relevant hydrological indicators that capture all facets of the flow regime.
- Considers both climate-induced change and combined climate and socio-economic pressures.
- Produces a new Ecological Risk due to Flow Alteration (ERFA) screening output by comparing future flows with a baseline.

## Methodology (five main components)
- Climate data: observed historical data (1961–1990) from CRU; future projections (2040–2069, “2050s”) from two GCMs (IPSL-CM4/IPCM4 and MIROC3.2/MIMR) under IPCC SRES A2.
- Socio-economic scenarios: four pan-European visions translated into quantitative scenarios using the SAS (Story-And-Simulation) approach:
  - Economy First (EcF)
  - Fortress Europe (FoE)
  - Policy Rules (PoR)
  - Sustainability Eventually (SuE)
- WaterGAP model: a continental-scale semi-distributed hydrological and water-use model (5' x 5' grid) with 590 dams; outputs daily water balances and river discharge; calibrated/validated against GRDC data.
- Monthly flow time series: baseline (1961–1990 naturalised flows) and future projections for 2040–2069 under the various climate and socio-economic scenarios.
- ERFA screening method: compares future flows against baseline using a set of flow indicators; aggregates results into a simple color-coded risk class.

## Data sources and inputs
- Climate data: CRU historical (1961–1990); GCM projections (IPCM4 and MIMR) under SRES A2.
- Socio-economic scenarios: narrative storylines (EcF, FoE, PoR, SuE) converted to quantitative inputs.
- Hydrology and water use: WaterGAP version 3.1 with 5' x 5' grid; includes management rules for 590 European dams; subset of cells selected to represent major European rivers (33,368 cells).
- Validation data: GRDC discharge data at 221 gauging stations across Europe.

## Model runs and outputs
- Eleven monthly flow series generated:
  - Baseline naturalised run using 1961–1990 climate data with no water use.
  - Ten future runs: for each GCM (IPCM4 and MIMR), one Natural run and four socio-economic scenarios (EcF, FoE, PoR, SuE).
- ERFA outputs per grid cell:
  - ERFA class codes for IPCM4 and MIMR under Natural and each scenario (total 10 scenario-specific codes per cell, plus Natural cases).
  - Output format includes 12 columns with coordinates and ERFA classifications (blue/no risk, green/low risk, amber/medium risk, red/high risk).

## ERFA indicators and thresholds
- Indicators reflect magnitude and variability of hydrological variables; derived from 16 indicators across 9 MFRI variables.
- Summary statistics used: medians and interquartile ranges (IQR), with monthly timings summarized by mode for discrete timing variables.
- Departure from baseline deemed significant if:
  - Median or IQR indicators differ by more than 30% from baseline.
  - Mode indicators differ by more than 1 month.
- Risk classification via color-coding:
  - 0: blue/no risk
  - 1: green/low risk
  - 2: amber/medium risk
  - 3: red/high risk

## Validation and method testing
- WaterGAP calibration/validation performed against measured annual discharge from GRDC at 221 stations.
- ERFA/MFRI method (RVA/IHA-based) tested against a daily-data benchmark for 683 WaterGAP cells along major rivers; results largely consistent across time steps, supporting method suitability for the study scope.

## Relevance for monitoring frameworks
- Demonstrates integration of climate projections, socio-economic narratives, hydrological modeling, and ecological risk assessment to produce actionable spatial risk outputs.
- Provides a transparent pipeline from data sources to indicators and risk classifications, suitable for dashboards, maps, and reports.
- Uses publicly sourced climate data and validated hydrological data; emphasizes the need for clear documentation of data sources, transformations, and governance.

## Key considerations for authors of monitoring frameworks
- Data availability and accessibility: leverage public data sources (e.g., CRU, GRDC, ELDRED2) and document data provenance.
- Metadata quality: ensure clear metadata for inputs, model configurations, and indicator definitions to enable reuse and verification.
- Data transformation: convert raw hydrological outputs into standardized indicators (MFRI) and thresholds that support cross-site comparability.
- Data governance: establish processes for data sharing, versioning, and update cycles to maintain current analyses while meeting openness requirements.
- Stakeholder engagement: align narrative storylines with quantitative modelling (SAS approach) to improve relevance and uptake in policy and decision-making.