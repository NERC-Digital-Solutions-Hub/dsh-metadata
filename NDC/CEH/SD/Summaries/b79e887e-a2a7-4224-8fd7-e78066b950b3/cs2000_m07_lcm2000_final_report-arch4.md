# Table 1. Broad Habitats and their relation to LCM2000 Target classes, Subclasses and Variants (the Suclasses are shown in their map display colours)

- Purpose and scope
  - Provides a comprehensive mapping between Broad Habitats and LCM2000 Target classes, Subclasses, and Variants (with Suclasses shown by map colors).
  - Sets up the context for comparing two data sources across the UK: the Land Cover Map 2000 (LCM2000) and CS2000 field survey (FS).

- Data sources and classifications
  - LCM2000: map-based habitat classifications across England, Wales, Scotland, Northern Ireland, and the UK as a whole.
  - CS2000/FS: field survey estimates used to validate and calibrate the map-based classifications.
  - Footnotes explain statistical and methodological details:
    - LCM2000 statistics from a full count of cover on a 25 m grid.
    - FS statistics from Haines-Young et al. 2000.
    - Differences between LCM2000 and FS are discussed; coastal coverage is variable due to tidal states and inclusion/exclusion of offshore inter-tidal areas.

- Key tables and what they show (selected highlights)
  - Table 5: Coverage (km2) of Subclasses from LCM2000 and Aggregate classes from LCM2000 and FS, by country and UK totals.
    - Example: Broadleaved/mixed woodland England LCM2000 = 10,963 km2; FS (England) = 8,460–11,480 km2 (range indicates 95% confidence).
    - Example: Coniferous woodland GB LCM2000 = 12,879 km2; FS Low/High = 10,672–16,808 km2.
    - Example: Arable & Horticultural (UK) LCM2000 = 57,630 km2; FS values vary by region.
  - Table 6: LCM2000 cover (uncalibrated) vs FS estimates at 95% confidence (per habitat type, by country and GB).
    - Demonstrates how map-based estimates compare with field survey estimates and their uncertainty ranges.
  - Tables 8–10: Summary correspondence matrices (results expressed per 1000 or per 1000s) comparing LCM2000 with CS2000 field squares in Great Britain and separately for England & Wales and Scotland.
    - Show how often particular CS2000 habitat categories correspond to LCM2000 categories, under weighting and bootstrapping to produce confidence intervals.
    - Include breakdowns by broad habitats, target classes, and aggregate classes, along with urban/generalisation considerations.
  - Across tables, totals are provided for England, Wales, Scotland, Northern Ireland, GB, and UK, illustrating scale and regional variation in both map-based and field-derived estimates.

- Methodology and uncertainty
  - Uses bootstrapping to calculate confidence intervals for correspondences.
  - Weights estimates based on strata (e.g., 40 Land Classes) to generalise results.
  - Distinguishes between target class, aggregate class, and fine-grained subclass mappings, highlighting potential misalignments between map classes and field observations.
  - Notes that coastal coverage and methods of inclusion/exclusion affect total area estimates.

- Regional breakdowns and scale
  - Presents region-specific figures (England, Wales, Scotland, Northern Ireland) and combined UK totals.
  - Highlights region-to-region differences in habitat area estimates and level of agreement between LCM2000 and FS data.
  - Emphasises that urban/generalised areas require careful handling when mapping to habitat classes.

- Implications for Data Leaders (Data Strategy and governance)
  - Data system perspective: the document demonstrates the importance of cross-wader data fusion (map-based vs field data) for a complete view of habitat extents.
  - Data availability and gaps: shows where FS fills include areas where LCM2000 may be uncertain or overlapping; highlights gaps in alignment and regional variability.
  - Metadata and standards: underscores the need for clear metadata about grid resolution (25 m), spatial extent (coastal considerations), and classification schema alignment between LCM2000 and field survey terminologies.
  - Data quality and verification: reveals imperfect matches between map-based classes and on-ground realities, emphasizing iterative product development with feedback from users and stakeholders.
  - Accessibility and calibration: illustrates that calibrating map products with field surveys (CS2000/FS) is essential for reliable decision-making; uncertainty quantification (confidence intervals) is critical for risk-aware planning.

- Practical takeaways for your data work
  - Use the mapping (Table 1) to align user-facing habitat products with LCM2000 classes, ensuring that end-user definitions and expectations are met.
  - Leverage the comparative tables (Tables 5–6) to identify where map estimates diverge from field observations and prioritize data improvements or additional validation in those areas.
  - Incorporate uncertainty information (confidence intervals from FS) into dashboards, risk assessments, and policy guidance to communicate data reliability.
  - Ensure documentation of data sources, grid scales, coastal treatment, and classification conversions to support governance and reproducibility.
  - Plan for cross-region coordination to harmonise classifications and improve consistency across England, Wales, Scotland, and Northern Ireland.

- Endnotes and caveats
  - Differences between LCM2000 and FS are explained in the accompanying text.
  - Coastal coverage variability reflects tidal states and offshore area treatment.
  - Totals vary by definitions of the FS population (1 km squares) and inclusion rules, requiring careful interpretation when aggregating results.

- Conclusion
  - The document provides a detailed, multi-table comparison between map-based habitat classifications (LCM2000) and field survey estimates (CS2000/FS) across the UK, including extensive regional breakdowns, uncertainty estimates, and methodological notes.
  - For Data Leaders, it offers a concrete case study in aligning large-scale data products with ground-truth observations, highlighting where data systems can improve governance, quality, and user-aligned product development.