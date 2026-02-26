# This dataset is the first assessment of river ecological risk due to flow alteration

## Overview and purpose
- Pan-European assessment of river ecological risk from flow alteration, covering 33,368 grid cells at 5' x 5' resolution.
- Considers all facets of the flow regime (climate change and socio-economic pressures) and produces monthly flow time series for baseline and future scenarios.
- Applies a new ERFA (Ecological Risk due to Flow Alteration) screening method to compare future flows against a baseline.

## Data sources and provenance
- Climate data:
  - Observed historical: 1961–1990 from Climate Research Unit (CRU, University of East Anglia).
  - Future projections (2040–2069, the 2050s): two GCMs chosen for representativeness: IPSL-CM4 (IPCM4) and MIROC3.2 (MIMR).
  - Emission scenario: IPCC SRES A2.
- Socio-economic scenarios:
  - Four pan-European narratives developed by a pan-European panel (PEP) and translated into quantitative scenarios using the SAS approach: Economy First (EcF), Fortress Europe (FoE), Policy Rules (PoR), Sustainability Eventually (SuE).
- Water model:
  - WaterGAP v3.1 (Water - Global Assessment and Prognosis) with a 5' x 5' grid, simulating hydrology and five water-use sectors.
  - Incorporates 590 European dams from ELDRED2 (EEA) and management rules.
- Validation data:
  - Calibration/validation against measured annual discharge from GRDC at 221 gauging stations across Europe.

## Modeling framework and outputs
- Five-component workflow:
  1) Climate data (historical and future) and 2) socio-economic scenarios (PEP SAS integration).
  3) Large-scale hydrological and water-use modeling (WaterGAP) to produce monthly flows.
  4) ERFA screening method to assess ecological risk relative to baseline.
  5) Comparison of future flows against baseline.
- Model runs:
  - 11 sets total: baseline naturalized (no water use) + 10 future runs (5 per GCM: IPCM4 and MIMR), including a natural run and four socio-economic scenarios (EcF, FoE, PoR, SuE).
  - Time horizon: 2040–2069 (the 2050s).
- Spatial scope:
  - Outlets of major European basins and nested sub-basins; minimum basin size represented is 63 km2.

## ERFA methodology and indicators
- Core concept: based on the Range of Variability Approach (RVA) and Indicators of Hydrological Alteration (IHA); ecologically relevant changes are detected across the full flow regime (magnitude, duration, timing, frequency, rate of change).
- Indicators (Monthly Flow Regime Indicators, MFRI):
  - 16 indicators derived from 9 MFRI variables (medians, IQRs, and modes for seasonal timings).
  - Includes indicators such as the number of high/low flow months, timing of maximum/minimum flows, and annual/seasonal mean flows.
- Derivation and interpretation:
  - Indicators calculated for baseline (1961–1990 naturalized flows) and each future scenario.
  - Departures quantified as absolute differences from baseline.
  - Thresholds for significance (expert-based):
    - Medians/IQRs: >30% difference from baseline.
    - Modes: >1 month difference.
- Classification into ERFA risk classes:
  - Simple color-coded system aggregated across indicators:
    - 0 differences → blue (no risk)
    - 1–5 differences → green (low risk)
    - 6–10 differences → amber (medium risk)
    - 11–16 differences → red (high risk)
  - Data encoded as 12 columns per cell, capturing different scenario-GCM combinations and coordinates:
    - X (latitude), Y (longitude)
    - ERFA_IPCM4_Natural, ERFA_MIMR_Natural
    - ERFA_IPCM4_EcF, ERFA_MIMR_EcF
    - ERFA_IPCM4_FoE, ERFA_MIMR_FoE
    - ERFA_IPCM4_PoR, ERFA_MIMR_PoR
    - ERFA_IPCM4_SuE, ERFA_MIMR_SuE

## Data quality, validation, and robustness
- Calibration/validation:
  - WaterGAP model validated against GRDC discharge data at 221 stations across Europe.
- Method testing:
  - MFRI/ERFA results compared to RVA/IHA daily-data approach for a subset of 683 cells along major rivers; findings were largely consistent across time steps (monthly vs daily).

## Data governance and stewardship implications
- Provenance and reproducibility:
  - Clear linkage of climate, socio-economic narratives, hydrology, and ecological risk outputs, with explicit scenario mappings and coordinate-based ERFA classifications.
- Metadata and documentation needs:
  - Detailed documentation of data sources, scenarios, thresholds, and indicator calculations to enable reuse and auditability.
- Update and interoperability considerations:
  - The framework supports updating with new climate projections or socio-economic narratives; however, large 5' x 5' grid, monthly-resolved outputs require robust storage and metadata standards.
- Practical use for data stewards:
  - Manage dataset lineage, ensure consistent versioning across GCMs and scenarios, and provide clear guidance on interpretation of ERFA class codes.
  - Maintain alignment with data quality checks (model validation against GRDC; cross-method consistency with RVA/IHA).
- Limitations and caveats:
  - Spatial resolution and aggregation may affect fine-scale applicability.
  - Thresholds based on expert judgement; future refinements may adjust sensitivity.
  - Output focuses on relative ecological risk (ERFA classes) rather than absolute ecological states.