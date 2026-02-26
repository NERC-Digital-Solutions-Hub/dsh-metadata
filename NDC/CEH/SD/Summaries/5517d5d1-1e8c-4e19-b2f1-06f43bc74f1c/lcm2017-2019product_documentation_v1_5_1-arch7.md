# The UKCEH Land Cover Maps for 2017, 2018 and 2019

- A user guide accompanying the release of three UKCEH land cover maps: LCM2017, LCM2018, and LCM2019.
- Maps cover 21 UKCEH Land Cover Classes (based on Biodiversity Action Plan Broad Habitats) and are produced automatically using Bootstrap Training and Random Forest classification.
- Aim is rapid, UK-wide annual land cover mapping with ongoing validation and documentation to aid informed use.

## Key goals and scope
- 21-class land cover framework aligned with LCM2015 and related to BAP Broad Habitats.
- Automatic production without manual accuracy corrections in this cycle; visual checks and formal validation still performed.
- Validation indicates maps are of similar quality to the latest predecessor (LCM2015), with around 78–79% overall accuracy across 2017–2019 using UK-scale validation data.
- Organization of data supports change detection and cross-year comparisons, with notes on class derivation and potential ambiguities.

## Data structure and geographical scope

- Dataset structure: for each year (2017, 2018, 2019) there are 42 datasets split across Great Britain (GB) and Northern Ireland (NI).
- Data products and resolutions include:
  - 20m Classified Pixels (new addition): per-pixel RF classifications with two bands (Band 1 = most likely class; Band 2 = classification Confidence 0–100).
  - Land Parcels: derived by intersecting 20m Classified Pixels with the UKCEH Land Parcel Spatial Framework; includes parcel-level attributes.
  - 25m Rasterised Land Parcels: summarised from Land Parcels into 25m rasters with 3 bands (Mode, Confidence, Purity).
  - 1km Raster datasets (intermediate aggregation):
    - 1km Percent Cover (21-band)
    - 1km Percent Aggregate Cover (10-band)
    - 1km Dominant Cover (1-band)
    - 1km Dominant Aggregate Cover (1-band)
- GB vs NI specifics:
  - GB: Classification Scenes built from overlapping 100x100 km tiles; 46-band GB Classification Scenes (36 spectral bands + 10 context layers).
  - NI: Single tile per year; 43-band Classification Scene (36 spectral + 7 context layers).
- A total of 42 datasets per year (GB + NI), with a complete list provided in Appendix 5.

## Production methodology

- Seasonal data and inputs:
  - Sentinel-2 Seasonal Composite Images (TOA reflectance, median per season; four seasons) at 20m resolution.
  - Seasons: winter, spring, summer, autumn; some gaps due to cloud.
  - Seasonals combined with 20m Context Rasters to form Classification Scenes.
  - Data originally considered Surface Reflectance (SR) but TOA was used for this production cycle; plan to review future inputs.
- Bootstrapping and training:
  - Bootstrap Training: automatic sampling of training observations from historic UKCEH maps (predominantly LCM2015) to train the RF classifier.
  - Strategy uses majority signal across years and aims to minimize manual data gathering.
- Classification:
  - Random Forest classifier trained with balanced sampling (10,000 samples per class) from Bootstrap Training data.
  - Software stack: bespoke UKCEH pipeline integrating Weka, PostGIS, and GDAL (open source).
- Contextual disambiguation:
  - 20m Context Rasters provide terrain, proximity, and land-use context to reduce spectral confusion (e.g., height, slope, distance to buildings/roads/coast/freshwater; urban foreshore; woodland presence).
- UKCEH Land Parcel Spatial Framework:
  - Used to generalise 20m Classified Pixels into land parcels (~0.5 ha MMU); framework preserved for comparability with later products, though parcel identifiers (gid) do not match LCM2015 exactly.
- Land parcel and raster products:
  - Land Parcels summarize 20m pixels within each parcel (attributes include hist, mode, purity, conf, stdev, n).
  - 25m Rasterised Land Parcels convert parcel attributes into a 25m raster with three bands (mode, conf, purity).
  - 1km rasters aggregate parcel-level data into broader grids (percent cover, percent aggregate cover, dominant cover, dominant aggregate cover).
