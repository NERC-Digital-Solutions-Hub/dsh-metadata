# Gridded data of water debt for year 2000

## Overview
- Defines water debt (WD) as the number of years the hydrological cycle must replenish water used to produce annual output of nine major crops.
- Crops: wheat, maize, rice, soybean, sugar cane, sugar beet, cotton, barley, sorghum.
- WD is produced at 5 arc-minute spatial resolution for the year 2000.
- WD per cell aggregates debt from all crops; for each cell, WD across water sources is the maximum debt among sources.

## Methodology
- WD per cell (WDs, l) is the ratio of the cell’s annual water footprint (WFcr,l) to the average renewable water available in the cell.
- Annual renewability rate is a long-term average from 1987–2013 to smooth anomalies.
- Water footprint for year 2000 (WFcr,l) equals the product of:
  - Local crop water footprint by source (CWFs,cr,l) expressed in m³ per ton
  - Annual production (Pcr,l) in tons
- Total WD for a cell from all crops (WDs,l) is the sum across crops.
- For each crop, WD across sources (WDcr,l) is taken as the maximum value across sources (groundwater, surface water, soil moisture), reflecting replenishment through precipitation.
- Full methodological details are available at the open-access DOI: 10.1029/2018WR023146

## Data and scope
- Spatial scope: global
- Spatial resolution: 5 arcminutes
- Coordinate reference system: WGS 84
- Temporal scope: 1997–2003 (circa year 2000)
- Temporal resolution: annual
- Units: years
- Data format: text files (txt); can be imported into MATLAB, Python, or R, or loaded directly into GIS by renaming to .ascii

## File naming and structure
- Each file corresponds to WD for all nine crops for one water source:
  - GW (groundwater)
  - SW (surface water)
  - SOILMOISTURE
  - allsources (combined across GW, SW, and SOILMOISTURE)

## Access and usage for monitoring
- Open-access dataset intended for standardized environmental monitoring and policy evaluation.
- Suitable for integrating with other datasets (e.g., rainfall, soil, crop production) to assess environmental health and water sustainability over time.
- Data are stored in a format that supports reproducible analysis and mapping of spatial patterns of water debt.