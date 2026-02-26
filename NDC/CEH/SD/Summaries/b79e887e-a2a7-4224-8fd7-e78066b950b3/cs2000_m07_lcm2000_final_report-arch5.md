# Table 1. Broad Habitats and their relation to LCM2000 Target classes, Subclasses and Variants (the Suclasses are shown in their map display colours).

- Overview and purpose
  - Presents the correspondence between broad habitats and the LCM2000 (Land Cover Map 2000) classification scheme, including Target Class, Subclasses, and Variants (with Suclasses shown by map colours).
  - Establishes a crosswalk between LCM2000 classifications and the CS2000 field survey framework, enabling comparison and integration of map-derived and field-survey data.

- Data structure and mapping components
  - LCM2000 classifications:
    - Target Class
    - Subclasses
    - Variants
    - Suclasses (displayed in map colours)
  - Tables and content referenced
    - Table 5: Coverage (km2) of Subclasses from LCM2000 and of Aggregate classes from LCM2000 and field survey (FS) across the UK and constituent countries.
    - Table 6: LCM2000 cover (km2) for BHs (Broad Habitats) with uncalibrated figures, compared to field survey estimates at 95% confidence (±2 standard errors).
    - Tables 8–10: Summary correspondence matrices comparing LCM2000 with CS2000 field survey squares (England, Wales, Scotland, NI, GB, and Oceanic regions), expressed per 1000 and weighted with bootstrap-based confidence intervals.
    - Footnotes and extensive notes clarifying methodology and definitions.

- Key data points and relationships highlighted
  - Broad habitat categories include major land-cover groups such as broad-leaved/mixed/yew woodland, coniferous woodland, arable and horticulture, improved grassland, neutral/calcareous/acid grasslands, bracken, dwarf shrub heath, fen/marsh/swamp, bog, inland bare ground, montane habitats, inland rock, built-up areas and gardens, supralittoral and littoral zones, and oceanic/seas classifications.
  - Totals and regional breakdowns are provided (England, Wales, Scotland, NI, GB, UK) for both LCM2000 and FS/CS2000 comparisons, with UK totals explicitly listed (e.g., UK LCM2000 totals and FS-derived totals where available).
  - Calibration and comparison status:
    - LCM2000 figures are described as uncalibrated in certain tables (e.g., Table 6).
    - FS (field survey) statistics are provided as Low and High estimates (where available) and are used to assess correspondence with LCM2000.
  - Coastal and urban adjustments:
    - Coastal coverage is variable due to tidal states and inclusion/exclusion of offshore inter-tidal areas.
    - Total coverage varies with the FS population definition (1 km squares) and some NI BHs are excluded from survey.
  - Unavailable data:
    - n/a entries indicate not available data in particular cells or regions.

- Methodological notes and caveats
  - LCM2000 statistics are based on full counts of cover using a 25 m grid; FS statistics follow Haines-Young et al. 2000 methodology.
  - Differences between LCM2000 and FS statistics are explained within the text.
  - Bootstrapping used to calculate confidence intervals for correspondence matrices (Tables 8–10), reflecting spatial stratification (e.g., 40 Land Classes) and field-generalisation considerations (urban areas).

- Implications for Data Stewards
  - Data integration and harmonisation
    - The document provides a formal crosswalk between map-based (LCM2000) and field-survey (CS2000/FS) data, essential for harmonising datasets used in biodiversity and land-cover analyses.
    - When merging LCM2000 with CS2000/FS data, note calibration status, grid resolutions (25 m vs 1 km squares), and region-specific data availability.
  - Metadata and provenance
    - Critical to document: classification scheme versions, grid resolution, calibration status, and the spatial extents (coastal vs inland) used in each table.
    - Include notes about which BHs are uncalibrated (Table 6) and which data are n/a or excluded (e.g., NI survey exclusions).
  - Data quality indicators
    - Capture and communicate uncertainties via the 95% confidence intervals from FS comparisons.
    - Record differences between LCM2000 and field-derived totals, and explain their sources (e.g., coastal coverage, urban generalisation).
  - Data governance and stewardship actions
    - Maintain the crosswalk as datasets are updated or reclassified (e.g., revisions to LCM or CS definitions).
    - Ensure consistent terminology and mapping rules across datasets to support reproducible analyses.
    - Provide usage notes for end-users on how to interpret uncalibrated vs calibrated figures and how coastal/urban adjustments may affect results.

- Practical guidance for users
  - Use Tables 5 and 6 to assess how LCM2000-derived cover compares with field-survey estimates across BHs and regions, and to understand where calibration is needed.
  - Consult Tables 8–10 for detailed correspondences between LCM2000 and CS2000, to inform data merging strategies and to interpret cross-dataset results.
  - Pay attention to footnotes on grid resolution, coastal variability, and NI survey limitations to interpret totals and regional comparisons accurately.
  - When communicating results, explicitly state the classification version, calibration status, and any region-specific data limitations that may influence interpretations.