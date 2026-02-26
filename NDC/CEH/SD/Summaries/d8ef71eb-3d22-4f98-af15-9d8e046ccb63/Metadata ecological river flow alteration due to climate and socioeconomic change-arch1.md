# ERFA: Ecological Risk due to Flow Alteration

- Purpose and scope:
  - First pan-European assessment of river ecological risk due to flow alteration.
  - Provides wide geographical coverage and a detailed river network at 5' x 5' resolution (33,368 grid cells).
  - Explicitly considers a set of ecologically relevant hydrological indicators across the full flow regime.
  - Accounts for both climate change and combined climate and socio-economic pressures.

- Data and inputs:
  - Climate data:
    - Observed historical (1961–1990) from Climate Research Unit (CRU, UK).
    - Projected future (2040–2069, the 2050s) from two GCMs: IPSL-CM4 (IPCM4) and MIROC3.2 (MIMR).
    - Emission scenario: IPCC SRES A2.
  - Socio-economic scenarios:
    - Four qualitative narratives translated to quantitative scenarios via SAS (Story-And-Simulation):
      - Economy First (EcF)
      - Fortress Europe (FoE)
      - Policy Rules (PoR)
      - Sustainability Eventually (SuE)
  - Hydrological model:
    - WaterGAP v3.1 (Water-GAP: Water - Global Assessment and Prognosis), grid-based (5' x 5').
    - Components: global hydrological model + global water-use model (domestic, electricity, manufacturing, irrigation, livestock).
    - Includes 590 European dams with management rules; calculates daily balances; accounts for human withdrawals.
  - Calibration/validation data:
    - Independent validation against measured annual discharge from GRDC at 221 gauging stations.

- Spatial and temporal scope:
  - 33,368 WaterGAP grid cells chosen to cover major European rivers and tributaries; smallest basin ~63 km².
  - Baseline (naturalised) flows: 1961–1990 (no withdrawals).
  - Future runs: 2040–2069 (2050s) under various climate and socio-economic combinations.
  - Ten future runs plus Natural baseline: IPCM4_EcF, IPCM4_PoR, IPCM4_FoE, IPCM4_SuE, MIMR_EcF, MIMR_PoR, MIMR_FoE, MIMR_SuE, plus IPCM4/MIMR Natural.

- ERFA methodology (Inductive screening):
  - Based on Range of Variability Approach (RVA) and Indicators of Hydrological Alteration (IHA).
  - Uses Monthly Flow Regime Indicators (MFRI) to capture magnitude, duration, timing, frequency, and rate of change of flow.
  - Indicators are derived for baseline (1961–1990 naturalised flows) and for every future projection.
  - Changes are aggregated into a simple, interpretable colour-coded risk classification.

- Indicators and data derivation:
  - 16 indicators in total (7 medians, 7 IQRs, 2 modes) derived from 9 MFRI variables.
  - Special handling for discrete variables:
    - Mode (months of maximum flow, mean flow months, etc.) used for timing-related indicators.
  - Thresholds for departure from baseline (expert-based):
    - Median or IQR changes > 30% from baseline considered significant.
    - Mode changes > 1 month considered significant.
  - Output summarization:
    - For practicality, differences aggregated into a per-cell risk class.
    - ColorCode mapping (converted to codes in dataset):
      - 0 = blue/no risk
      - 1 = green/low risk
      - 2 = amber/medium risk
      - 3 = red/high risk

- Output dataset and codes:
  - 12 columns compiling per-cell ERFA classifications.
  - Key columns include:
    - X, Y: coordinates (WGS 1984)
    - ERFA_IPCM4_Natural, ERFA_MIMR_Natural: risk classes using IPCM4 or MIMR with natural baseline
    - ERFA_IPCM4_EcF, ERFA_MIMR_EcF: IPCM4/MIMR under Economy First
    - ERFA_IPCM4_FoE, ERFA_MIMR_FoE: IPCM4/MIMR under Fortress Europe
    - ERFA_IPCM4_PoR, ERFA_MIMR_PoR: IPCM4/MIMR under Policy Rules
    - ERFA_IPCM4_SuE, ERFA_MIMR_SuE: IPCM4/MIMR under Sustainability Eventually

- Method testing and validation:
  - WaterGAP calibration and validation performed against GRDC data at 221 stations.
  - MFRI/ERFA method compared with RVA/IHA (daily data-based method) for 683 WaterGAP cells along major rivers.
  - Findings: results largely consistent across time steps; MFRI/ERFA deemed suitable for the study’s scope.

- Practical implications:
  - Provides a scalable, pan-European screening tool linking hydrological change to ecological risk.
  - Enables identification of regions where climate and socio-economic pressures are likely to cause ecologically meaningful flow alterations.
  - Facilitates reporting and interpretation through a standardized, easily plottable risk classification.

- Key considerations and notes:
  - The approach emphasizes ecologically meaningful aspects of flow regime (magnitude, timing, duration, frequency, rate of change).
  - Thresholds and classifications are based on expert judgment to balance interpretability with ecological relevance.
  - The dataset balances computational feasibility with ecological detail by using a 5' x 5' grid and a fixed set of 16 indicators.