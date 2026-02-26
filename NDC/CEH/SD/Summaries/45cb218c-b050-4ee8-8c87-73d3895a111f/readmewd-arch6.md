# Gridded data of water debt for year 2000

## Overview
- Defines water debt (WD) as the number of years required by the hydrological cycle to replenish water sources (soil moisture, surface water, groundwater) used to accomplish the annual production of nine major crops: wheat, maize, rice, soybean, sugar cane, sugar beet, cotton, barley, and sorghum.
- WD for a grid cell and crop-source combination is the ratio of the annual water footprint (WF) for that crop-source in the cell to the average renewable water volume annually available in the cell.
- The annual renewable rate is calculated as a long-term average across 1987–2013 to smooth year-to-year variability.
- WD for a cell is computed per crop by summing the WD contributions across all crops; for the three water sources, the WD across sources is the maximum WD value among sources for each crop.
- Year 2000 is used as the reference year because it is the most referenced year in agricultural datasets in the literature.
- Full methods are available in open access at the provided DOI.

## Methodology
- WFcr,l = CWFs,cr,l × Pcr,l, where:
  - CWFs,cr,l is the local crop water footprint by source (cubic meters per ton of crop),
  - Pcr,l is the annual production (tons of crop).
- WDcr,l (per crop, per source, per location) is the WD contribution from that crop-source.
- WDsl (total per source) is the sum of WDcr,l across all crops for that source in the cell.
- WD across three sources for a cell and crop is the maximum WDcr,l value across sources.
- Data are globally gridded at 5 arcmin resolution; temporal scope is 1997–2003 (circa year 2000); annual temporal resolution.
- Spatial reference system: WGS 84.
- Units: years.

## Data specifications
- Spatial scope: global
- Spatial resolution: 5 arcminutes
- Coordinate reference system: WGS 84
- Temporal scope: 1997–2003 (circa year 2000)
- Temporal resolution: annual
- Units: years
- Format: txt (text files)
- Compatibility: can be imported into MATLAB, Python, or R; can be loaded directly into GIS by renaming the extension to ".ascii"
- File naming: each file corresponds to the WD for all nine crops for one water source:
  - GW (groundwater), SW (surface water), SOILMOISTURE (soil moisture), and allsources (combined groundwater, surface water, and soil moisture)

## How to use / Data products
- Load and process the ASCII/text files to generate maps or dashboards of water debt by crop, source, and region.
- Create self-serve data products (e.g., pivot tables, charts) to explore WD by crop, source, and location.
- Combine with other data to inform water resource management, agricultural planning, and policy assessment.

## Practical notes for data support
- The dataset uses a long-term average for renewability to smooth extremes, with 2000 as the reference year.
- Outputs are provided per crop-source and can be aggregated per source or all sources.
- Users should be mindful of potential differences across sources and crops when interpreting cross-source WD values.