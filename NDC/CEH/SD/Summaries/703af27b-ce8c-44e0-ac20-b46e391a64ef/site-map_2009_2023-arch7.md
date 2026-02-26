# Site Names and Locations for River Monitoring Stations

## Overview
- A compact registry of site codes paired with human-readable site names, indicating the river and location for each site.
- Focuses on the Thames catchment and its tributaries, with several additional rivers in southern England.

## Data structure and contents
- Each line follows the pattern: Code, Site name = River at Location
- Examples:
  - Tm, Site name = Thame at Wheatley
  - Ra, Site name = Ray at Islip
  - Ch, Site name = Cherwell at Hampton Poyle
  - Ev, Site name = Evenlode at Cassington Mill
  - TS, Site name = Thames at Swinford
  - TN, Site name = Thames at Newbridge
  - Wi, Site name = Windrush at Newbridge
  - Le, Site name = Leach at Lechlade (Mill Lane)
  - Cl, Site name = Cole at Lynt Bridge
  - Cn, Site name = Coln at Whelford
  - Oc, Site name = Ock at Abingdon
  - Pa, Site name = Pang at Tidmarsh
  - TSo, Site name = Thames at Sonning
  - Lo, Site name = Lodden at Charvil
  - TR, Site name = Thames at Runnymede
  - Wy, Site name = Wye at Bourne End
  - TW, Site name = Thames at Wallingford
  - TH, Site name = Thames at Hannington Wick
  - Ke, Site name = Kennet at Woolhampton
  - En, Site name = Emborne at Brimpton
  - Ju, Site name = Jubilee River at Pocock's Bridge
  - TT, Site name = Thames at Taplow
  - TG, Site name = Thames at Goring
  - Cs, Site name = Colne at Staines

## Geographic coverage
- Rivers represented include:
  - Thames and its various sites (e.g., Swinford, Newbridge, Sonning, Runnymede, Wallingford, Hannington Wick, Taplow, Goring)
  - Tributaries and nearby rivers: Ray, Evenlode, Windrush, Leach, Cole, Coln, Ock, Pang, Lodden (Loddon), Wye, Kennet, Jubilee River, Emborne/Embourne
- Concentrated in southern England regions around the Thames basin.

## GIS usage implications
- Serves as a reference table for linking site codes to precise riverine locations in map-based data products.
- Can be joined with spatial layers (river network, basemaps) and time-series hydrological data.
- Useful for creating map visualizations of monitoring sites and for spatial analyses across river systems.

## Data quality considerations
- Verify spelling and consistency of river names (e.g., Lodden likely intended to be Loddon).
- Ensure uniformity of site coding conventions (mix of two- and three-letter codes).
- Consider enriching with coordinates and metadata (measurement types, data availability, time coverage) for full GIS utility.

## Next steps for GIS specialists
- Acquire or compute precise coordinates for each site to enable accurate mapping.
- Link each site code to measurement datasets (parameters, time series, units).
- Validate and standardize river names and locations across related datasets.
- Integrate with river network shapefiles to support spatial analyses and visualization.