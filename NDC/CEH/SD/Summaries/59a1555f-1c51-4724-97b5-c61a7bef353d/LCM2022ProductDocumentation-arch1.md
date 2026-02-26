# The UKCEH Land Cover Map for 2022

## Purpose
- User guide for LCM2022, describing production, validation, and accuracy to help informed use.
- LCM2022 comprises seven datasets: three datasets for Great Britain and three for Northern Ireland (a 10 m classified pixels dataset, a land parcel dataset, and a 25 m rasterised land parcels dataset) plus a 1 km summary raster product covering both GB and NI.
- Emphasises understanding data structure and limitations to support current and future work.

## Datasets and Data Structure
- 10 m Classified Pixel datasets (GB and NI): per-pixel land cover classification with a second band indicating classification confidence.
- Land Parcel datasets (GB and NI): results of intersecting 10 m pixels with the UKCEH Land Parcel Spatial Framework to produce parcel attributes.
- 25 m Rasterised Land Parcel datasets (GB and NI): raster format of land parcels with three bands capturing dominant class, confidence, and purity.
- 1 km Summary rasters (GB and NI): dominant class rasters and percentage cover rasters summarised from 25 m data.
- UKCEH Land Cover Classes: 21 classes linked to Biodiversity Action Plan (BAP) Broad Habitats, with notes on cross-walk and ambiguities.
- Appendix 3 lists official dataset names; Appendix 5/6 provide color recipes for display.

## Data Production and Methods
- Classification Scene: Sentinel-2 Seasonal Composite Images (four seasons) combined with Context Rasters to reduce spectral confusion.
- Seasonal Composite Images: four seasonal midpoints, using 10 Sentinel-2 bands; occasional cloud gaps present but classification tolerates gaps.
- Context Rasters (10 m for GB; 10 m equivalents for NI): include terrain (height, aspect, slope) and proximity masks (distance to buildings, roads, tidal water, freshwater, foreshore, woodlands, saltmarsh, etc.).
- Bootstrap Training: automatic training using historic LCM maps (LCM2019, LCM2020, LCM2021) with pixels >80% probability and consistent class across years; used to generate training samples for RF.
- Random Forest Classification: balanced training (10,000 samples per bag) to yield 10 m classified pixels; employs bespoke UKCEH software integrating Weka, PostGIS, and GDAL.
- Classification Scenes: GB classified in 32 tiles; NI uses a single 49-band 40-band sentinel-based scene (with NI context rasters).
- The UK Land Parcel Spatial Framework: parcels of ~0.5 ha MMU derived by generalising national cartography; parcels provide a stable structure for change detection.
- Data Processing and Workflow: primarily open-source tools; RF-based classification with bootstrap approach to maintain temporal consistency.

## Validation and Accuracy
- Product validation used 33,107 reference points covering all 21 classes.
- Overall accuracy: 86.1% at full thematic detail.
- Validation dataset composed from countryside surveys, inventory data, and bespoke validation points.

## Known Issues and caveats
- Some land parcel vectors have missing polygons, causing nodata in 25 m raster parcels; negligible effect on 1 km products; 10 m pixels unaffected.
- 10 m classified pixels are not generalised by the Land Parcel Framework, preserving fine-scale detail not present in the 25 m parcel product.
- Training data limitations for certain classes (e.g., arable vs improved grassland) due to historical labeling; some distinctions rely on alternative sources.
- Saltwater classification can be less accurate than Freshwater; coastal water tendencies are influenced by coastal Context Rasters; occasional confusion with near-coast non-vegetated surfaces.
- Changes between maps may reflect both real land-cover change and methodological updates; annual maps aid change detection by distinguishing persistent changes from random errors.

## Access, citation, and references
- Each LCM2022 dataset has a DOI; table of DOIs and citations is provided (Table 5).
- References include Marston et al. (2023, 2024) for production methods and dataset-specific papers.
- Users are encouraged to cite the relevant dataset DOIs and Marston et al. where appropriate.

## Display and color conventions
- Appendix 5: Recommended color recipe for displaying UKCEH Land Cover Classes (with both standard and color-blind friendly versions in Appendix 6).
- QGIS symbology files (lcm_raster.qml and lcm_raster_cb_friendly.qml) provided to apply the recommended color schemes.

## Appendices – key context
- Appendix 1: Notes on UKCEH Land Cover Classes; guidance on interpretation and potential spectral confusion between classes.
- Appendix 2: Biodiversity Action Plan (BAP) Broad Habitats definitions and their relationship to UKCEH classes.
- Appendix 3: Full list of LCM2022 datasets with official names and DOIs.
- Appendix 4: Correspondence matrices (confusion and accuracy detail across classes; producer and user accuracy figures).
- Appendix 5 & 6: Display color schemes (standard and color-blind friendly) and associated QGIS files.