# Sediment yield measurements for fire-affected locations in the United Kingdom (2018-2019), Tenerife (2018-2019) and Australia (2019-2020)

## Overview
- A dataset of sediment transported by runoff in three fire-affected locations: Madre del Agua (Tenerife, Spain), Thompson reservoir (Victoria, Australia), and Higher Swineshaw reservoir (Manchester, UK).
- Temporal coverage varies by site: Madre del Agua 17/08/2018–14/11/2019; Thompson 13/05/2019–14/01/2020; Swineshaw 03/08/2018–30/10/2019.
- Purpose: monitoring sediment transport during rain events in burned areas using standardized erosion plots and silt fences.

## Data assets and files
- Data files: sed_yield_ma.csv (Madre del Agua), sed_yield_ts.csv (Thompson), sed_yield_sw.csv (Swineshaw).
- Data fields include: plot id, treatment, date, sediment yield (T/ha), and collection date.
- Completeness: full record for all three sites.

## Spatial and temporal coverage
- Locations with precise coordinates and UTM references:
  - Madre del Agua, Tenerife: UTM 28N 28R 343340 3119657
  - Thompson reservoir, Australia: UTM 55H 441956 5822296
  - Higher Swineshaw reservoir, UK: UTM 30U 566670 5927917
- Time windows as noted above.

## Methodology and data capture
- Experimental design: six erosion plots (3x8 m2) per treatment; silt fences per plot following Robichaud et al. 2002 protocol.
- Sampling: after rain events with precipitation depths > 10 mm.
- Sediment processing: field-weighed sediments; subsampled for lab moisture content (oven-dried at 105°C for 48 h) and corrected.
- Calculation: sediment yields (T/ha) derived by dividing corrected sediment weight by plot area.

## Data structure and variables
- Features: plot id, treatment, date, sediment yield (T/ha), collection date.
- Replication: Madre del Agua has 6 plots per treatment.
- Periodicity: measurements taken after qualifying rain events.
- Observations: Madre del Agua 102; Thompson 90; Swineshaw 84.

## Treatments and site specifics
- Madre del Agua (Tenerife): Control; wood mulch; pine needle mulch at 1.5, 5, 8, 12 t/ha (n1, n2, w1, w2 representations).
- Thompson (Australia): Low, Moderate, High fire severity.
- Swineshaw (UK): High (HS) and Extreme (ES) fire severity per Parsons et al. 2010.

## Data quality, standards, and provenance
- Spatial references and units consistently recorded (T/ha).
- Adheres to established protocols (Robichaud et al., 2002) with audit-friendly methodology and references.
- Data provenance: authors listed (Dr Jonay Neris Tome, Dr Carmen Sánchez-García, Dr Cristina Santín, Prof. Stefan Doerr, Dr Gary Sheridan).

## Access, reuse, and governance
- Data files are clearly named per site, enabling discoverability and site-level reuse.
- Suitable for cross-site comparisons of post-fire sediment transport, assessment of erosion-control treatments, and meta-analyses.
- Metadata provides traceability to methodologies; licensing information is not provided in the text.

## References
- Robichaud, P.R., Brown, R.E. 2002. Silt fences: An economical technique for measuring hillslope soil erosion.
- Parsons, A., Robichaud, P.R., Lewis, S.A., Napper, C., Clark, J.T. 2010. Field guide for mapping postfire soil burn severity.