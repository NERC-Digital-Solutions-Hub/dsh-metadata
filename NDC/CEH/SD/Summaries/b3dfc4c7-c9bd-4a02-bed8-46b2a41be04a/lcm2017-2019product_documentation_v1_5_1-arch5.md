# The UKCEH Land Cover Maps for 2017, 2018 and 2019

## Overview
- User guide for three new UKCEH Land Cover Maps: LCM2017, LCM2018, and LCM2019.
- Describe the data content, production workflow, validation, production decisions, and future plans.
- Aims to help users choose appropriate uses and understand dataset lineage and limitations.

## Data and Class Structure
- Maps cover 21 UKCEH Land Cover Classes (based on Biodiversity Action Plan Broad Habitats; not a direct UK BAP classification, but closely aligned for continuity).
- Yearly product suite duplicated for Great Britain (GB) and Northern Ireland (NI), yielding 42 datasets across 2017–2019.
- Data hierarchy and outputs:
  - 20m Classified Pixels (new in this release): RF classification results with two bands per pixel (class and confidence 0–100). Preserves fine landscape detail.
  - Land Parcels: datasets produced by intersecting 20m classified pixels with the UKCEH Land Parcel Spatial Framework. Attributes include gid, hist, mode, purity, conf, stdev, n (with minor attribute name changes from LCM2015).
  - 25m Rasterised Land Parcels: rasterised version of Land Parcels with 3 bands (mode, conf, purity).
  - 1km Rasters derived from 25m parcels: 1km Percent Cover (21 bands), 1km Percent Aggregate Cover (10 bands), 1km Dominant Cover (1 band), 1km Dominant Aggregate Cover (1 band).
- Classification process:
  - Seasonal Composite Images from Sentinel-2 (TOA reflectance; four seasons) plus 20m Context Rasters to create Classification Scenes.
  - GB: 100x100 km tile system; 74 overlapping Classification Scenes used to train and classify; NI: single 43-band scene per year.
  - Bootstrap Training: automatic training using historic LCM2015-derived data to bootstrap 2017–2019 maps, enabling near-automatic updates without new field data.
  - Random Forest classifier with balanced sampling (10,000 samples per class per training bag).
- Context and inputs:
  - 20m Context Rasters (GB and NI) include height, aspect, slope, proximity to buildings/roads/seas/freshwater, foreshore, tidal water, woodland, etc.
  - Bands and seasonal inputs described; Sentinel-2 bands and resolutions are listed.
- Classification and validation notes:
  - No manual corrections in this release; automated classification with visual checks and formal validation.
  - Validation against GB countryside survey 2019 data, National Forest Inventory, IACS, and bespoke validation points (22,325 total).
  - Reported overall accuracy (21-class): LCM2017 = 78.6%, LCM2018 = 79.6%, LCM2019 = 79.4%.

## Production and Methodology
- UKCEH Land Parcel Spatial Framework:
  - 0.5 ha minimum mappable unit (MMU); parcels are fixed from prior generalisations to support time-series comparisons.
  - gid serves as a parcel identifier; in 2017–2019 gid values do not match LCM2015 parcels, so comparisons require spatial overlap rather than parcel-by-parcel IDs.
- Bootstrap Training and Time-series:
  - Bootstrap Training uses 2015-derived high-purity parcels (≥99% purity) to initialize the classifier.
  - Future updates (LCM2020, LCM2021) planned to use majority signals across multiple years (e.g., 2017–2019; 2018–2020).
- Data structure and metadata:
  - Each year has GB and NI datasets for all outputs; all GB NI data are provided in parallel.
  - Attribute naming differences introduced for production workflow alignment (e.g., Hist, Purity, Conf naming).
  - General guidance on class derivation and relationships with UK BAP Broad Habitats provided in appendices.

## Datasets and Access
- Product suite per year:
  - GB: 20m Classified Pixels; Land Parcels; 25m Rasterised Land Parcels; 1km Dominant Cover; 1km Dominant Aggregate Cover; 1km Percent Cover; 1km Percent Aggregate Cover.
  - NI: same structure as GB where applicable (except some inputs/adoptions of context layers differ).
- Total datasets: 42 (21 classes x GB/NI x 3 years) plus corresponding parcel and raster products.
- Outputs are designed for rapid, annual updates to support land cover change analysis and monitoring.
- Data availability and governance considerations:
  - Data are produced to support wide reuse; provenance, processing steps, and validation metrics are documented.
  - Users should note gid changes when comparing to LCM2015; cross-year comparisons should rely on spatial overlap or gid where applicable.

## Validation and Quality
- Validation process and caveats:
  - Validation uses multiple sources; established validation points reflect a variety of data types but are not an absolute truth.
  - Currency of validation points relative to product year varies.
- Reported accuracy:
  - Approximately 78–80% overall accuracy across LCM2017–2019 for the 21-class scheme.
  Recognition that accuracy could improve as methods mature; ongoing effort to secure improved validation data.

## Practical Implications for Data Stewards
- Data governance and lineage:
  - Clear documentation of production steps, inputs, and validation to support data stewardship and audit trails.
  - gid changes across years require careful handling for near-continuous time-series analysis; spatial overlap is the recommended comparison method when gid differs.
- Metadata and interoperability:
  - Metadata reflects the 21-class scheme, 20m/25m/1km products, and context inputs; observe naming conventions and attribute changes when integrating with other datasets.
  - Be aware of class mapping relationships to BAP Broad Habitats and the nuanced differences noted in Appendix materials.
- Update cadence and planning:
  - An annual release cycle is intended; LCM2020 planned for 2021 with bootstrap-based updates.
  - Consider future expansions of input data types and broader thematic detail as production evolves (e.g., exploring other optical sources or radar data to fill gaps).

## Challenges and Considerations
- Incomplete view of user needs and priorities; need to align outputs with diverse user requirements.
- Timely data delivery and coordination with data producers.
- Metadata and standardisation across rapidly evolving production pipelines.
- Interoperability across different systems, formats, and coordinate grids (GB vs NI; GNSS/GRID differences).
- Managing large data volumes (20m Classified Pixels and associated parcel-level attributes) and updating parcel frameworks.

## Future Plans
- Continue annual LCM releases with ongoing evaluation of training data and feature inputs.
- Potential enhancements include expanded contextual information, alternative sensors to address cloud gaps, and refined upland vegetation mappings.
- Ongoing refinement of the UK Land Parcel Spatial Framework and related metadata to better support cross-year comparisons.