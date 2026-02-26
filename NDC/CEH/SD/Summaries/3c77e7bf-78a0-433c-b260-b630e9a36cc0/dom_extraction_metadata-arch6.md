# Data deposit for: Water chemistry data and elemental content of dissolved organic matter extracted from freshwaters in the UK, 2018-19 Moody, C.S.

## Overview
- Provides data on water chemistry and elemental content of dissolved organic matter (DOM) from UK freshwaters (2018–2019).
- Data generated using multiple DOM extraction methods; QC applied (e.g., values below detection limits).
- Data intended to enable comparison of extraction methods, assessment of DOM composition, and cross-site analyses.
- Documentation references the manuscript: A comparison of methods for the extraction of dissolved organic matter from freshwaters, Water Research 2020.

## Data files and structure
Five CSV files are included, each with specific purposes and fields:

- DOMextraction SITES
  - Type of waterbody (headwater, stream, lake/loch, reservoir inlet/outlet)
  - Site numbers across waterbody types
  - Elevation (m asl): min/max for each waterbody category
  - Catchment area (km2): min/max per waterbody category
  - pH: min/max per waterbody category
  - DOC (mg C L-1): min/max per waterbody category
  - POC (mg C L-1): min/max per waterbody category
  - Dominant soil type (peat vs mineral) per waterbody category

- DOMextraction CHN
  - Site (site number)
  - DOC (mg C L-1) of initial water sample
  - Method (extraction method used)
  - Raw %content: Total%C, Total%N, Total%H, OrganicC%
  - Rate (mL hr-1)
  - Time to final DOM sample collection (per volume of sample)
  - Recovery% (relative to original water DOC)
  - Relative to RE: Total%C, Total%N

- DOMextraction REreps
  - Site (site number)
  - Method (replicate = A or B)
  - Raw %content: Total%C, Total%N, Total%H

- DOMextraction RECOVERY
  - Site (site number)
  - Method (extraction method)
  - Volume (mL)
  - DOMmass (mg)
  - DOMtotal%C
  - DOC mass (mg)
  - DOC mass per volume (mg L-1)
  - DOC mg L-1 (dissolved organic carbon concentration)
  - Recovery% (compared to DOC concentration in original water)

- DOMextraction SCORES
  - Method
  - N (number of samples)
  - Rate mL hr-1 (mean)
  - Recovery% (mean)
  - Recovery SE (standard error)
  - Cost per sample (£)
  - Large equipment cost (£)
  - Score components: Rate score, Recovery score, Cost score
  - Large equipment penalty
  - Sum of scores and Rank (1–9)

## Key variables and methods
- Extraction methods (as described in the associated manuscript):
  - DRY-6: dry down at 60°C
  - RE: rotary evaporation
  - RO-DF: reverse osmosis followed by dry down at room temperature
  - RO-RE: reverse osmosis followed by rotary evaporation
  - SPE: solid phase extraction
  - DRY-F: dry down at room temperature
  - FD: freeze drying
  - DIA-FD: dialysis followed by freeze drying
  - DIA-FH: dialysis followed by dry down at room temperature
- Carbon, nitrogen, hydrogen metrics:
  - Total%C, Total%N, Total%H
  - OrganicC%
  - DOC concentration (mg C L-1)
- Performance metrics:
  - Rate (mL hr-1)
  - Recovery% (relative to original DOC)
  - Time to final DOM sample
  - Cost indicators and equipment requirements

## Processing and quality assurance
- Data collection and generation methods are described in the associated manuscript (Water Research 2020).
- Data are quality controlled; e.g., values below detection limits flagged/adjusted as part of QC.
- Recovery percentages may exceed 100% due to methodological differences (e.g., filtration steps removing colloidal matter differently from DOC analysis).

## How to use and combine the data
- Build cross-site comparisons of DOM composition by linking DOMextraction CHN data with SITES metadata.
- Compare extraction methods using DOMextraction SCORES (rate, recovery, cost) and RECOVERY metrics to identify efficient, accurate approaches.
- Use REreps to assess replicate precision for each site/method.
- Create dashboards or self-serve reports:
  - Method performance by site type (headwaters vs. reservoirs)
  - Variation of DOC, POC, and elemental content across waterbody categories
  - Cost-effectiveness analyses integrating rate, recovery, and equipment costs
- Potential analyses:
  - Correlation of DOM elemental composition with site characteristics (elevation, catchment area, pH)
  - Method-to-method comparability assessments relative to the RE (rotary evaporation) reference

## Considerations for data support and reuse
- Data are multi-table and require careful linkage via site numbers and method codes.
- Some recovery values may exceed 100% due to differences in sample preparation vs. direct DOC measurement; interpret accordingly.
- Replicates (A/B) in REreps should be considered for variability assessments.
- The dataset is tied to a specific UK freshwater context (2018–2019) and to the cited Water Research 2020 manuscript; users should consult that manuscript for full methodological descriptions and caveats.

## Access and provenance
- Data deposited alongside the study: "Water chemistry data and elemental content of dissolved organic matter extracted from freshwaters in the UK, 2018-19 Moody, C.S."
- QC and documentation aim to support transparent, reproducible analysis and data product development.