- Validation approach:
  - UK-scale validation using GB countryside survey data (2019), National Forest Inventory, IACS, and bespoke LCM validation points (22,325 total points).
  - Reported overall accuracy around 78.6–79.6% across 2017–2019; notes that validation is not absolute truth and validation data differ in purpose.

## Datasets and products: what’s inside

- 20m Classified Pixels
  - 2-band raster per year: band 1 = most likely UKCEH Land Cover Class; band 2 = class membership probability (0–100) for confidence.
  - Preserves fine landscape detail (e.g., narrow features) not present in later parcel-based products.
- Land Parcels
  - Parcel-level attributes linked to 20m classified pixels; updated metadata vs LCM2015; includes histogram representation of pixel class counts within each parcel.
  - gid remains stable, but new parcel identifiers are not guaranteed to match LCM2015.
- 25m Rasterised Land Parcels
  - 3-band raster: mode, conf, purity; designed to provide a compact, landscape-wide summary with richer confidence than earlier two-band rasters.
- 1km Raster Products
  - 1km Percent Cover (21-band)
  - 1km Percent Aggregate Cover (10-band)
  - 1km Dominant Cover (1-band)
  - 1km Dominant Aggregate Cover (1-band)
- Seasonal Composite Images and Classification Scenes
  - GB: 74 overlapping 100x100 km GB Classification Scenes (36 spectral bands + 10 context layers; total ~46 bands per scene).
  - NI: Single 43-band Classification Scene per year (36 spectral + 7 context).
  - Scenes are processed independently and overlapped to ensure balanced training data; visual checks guide final precedence in overlaps.
- Colour and documentation
  - Appendix 3 provides a recommended RGB color recipe for displaying the 21 UKCEH Land Cover Classes.
  - Appendix 1–2 provide notes on the UKBAP Broad Habitat definitions and class derivations to aid interpretation and crosswalks.

## Validation, accuracy, and caveats

- Validation framework:
  - Cross-year validation using independent datasets and bespoke validation points; results presented as overall accuracy by class and producer/user accuracy metrics.
- Key caveats:
  - Approximately 80% agreement across 21-class maps when compared to validation data; some classes exhibit lower producer accuracy (e.g., Heather grassland, Acid grassland) due to spectral ambiguity and training data limitations.
  - Validation data originate from datasets with different purposes and class schemes; conversions introduce subjectivity.
  - No manual accuracy corrections were applied for these annual maps to enable rapid production; automated classifications may generate detectable but non-systematic errors that should persist for real change detection.

## Appendices and notable references

- Appendix 1: Notes on UKCEH Land Cover Classes (class-level interpretations and spectral/detection caveats for each class).
- Appendix 2: Biodiversity Action Plan (BAP) Broad Habitats (definitions and cross-walk to UKCEH classes).
- Appendix 3: RGB colour recipe for displaying the 21 UKCEH Land Cover Classes.
- Appendix 4: Validation details, confusion matrices, producer’s and user’s accuracies by class (for 2017–2019 validation points).
- Appendix 5: Full list of datasets for LCM2017, LCM2018, and LCM2019 (dataset names and scope, GB vs NI).
- References: Key literature for Random Forest, Bootstrap Training, Sentinel-2 processing, and UK land cover methodologies.

## Data formats, scales, and coordinate systems

- GB datasets: Great Britain – British National Grid (EPSG: 27700).
- NI datasets: Northern Ireland – Irish Grid (TM75, EPSG: 29903).
- Pixel/grid specifications:
  - 20m Classified Pixels: primary per-pixel product.
  - 25m Rasterised Land Parcels: parcel-derived raster with 25m pixels.
  - 1km rasters: aggregated products for broad-area analyses.
- Data access and structure:
  - Each year’s suite contains GB and NI datasets; overall product suite is designed to support change detection and multi-year analyses.

## Future directions and planning

- Annual LCM releases continue (aim to maintain yearly updates).
- Potential enhancements include expanding input satellite data, exploring additional sources (e.g., Sentinel-1), and refining Bootstrap Training with newer year signals.
- Ongoing work to improve training data diversity and validation resources to raise overall accuracy in future deployments.