# Overview

- What: Shapefiles of stream networks, including both natural and artificial watercourses (rivers, streams, canals, etc.)
- Where: Mundeni Aru, Maduru Oya, and Miyangolla Ela river basins in eastern Sri Lanka
- How: Stream networks manually mapped using satellite imagery from Google Earth
- Why: Created for hydrologic modelling for the C-FLOOD project (Compound flooding from tropical cyclone-induced sea surge and precipitation in Sri Lanka)
- Who: J.B.R Matthews mapped the stream networks; R. Jayaratne and A. Raby provided oversight and advice
- Completeness: Aimed for sufficient detail for the intended modelling purpose; watercourses not visible in Google Earth imagery (e.g., due to dense vegetation) could not be mapped

## Collection / generation / transformation methods

- Mapping used the most appropriate historic Google Earth imagery for each location, prioritising river level, image age, and image quality
- OpenStreetMap (OSM) used as a starting point; watercourses already in OSM were re-mapped
- Dense vegetation prevented mapping of certain watercourses (e.g., southern Mundeni Aru basin); some minor canals were not mapped
- Missing watercourses should be accounted for when using the networks for hydrologic modelling
- Centrelines were manually traced and snapped together at vertices using QGIS to form the stream network
- Flow direction is indicated by the order of points along each line segment (downhill)
- Uncertainty in flow directions exists in flat areas (e.g., Mundeni Aru delta) where elevations from NASADEM/CoastalDEM have limited variance
- Breaks exist in the networks where lakes occur
- Widths were assigned from the maximum breadth observed in Google Earth; transitions between line segments may require smoothing for modelling

## Nature and units of recorded values

- Shapefiles contain the centrelines of watercourses and use the coordinate system EPSG:32644 (UTM Zone 44N)
- Width_m attribute provides the width of watercourses in meters; watercourses are divided into segments to capture width variations
- Widths are provided with high precision for measurement convenience but should be treated as general indications rather than exact along the entire length

## Quality control

- Data integrity checked, including vertex connections and the indicated flow directions based on point ordering

## Details of data structure

- Data organized into separate shapefile folders per river basin:
  - CFLOOD_MundeniAru_StreamNetwork_utm
  - CFLOOD_MaduruOya_StreamNetwork_utm
  - CFLOOD_MiyangollaEla_StreamNetwork_utm
- Each shapefile contains a single attribute: Width_m (watercourse width in meters)