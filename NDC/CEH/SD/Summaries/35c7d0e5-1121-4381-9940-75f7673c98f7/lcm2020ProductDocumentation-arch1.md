# The UKCEH Land Cover Map for 2020

- Scope and data products
  - LCM2020 comprises six datasets across GB and Northern Ireland: for each region, three datasets are produced — a 10m Classified Pixel dataset, a Classified Land Parcel dataset, and a 25m Rasterised Land Parcel dataset.
  - 21 UKCEH Land Cover Classes are used, aligned with Biodiversity Action Plan (BAP) Broad Habitats terminology, with careful notes on distinctions and cross-walking between UKCEH classes and BAP Broad Habitats.

- Data product details
  - 10m Classified Pixel datasets
    - Derived from Classification Scenes; each pixel has a most-likely UKCEH Land Cover Class (band 1) plus a probability/confidence value (band 2).
    - No generalisation to the Land Parcel Spatial Framework to preserve fine-scale features.
  - Classified Land Parcel datasets
    - Created by intersecting the 10m Classified Pixels with the UKCEH Land Parcel Spatial Framework to assign parcel-level attributes.
  - 25m Rasterised Land Parcel datasets
    - Rasterised per land parcel into 25m pixels; three attributes per parcel are carried: dominant class (_mode_), mean confidence (_conf_), and _purity_ (how dominant the parcel’s land cover is).
  - GB vs NI specifics
    - GB: Classification Scenes are 100x100 km tiles, producing 46-band GB Classification Scenes; 74 overlapping scenes classified per year to cover the GB land surface.
    - NI: A single 36-band Classification Scene (plus context layers) is used for the year.

- Classification methodology
  - Sentinel-2 Seasonal Composite Images (winter, spring, summer, autumn) plus 10 Context Rasters to reduce spectral confusion.
  - Bootstrap Training and Random Forest classifier
    - Bootstrap Training automatically samples training observations from historic land maps, enabling wall-to-wall training data without new field work.
    - Training data for LCM2020 come from LCM2017, LCM2018, and LCM2019; only parcels with >99% purity across all three years are kept.
    - GB training set: 941,027 objects; NI training set: 214,833 objects.
    - Random Forest training uses balanced sampling (10,000 samples per class per bag) to ensure rare classes are adequately learned.
  - Software
    - Custom RF classifier integrating Weka, PostGIS, and GDAL; all open-source components.

- Data production workflow
  - Classification Scenes are built from 36-band Sentinel-2 seasonal data plus 10 context rasters (GB) or 7 context rasters (NI) to form 43–46 band Classification Scenes.
  - Each Classification Scene is trained and classified independently; overlaps are resolved by manual precedence checks (a single manual step in GB).
  - Land Parcel Spatial Framework (MMU ~0.5 ha) is used to aggregate 10m pixels into parcels for the parcel datasets.
  - The aim is annual production to support change detection and monitoring; random errors are expected to flicker over time, while real changes persist.

- Context rasters and spectral context
  - GB context rasters (10m) include height, aspect, slope, distances to buildings/roads/sea/freshwater, foreshore and tidal masks, and a woodland mask.
  - NI context rasters (10m) include height, aspect, slope, urban mask, distance to coast, distance to freshwater, and distance to roads.

- Validation and accuracy
  - Validation data drawn from GB countryside survey data (2019/2020), open National Forest Inventory data, IACS data, and bespoke validation points (total 34,715 points).
  - Overall accuracy: 79.2% (full thematic detail), with Appendix 4 providing per-class confusion matrices and both User’s and Producer’s accuracies.

- Land Cover Class relationships and notes
  - 21 UKCEH Land Cover Classes are related to BAP Broad Habitats but are not a one-to-one match; some classes are split or combined to fit remote-sensing capabilities.
  - Appendices document detailed notes on individual classes, including known spectral confusions (e.g., Bracken vs Acid Grassland, upland vegetation, peatland communities) and guidance on interpretation.

- Data management and accessibility
  - Dataset descriptors and official names are provided; Appendix 5 lists the full set of LCM2020 datasets (GB and NI).
  - Data provenance and metadata are tracked to support discoverability; datasets are prepared for potential portal upload with rich metadata.

- Practical guidance and cautions
  - The 10m Classified Pixel dataset preserves fine spatial detail but has not been generalised to the Land Parcel Framework; users should be aware of potential higher variability in edges and small patches.
  - Annual maps help distinguish random classification noise from real change; expect occasional misclassifications, particularly for spectrally similar or structurally ambiguous habitats.
  - Differences in land parcel identifiers between LCM2015 and LCM2020 may affect direct parcel-ID comparisons over time; spatial overlap methods remain reliable for change analysis.

- Appendices highlights
  - Appendix 1: Notes on UKCEH Land Cover Classes with interpretation guidance and potential confusions.
  - Appendix 2: Biodiversity Action Plan (BAP) Broad Habitats definitions.
  - Appendix 3: Colour recipes for displaying each UKCEH Land Cover Class.
  - Appendix 4: Detailed correspondence matrices and accuracy metrics by class (confusion matrices, User’s and Producer’s accuracies).
  - Appendix 5: Full list of LCM2020 datasets and their official names.