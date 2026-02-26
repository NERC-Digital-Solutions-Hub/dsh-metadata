# Gridded data of water debt for year 2000

## Overview
- Global gridded dataset describing water debt (WD): the number of years the hydrological cycle would need to replenish water used to produce annual yield of nine major crops.
- Crops included: wheat, maize, rice, soybean, sugar cane, sugar beet, cotton, barley, sorghum.
- Data designed for GIS visualization and map-based analyses at a regional to global scale.
- WD values are computed for year 2000 and provided at a 5 arcminute resolution.

## Methodology
- WD is calculated as the ratio of the cell’s annual water footprint (WF) for each crop-source-location to the cell’s average renewable water volume per year.
- Annual renewability rate is a long-term average from 1987–2013 to smooth out variability.
- Water footprint (WF) for a given crop-source-location is the product of:
  - Local crop water footprint by source (CWFs,cr,l, in m³ per ton)
  - Annual crop production (Pcr,l, in tons)
- Total WD for a cell from all crops: sum of WD across crops.
- The WD across the three sources (groundwater, surface water, soil moisture) for a crop-cell is the maximum WD across sources: WDcr,l = max_s(WDs,l,cr).
- Full methodological details are available in the referenced open-access article (DOI provided).

## Data scope and structure
- Spatial scope: Global; spatial resolution: 5 arcminutes; coordinate system: WGS 84 (EPSG:4326).
- Temporal scope: Annual data around year 2000, with a period coverage of 1997–2003 (circa year 2000).
- Units: Years.
- Data packaging: Text files (".txt"), designed for import into MATLAB, Python, or R; can also be imported into GIS by changing the file extension to ".ascii".

## Content and naming conventions
- Each file corresponds to the WD for all nine crops for one water source:
  - GW: groundwater
  - SW: surface water
  - SOILMOISTURE: soil moisture
  - allsources: combined across all three sources
- File naming reflects the associated water source; each file covers all nine crops for that source.

## How to use in GIS
- Load ASCII/.ascii file into GIS software to create rasters or grids.
- Verify and set CRS to WGS 84 (EPSG:4326).
- For multi-source analyses, compute per-cell WD across sources by applying the max rule (WDcr,l = max across s).
- Visualize spatial patterns of water debt, compare across sources (GW, SW, SOILMOISTURE) and the combined all-sources dataset.
- Use long-term renewal rate to understand regional water stress by comparing WD values with available water resources.

## Notes for data handling and interpretation
- WD values reflect a century-spanning average for water renewability to avoid extremes from atypical years.
- The approach takes the maximum WD across water sources per crop to represent the replenishment constraint due to precipitation-driven recharge.
- Data may require harmonization if combined with other datasets (e.g., different resolutions or timeframes).

## Reference
- Methodological details and full approach are published in: https://doi.org/10.1029/2018WR023146