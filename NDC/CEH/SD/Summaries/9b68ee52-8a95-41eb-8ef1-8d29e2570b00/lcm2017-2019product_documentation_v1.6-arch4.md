# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.6 18/06/2020

- Purpose and scope
  - User guide for three UKCEH land cover maps: LCM2017, LCM2018, and LCM2019.
  - 21 UKCEH Land Cover Classes based on Biodiversity Action Plan (BAP) Broad Habitats; designed for near-continuous annual production.
  - Maps produced automatically using Bootstrap Training plus Random Forest classification, with Sentinel-2 Seasonal Composite Images and 20m context rasters.
  - Objective: enable informed use, validation, and planning around land cover change within a data-system perspective.

- Data products and structure
  - Product suite spans 42 datasets (GB and Northern Ireland), year-by-year.
  - Main dataset families and resolutions:
    - 20m Classified Pixels (GB and NI): per-pixel RF classification with class label and a per-pixel confidence (0–100).
    - Land Parcels: parcels intersecting 20m classified pixels with attributes describing composition within each parcel (e.g., _hist, _mode, _purity, _conf, _stdev, _n); parcel identifiers (gid) are updated from LCM2015.
    - 25m Rasterised Land Parcels: three-band rasters (band 1 = _mode, band 2 = _conf, band 3 = _purity) representing parcel-aggregated results.
    - 1km Dominant/Percent Cover and Aggregate variants: 1km rasters summarising parcel-level results into percentage, dominant class, and dominant aggregate class.
    - 1km Percent Cover (21 bands) and 1km Percent Aggregate Cover (10 bands): aggregated 1km summaries; ensure percentages may not sum exactly to 100 due to rounding and coastal mapping effects.
  - GB vs NI specifics
    - GB: 100x100 km Classification Scenes used to generate 46-band classification datasets; multiple overlapping scenes to ensure robust training.
    - NI: single 43-band Classification Scene per year, sized to NI extent.
  - Coordinate systems
    - Great Britain: British National Grid (EPSG:27700)
    - Northern Ireland: Irish Grid (TM75, EPSG:29903)

- Data generation and methodology
  - Seasonal inputs: Sentinel-2 Seasonal Composite Images per season (winter, spring, summer, autumn) derived from Google Earth Engine; TOA reflectance used (SR was evaluated but TOA used due to current performance).
  - Data inputs and context
    - Seasonal composites combined with 20m Context Rasters to form Classification Scenes; context rasters include terrain (height, aspect, slope) and proximately related features (distance to buildings, roads, coast, freshwater, etc.).
  - Bootstrap Training and classification
    - Bootstrap Training automatically samples training data from historic LCMs (not requiring field data). Training data for 2017–2019 derived from LCM2015 majority signals.
    - Random Forest classifier trained with balanced sampling (10,000 samples per class per training bag) across 21 UKCEH Land Cover Classes.
    - Production software integrates WEKA, PostGIS, and GDAL.
  - Land Parcel Spatial Framework
    - UKCEH Land Parcel Spatial Framework used to structure 20m Classified Pixels into parcels (~0.5 ha MMU); parcels provide a fixed, time-stable basis for change detection and product summarisation.
    - Framework retained for compatibility, though 2017–2019 products use updated indices and storage; gid values for 2017–2019 differ from LCM2015, but gid-based comparisons are supported.
    - Encourages user-defined parcel structures beyond the built-in framework.
  - Validation and quality control
    - UK-scale validation against GB countryside survey (2019), National Forest Inventory, IACS, and bespoke validation points (Calcacous grassland example) totaling 22,325 points.
    - Reported accuracies at the 21-class level (overall) around 78.6% for 2017, 79.6% for 2018, and 79.4% for 2019.
    - Validation data treated as best-available indicators rather than absolute truth; cross-year comparisons may be affected by class reformulations and training data alignment.
  - Outputs and interpretation
    - 20m Classified Pixels preserve fine landscape detail (e.g., narrow features) not present in aggregated parcel products.
    - Land Parcel attributes provide detailed parcel-level composition summaries to support interpretation, with explicit definitions for hist, mode, purity, conf, stdev, and npix.

- Data quality, limitations, and considerations
  - Automated classification vs manual corrections
    - This release uses automatic classification; no manual region corrections were applied as in earlier editions.
    - Visual checks and formal validation performed; errors are generally randomly distributed across space year-to-year, not persistent at the same location.
  - Data gaps and spectral ambiguity
    - Some seasonal gaps due to cloud in Seasonal Composite Images; the classifier tolerates incomplete spectral information but future work may fill gaps with alternative optical sources or radar (Sentinel-1).
  - Class relationships and mapping considerations
    - 21 Land Cover Classes align with UKCEH LCM2015 and earlier mapping lanes; not a direct one-to-one replication of the older BAP Broad Habitats in the field, as remote-sensing detectability differs from in-situ definitions.
    - Appendix material provides detailed crosswalks and caveats regarding spectral detectability (e.g., upland peatland complexity, bracken vs acid grassland, saltwater vs freshwater near coasts).
  - Temporal dynamics and bootstrap strategy
    - Bootstrap Training emphasizes the majority signal across years; future maps plan to base bootstraps on progressively larger year ranges to improve stability and accuracy.

- Accessibility, visualization, and metadata
  - Datasets include recommended color schemes and color-blind friendly options (Appendix 3 and Appendix 4), plus associated QGIS symbol files.
  - Full dataset metadata and confusion matrices are provided (Appendix 5) to support user assessment of class-level performance and error patterns.
  - Appendix 6 lists the full dataset inventory and naming conventions for 2017–2019 products across GB and NI.

- Practical takeaways for data leadership and strategy
  - Automated, annually-updating LCMs enable timely monitoring of land cover change with consistent class definitions and a fixed spatial framework, supporting near-term decision-making and trend analysis.
  - The combination of 20m detail, parcel-level attributes, and 1km summary rasters provides flexible aggregation for different analytical needs and stakeholders.
  - Documentation emphasizes traceability (Bootstrap Training lineage from 2015, gid changes, and schema differences) and encourages users to adapt parcels to their own boundaries for change detection.
  - While accuracy is promising (roughly 80% overall for 21-class mapping), per-class performance varies; stakeholders should consult confusion matrices (Appendix 5) and consider class-specific limitations in interpretation and reporting.
  - The architecture supports expansion (annual releases, broader input sources, potential integration with radar data) to improve temporal resolution and resilience to cloud cover, aligning with data strategy goals for robust, scalable geospatial data systems.