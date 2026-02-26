# Dataset Documentation

## Overview
- Dataset name: Soil pH at Roudsea Wood National Nature Reserve 1961
- Description: Soil pH values from samples taken at 5–10 cm depth along transects and from under oak trees in Roudsea Wood, Cumbria.
- Geographic coverage: Roudsea Wood, Cumbria, England (SD347807)
- Time period: August 1961
- Data categories: Soil pH from transect points (mean pH) and soil pH from under oak trees (single sample)
- Originator: A. Carlisle, Woodlands Research Section, The Nature Conservancy, Merlewood Research Station, Cumbria
- Format: ESRI Shapefile (Roudsea_soil_pH_1961.shp) with fields pH, TYPE, Point_X, Point_Y
- Spatial reference: OSGB 1936 (Eastings/Northings)

## Dataset Content and Structure
- Data fields:
  - pH: pH value of soil sample
  - TYPE: TRANSECT (mean pH from transect points) or UNDER OAK (spot pH under oak trees)
  - Point_X: OSGB 1936 Easting (metres)
  - Point_Y: OSGB 1936 Northing (metres)
- Sampling design:
  - Transect samples: mean of 3 samples per point
  - Under oak samples: single spot sample
- Data origin and digitisation:
  - Original paper map stored at Centre for Ecology & Hydrology, Lancaster; points digitised using ESRI ArcMap
  - Points recorded on a 1:25,000 map (enlarged); exact spatial accuracy not precisely known, likely <50 m
- Data entry quality:
  - Values range-checked and double-checked against the original map
  - No retention of original samples

## Methods and Provenance
- Experimental design: Soil samples collected across transects and under trees to assess pH
- Measurement method: pH determined from fresh soil using 1:2 soil-to-distilled-water mixture with a glass electrode
- Background: Part of ongoing Nature Conservancy soil studies at Roudsea Wood post-1955 acquisition as a National Nature Reserve

## Quality, Limitations, and Caveats
- Sampling metadata: Comprehensive quality notes about sampling are not on record
- Sample retention: Original soil samples were not kept
- Spatial accuracy: Exact accuracy unknown; digitised points likely within ~50 m
- Reuse considerations: Limited metadata on methodological details beyond the stated procedures; suitability best assessed for historical or geospatial analyses within the 1961 context

## Geographical Coverage
- Western side of Roudsea Wood, Cumbria (SD347807)

## Related References
- Carlisle, A., & Brown, A. H. F. (1965). The assessment of the taxonomic status of mixed oak (Quercus spp.) populations. Watsonia, 6(2), 120-127.