# The UKCEH Land Cover Map for 2020

## Purpose and scope
- UKCEH LCM2020 is an annual land cover map for the UK, created from classified Classification Scenes built from Sentinel-2 seasonal composites and 10 context rasters.
- The product comprises six geospatial datasets across Great Britain and Northern Ireland: three datasets per geography (10m classified pixels, land parcels, and 25m rasterised land parcels), plus related 8-bit raster products.
- LCM2020 presents 21 UKCEH Land Cover Classes linked to Biodiversity Action Plan (BAP) Broad Habitats, with careful attention to terminology and distinctions between UKCEH classes and BAP Broad Habitats.
- The goal is to support change detection, temporal consistency, and broad environmental objective monitoring, with annual updates enabled by automated methods.

## Data products and structure
- 10m Classified Pixel datasets (GB and NI)
  - Output: two-band raster per geography
    - Band 1: most likely UKCEH Land Cover Class id
    - Band 2: probability/confidence of the classification
  - Rationale: preserves detailed landscape features not generalised by parcel framework; intended for specialist users aware of uncertainties.
- Land Parcel datasets
  - Derived by intersecting 10m Classified Pixels with the UKCEH Land Parcel Spatial Framework.
  - Attributes include per-parcel histograms, mode, confidence, purity, and aggregated class (agg).
  - Spatial Framework: parcels have a minimum area of ~0.5 ha (MMU), designed to capture discrete real-world units and support change detection.
- 25m Rasterised Land Parcel datasets
  - Rasterise land parcels to 25m pixels; 3-band rasters per parcel:
    - Band 1: per-parcel dominant land cover (mode)
    - Band 2: mean confidence (conf)
    - Band 3: parcel purity (purity)
- 20m Classified Pixel dataset (NI) and related NI datasets
- Dataset extents, coordinate systems, and naming conventions are provided (GB: EPSG 27700; NI: EPSG 29903).

## Data production and methodology
- Seasonal Composite Images
  - Based on Sentinel-2 surface reflectance; four seasons (winter, spring, summer, autumn).
  - Bands used: 2, 3, 4, 5, 6, 7, 8, 11, 12; some seasonal gaps due to cloud are handled without manual gap filling.
- Context Rasters
  - 10 context rasters to reduce spectral confusion (GB: height, aspect, slope, distances to buildings/roads/sea/freshwater, foreshore mask, tidal mask, woodland mask).
  - NI context rasters include similar measures plus an urban mask and coastal/freshwater/road distance layers.
- Classification Scenes
  - GB uses overlapping 100x100 km tiles to create 36-band Seasonal Composite Images; 74 GB Classification Scenes classified independently and overlapped to ensure range and balance of training data.
  - NI uses a single 43-band Classification Scene per year derived from NI extent.
- Bootstrap Training
  - Fully automatic training using historical LCM data (Bootstrap Training) to sample current imagery for training, enabling wall-to-wall coverage without fresh field data.
  - Training dataset size: GB ~941,027 objects; NI ~214,833 objects, derived from LCM2017–2019 with >99% purity across three years.
- Random Forest classification
  - Balanced sampling: 10,000 samples per class per bag to train the RF classifier.
  - Output: 10m Classified Pixels (GB/NI) with class and confidence.
  - Software: bespoke UKCEH pipeline integrating Weka, PostGIS, and GDAL (open-source tools).
- Validation and accuracy
  - Validation using GB countryside surveys (2019–2020), open data (National Forest Inventory, IACS), and bespoke validation points (34,715 points total).
  - Overall accuracy: 79.2% at full thematic detail (Appendix 4).

## The UKCEH Land Parcel Spatial Framework and data governance
- Spatial Framework
  - Based on prior frameworks (LCM2007; modified for LCM2015) with minor changes; parcel IDs (gid) differ from LCM2015, affecting exact longitudinal comparisons by parcel identifier.
  - MMU of ~0.5 ha ensures parcels represent discrete real-world units (fields, parks, urban areas, etc.).
  - Parcel geometry aids noise reduction and enables robust change detection over time.
- Data governance and transparency
  - The product emphasizes automated processing, traceable methods, and reproducibility.
  - Validation methodology and confusion matrices are documented (Appendix 4), supporting user assessment of reliability by class.
  - The data production process is designed to differentiate real land cover change from random classification errors thanks to the time-series approach.

## Relationship to UK BAP Broad Habitats and classification notes
- The 21 UKCEH Land Cover Classes align closely with UK BAP Broad Habitats but are not identical; some mappings are explicitly italicised to distinguish BAP meanings from UKCEH classes.
- Appendices describe detailed mappings and notable nuances (e.g., flats between arable/grassland, differences between upland peatland vegetation classes, and how context rasters aid in challenging separations such as Neutral Grassland, Bracken, and Bog).
- Appendix 1 provides class-level notes to help interpret spectral and contextual cues, while Appendix 2 summarises BAP Broad Habitats definitions.

## Access, metadata, and appendices
- Appendix 5 lists the official dataset names and holdings for LCM2020, including 10m Classified Pixels (GB/NI), Land Parcel products, and 25m raster products.
- Appendices include:
  - Appendix 1: UKCEH Land Cover Classes notes and guidance for interpretation.
  - Appendix 2: Biodiversity Action Plan (BAP) Broad Habitats definitions.
  - Appendix 3:Recommended color recipe for displaying UKCEH Land Cover Classes.
  - Appendix 4: Correspondence/Confusion matrices for LCM2020 (class-by-class performance and accuracy metrics).
  - Appendix 5: Full list of datasets and citations.

## Practical implications for data stewards
- Annual, automated production supports timely monitoring of land cover change across the UK, with methods designed for temporal consistency and change detection.
- Rich metadata and detailed validation enable informed governance, selective reuse, and transparent assessment of uncertainty (e.g., classification probability in the 10m pixel product; known context-related confusions).
- The Land Parcel Spatial Framework provides a stable structure for longitudinal analyses, though users should account for gid changes when performing direct parcel-ID based comparisons between LCM2020 and earlier maps.
- The open-source tooling and explicit methodology support reproducibility and potential methodological updates in future cycles if accuracy improvements justify re-application across the catalog.