# Dataset name Sediment yield measurements for fire-affected locations in the United Kingdom (2018-2019), Tenerife (2018-2019) and Australia (2019-2020)

## Overview
- Multi-site dataset measuring sediment transported by runoff after fire events.
- Locations: Madre del Agua (Tenerife, Spain), Thompson reservoir (Victoria, Australia), Higher Swineshaw reservoir (Manchester, UK).
- Time spans: Madre del Agua 17/08/2018 – 14/11/2019; Thompson 13/05/2019 – 14/01/2020; Swineshaw 03/08/2018 – 30/10/2019.
- Data collected with erosion plots (3 x 8 m2) and silt fences following Robichaud et al. (2002) protocol; yields expressed as tonnes per hectare (T/ha) per plot per collection date.

## Data files
- sed_yield_ma.csv (Madre del Agua)
- sed_yield_ts.csv (Thompson reservoir)
- sed_yield_sw.csv (Higher Swineshaw)

## Study locations and coordinates
- Madre del Agua, Tenerife, Spain: UTM 28N 28 R 343340 3119657
- Thompson reservoir, Victoria, Australia: UTM 55 H 441956 5822296
- Higher Swineshaw reservoir, Manchester, UK: UTM 30 U 566670 5927917

## Data collection and methodology
- Purpose: Monitoring sediment transport during rain events in burned areas.
- Method: Six erosion plots per treatment per site (3 x 8 m2) with silt fences; rain events >10 mm trigger collection.
- Processing: Sediments weighed in the field; subsampled to determine water content; oven-dried at 105°C for 48 h and weighed again to correct field weights.
- Yield calculation: Sediment yields (T/ha) calculated by dividing corrected sediment weight by plot area.

## Treatments and replication
- Madre del Agua: Treatments include Control, wood mulch (C), pine needle mulch at 1.5 T/ha (n1), 5 T/ha (n2), 8 T/ha wood chips mulch (w1), 12 T/ha wood chips mulch (w2); 6 plots per treatment.
- Thompson: Fire severity levels Low, Moderate, High.
- Swineshaw: Fire severity High (HS) and Extreme (ES) per Parsons et al. (2010).

## Data structure and content
- Variables include: plot id, treatment, date of collection, sediment yield per plot (T/ha), and site identifier.
- Completeness: Full record of calculated sediment yields per site, plot, and collection date.

## Data quality and provenance
- Data produced by Dr Jonay Neris Tome, Dr Carmen Sánchez-García, Dr Cristina Santín, Prof. Stefan Doerr, and Dr Gary Sheridan.
- References and protocols:
  - Robichaud, P.R., Brown, R.E. 2002. Silt fences: An economical technique for measuring hillslope soil erosion.
  - Parsons, A. et al. 2010. Field guide for mapping postfire soil burn severity.