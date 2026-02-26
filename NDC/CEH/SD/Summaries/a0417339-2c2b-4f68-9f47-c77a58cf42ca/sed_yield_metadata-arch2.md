# Sediment yield measurements for fire-affected locations in the United Kingdom (2018-2019), Tenerife (2018-2019) and Australia (2019-2020)

## Overview
- Dataset capturing sediment transported by runoff in three fire-affected locations: Madre del Agua (Tenerife, Spain), Thompson reservoir (Victoria, Australia), and Higher Swineshaw reservoir (Manchester, UK).
- Timeframes: Madre del Agua 17/08/18–14/11/2019; Thompson 13/05/19–14/01/2020; Swineshaw 03/08/18–30/10/2019.
- Data files: sed_yield_ma.csv (Madre del Agua), sed_yield_ts.csv (Thompson reservoir), sed_yield_sw.csv (Swineshaw).
- Purpose: monitor sediment transport during rain events in burned areas; support environmental health monitoring and policy evaluation.

## Data files and structure
- Files contain erosion-plot based measurements (3x8 m plots) with sediment fences, following Robichaud et al. (2002) protocol.
- Variables include: plot id, treatment, date, sediment yield (T/ha) per plot and collection date, output per site.
- Data are presented per site and per collection date, enabling temporal analysis.

## Locations, methods, and site specifics
- Madre del Agua, Tenerife, Spain (UTM 28N 343340 3119657)
  - Plot setup: 6 plots per treatment; silt fences cleaned after rain events.
  - Periodicity: after rainfall events >10 mm.
  - Treatments: control, wood mulch (C), pine needle mulch at 1.5 t/ha (n1), pine needle mulch at 5 t/ha (n2), wood chips mulch at 8 t/ha (w1), wood chips mulch at 12 t/ha (w2).
  - Observations: 102 measurements across all treatments.
- Thompson reservoir, Victoria, Australia (UTM 55 H 441956 5822296)
  - Periodicity: after rain events >10 mm.
  - Treatments: low, moderate, high fire severity.
  - Observations: 90 measurements across treatments.
- Higher Swineshaw reservoir, Manchester, UK (UTM 30 U 566670 5927917)
  - Periodicity: after rain events >10 mm.
  - Treatments: high (HS) and extreme (ES) fire severity.
  - Observations: 84 measurements across treatments.

## Methodology
- Sediment collection: erosion plots with silt fences; field weighing of sediments; subsample for water content; oven-drying at 105°C for 48 h; re-weighing to obtain corrected sediment weight.
- Calculation: sediment yields (T/ha) = corrected sediment weight per plot per collection date divided by plot area (3x8 m^2).
- Data completeness: designated as Full record.

## Data quality, completeness, and references
- Completeness: Full record across all three sites.
- Quality assurance: Standard protocol ( Robichaud et al., 2002) for silt fences and erosion plots; lab processing for moisture correction.
- References:
  - Robichaud, P.R., Brown, R.E. (2002). Silt fences: An economical technique for measuring hillslope soil erosion. Gen. Tech. Rep. RMRS-GTR-94. U.S. Forest Service.
  - Parsons, A. et al. (2010). Field guide for mapping postfire soil burn severity. Gen. Tech. RMRS-GTR-243. U.S. Forest Service.

## Data stewardship and usage
- Data are stored as separate site-specific CSV files and include metadata on plot, treatment, date, and calculated sediment yield per site.
- Analysts can:
  - compare sediment yields across sites and fire severities,
  - assess the effectiveness of mulching and other treatments on reducing erosion,
  - model sediment transport responses to rainfall events and fire severity.
- Data management considerations for portals: ensure proper site metadata, coordinate systems, collection dates, and treatment classifications are uploaded for interoperability.

## How this supports environmental monitoring
- Provides standardized, repeatable measurements of post-fire sediment transport across multiple regions.
- Enables cross-site comparisons and long-term trend analysis in environmental health and policy performance.
- Supports data integration with rainfall, soil, and land-management datasets to enhance understanding of erosion dynamics after fires.