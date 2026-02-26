# The UKCEH Land Cover Map for 2021

- Purpose and scope
  - UKCEH LCM2021 is the ninth UK land cover map, produced annually, to monitor environmental state and change.
  - Product comprises six geospatial datasets (split across Great Britain and Northern Ireland): three for each region (10 m classified pixels, land parcels, and 25 m rasterised land parcels), plus 1 km raster products derived from the 25 m data.
  - Formal validation reports an overall accuracy of 82.6% at full thematic detail (95% CI 82.19%–82.99%).

- UKCEH Land Cover Classes and BAP relationship
  - The map uses 21 UKCEH Land Cover Classes (aligned with Biodiversity Action Plan Broad Habitats, but not identical to BAP). 
  - Some BAP/Broad Habitat mappings are split or merged to suit satellite-based classification; appendices provide definitions and crosswalk details.
  - Relationship information is provided to aid interpretation and comparability with earlier products.

- Data production and technical approach
  - Data sources and inputs
    - Seasonal Composite Images derived from Sentinel-2, combined with 10 Context Rasters (terrain, proximity to features, etc.) to reduce spectral confusion.
    - Seasonal data cover four periods (Jan–Mar, Apr–Jun, Jul–Sep, Oct–Dec) with some cloud-caused gaps managed by the classifier.
  - Classification and training
    - Bootstrap Training: an automatic, iterative training approach that uses historic LCM maps (LCM2018–LCM2020) to generate training data without new field campaigns.
    - Random Forest classifier trained on bootstrapped samples to assign per-pixel land cover classes.
    - Training data are balanced across classes by sampling with replacement; to counter class imbalance and improve detection of rarer classes.
  - Spatial framework and data structure
    - UKCEH Land Parcel Spatial Framework used to generalise features and create land parcels (~0.5 ha minimum) to stabilise change detection.
    - 10 m classified pixels preserve detailed features; 25 m rasters represent the parcel framework with three bands (dominant class, confidence, purity).
    - Acknowledgement that 10 m pixels were not validated against the parcel dataset; users should be aware of this when interpreting fine-scale outputs.
  - Validation and accuracy
    - Validation used 35,182 reference points covering all 21 classes, drawn from GB countryside surveys, National Forest Inventory, Rural Payments data, and bespoke validation points.
    - Overall accuracy: 82.6% (95% CI 82.19%–82.99%).
  - Reproducibility and software
    - Custom UKCEH pipeline integrating Weka (machine learning), PostGIS, and GDAL; designed for automated, repeatable processing.

- Datasets and outputs (GB and NI)
  - 10 m Classified Pixel datasets
    - Pixel-level class assignment with two bands: UKCEH Land Cover Class ID and the associated class probability/confidence.
    - Not generalised by the Land Parcel Spatial Framework to preserve fine-scale features; intended for specialist users who understand the implications of classification confidence.
  - Land Parcel datasets
    - Result from intersecting 10 m classified pixels with the UKCEH Land Parcel Spatial Framework.
    - Include per-parcel attributes (gid, hist, mode, conf, stdev, agg, n, etc.) and a crosswalk to UKCEH and UK BAP Broad Habitats.
  - 25 m Rasterised Land Parcel datasets
    - Rasterised version of parcels at 25 m with three bands: per-parcel dominant class (_mode), mean confidence (_conf), and purity (_purity).
  - 1 km raster products
    - Summaries derived from 25 m data: dominant class per 1 km pixel (21-band and 10-band aggregations) and percentage cover per class and per aggregate class.
    - Percentage outputs are integer values and may not sum exactly to 100 due to rounding; coastal pixels may sum to less than 100 due to mapping extent.
  - Seasonal Composite Images
    - Sentinel-2 derived, resampled to 10 m; four seasonal composites used to train and classify; occasional gaps in data handled by the classifier.
  - Context Rasters
    - 10 m context layers to resolve spectral confusion (e.g., terrain, proximity to buildings/roads/coast, water bodies, urban masks, etc.) for GB and NI.
  - Classification Scenes
    - GB: grid of classification tiles (~100 x 100 km) processed as 50-band scenes; NI: single 49-band scene for full NI extent.
  - Coordinate systems and extents
    - GB: British National Grid (EPSG: 27700); NI: Irish Grid (TM75, EPSG: 29903).
    - GB/NI parcel counts and extents differ; parcel identifiers (gid) do not match across LCM2015 to LCM2021, affecting exact cross-year parcel-id comparisons.

- Practical use and interpretation for environmental monitoring
  - Temporal monitoring and change detection
    - Annual production enhances ability to distinguish real land cover change from random classification errors (errors tend to flicker year-to-year).
  - Data comparability and continuity
    - Aims for temporal consistency and comparability across years; potential re-application of improved methods across the catalog to maximise consistency.
  - Data handling and caveats
    - 10 m classified pixels retain finer details but lack parcel-level generalisation; formal validation was performed on the 25 m raster parcel dataset.
    - When conducting longitudinal analyses, use parcel-level outputs for stable units; be cautious with pixel-level outputs and cross-year parcel identifiers.
  - Accessibility and dissemination
    - Datasets are stored and uploaded to appropriate portals; intended to support a broad range of environmental objective assessments and decision-making.

- How this supports the Analysts Monitoring the Environment archetype
  - Delivers a standardised, reproducible, and auditable data product for environmental health and change assessment over time.
  - Combines high-resolution classification with robust spatial frameworks and parcel-based change detection units.
  - Provides both detailed, pixel-level outputs and higher-level parcel and 1 km summaries to support diverse analytical needs.
  - Includes documentation on data provenance, validation, class definitions, and crosswalks to aid interpretation and long-term monitoring.

- Additional notes
  - Methods are evolving; if new methods yield significant accuracy improvements, UKCEH will consider re-applying across the entire catalog to maximise temporal comparability.
  - Appendix materials offer in-depth definitions of UKCEH Land Cover Classes and their BAP Broad Habitat counterparts, including nuances, potential confusions, and guidance for interpretation.