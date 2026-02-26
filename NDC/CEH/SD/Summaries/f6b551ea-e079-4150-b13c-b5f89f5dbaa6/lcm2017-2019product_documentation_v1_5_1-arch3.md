# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1 30/06/2020

## Purpose and scope
- User guide accompanying the release of three UKCEH Land Cover Maps (LCM2017, LCM2018, LCM2019).
- Maps cover 21 UKCEH Land Cover Classes (based on Biodiversity Action Plan Broad Habitats) and match the convention used in LCM2015.
- Focus on how data were produced, validated, and how users can apply them in current and future work.
- Emphasises that annual maps are produced automatically to enable rapid understanding of land cover change, with ongoing plans for yearly releases.

## Data architecture and datasets
- Datasets across years (GB and NI) include:
  - 20m Classified Pixels: new per-pixel classifications with class probability (0–100) and a 2-band raster; preserves fine landscape detail.
  - Land Parcels: attributes summarising 20m classifications within fixed parcels (0.5 ha MMU); key fields include gid, _hist, _mode, _purity, _conf, _stdev, etc.
  - 25m Rasterised Land Parcels: three-band rasters (mode, conf, purity) derived from parcel summaries.
  - 1km Raster datasets: Percent Cover (21 bands), Percent Aggregate Cover (10 bands), Dominant Cover (1 band), Dominant Aggregate Cover (1 band).
  - Classification Scenes: GB uses 100x100 km tiles; NI uses a single tile; 74 overlapping GB scenes classified to produce 46-band GB scenes; overlaps may yield minor differences, resolved by visual/manual precedence checks.
- Spatial framework and class relationships
  - UK Land Parcel Spatial Framework used to generalise national cartography; 21 UKCEH Land Cover Classes and 21 aggregates mapped.
  - gid identifiers do not match LCM2015 parcel IDs due to framework changes; parcel-level comparisons across years use gid.
- Terminology and mapping
  - Relationships and mappings between UKCEH Land Cover Classes and UK BAP Broad Habitats documented (Appendices 1–2).
  - Color recipes and figure illustrations provided for visualization.

## Production methodology
- Bootstrap Training
  - Fully automatic training process that uses historic UKCEH LCMs (LCM2015) as a training source to sample spectral training observations from current satellite imagery.
  - Bootstrap set is derived from high-purity parcels (≥99% purity from LCM2015) to seed the training data; designed to enable rapid updates without fresh field data.
  - Future plans: use majority signal across 2017–2019 (and later across 2018–2020) for successive bootstraps (LCM2020 planned for 2021).
- Random Forest classification
  - Training data drawn with replacement to ensure class balance; 10,000 samples per class.
  - Production software integrates WEKA, PostGIS, and GDAL (all open source).
- Data inputs and scene construction
  - Seasonal Composite Images derived from Sentinel-2 via Google Earth Engine (TOA reflectance used; surface reflectance (SR) evaluated but did not improve results in this study).
  - Seasonal information: median reflectance per season (winter, spring, summer, autumn) across nine Sentinel-2 bands.
  - Context Rasters (20m) provide terrain, proximity, and land-use context (e.g., height, aspect, slope, distances to buildings/roads/coast/freshwater, urban/foreshore masks, etc.).
- Classification Scenes and processing
  - GB: 100x100 km tiles, 36-band Seasonal Composite Images combined with 20m Context Layers to form 46-band GB Classification Scenes; 74 overlapping scenes classified independently; overlapping regions resolved by visual checks to select best results.
  - NI: single 43-band Classification Scene per year for the landmass extent.
  - UKCEH Land Parcel Spatial Framework used to generate parcel-level outputs and to structure 20m classified pixels into a fixed, consistent framework.

## Validation and data quality
- Product validation
  - UK-scale validation using 22,325 validation points from countryside survey 2019, National Forest Inventory data, IACS, and bespoke LCM validation points.
  - Reported overall accuracy (producer’s and user’s accuracy tables provided by year):
    - LCM2017: ~78.6% overall accuracy
    - LCM2018: ~79.6% overall accuracy
    - LCM2019: ~79.4% overall accuracy
  - Validation data used across the three products; accuracy figures reflect currency relative to each product and include caveats about class mapping and potential mislabeling.
- Interpretive notes and limitations
  - No manual corrections were applied for these latest maps (automatic classification only); visual checks and formal validations performed.
  - Some classes (notably upland peatland and spectrally similar vegetation groups) show inter-class confusion; BAP Broad Habitats were not designed for satellite detection, leading to inherent limitations in spectral separability.
  - Coastal Saltwater vs Freshwater distinctions can be challenging near tidal areas; some coastal misclassifications are expected but generally manageable.
  - Historical-class alignment: changes in class naming and the Land Parcel framework mean cross-year parcel ID matching is constrained; core comparisons can be made via gid rather than parcel IDs.

## Data availability, metadata, and governance
- Data structure supports transparent, reproducible monitoring outputs with detailed metadata (Tables 2–4, Appendix 4).
- Metadata enhancements and explicit documentation accompany datasets; open-source production tools used.
- Data sharing considerations acknowledged; some attributes and schemas were updated to align with production software, improving clarity and usability (with notes on potential user inconvenience for renamed attributes).
- Appendices provide detailed mappings between class systems (UKCEH vs UK BAP), color schemes, and full dataset lists (Appendix 5).

## Relevance for monitoring frameworks
- Timeliness and scalability
  - Enables annual, nationwide land-cover mapping with a fully automated workflow, reducing the need for costly field data collection for every update.
- Provenance and transparency
  - Clear lineage from Sentinel-2 imagery, through bootstrap training and RF classification, to final 20m, 25m, and 1km products; full methodological description supports auditability.
- Data granularity and flexibility
  - 20m Classified Pixels preserve detailed landscape features; 25m Land Parcels summarise locally; 1km datasets provide generalized, policy-relevant metrics (percent cover, dominant/aggregate cover).
- Data governance and openness
  - Emphasis on public sharing of data and underlying inputs; explicit notes on data management standards, metadata, and reproducibility.
- Limitations and decision context for policy use
  - Acknowledges potential data gaps, silos, and metadata quality issues; class definitions reflect BAP-linked habitats but are constrained by remote-sensing capabilities.
  - Advice on interpreting changes over time, considering that improvements in methodology (bootstrap approach, scene overlaps) aim to enhance comparability and reliability for monitoring and decision-making.

## Appendices and technical specifics (high level)
- Appendix 1–2: Notes on UKCEH Land Cover Classes and BAP Broad Habitats, including detection considerations and class derivations.
- Appendix 3: RGB color recipes for visualizing UKCEH Land Cover Classes.
- Appendix 4: Validation details and confusion matrices across LCM2017–LCM2019 (class-level accuracies and producer/user accuracies).
- Appendix 5: Full list and descriptions of dataset components for LCM2017, LCM2018, and LCM2019.