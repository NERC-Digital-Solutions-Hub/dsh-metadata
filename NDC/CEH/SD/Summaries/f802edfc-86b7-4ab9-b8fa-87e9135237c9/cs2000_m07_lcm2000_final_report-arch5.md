# Table 1. Broad Habitats and their relation to LCM2000 Target classes, Subclasses and Variants (the Suclasses are shown in their map display colours)

- Overview
  - Describes how Broad Habitats (BH) map to LCM2000 Target Class, Subclasses, and Variants (with Suclasses shown by map colours).
  - Sets up the framework for comparing LCM2000 classifications with field survey data (CS2000) and summarising habitat extent across the UK and constituent countries.

- Data model and classifications
  - LCM2000 uses a hierarchy of Target Class, Subclasses, and Variants to describe habitat types.
  - CS2000 represents field survey classifications used for cross-walking with LCM2000.
  - Footnotes indicate nuances in mapping, including where categories are broad or where variants are numerous (e.g., woodland types, grasslands, coastal and urban classes).

- Key tables and what they cover
  - Table 5: Coverage (km2) of Subclasses from Land Cover Map 2000 (LCM2000) and Aggregate classes from LCM2000 and field survey (FS) in the UK and constituent countries
    - Provides country-level totals for each Broad Habitat subclass, Subclass, and aggregate class.
    - Totals show large-scale mapping differences across England, Wales, Scotland, Northern Ireland, and the UK overall.
    - Notable: UK total LCM2000 coverage is given; FS totals are sometimes incomplete or not available for all categories.
    - Coastal coverage is variable due to tidal states and inclusion/exclusion of offshore inter-tidal areas.
  - Table 6: LCM2000 cover (km2) for BHs (uncalibrated) for England, Wales, Scotland, Northern Ireland and GB, compared with field survey estimates at 95% confidence
    - Presents uncalibrated LCM2000 estimates by broad habitat type, with field survey (FS) lower and upper bounds (Low/High) where available.
    - Includes cross-country comparisons (England, Wales, Scotland, Northern Ireland, GB) for each broad habitat.
    - Highlights uncertainties and ranges used to compare modelled vs. field-derived extents.
  - Table 8: Summary correspondence matrix (results expressed per 1000) comparing LCM2000 with CS2000 field survey squares in Great Britain
    - Weighted estimates using strata based on 40 Land Classes; bootstrapped confidence intervals.
    - Shows correspondences for Broad Habitats (plus urban generalisation considerations) at Target Class and Aggregate levels.
  - Table 9: Summary correspondence matrix (England and Wales)
    - Similar structure to Table 8, focused on England & Wales data.
  - Table 10: Summary correspondence matrix (Scotland)
    - Similar structure, focused on Scotland data.
  - Note: Footnotes explain crosswalk mappings between CS2000 and LCM2000 categories, including some illustrative examples and limitations of the crosswalks.

- Data quality, calibration, and limitations
  - The tables present uncalibrated LCM2000 data and use field survey results (CS2000) for comparison.
  - Differences between LCM2000 and FS are acknowledged and explained in the accompanying text.
  - Coastal coverage varies with tidal states and inclusion criteria for offshore areas.
  - Data gaps exist in certain regions (e.g., Northern Ireland FS data limitations; some FS values not available).
  - Some crosswalk mappings rely on broad categories, which can reduce precision in matching LCM2000 and CS2000 classes.

- Provenance, metadata, and governance considerations
  - Data originate from LCM2000 (as of 2000) and CS2000 field surveys; Tables rely on their respective classifications and extents.
  - Documentation includes explicit notes on calibration status (uncalibrated), confidence intervals, and definitions of broad habitats, target classes, and variants.
  - Footnotes provide essential context for reproducibility, including scope of coastal areas and the impact of definition differences on totals.

- Implications for data stewardship and reuse
  - For data stewards, the document highlights:
    - The importance of maintaining clear crosswalks between classification schemes (LCM2000 and CS2000) and documenting any updates or calibrations.
    - The need to capture provenance, scale, and time frame (LCM2000 = 2000) in metadata.
    - The necessity of reporting uncertainties and confidence intervals when comparing modeled vs. field-derived data.
    - The impact of regional differences and data gaps on UK-wide totals and comparability across England, Wales, Scotland, and Northern Ireland.
  - Recommendations for governance and sharing:
    - Include explicit lineage and calibration status in metadata.
    - Provide transparent crosswalk mappings with documented assumptions and limitations.
    - Preserve both uncalibrated and calibrated traces where available, along with 95% confidence intervals for comparability.
    - Highlight coastal and intertidal area considerations to avoid misinterpretation of totals.
    - Ensure updates or re-aggregations are versioned and clearly communicated to data users.

- Practical takeaways for discovery and use
  - The document offers a structured mapping framework to relate broad habitat categories to a standardized classification system and to relate modelled map data to field survey data.
  - Useful for researchers aiming to quantify habitat extents, compare map-based estimates with field data, or perform UK-wide habitat trend analyses.
  - Users should pay attention to calibration status, regional differences, and the limitations of crosswalks when aggregating across countries or when interpreting small-area classes.