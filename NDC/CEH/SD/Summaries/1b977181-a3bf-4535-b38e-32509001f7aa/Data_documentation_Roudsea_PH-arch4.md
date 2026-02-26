# Dataset Documentation

## Overview
- Documentation for the dataset "Soil pH at Roudsea Wood National Nature Reserve 1961".
- Describes soil pH measurements taken in August 1961 at Roudsea Wood, Cumbria, England.
- Aims to capture spatially-referenced soil pH data to support ecological and woodland research.

## Dataset Details
- Geographic Coverage: Roudsea Wood, Cumbria, England (SD347807); western side of the reserve.
- Time Period: August 1961.
- Data Categories:
  - Soil pH from samples along transects (mean pH values from points along transects).
  - Soil pH from under oak trees (single spot pH samples under oaks).
- Originator Details: A. Carlisle, Woodlands Research Section, The Nature Conservancy, Merlewood Research Station, Cumbria.
- Background: Routine soil pH measurements conducted after reserve acquisition (1955). Original map later digitised (ArcMap) by Centre for Ecology & Hydrology, Lancaster.

## Methods and Provenance
- Experimental Design:
  - Samples collected from 5–10 cm depth.
  - Transect samples: mean pH from 3 samples per point.
  - Under oak trees: single spot pH sample.
  - pH determined from fresh soil using a 1:2 soil-to-water mixture with a glass electrode (standard practice of the time).
- Map and Digitisation:
  - Original map at 1:25,000 scale (enlarged) used for digitisation.
  - Points recorded with OSGB 1936 coordinates; spatial accuracy estimated to likely be within <50 m.
  - Data later stored as ESRI Shapefile by CEH Lancaster.

## Data Structure and Content
- File Format: ESRI Shapefile (Roudsea_soil_pH_1961.shp).
- Attributes/Columns:
  - pH: numeric pH value for each sample.
  - TYPE: categorical indicating sample type (TRANSECT for mean pH along transects; UNDER OAK for oak-under pH).
  - Point_X: OSGB 1936 Easting (metres).
  - Point_Y: OSGB 1936 Northing (metres).
- Coverage Note: Samples cover the western side of the reserve.

## Data Quality and Limitations
- Quality Information: Not fully recorded regarding sampling quality beyond the noted checks.
- Sample Handling: Samples were not retained; only recorded pH values.
- Data Entry/Validation: Values have undergone range checks and been cross-checked against the original map.

## Spatial Information
- Coordinate Reference System: OSGB 1936.
- Spatial Accuracy: Likely within 50 m, though exact accuracy is not documented.
- Granularity: Transect points provide mean pH values; oak-under samples are single-point measurements.

## Data Access and Reuse
- Data Asset: Soil pH measurements from 1961, digitised into a shapefile for inclusion in GIS analyses.
- Origin/Custodian: Nature Conservancy (now CEH Lancaster) and associated Woodlands Research Section.
- Related Materials: Connected literature includes Carlisle & Brown (1965) on oak taxonomic status (for context on forest composition).

## Related Reading
- Carlisle, A., & Brown, A. H. F. (1965). The assessment of the taxonomic status of mixed oak (Quercus spp.) populations. Watsonia, 6(2), 120-127.