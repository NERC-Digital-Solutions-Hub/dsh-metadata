# Table 1. Broad Habitats and their relation to LCM2000 Target classes, Subclasses and Variants (the Suclasses are shown in their map display colours)

- Purpose and scope
  - Presents the correspondence between Broad Habitats and LCM2000 (Land Cover Map 2000) Target Classes, Subclasses, and Variants; Suclasses are shown by map display colours.
  - Supports interpretation of how LCM2000 categories map to real-world habitats across the UK in a single reference frame.

- Data sources and definitions
  - LCM2000 statistics come from a full count of cover on a 25 m grid.
  - Field Survey (FS) statistics come from Haines-Young et al. 2000 and are used for comparison.
  - Differences between LCM2000 and FS statistics are explained in the accompanying text.
  - Coastal coverage varies due to tidal states and inclusion/exclusion of offshore inter-tidal areas.
  - Total coverage depends on whether the population is defined in 1 km squares; in Northern Ireland, some BHs are excluded from the survey.
  - Footnotes indicate that some data are “n/a” or not available for certain regions (e.g., NI FS).

- Key datasets and indicative findings
  - Table 5: Coverage (km²) of Subclasses from LCM2000 and Aggregates from LCM2000 and FS across the UK nations.
    - Examples of UK totals (LKCM2000): England 130,362; Wales 20,689; England & Wales 151,051; Scotland 77,898; NI 17,739; UK total 246,688.
    - FS totals shown alongside LCM2000 totals for England, Wales, Scotland, and the UK where provided (e.g., England & Wales FS 142,355; Scotland FS 78,730; NI FS not available).
    - Demonstrates wide variation in the size of different habitat types (e.g., Broadleaved woodland, Coniferous woodland, Arable & Horticultural, Improved grassland, Built up areas, etc.).
  - Table 6: LCM2000 cover (uncalibrated) for Broad Habitats (BHs) for England, Wales, Scotland, NI, GB, with field-survey (FS) comparison at 95% confidence.
    - Provides Low/High FS estimates where available, enabling a sense of uncertainty and calibration needs.
  - Tables 8–10: Summary correspondence matrices comparing LCM2000 with the CS2000 field survey squares (GB, England & Wales, and Scotland) expressed per 1000 (or per 1000s) and bootstrapped confidence intervals.
    - Tables show how often LCM2000 target classes, broad habitats, and aggregates correspond to CS2000 field-survey classifications.
    - Tables include weighting by strata (40 Land Classes) and note that confidence intervals are generated via bootstrapping.
    - The Scotland-specific Table 10 extends the same approach to a more localized comparison across habitat types and CS2000 mappings.
  - Overall interpretation
    - The correspondence matrices reveal varying degrees of alignment between LCM2000 classifications and CS2000 field data, with some habitat types showing good agreement and others exhibiting notable discrepancies.
    - The results underscore the importance of calibration, metadata, and clear definitions when harmonizing broad habitat maps with field surveys.

- Metadata, quality, and governance considerations for data leaders
  - Data lineage and harmonisation: LCM2000 is grid-based and broad; CS2000/FS offers field-validated perspectives. Users should account for methodological differences during integration.
  - Documentation and metadata: The tables come with extensive footnotes describing methodology, regional coverage, and data limitations; preserving this metadata is essential for correct interpretation and reuse.
  - Data quality and uncertainty: The 95% confidence ranges in FS, as well as uncalibrated LCM2000 figures, indicate substantial uncertainty in some classes; decision-making should incorporate these uncertainty bounds.
  - Regional variation and accessibility: Data are presented separately for England, Wales, Scotland, NI, GB, and UK totals; some regional data (e.g., NI FS) may be incomplete or not available.
  - Data governance implications: When integrating LCM2000 into a broader data strategy, align targets with standardized definitions, ensure discoverability of the mapping between Target Classes, Subclasses, and Variants, and consider ongoing validation with field data to maintain data quality over time.

- Practical takeaways for data strategy and use
  - Use Table 1 as a reference for mapping LCM2000 classifications to real-world habitats when compiling dashboards, reports, or decision-support tools that rely on habitat data.
  - Leverage Table 5 and Table 6 to understand the scale and regional distribution of habitat types and to assess the need for calibration against field data.
  - Consider Table 8–10 correspondences when aggregating LCM2000 data with CS2000/FS datasets to support cross-dataset analyses and comparability.
  - Maintain rigorous metadata and provenance, given the documented differences between grid-based maps and field surveys, and clearly communicate uncertainties and regional caveats to data users.