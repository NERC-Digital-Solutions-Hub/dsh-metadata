# Perch weekly mean sizes from Green Tuft 19462012

## Overview
- A dataset of weekly mean sizes of mature perch (Perca fluviatilis) from Green Tuft, Windermere, Cumbria, sampled 1946–2012.
- Collected originally by the Freshwater Biological Association (FBA) and since 1989 by the Centre for Ecology & Hydrology (CEH) and its predecessors.
- Associated with a broader suite of Windermere fish and environmental datasets (e.g., related perch catches and Windermere monthly temperatures).

## Data structure and contents
- File: PerchWeeklyMeanSizesGreenTuft1946_2012.csv
- Columns:
  - Year: Year to which catch pertains
  - Week: Week of the year to which catch pertains
  - Mean_size: Mean size (cm) of mature perch caught at Green Tuft
  - QA_code: Quality code ('NS' = week not sampled; 'ID' = week with insufficient data)
- Size: approximately 10 KB (CSV format)
- Sampling site: Green Tuft, Windermere, north basin (OS Grid NY374019)

## Spatial coverage
- Location-level data centered on Green Tuft, Windermere lake (north basin). Spatial context suitable for mapping as a point feature or as part of a broader Windermere basin dataset.

## Temporal coverage
- 1946–2012, with weekly sampling data. Data reflect weekly mean sizes during trapping periods, typically with six trap sets per spawning season.

## Sampling design and measurement methods
- Perch were sampled using unbaited, wire-netting traps (dimensions provided) deployed for six weeks per year in groups of five.
- Traps placed on perch spawning ground (depths 2–7 m); traps lifted after about one week, repeated for six sets.
- In the lab, all captured perch were measured (to 1 mm), weighed (to 1 g), sexed, and assessed for reproductive state.
- Mean mature perch size calculated for each sampling week.
- Data quality controlled by measurements from three individuals.

## Data quality and limitations
- QA_code flags missing or insufficient data weeks; users should filter NS/ID as appropriate.
- Sampling effort and site variation exist across years, which may affect comparability.
- Mixed data collection responsibility (FBA before 1989; CEH after) but with continuity in methodology described.

## Related datasets and references
- Related: Windermere weekly catches (Winfield et al., 2014) and Windermere monthly temperatures (Winfield & Fletcher, 2014).
- Primary citation: Winfield, I. J., Fletcher, J. M. & James, J. B. (2014). Perch weekly mean sizes from Green Tuft 1946-2012.
- Data provenance notes: Data collected at Green Tuft, Windermere north basin; methodology aligned with Paxton et al. (2004) for traps.

## GIS-relevant considerations and usage
- Suitable for time-enabled mapping of mean perch size at Green Tuft; can be combined with Windermere environmental layers (e.g., temperature) to explore phenology or trophic interactions.
- Handle missing weeks via QA_code; NS/ID weeks should be treated as missing data in visualizations.
- Visualization options include: time-series displays, weekly heatmaps at a fixed site, or animated maps showing size changes over years.
- Metadata supports data cleaning: trap type, sampling depth, and deployment regime aid in documenting potential biases and comparability across years.
- Could be integrated with related datasets to build a multi-layer Windermere index (fish size, catches, and temperature).

## Access and usage notes
- Rights: Database rights/copyright © NERC - Centre for Ecology & Hydrology / Freshwater Biological Association (FBA).
- Data format: CSV; ensure proper handling of QA_code and weekly-resolution time data for GIS workflows.