# CFLOOD Stream Network Shapefiles for Mundeni Aru, Maduru Oya and Miyangolla Ela Basins, Sri Lanka

## Overview
- What: Shapefiles of stream networks including natural and artificial watercourses (rivers, streams, canals, etc.)
- Where: Mundeni Aru, Maduru Oya, and Miyangolla Ela river basins in eastern Sri Lanka
- How: Manually mapped from satellite imagery in Google Earth
- Why: For hydrologic modelling for the C-FLOOD project (compound flooding from tropical cyclone-induced sea surge and precipitation)
- Who: Mapped by J.B.R Matthews; oversight by R. Jayaratne and A. Raby
- Completeness: Aims for sufficient detail for modelling; watercourses not visible in imagery (dense vegetation) could not be mapped

## Collection and transformation methods
- Used the most appropriate historic Google Earth imagery for each location
- Factors considered: river level (larger breadth preferred), image age (more recent preferred), image quality
- OpenStreetMap (OSM) initial points used; existing OSM watercourses re-mapped
- Dense vegetation prevented mapping of certain watercourses; some minor canals omitted
- Missing watercourses should be accounted for when using the networks in modelling
- Centrelines manually traced and snapped at vertices using QGIS; line order indicates flow direction
- Flow-direction uncertainty in flat areas (e.g., deltas) due to low elevation variation
- Breaks occur where lakes exist
- Widths assigned from the maximum breadth observed in imagery; transitions between line segments may need smoothing for modelling

## Nature and units of recorded values
- Shapefiles contain centrelines of watercourses in UTM Zone 44N (EPSG:32644)
- Width_m attribute provides watercourse width in meters; watercourses are segmented to capture width variation
- Width values are high-precision for measurement convenience but should be treated as general indications along each segment

## Quality control
- Integrity checks of stream networks, including vertex connections and flow-direction order

## Details of data structure
- Data organized in three separate shapefile folders:
  - CFLOOD_MundeniAru_StreamNetwork_utm
  - CFLOOD_MaduruOya_StreamNetwork_utm
  - CFLOOD_MiyangollaEla_StreamNetwork_utm
- Each shapefile contains a single attribute: Width_m (width in meters)