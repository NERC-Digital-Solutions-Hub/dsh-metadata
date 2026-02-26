# The UKCEH Land Cover Map for 2021

## Aim and scope
- User guide for UKCEH Land Cover Map 2021 (LCM2021), the ninth UK land cover map.
- LCM2021 comprises six geospatial datasets: three for Great Britain and Northern Ireland each (GB and NI) including a 10 m classified-pixel dataset, a classified land parcel dataset, and a 25 m pixel rasterised land parcel dataset.
- Purpose is to enable informed use by providing production, validation, accuracy details and guidance on applications, limitations, and data governance.

## Data product suite (structure and contents)
- 10 m Classified Pixel datasets (GB and NI): mosaicked classifications from Classification Scenes; first band = UKCEH Land Cover Class; second band = class membership probability/confidence.
- Land Parcel datasets (GB and NI): derived by intersecting 10 m pixels with the UKCEH Land Parcel Spatial Framework; include parcel-level attributes and statistics.
- 25 m Rasterised Land Parcel datasets (GB and NI): raster version of land parcels with three bands (dominant class, confidence, purity).
- 1 km Summary rasters (GB and NI): 1 km dominant class and percentage cover products, summarising 25 m data into 1 km pixels.
- Official dataset names and metadata are provided in Appendix 3; coordinates and extents are specified per region.

## Datasets, structure, and provenance
- GB and NI cover the same three dataset types, yielding a total of six datasets.
- Coordinate systems: GB = British National Grid (EPSG 27700); NI = Irish Grid (TM75, EPSG 29903).
- Land Parcel Spatial Framework: minimum mapping unit (MMU) of ~0.5 ha; parcels are designed to reflect discrete real-world units and reduce classification noise.
- Bootstrap Training: automatic training approach using historic LCMs (LCM2018–LCM2020) with >80% purity to generate training data for current classification, reducing need for new field data.
- Random Forest classification: balanced training with 10,000 samples per class per Classification Scene; uses Bagging to classify 50-band Classification Scenes.
- Seasonal Composite Images: derived from Google Earth Engine using Sentinel-2 data resampled to 10 m; four seasonal composites (Jan–Mar, Apr–Jun, Jul–Sep, Oct–Dec) with 10 spectral bands; occasional cloud gaps are accommodated.
- Context Rasters: 10 GB context rasters (terrain, distance to buildings/roads/coast/freshwater, foreshore, tidal water, woodland); NI includes urban mask and proximity layers.
- Classification Scenes: GB classified in 32 tiles of ~100 x 100 km; NI uses a single scene; scenes include 50-band inputs (Seasonal + Context).

## Data production, validation, and accuracy
- Production goal: annual updates to maximize temporal consistency, comparability and change-detection potential.
- Validation: 35,182 validation points across all 21 classes; composite reference data from GB countryside survey, National Forest Inventory, Rural Payment Agency data, and manual/field validation.
- Overall accuracy: 82.6% with 95% confidence interval 82.19%–82.99%.
- Validation is performed against the 25 m Rasterised Land Parcel dataset; the 10 m Classified Pixel product was not directly validated against the parcel framework.
- Class-level performance varies (see Appendix 4 confusion/producer’s/user’s accuracy matrices); some known challenges include spectral confusion among certain habitats (e.g., bog, heath, mixed grasslands) and coastal/marine interfaces.
- Appendix 4 provides detailed confusion matrices and producer’s/user’s accuracy by UKCEH Land Cover Class.

## Class relationships and interpretation
- UKCEH 21 Land Cover Classes are aligned with, but not identical to, UK BAP Broad Habitats (BAP); some deviations exist due to historical mapping goals.
- When referring to UK BAP Broad Habitats, formatting and italicization are used to reduce ambiguity.
- Appendix 1 and Appendix 2 provide detailed notes on class definitions, common spectral/confusion issues, and crosswalks to BAP Broad Habitats.

## Data interpretation, usage notes, and display
- The 10 m pixel product preserves fine-scale features not generalized to the Land Parcel framework; intended for specialist users aware of the implications for validation and interpretation.
- Temporal dimension: annual maps help distinguish random classification noise from real land-cover change; real changes persist over time while random errors “flicker” year to year.
- The product is designed to support monitoring of state and change in the UK countryside and to underpin environmental objectives.
- Display: Appendix 5 and Appendix 6 provide recommended color recipes (standard and color-blind-friendly) for visualising UKCEH Land Cover Classes; accompanying QGIS symbology files are provided.

## Data governance, access, and documentation
- Methodologies, validation, and class definitions are documented to support governance and reproducibility (including references to relevant literature and internal UKCEH reports).
- Bootstrap Training and RF classification rely on open-source tools (Weka, PostGIS, GDAL) integrated via bespoke UKCEH software.
- The UKCEH Land Parcel Spatial Framework and dataset identifiers may change across versions (gid identifiers updated since LCM2015), affecting cross-version parcel comparison based on IDs rather than spatial overlap.
- Appendix 3 lists the complete dataset catalog for LCM2021; Appendix 4 contains correspondence/confusion matrices; Appendices 5–6 supply visualization resources.

## Practical considerations for data stewards
- Plan for annual data updates; document methodology changes and dataset versioning to maintain data lineage.
- Use the 25 m rasterised land parcel dataset for cross-comparisons with parcel-based analyses; exercise caution when comparing to the 10 m Classified Pixel dataset due to differences in validation scope and spatial generalisation.
- Be mindful of the MMU and the fixed spatial framework when aggregating or comparing across scales (10 m vs 25 m vs 1 km).
- Leverage the provided color recipes and QGIS symbology to ensure consistent visualization and communication of land cover classes.
- Reference Appendix 4 for class-specific accuracy and confusion patterns to inform uncertainty assessments in downstream analyses.