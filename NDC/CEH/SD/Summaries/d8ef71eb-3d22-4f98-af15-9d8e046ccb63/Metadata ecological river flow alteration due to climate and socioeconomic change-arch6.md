# This dataset is the first assessment of river ecological risk due to flow alteration

## Aim and scope
- Provides pan-European geographical coverage of river ecological risk due to flow alteration.
- Uses a detailed river network at 5' x 5' resolution (33,368 cells) to assess ecologically relevant hydrological indicators across the flow regime.
- Considers both climate-induced and combined climate–socio-economic pressures.
- Delivers outputs (data products) to enable end users to explore and interpret ecological risk under different futures.

## Data sources and inputs
- Climate data
  - Observed historical: 1961–1990 from Climate Research Unit (CRU, UK).
  - Projected future (2040–2069, the 2050s): two GCMs – IPSL-CM4 (IPCM4) and MIROC3.2 (MIMR).
  - Emission scenario: IPCC SRES A2; expert selection to align with socio-economic narratives.
- Socio-economic scenarios
  - Four pan-European visions converted from qualitative storylines to quantitative scenarios using fuzzy sets and Story-And-Simulation (SAS): Economy First (EcF), Fortress Europe (FoE), Policy Rules (PoR), Sustainability Eventually (SuE).
- Hydrological modelling
  - WaterGAP v3.1: a continental-scale, semi-distributed model with a hydrological component and a water-use component across five sectors (domestic, electricity, manufacturing, irrigation, livestock).
  - Includes 590 dams (ELDRED2) with management rules.
  - Calibrated/validated against measured annual discharge from GRDC at 221 gauging stations in Europe.

## Data coverage and grid
- Network: river basins/outlets represented on a 5' x 5' grid, covering major European rivers and tributaries; smallest basin ~63 km².
- Baseline and scenarios: 11 model runs in total, with baseline natural flows (1961–1990) and ten future runs (2040–2069) under different climate and socio-economic combinations.

## Experimental design and model runs
- Baseline: naturalised flows with hydrology only (no water withdrawals) using CRU climate data.
- Future runs: five per GCM (IPCM4 and MIMR) including Natural and four socio-economic scenarios (EcF, FoE, PoR, SuE).
- Outputs: monthly flow time series used as inputs for the ERFA screening method.

## ERFA screening method
- Conceptual basis: Range of Variability Approach (RVA) with Indicators of Hydrological Alteration (IHA); ecologically relevant departures from baseline expected to alter ecosystems.
- Indicators: Monthly Flow Regime Indicators (MFRI) used to derive 16 indicators (based on 9 MFRI variables) describing magnitude and timing, frequency, and rate of change of flows.
- Derivation and thresholds
  - Baseline vs future indicators compared; departures defined as:
    - Median or IQR indicators > 30% difference from baseline.
    - Mode indicators differ by more than 1 month.
  - Aggregated into a simple color-coded ERFA risk classification per site:
    - 0 indicators differ: blue (no risk)
    - 1–5: green (low risk)
    - 6–10: amber (medium risk)
    - 11–16: red (high risk)
  - Dataset records include 12 columns with coordinates and ERFA classifications for each GCM and socio-economic pairing (IPCM4/MIMR combined with Natural and EcF, FoE, PoR, SuE).

## Indicators and data processing
- Indicators summarize annual hydrological variables over the full record using:
  - Magnitude: median or mean
  - Variability: interquartile range (IQR) or standard deviation
- Preference for median and IQR due to robustness to outliers and non-normal distributions.
- Monthly timing indicators (e.g., month of maximum flow) summarized by mode due to discrete 1–12 scale.
- Indicators derived from the 16 MFRI-based metrics, then differences calculated against the baseline.

## Data quality, validation and method testing
- WaterGAP calibration/validation:
  - Independently calibrated/validated against GRDC data at 221 European gauging stations.
- Method testing:
  - MFRI/ERFA compared to the RVA/IHA standard (daily data) on a subset of ~683 WaterGAP cells along major rivers.
  - For the majority of sites, results were consistent across time steps; thus MFRI/ERFA deemed appropriate for the study scope.

## Outputs, accessibility, and use
- Provides ERFA classifications and associated coordinates for each grid cell under multiple climate and socio-economic scenarios.
- Enables end users to:
  - Identify regions and basins at higher ecological risk due to flow alteration.
  - Compare risk across different climate futures and socio-economic paths.
  - Explore monthly-flow indicators and how departures from baseline drive risk classifications.
- Facilitates data-driven decision support for ecosystem management, policy planning, and risk assessment.

## Practical considerations and caveats
- Uncertainties stem from climate model choice, emission scenarios, and socio-economic narrative-to-quantitative mapping.
- Results are aggregated at the 5' x 5' grid cell level; finer-scale interpretation should consider local context and data availability.
- The iterative SAS approach links narrative futures with modelling results, meaning scenario interpretation depends on the chosen storylines.