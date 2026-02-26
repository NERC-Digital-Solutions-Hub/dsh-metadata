# Soil pH at Roudsea Wood National Nature Reserve 1961

## Overview
- Dataset documenting soil pH measurements from 5–10 cm depth at Roudsea Wood, Cumbria, England (August 1961).
- Purpose: support environmental monitoring and assessment of soil chemistry within the reserve.

## Data collection and scope
- Geographic coverage: Roudsea Wood, Cumbria (SD347807), western side of the reserve.
- Data categories:
  - Soils pH from transect samples (mean pH per point).
  - Soil pH from under oak trees (single spot sample).
- Experimental design: transect samples provide mean pH from multiple samples; under oak samples are single measurements.
- Depth: 5–10 cm.
- Time period: August 1961.
- Data origin: routine measurements by the Woodlands Research Section of The Nature Conservancy at Merlewood Research Station.

## Methods and provenance
- pH determination: fresh soil in a 1:2 soil:distilled water mixture using a glass electrode, following standard practice of the time.
- Map-to-digital process: original paper map (scale 1:25,000, enlarged) digitised into a shapefile; Centre for Ecology & Hydrology, Lancaster, archived the legacy map and digitised points.
- Spatial accuracy: likely within 50 meters; exact accuracy not precisely recorded.

## Data quality and limitations
- Quality information on sampling is not on record; samples were not retained.
- Data entry: pH values range-checked and cross-verified against the original map.
- No accompanying metadata on sampling protocols beyond described methods.

## Dataset structure and file details
- File: Roudsea_soil_pH_1961.shp (ESRI Shapefile).
- Columns:
  - pH: soil pH value.
  - TYPE: sample type (TRANSECT or UNDER OAK).
  - Point_X: OSGB 1936 Easting (metres).
  - Point_Y: OSGB 1936 Northing (metres).

## Geographical and contextual notes
- OS grid coordinates (OSGB 1936) used; spatial points correspond to the western side of Roudsea Wood.
- Related reading: Carlisle, A., & Brown, A. H. F. (1965). The assessment of the taxonomic status of mixed oak (Quercus spp.) populations. Watsonia, 6(2), 120–127.

## Access, storage, and provenance
- Original map stored at the Centre for Ecology & Hydrology, Lancaster; digitised points stored as an ESRI shapefile.
- Dataset lineage: initiated by A. Carlisle (Nature Conservancy) with later digitisation by CEH/Lancaster.