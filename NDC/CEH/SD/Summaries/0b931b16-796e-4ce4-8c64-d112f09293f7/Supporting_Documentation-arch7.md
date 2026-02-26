# Long-term vegetation monitoring data from the Hard Hill burning plots, Moor House, 1954-2013. Rose, R.J., Marrs, R.H., O'Reilly, J. & Furness, M.

## Overview
- Long-term study of vegetation change at Moor House National Nature Reserve to investigate effects of rotational burning and grazing.
- Timeframe spans 1954–2013 with multiple burning, fencing, and grazing treatments across four blocks (A–D).

## Experimental design
- Location and layout
  - Moor House NNR, OS grid NY730320; altitude 594–625 m.
  - Four replicate blocks (A–D), each 90 m long and 60 m wide, split into two 90 m × 30 m strips: fenced vs unfenced (grazing access).
  - Strips subdivided into three 30 m × 30 m cells.
- Treatments
  - Burning: No burning (N) since 1954, Short rotation burn (S, ~10-year intervals), Long rotation burn (L, ~20-year intervals).
  - Fencing: Fenced (to exclude grazing) vs unfenced (grazed by sheep; some plots grazed by grouse/small mammals in designated areas).
- Burn history
  - Burns occurred in 1954/55; 1964/65 (short rotation); 1974/75 (short and long); 1984/85 (short); 1994/95 (short and long); 2006/07 (short); 2016/17 (short and long).
  - Winter burns planned to remove surface litter while protecting deeper peat.
- Field layout reference
  - Permanent fences mark blocks; central vegetation recording plots within each cell.

## Data collection methods

### Quadrat method (1961 and 1965)
- Purpose: initial vegetation recording via species abundance estimates.
- Quadrat setup
  - 1961: twenty-five 1 m² quadrats per plot arranged on a 5 m grid; quadrats numbered 1–25.
  - 1965: ten quadrats per plot (points 6–15) with the same 1 m² size.
- measurement
  - Domin scale used for cover estimation (scores  -1, 1–9; defined cover ranges).
- Data structure
  - Single CSV per dataset with fields: Year (1961, 1965); Block (A–D); Treatment (N, L, S); Fenced (UF or F or grazed); Quadrat (1–25); DOMIN score; Species number; Species name.

### Pin method (1972 onward)
- Purpose: finer, repeated vegetation recording at greater spatial resolution.
- Sampling schedule
  - From 1972, surveys conducted during the 8th growing season in July–August: years 1972, 1982, 1992, 2001, 2013.
- Plot and transect layout
  - Within each 30 m × 30 m cell: central sampling plot 14 m across the slope and 6 m up the slope.
  - 7 transects per plot, starting 1 m from the plot marker, at 2 m intervals; each transect can be recorded on the left or right (A or B).
  - Along each transect: six 1 m quadrats (1–6, up the slope).
  - Total: 82 1 m × 1 m quadrats per plot.
- Pin frame sampling
  - 1 m long frame with 10 pins spaced every 10 cm; pins positioned at 5 cm (start) to 95 cm along the frame.
  - For each quadrat, 5 frame positions are used; a single pin location is recorded at each frame position (1–5), representing distance from the quadrat origin.
  - Each sampling includes a random assignment of pin positions 1–10.
  - Strata (vegetation height bands) recorded for vascular plants: >30 cm (1), 20–30 cm (2), 10–20 cm (3), 0–10 cm (4); unstratified (99) used when height data not recorded or for non-vascular plants.
  - Non-vascular plants, bryophytes, lichens, and non-living materials are recorded as unstratified (99) with presence/absence (1) but no height strata.
- Data collection methods
  - Absolute counts: number of touches per species within height strata (for vascular plants); presence/absence for non-vascular and other components.
- Data structure
  - Single CSV per dataset with fields: Year (1972, 1982, 1992, 2001, 2013); Block (A–D); Treatment (N, L, S); Fenced (UF or F or grazed); Stratified (s or u); Transect (1A–7B); Quadrat (1–6); Frame (1–5); Pin; Strata (1–4, 99); Score (touch counts where applicable); Species number; Species name.

## Quality control and provenance
- Surveys conducted by experienced botanical surveyors working in pairs; consistent methods and equipment across surveys.
- Supporting documentation and references available (see misc documents below).
- Species coding follows VESPAN numbers used in the Environmental Change Network (ECN) database; nomenclature updated over time.

## Usage notes for GIS specialists
- The dataset provides spatially explicit records aligned to blocks, fencing status, and burning regime, enabling map-based analysis of vegetation responses to management.
- Two distinct data collection regimes (1961/1965 quadrats and 1972–2013 pin quadrats) require harmonization if used together; DOMIN-based abundance data (1961/1965) vs height-stratified touch counts (1972–2013) correspond to different analytical approaches.
- Key attributes to link for GIS mapping: Block, Treatment, Fenced, Strata, Transect, Quadrat, Frame, Pin, Year, DOMIN score, Score (touch counts), Species number/name.
- Temporal coverage spans mid-20th century to early 2010s with multiple burn cycles; can be analyzed for long-term trends in response to grazing and burning regimes.

## Miscellaneous supporting documents
- Marrs et al. (1986): guide to recording methods and database.
- Adamson & Kahl (2001): vegetation changes within sheep-exclosure plots.
- www.ecn.ac.uk for ECN references.