# Long-term vegetation monitoring data from the Hard Hill burning plots, Moor House, 1954-2013. Rose, R.J., Marrs, R.H., O'Reilly, J. & Furness, M.

## Overview
- Long-term study to investigate effects of rotational burning and grazing on blanket bog vegetation at Moor House National Nature Reserve.
- Temporal span: burns and vegetation data collected from 1954 to 2013.
- Data are organized to allow assessment of environmental health and policy-relevant outcomes related to burning/grazing management.

## Experimental design
- Location: Moor House NNR, OS grid NY730320.
- Structure: four replicate blocks (A, B, C, D) spanning altitude 594–625 m.
- Experimental layout: randomized split-plot design with permanent fences to create fenced (excludes sheep) vs unfenced (grazed) strips.
- Each block consists of two 90 m × 30 m strips (fenced and unfenced), which are subdivided into three 30 m × 30 m cells.
- Treatments within cells: three burning sub-treatments assigned within each strip and cell - no burn (N), short-rotation burn (S, 10-year interval), long-rotation burn (L, 20-year interval).
- Burning timing: winters with suitable conditions; burns occurred in 1954/55, 1964/65, 1974/75, 1984/85, 1994/95, 2006/07 (two-year delay), and 2016/17.

## Data collection timeline and methods
- 1961 and 1965: initial post-burn vegetation recordings using quadrats and the DOMIN cover scale.
  - 1961: 25 quadrats per block (1 m² each) positioned on a 5 m grid, cover estimated via DOMIN scores.
  - 1965: 10 quadrats per plot (recording points 6–15), same DOMIN scale.
- 1972 onwards: vegetation recorded with pin quadrats.
  - Plot setup: within each 30 m × 30 m cell, a central sampling plot 14 m across × 6 m up the slope; 7 transects starting 1 m from the marker at 2 m intervals.
  - Recording positions: along each transect, 6 quadrats (1–6) with left/right side designation (A/B) giving 82 1 m × 1 m quadrats per plot.
  - Sampling frame: 1 m long pin frame with 10 pins at 10 cm intervals; 5 frame positions per quadrat.
  - Survey scale: 480 quadrats per survey (20 quadrats per treatment per block; 6 treatments per block across 4 blocks).
  - Data captured per vascular plant: number of touches per plant within four height strata; non-vascular plants and other features recorded as presence/absence or unstratified.
  - Height strata (for vascular plants): >30 cm, 20–30 cm, 10–20 cm, 0–10 cm; unstratified = 99.
  - Non-vascular, bryophytes, lichens, litter, bare soil, peat, etc.: recorded unstratified (99) with presence/absence only.

## Fieldwork and instrumentation
- Permanent fences indicate block boundaries; smaller posts mark treatment extents; central plots tracked for vegetation.
- Quadrats: 1961/1965 data collected with a quadrat method; 1972 onward data collected with pin quadrats.
- Quality control: surveys conducted by experienced botanical surveyors in pairs, maintaining consistent methods and equipment.

## Data structure and datasets
- Quadrat method dataset (1961 and 1965):
  - Columns: Year (1961, 1965); Block (A–D); Treatment (N, L, S); Fenced (UF or F); Quadrat (1–25); DOMIN score (-1, 1–9); Species number (VESPAN code); Species name (updated nomenclature).
- Pin method dataset (1972 onwards):
  - Columns: Year (1972, 1982, 1992, 2001, 2013); Block (A–D); Treatment (N, L, S); Fenced (UF or F); Stratified (s or u); Transect (1A–7B); Quadrat (1–6); Frame (1–5); Pin (position along frame); Strata (1 for >30 cm, 2 for 20–30 cm, 3 for 10–20 cm, 4 for 0–10 cm, 99 unstratified); Score (number of touches for vascular plants in stratified data); Species number; Species name.
  - Notes: Stratified data available for most vascular plants in 1972, 1982 Block B, 1982 Blocks A/C/D, 1992, 2001, 2013; non-vascular data largely unstratified.
- Data formats: both datasets stored as CSV files with explicit column headers and consistent coding schemes; VESPAN codes used for species identifiers (ECN database).

## Data quality and management
- Data collected by trained observers using standardized protocols across decades.
- Consistent replication and randomization within blocks to support robust comparisons among burning and grazing treatments.
- Data curated to align nomenclature with updated plant taxonomy; integration with Environmental Change Network (ECN) standards via VESPAN codes.

## Related resources
- Supporting documents:
  - Marrs et al. (1986) guide to recording methods and the Moor House database.
  - Adamson & Kahl (2001) vegetation changes in sheep exclosure plots.
  - Environmental Change Network (ECN) resources: www.ecn.ac.uk

## Relevance for environmental monitoring and analysis
- Provides a long-term, standardized dataset to evaluate how grazing exclusion and rotational burning influence vegetation dynamics on blanket bog, with explicit treatment structures and time-series data.
- Enables assessment of management policies against ecological outcomes across multiple temporal scales and environmental conditions.