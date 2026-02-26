# The UKCEH Land Cover Map for 2022

## Overview and Purpose
- User guide for the UKCEH Land Cover Map 2022 (LCM2022), the tenth national land cover map.
- LCM2022 comprises seven geospatial datasets (GB and NI), plus a 1 km summary raster product covering GB and NI.
- Purpose is to enable informed use of LCM2022 data, describing data production, validation, and data accuracy to support decision-making.

## Data Products and Structure
- Datasets (three per Great Britain and Northern Ireland, plus a 1 km summary product):
  - 10 m Classified Pixel datasets (GB and NI): automatic classification of land cover from Classification Scenes; first band = most likely UKCEH Land Cover Class, second band = classification confidence/probability.
  - Land Parcel datasets (GB and NI): derived by intersecting 10 m pixels with the UKCEH Land Parcel Spatial Framework.
  - 25 m Rasterised Land Parcel datasets (GB and NI): rasterised parcels with three bands per parcel: dominant land cover mode, confidence, and purity.
  - 1 km summary rasters (GB and NI): dominant class per 1 km pixel and percentage cover for classes (21 class bands for classes; 10 bands for aggregates); values are integers and may not sum to exactly 100 due to rounding.
- Classification framework:
  - 10 m pixels produced from Classification Scenes composed of Sentinel-2 Seasonal Composite Images plus Context Rasters.
  - 32 GB Classification Scenes; NI uses a single Classification Scene.
  - 1 km products are derived by aggregating 25 m rasters.
- Seasonal and contextual inputs:
  - Seasonal Composite Images: four-season Sentinel-2 data (January–March, April–June, July–September, October–December).
  - Context Rasters: 10 m layers (terrain, proximity to buildings/roads/water, foreshore, woodlands, etc.) to reduce spectral confusion.
- Geographic scope and formats:
  - GB: British National Grid (EPSG: 27700).
  - NI: TM75 Irish Grid (EPSG: 29903).
  - Parcel counts: GB ~6.74 million parcels; NI ~0.90 million parcels.
  - Pixel resolutions: 10 m (both GB and NI) and 25 m rasterised parcels; 1 km summary rasters (GB+NI).
- Datasets have official DOIs for citation; see Table of DOIs in the document.

## Data Production, Methodology, and Validation
- Bootstrap Training:
  - Automatic training data generation using historic LCMs (2019–2021) to sample current imagery.
  - Pixels with >80% probability and consistent class across three years are used for training.
  - Aims to minimize need for new field data while supporting rapid map updates.
- Random Forest Classification:
  - RF classifier trained on Bootstrap Training samples; 10,000 samples per bag with replacement to balance class representation.
  - Produces the 10 m Classified Pixel dataset (class ID and confidence per pixel).
- Seasonal and Context Integration:
  - Seasonal signals and contextual information used to differentiate spectrally similar land covers.
- Validation and Accuracy:
  - Formal validation using 33,107 reference points across all 21 LCM classes.
  - Overall accuracy: 86.1%.
  - Validation draws from GB countryside survey, National Forest Inventory data, Rural Payments data, and bespoke validation points.
- Known Issues:
  - A small number of polygons missing from vector land parcel products (affects 25 m rasterised parcels slightly; 10 m classified pixels are unaffected).
  - Some inter-class confusion remains (notably among peatland, bog, heather, fen, and related upland classes) due to spectral similarity and historical class definitions.
- Methodology notes:
  - Methods are continuously evolving; future significant improvements may be reapplied across the catalogue to maximise temporal consistency and change detection.

## Data Framework, Standards, and Accessibility
- UKCEH Land Parcel Spatial Framework:
  - MMU ~0.5 ha; parcels derived from generalized national cartography to represent discrete land units (fields, parks, urban areas, etc.).
  - Parcel identifiers (gid) may not match LCM2015 when comparing by parcel ID due to framework changes.
- Data Management:
  - 10 m Classified Pixels preserve detailed landscape features (not generalized to the Land Parcel Spatial Framework).
  - Land Parcel products provide a fixed, time-series-friendly structure for change detection.
- Metadata and Citations:
  - Each LCM2022 dataset has a DOI; recommended citation includes Marston et al. (2024) references for the data products.
  - Users are encouraged to cite the relevant DOI for the specific product (10 m Classified Pixels, 25 m Rasterised Land Parcels, Land Parcels, 1 km Summary rasters).
- Documentation and Appendices:
  - Appendix 1 and 2 outline UKCEH Land Cover Classes and their relationship to Biodiversity Action Plan (BAP) Broad Habitats.
  - Appendix 3 lists the full dataset catalog and DOIs.
  - Appendix 4 provides correspondence matrices detailing classification accuracy across classes.
  - Appendix 5 and 6 provide color recipes (standard and color-blind friendly) and accompanying QGIS symbol files.

## Data Quality, Limitations, and Cautions
- Validation indicates an 86.1% overall accuracy at full thematic detail.
- Known issues are minor but possible: occasional missing vector land parcel polygons; method changes can cause apparent differences year-to-year beyond real land-cover change.
- Temporal consistency is enhanced by annual mapping, aiding separation of real change from classification noise; random errors are expected to flicker over time.

## Implications for Data Leaders (How to Use and Govern)
- Strategic value:
  - Provides a rich, annually updated time series for monitoring UK countryside state and change.
  - Facilitates change detection and supports environmental objectives through consistent data lineage and validation reporting.
- Governance and integration:
  - Use Bootstrap Training approach to minimize field-data requirements for future updates; ensure training data provenance is tracked.
  - Leverage multiple product scales (10 m, 25 m parcels, and 1 km summaries) for diverse analyses from granular to landscape-level.
  - Be aware of the GIS framework changes (gid identifiers) when comparing with earlier years or datasets.
- Data utilization practices:
  - Prefer 10 m Classified Pixels for detailed analyses; use 25 m parcel rasters for stable time-series comparisons; use 1 km rasters for broad-scale monitoring.
  - Incorporate Context Rasters and Seasonal Composite inputs to improve classification in spectral-confusion zones (coasts, urban, uplands).
  - Validate locally when applying to policy or regional planning by cross-referencing with other data sources and noting known classification ambiguities.
- Community and standards alignment:
  - Align with UKCEH’s ongoing improvements to maximise temporal comparability across the full catalogue.
  - Reference the provided appendices for consistent interpretation of land cover classes and their relationship to BAP Broad Habitats.

## Appendices and Additional Resources (Highlights)
- Appendix 1 & 2: Detailed notes on UKCEH Land Cover Classes and BAP Broad Habitats, including interpretation guidance and potential ambiguities.
- Appendix 3: Full list of LCM2022 datasets and DOIs.
- Appendix 4: Correspondence matrices (classification performance by class).
- Appendix 5 & 6: Colour recipes for visualizing land cover classes (standard and color-blind friendly) and associated QGIS symbol files (lcm_raster*.qml).