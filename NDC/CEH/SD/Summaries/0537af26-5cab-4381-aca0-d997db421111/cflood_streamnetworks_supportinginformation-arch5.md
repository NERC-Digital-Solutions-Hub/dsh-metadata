# Overview

- What: Shapefiles of stream networks, including natural and artificial watercourses (rivers, streams, canals, etc.)
- Where: Mundeni Aru, Maduru Oya, and Miyangolla Ela river basins in eastern Sri Lanka
- How: Manually mapped using satellite imagery from Google Earth
- Why: For hydrologic modelling for the C-FLOOD project (compound flooding from tropical cyclone-induced sea surge and precipitation)
- Who: Mapped by J.B.R Matthews; oversight and advice by R. Jayaratne and A. Raby
- Completeness: Intended to be detailed enough for modelling; watercourses not visible in Google Earth imagery (e.g., due to dense vegetation) could not be mapped

## Collection, generation, transformation methods

- Stream mapping used the most appropriate historic Google Earth imagery for each location, considering river level, image age, and image quality
- OpenStreetMap (OSM) used as a starting point; watercourses already in OSM were re-mapped
- Dense vegetation prevented mapping of some watercourses; some minor canals not mapped
- Missing watercourses should be accounted for when using the networks for hydrologic modelling
- Centrelines manually traced and snapped at vertices using QGIS to form the network; the order of line points indicates flow direction; uncertainty in flat areas where elevations are similar
- Breaks occur where lakes exist
- Widths assigned based on the maximum breadth observed in images; smoothing of transitions may be needed for modelling

## Nature and Units of recorded values

- Shapefiles contain centrelines of watercourses in UTM Zone 44N (EPSG:32644)
- Width_m attribute provides watercourse width in metres; watercourses are segmented to capture width variation
- Widths are precise for measurement convenience but should be treated as general indicators for modelling along the segments

## Quality control

- Integrity checks include proper connections at vertices and consistency of flow directions indicated by point ordering

## Details of data structure

- Data organized in three separate shapefile folders:
  - CFLOOD_MundeniAru_StreamNetwork_utm
  - CFLOOD_MaduruOya_StreamNetwork_utm
  - CFLOOD_MiyangollaEla_StreamNetwork_utm
- Each shapefile contains a single attribute: Width_m (width in metres)