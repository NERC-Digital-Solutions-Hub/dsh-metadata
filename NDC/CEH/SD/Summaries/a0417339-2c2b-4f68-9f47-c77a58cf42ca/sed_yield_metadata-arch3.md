# Sediment yield measurements for fire-affected locations in the United Kingdom (2018-2019), Tenerife (2018-2019) and Australia (2019-2020)

## Overview
- Objective: Monitoring sediment transport during rain events in burned areas to inform post-fire erosion risk and management.
- Locations: Madre del Agua (Tenerife, Spain), Thompson reservoir (Victoria, Australia), Higher Swineshaw reservoir (Manchester, UK).
- Timeframe: 2018–2019 for Tenerife and UK; 2019–2020 for Australia.

## Dataset contents
- Data files:
  - sed_yield_ma.csv (Madre del Agua, Tenerife)
  - sed_yield_ts.csv (Thompson reservoir, Australia)
  - sed_yield_sw.csv (Higher Swineshaw reservoir, UK)
- Common structure: per-site records of sediment yield by plot and collection date.
- Key variables include: plot id, treatment, date, sediment yield (T/ha), and plot area.

## Location, timing and data scope
- Madre del Agua (Tenerife, Spain)
  - Period: 17/08/2018 – 14/11/2019
  - Plot-based erosion measurements after fire-affected events
- Thompson reservoir (Victoria, Australia)
  - Period: 13/05/2019 – 14/01/2020
- Higher Swineshaw reservoir (Manchester, UK)
  - Period: 03/08/2018 – 30/10/2019

## Methodology and calculation
- Experimental setup: Six erosion plots (3 m × 8 m) with sediment fences per treatment, following Robichaud et al. (2002) protocol.
- Data collection: Sediment collected after rain events; fences cleaned between events.
- Laboratory processing: Sediments weighed in field; subsample to determine water content; oven-dried at 105°C for 48 h; weighed again.
- Calculation: Sediment yields (T/ha) per plot and collection date by dividing corrected sediment weights by plot area.
- Outputs: Calculated sediment yields per site, per plot, per collection date.

## Treatments and replication
- Madre del Agua (Tenerife): Treatments include Control; wood mulch (C); 1.5 T/ha pine needle mulch (n1); 5 T/ha pine needle mulch (n2); 8 T/ha wood chips mulch (w1); 12 T/ha wood chips mulch (w2); replication ≈ 6 plots per treatment.
- Thompson (Australia): Fire severity levels — Low, Moderate, High.
- Swineshaw (UK): Fire severity — High (HS) and Extreme (ES) per Parsons et al. (2010); replication ≈ 6 plots per treatment.
- Periodicity: After rain events with precipitation depths > 10 mm.

## Data quality, completeness and governance
- Completeness: Full record for all sites.
- Metadata and provenance: Detailed contextual notes included (locations, dates, treatments, replicate structure, methodology).
- Data standardization: Uses a consistent metric (sediment yield in T/ha) and a common calculation approach (corrected field weights, plot-area normalization).
- Data sharing and openness: Datasets are provided as CSVs with clear field definitions; provenance includes researchers involved and published protocols (Robichaud 2002; Parsons et al. 2010).

## Relevance for monitoring frameworks
- Demonstrates a replicable, field-based approach to quantify sediment transport after fires, suitable for informing policy evaluation and decision-making.
- Highlights importance of:
  - Standardized measurement protocols (to enable inter-site comparability).
  - Transparent metadata and data provenance.
  - Data governance considerations, including data sharing obligations and updates.
- Provides a time-series dataset across multiple fire-affected regions, enabling cross-location comparisons and trend assessment in post-fire erosion control strategies. 

## References
- Robichaud, P.R., Brown, R.E., 2002. Silt fences: An economical technique for measuring hillslope soil erosion. Gen. Tech. Rep. RMRS-GTR-94.
- Parsons, A., Robichaud, P.R., Lewis, S.A., Napper, C., Clark, J.T., 2010. Field guide for mapping postfire soil burn severity. Gen. Tech. Rep. RMRS-GTR-243.