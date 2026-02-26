LCM2000 Final Report

- Purpose and scope
  - Assess and calibrate the LCM2000 land cover map against the CS2000 field survey (FS) data as an aid to UK biodiversity habitat assessment and reporting.
  - Provide a framework to derive Broad Habitat (BH) and Target-class statistics from the wide coverage of LCM2000, with comparison to detailed FS data.

- Data sources and classification framework
  - Data: LCM2000 satellite-derived classifications (1 km scale units; 25 m input pixels for mapping), and CS2000 FS field survey data (569 squares across Great Britain; detailed site-level coding).
  - Classification layers: BHs, Target classes, Subclasses, and Variants; aggregates used for reporting.
  - Mapping approach: Spectral classification supplemented by contextual data; recognition of differences between BH equivalents, Target classes, and Subclasses; some components are aggregated for display and reporting.

- Calibration methodology
  - Instrument: ARC/Info GIS tools used to create correspondence matrices at multiple spatial/raster/vector levels.
  - Tests conducted:
    - Per-pixel: direct overlay to quantify spatial differences.
    - Per-segment: dominant FS class within LCM2000 segments.
    - Per-parcel: FS parcels matched to LCM2000-derived labels.
  - Thematic levels analyzed: BH level (excluding certain boundaries/linear features), Target-class level, and Aggregate class level.
  - Confidence estimation: bootstrapping to generate 95% confidence intervals for correspondence measures.

- Key findings: correspondence and accuracy
  - Across GB (per-pixel, BH-level): ~54% correspondence; per-parcel ~62%; per-segment ~58%.
  - England & Wales: higher correspondence (per-pixel ~60%; per-parcel ~69%; per-segment ~64%).
  - Scotland: lower correspondence (per-pixel ~44%; per-parcel ~48%; per-segment ~47%).
  - Target-class level (parcel-based): GB ~65% overall; England/Wales ~73%; Scotland ~51%.
  - With aggregation to Aggregate and BH-levels, LCM2000 generally aligns more closely with FS when broader categories are used.
  - Overall accuracy at Target-class level is realistically around 85–87% (recognizing that FS is not a strict ground truth and differences arise from resolution, timing, and class definitions).
  - Notable sources of mismatch:
    - FS higher spatial resolution vs. LCM2000 25 m parcels and >0.5 ha minimum mapping unit (MMU) for LCM2000 vs FS 0.04 ha MMU.
    - Time differences between FS (1998–1999) and LCM2000 (images from 1998–2001) causing changes and misclassification.
    - Differences in class definitions and spectral/contextual distinctions (e.g., semi-natural vs. improved grassland, bogs vs dwarf shrub heath, peat depth in bog classification).
    - Urban/rural context and how built-up areas are represented differently in FS and LCM2000.
  - Specific habitat-discrepancy examples:
    - Broadleaved/mixed and Coniferous woodland: LCM2000 often misses small woodland patches (<0.5 ha) present in FS; openings in woodland may be misrepresented.
    - Arable and horticultural land: generally close, but some misclassifications between grassland and arable or between arable and built-up land.
    - Improved vs semi-natural grassland: FS tends to identify management-driven differences not always detectable spectrally; ~20% of FS 'improved grassland' mapped by LCM2000 as semi-natural.
    - Neutral/Calcareous/Acid grasslands: spectral data alone poorly separates these; soil-acidity context helps but remains imperfect.
    - Bracken, fen/marsh/swamp, bog, montane, inland bare ground: often mapped differently due to definition differences (peat depth, altitude thresholds) and limited field context.
    - Coastal BHs and intertidal areas: small and near resolution; differences due to tidal state at imaging; often treated as aggregates for reporting.
    - Boundary and linear features: not targeted by LCM2000; FS maps include these, contributing to differences in some tests.

- Change detection and temporal analysis
  - Change detection between 1990 (LCMGB) and 2000 (LCM2000) is challenging due to small overall changes and higher error rates from satellite mapping and differing data structures.
  - A segment-based approach yields different results from 1990 rasters; BH-based classifications complicate direct comparison.
  - Future work suggested: intelligent, pattern-based change detection using prior FS data and known patterns of change to separate true change from classification or data artifacts.

- Data products and recommendations for data support
  - Calibration against FS enables generation of Broad Habitat statistics from the broad coverage of LCM2000, leveraging FS precision where needed.
  - Recommendation to use Target-class and Aggregate-class Level analyses for robust nationwide statistics, with BH-level results where finer detail is not required.
  - Potential improvements:
    - Integrate LCM2000 with FS and external datasets to refine peatland (bog) mapping and to better separate neutral/calcareous/acid grasslands.
    - Use Variant-level distinctions (e.g., rough grass vs. improved) in follow-up analyses to enhance interpretability.
    - Consider refining the peat-depth/peatland logic and including context maps for improved bog vs heath delineation.
  - Note on data interpretation:
    - FS cannot be treated as ground truth; differences stem from resolution, timing, and methodological disparities.
    - The 0.5 ha MMU used by LCM2000 excludes many small features; users should account for under-representation of smaller habitats in LH data.

- Appendix highlights
  - Appendix II (not excerpted here) includes Table 2 mapping of LCM2000 class Variants to BHs and color codes for visualization.
  - Appendix I: A brief review of Broad Habitats with notes on distinguishing features and how they relate to LCM2000 mapping (e.g., woodland types, grassland categories, bogs, fens, etc.).

- Practical implications for data support
  - When using LCM2000 for policy, planning, or public data products, expect robust results for broad habitat extents and many major habitats, but be cautious about small patches, fine-grained distinctions (e.g., semi-natural vs improved grassland), and peatland/bog delineations.
  - Use aggregation and cross-walks to FS where high precision is required; apply caution in change-detection analyses due to timing differences and resolution constraints.
  - Data calibration and integration with external datasets is essential to improve accuracy for specialist habitats (peatlands, montane, bracken-rich areas) and coastal BHs.

- Bottom line
  - LCM2000 provides broad, nationwide habitat mapping with substantial coverage and reasonable accuracy at aggregated levels and Target classes, but individual BHs and small features show notable misalignments with the detailed CS2000 FS data. The calibration framework enables generation of comparable statistics and informs improvements and future integration with field data to enhance data quality for data-support oriented analysis and decision-making.