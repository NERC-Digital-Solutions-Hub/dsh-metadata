# The UKCEH Land Cover Map for 2021

- LCM2021 provides annual, standardized UK land-cover data to support environmental monitoring, policy evaluation, and decision-making.
- Outputs span Great Britain and Northern Ireland, enabling state-and-change analysis and aiding change-detection over time.

## Purpose and Monitoring Context

- Designed to help identify environmental health measures and inform future policy decisions.
- Aims to maximize temporal consistency and interpretability of change by offering annual maps.
- Emphasizes distinguishing real land-cover change from random classification errors as series matures.
- Formal validation reports an overall accuracy of 82.6% at full thematic detail (95% CI 82.19%–82.99%).

## Data Products and Coverage

- LCM2021 comprises six geospatial datasets in total (three per region: GB and NI):
  - 10 m Classified Pixel datasets
  - Land Parcel datasets (within the UKCEH Land Parcel Spatial Framework)
  - 25 m Rasterised Land Parcel datasets
- Additional derived products include 1 km summaries:
  - Dominant cover and percentage cover products for 1 km x 1 km pixels (both class-based and aggregate-class-based).
- Coordinate systems:
  - Great Britain: British National Grid (EPSG 27700)
  - Northern Ireland: Irish Grid TM75 (EPSG 29903)
- Land mass extents and parcel counts:
  - GB parcels: ~6.74 million
  - NI parcels: ~0.90 million
- Class framework:
  - 21 UKCEH Land Cover Classes, linked to Biodiversity Action Plan (BAP) Broad Habitats (with careful notes on non-identical mappings).

## How the UKCEH Built LCM2021

- Seasonal data foundation:
  - Seasonal Composite Images from Sentinel-2 (10-band spectral data) at 10 m resolution, aggregated into four seasons.
  - Seasonal data complemented by 10 Context Rasters to reduce spectral confusion.
- Contextual information:
  - GB Context Rasters include terrain (Height, Aspect, Slope), proximity measures (distance to buildings/roads/coast/freshwater), foreshore and tidal water masks, and woodland mask.
  - NI Context Rasters include terrain plus urban mask and distance-to-coast/freshwater/road layers, plus foreshore and tidal masks.
- Classification framework:
  - Classification Scenes: GB classified in 32 tiles (based on a modified OS 100 x 100 km grid); NI uses a single scene determined by the NI land-mass extent.
  - Bootstrap Training: automatically generated training data from historic LCMs (LCM2018–LCM2020) filtered for >=80% purity and consistent class across years.
  - Random Forest: trained with balanced sampling (10,000 samples per class per bag) to produce the 10 m Classified Pixel dataset; probability/confidence scores accompany class IDs.
- Land Parcel Spatial Framework:
  - Parcels (~0.5 ha minimum MMU) derived from generalised national cartography; provide fixed units to reduce classification noise and aid change detection.
  - 10 m classified pixels are aggregated into land parcels for parcel-level attributes and cross-year comparisons.
- Validation strategy:
  - 35,182 validation points from GB/Northern Ireland data sources, including fieldwork and interpretation-based points.
  - Validation dataset intersects with 25 m rasterised parcel data to determine correspondence.

## Practical Data Details and Access

- 10 m Classified Pixel dataset:
  - Retains fine landscape features (e.g., narrow patches) by not generalising with the Land Parcel Framework.
  - Not formally validated against the Land Parcel dataset; targeted at specialist users aware of this limitation.
- 25 m Rasterised Land Parcel dataset:
  - Provides three-attribute rasters per parcel: dominant land cover (mode), mean confidence (_conf), and purity (_purity).
- 1 km products:
  - Summaries of 25 m rasters to provide dominant class and percentage cover per 1 km pixel, with rounding that may cause sums to deviate slightly from 100%.
- Data governance and openness:
  - Outputs are designed for broad dissemination with emphasis on data quality, metadata, and governance; underlying data sharing is facilitated to support transparency, though some barriers may arise in practice.

## UKCEH Land Cover Classes and BAP Relationships

- The 21 UKCEH Land Cover Classes were developed to align with BAP Broad Habitats but are not exact equivalents.
- Appendices detail nuanced relationships and mappings, including cases where a single UKCEH class represents multiple BAP broad habitats or where splits are applied (e.g., Heather vs. Heather Grassland; Urban vs. Suburban).
- The relationship table and appendices emphasize careful interpretation when translating between land-cover classes and BAP habitat designations.

## Methodological Highlights

- Bootstrap Training:
  - Uses historic, wall-to-wall maps as a cost-effective training data source for current classification.
  - Ensures broad coverage and large training samples, balancing class representation via sampling with replacement.
- Random Forest classification:
  - Classifies 50-band Classification Scenes with RF, generating both class membership and associated probability/confidence metrics.
  - The UKCEH pipeline uses open-source tools (WEKA, PostGIS, GDAL) integrated in a bespoke workflow.
- Seasonal and Context data integration:
  - Seasonal bands provide phenological information to improve discrimination of vegetation types.
  - Context rasters help resolve spectral confusion (e.g., bare rock vs. urban surfaces).
- Classification Scene design:
  - GB mapped with 32 tiles to manage processing and local phenology; NI uses a single scene due to smaller area.
- UKCEH Land Parcel Spatial Framework:
  - Maintains consistent, discrete land units for temporal comparison and change detection.
  - Acknowledges that parcel IDs do not directly match LCM2015 IDs due to pipeline changes.

## Validation and Accuracy in Practice

- Validation dataset comprises 35,182 points from diverse sources, intersected with 25 m rasterised parcel data.
- Reported overall accuracy: 82.6% with 95% confidence interval 82.19%–82.99%.
- Appendix A–D (noted in the document) provide detailed confusion matrices and producer/user accuracy by class, illustrating common misclassifications and reliability across classes.

## Guidance for Monitoring Framework Use

- What it enables:
  - State-and-change monitoring at multiple scales (10 m pixel detail; 25 m parcels; 1 km summaries).
  - Clear, auditable data lineage from seasonal imagery to final land-cover class.
  - Change detection opportunities across annual maps, aided by the assumption that most errors are random.
- What to watch:
  - 10 m Classified Pixels: high detail but not cross-validated against Land Parcel framework; use with caution for parcel-level decision-making.
  - 25 m Parcel-derived attributes: robust for parcel-based analysis and time-series containment, with explicit metrics (_conf, _purity).
  - 1 km summaries: suitable for broad policy indicators and landscape-scale monitoring; rounding may affect strict total consistency.
  - Coastal and near-coastal areas require careful interpretation due to potential Saltwater/Freshwater misclassification near tidal zones.
- Data governance implications:
  - The framework supports data sharing and reproducibility, with explicit metadata and documentation; ensure alignment with internal data governance standards when integrating into monitoring dashboards or policy reports.

## Appendices at a Glance (for Context and Implementation)

- Appendix 1: Notes on UKCEH Land Cover Classes (class definitions and field of view for training and mapping).
- Appendix 2: Biodiversity Action Plan (BAP) Broad Habitats (definitions and alignment notes; color coding notations).
- Appendix 3: Full list of LCM2021 datasets (GB and NI, with dataset names and citations).
- Appendix 4: Correspondence matrices (detailed class-by-class confusion and accuracy metrics; producer/ user accuracy per class).
- Appendix 5–6: Colour recipes for displaying UKCEH Land Cover Classes (standard and color-blind friendly palettes).