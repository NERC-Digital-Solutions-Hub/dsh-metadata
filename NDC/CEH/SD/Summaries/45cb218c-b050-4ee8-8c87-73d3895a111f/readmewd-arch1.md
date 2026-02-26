# Gridded data of water debt for year 2000

## Overview
- Defines water debt (WD) as the number of years required by the hydrological cycle to replenish water sources used to produce annual yields of nine major crops: wheat, maize, rice, soybean, sugar cane, sugar beet, cotton, barley, sorghum.
- WD is intended to quantify the sustainability of crop production by comparing water withdrawals with renewable water availability in a spatial grid.

## Data and methodology
- Spatial resolution and scope: global coverage at 5 arcminute grid cells.
- Temporal scope: annual data around year 2000; metadata covers 1997–2003 (circa year 2000) with annual resolution.
- WD calculation: WD,l = sum over crops of WDcr,l, where each WDcr,l is the WD for crop cr in cell l from all water sources.
- Crop-level WD across sources: for each crop and cell, WDcr,l is computed as the maximum of the per-source debts across water sources (groundwater, surface water, soil moisture).
- Water footprint component: WDcr,l is derived from the product of
  - local crop water footprint (CWFs,cr,l, m3 per ton) for each source, and
  - annual crop production (Pcr,l, tons), yielding WFs,cr,l, and then WDcr,l = WFs,cr,l divided by the cell’s average renewable water annually available.
- Availability denominator: the annual renewability rate is a long-term average (1987–2013) to smooth out extreme years.
- Final WD per grid cell: sums WDcr,l across all nine crops to produce WDs,l for each cell.
- Data release: full methods are available in open access at the linked DOI.

## Data format, structure, and file naming
- Files are provided as text (.txt) to be imported in MATLAB, Python, or R, and can also be loaded directly into GIS by changing the extension to ".ascii".
- File types include:
  - GW: WD associated with groundwater
  - SW: WD associated with surface water
  - SOILMOISTURE: WD associated with soil moisture
  - allsources (or “allsources”): WD combining all three water sources
- File naming convention: each file corresponds to WD for all nine crops in a given cell, for one water source or all sources combined.

## Spatial and data details
- Coordinate reference system: WGS 84
- Units: years
- Formats: txt (ASCII-friendly for GIS/analysis tools)
- Spatial aggregation: gridded representation enables cross-region comparisons and downstream analysis

## How to use
- Import instructions: read the txt files into your preferred data analysis tool (MATLAB, Python, R) or load into a GIS after renaming to .ascii.
- Analyses you can perform:
  - Compare WD across water sources (GW, SW, SOILMOISTURE) and all-sources
  - Aggregate or re-grid to other spatial resolutions for regional assessments
  - Analyze WD correlations with production volumes, crop types, or hydrological indicators
  - Integrate with other data layers (soil, climate, governance indicators) to model drivers of water debt
- Reproducibility: refer to the full methodology in the cited open-access paper for exact computations and data generation steps.

## Key considerations
- WD represents an interpretive metric (years of renewable water needed) rather than a direct physical shortage measure; comparisons should account for differences in renewable availability and agricultural practices.
- The calculation uses a long-term average renewable water availability to smooth interannual variability, which may affect sensitivity to drought years.
- The per-crop, per-source, per-cell max rule (for WDcr,l) captures the most limiting source for each crop, before aggregating across crops.

## Reference
- Full methods: https://doi.org/10.1029/2018WR023146