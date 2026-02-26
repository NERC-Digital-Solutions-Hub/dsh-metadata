# Perch weekly catches from Green Tuft 1946-2012

## Overview
- Dataset of total weekly catches of mature perch (Perca fluviatilis) from Green Tuft, Windermere, Cumbria, sampled 1946–2012.
- Collected originally by the Freshwater Biological Association (FBA); data management by CEH (Centre for Ecology & Hydrology) and its predecessors since 1989.
- Used in ecological research (e.g., Ohlberger et al. 2014) on phenology and population response to trophic mismatch.

## Spatial and temporal coverage
- Spatial:
  - Location: Green Tuft, Windermere lake, Cumbria, Great Britain.
  - Primary sampling site within Windermere’s north basin; approximate coordinates provided.
  - OS Grid Reference: NY374019; Easting/Northing: 337402, 501968; latitude/longitude (WGS84): 54.409297, -2.965951.
- Temporal:
  - Time period: 1946–2012.
  - Data organized by Year and Week (week of year).

## Data schema and format
- File: PerchWeeklyCatchesGreenTuft1946_2012.csv
- Size/format: 8 KB, CSV.
- Columns:
  - Year: Year to which catch pertains.
  - Week: Week of the year to which catch pertains.
  - Catch: Number of mature perch caught at Green Tuft.
  - Not_sampled: Code 'NS' indicates not sampled in that week.

## Sampling design and measurement details
- Sampling site: Green Tuft in Windermere’s north basin.
- Collection method:
  - Unbaited wire-netting traps (dimensions specified) deployed for 6 weeks per year.
  - Traps deployed in gangs of five, at depths 2–7 m, during spawning season (late April to early June); typically six sets per season.
  - All perch from traps processed in lab; data aggregated per site per week.
- Laboratory processing (for broader context, not necessarily all in the CSV):
  - Measurements: total length (to 1 mm), wet mass (to 1 g), sex, reproductive state.
  - Used to calculate total counts of mature perch per sampling week.
- Quality control:
  - Measurements validated by permutations of three individuals.

## Data quality, provenance, and related sources
- Provenance: data originally collected by FBA; maintained by CEH and predecessors since 1989.
- Related datasets:
  - Winfield, I. J., Fletcher, J. M. & James, J. B. (2014). Perch weekly mean sizes Green Tuft 1946-2012.
  - Winfield, I. J. & Fletcher, J. M. (2014). Windermere monthly temperatures 1946-2012.
- Primary reference for sampling and enumeration methods: Paxton et al., 2004.

## GIS considerations and potential uses
- Suitable for map-based visualization of weekly mature perch counts at Green Tuft over 1946–2012.
- Spatial considerations:
  - Data centered on a single site with approximate coordinates; could be used as a point time-series layer.
  - If integrating with other Windermere basins datasets, ensure consistent CRS (OSGB36 vs WGS84) and coordinate transformation.
- Temporal analyses:
  - Week-level resolution enables phenology and seasonal trend mapping.
  - Potential to link with related environmental datasets (e.g., temperature) to explore drivers.
- Data preparation tips:
  - Convert Week+Year to a continuous time index for temporal GIS analyses.
  - Handle Not_sampled entries (NS) as missing data in spatial visualizations.
  - Combine with other Green Tuft or Windermere datasets to create multi-layer GIS products (e.g., basins, temporal heatmaps).

## Access, rights, and citations
- Copyright: © NERC - Centre for Ecology & Hydrology / Freshwater Biological Association.
- Use should include proper citation to the source and related publications (e.g., Ohlberger et al. 2014; Paxton et al. 2004).