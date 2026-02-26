# Table 1. Broad Habitats and their relation to LCM2000 Target classes, Subclasses and Variants (the Suclasses are shown in their map display colours).

## Overview
- Document presents a detailed crosswalk between LCM2000 (Land Cover Map 2000) broad habitats, their target classes, subclasses, and variants, including how these map to CS2000 field survey classifications.
- Primary data sources referenced: LCM2000, CS2000, and field survey (FS) data, with tables comparing area coverage and correspondence.
- Includes regional breakdowns for England, Wales, Scotland, Northern Ireland, and the UK as a whole.
- Highlights data quality considerations, calibration status, and methodological notes (e.g., bootstrapping, confidence intervals).

## Datasets and Classification
- LCM2000 provides:
  - Target classes, subclasses, and variants for broad habitat types (e.g., inshore sublittoral, standing water, littoral rock, supra-littoral, various woodland and grassland types, urban/built-up areas, etc.).
- CS2000 (field survey) provides cross-classifications used for validation and cross-walks.
- FS (field survey) data serve as ground-truth comparisons.
- Tables include taxonomic mappings and specific variant names (e.g., sea/estuary, water inland, rock/Littoral categories, arable and horticulture variants, urban/suburban variants).

## Key Tables and Findings

- Table 5: Coverage (km^2) of Subclasses and Aggregate Classes
  - Reports area coverage for each LCM2000 subclass and aggregate class (bold) across England, Wales, Scotland, Northern Ireland, and the UK.
  - Provides UK totals (e.g., total LCM2000 area by habitat class) and corresponding field-survey figures where available.
  - Distinguishes between LCM2000 totals and field-survey totals (FS) and notes that coastal coverage is variable due to tidal states and inclusion/exclusion of intertidal areas.
  - Highlights that total coverage definitions can vary depending on FS population definitions (e.g., some Northern Ireland BHs excluded from survey).

- Table 6: LCM2000 Cover (uncalibrated) for Broad Habitats (BHs) vs Field Survey Estimates (95% CI)
  - Presents uncalibrated LCM2000 estimates for broad habitat groups (e.g., broad-leaved/mixed/yew woodland, coniferous woodland, arable and horticulture, improved grassland, neutral/calcareous/acid grasslands, bracken, dwarf shrub heath, fen/marsh/swamp, bog, montane habitats, inland rock, built-up areas/gardens, supralittoral rock/sediment, littoral rock/sediment, littoral categories, oceanic seas).
  - For each habitat, provides FS low and high estimates (where available) to indicate uncertainty and validation against field data, along with UK-wide totals.
  - Highlights discrepancies between LCM2000 and FS at national and regional levels, underscoring calibration needs and dataset reliability concerns.
  - Notes uncalibrated status of LCM2000 cover figures and the need for calibration against CS2000/FS for improved accuracy.

- Tables 8–10: Summary Correspondence Matrices (LCM2000 vs CS2000)
  - Table 8: GB comparison (results per 1000) across Broad Habitats, Target Class, and Aggregate class; uses weighted estimates (strata based on 40 Land Classes) and bootstrapped confidence intervals.
  - Tables 9–10: England & Wales and Scotland-specific correspondences, with detailed cross-walks between LCM2000 and CS2000 classes; results presented per 1000 and include notes on urban generalisation and weighting.
  - Footnotes clarify mappings (e.g., cross-references between CS2000 broad/narrow categories and LCM2000 classes), interpretation of “Low/High” FS estimates, and potential mismatches in class definitions.
  - Indicate general alignment patterns and areas of mismatch between satellite-derived (LCM2000) classifications and field-based (CS2000/FS) classifications, including urban generalisation issues.

## Regional Focus and Data Quality

- Regional coverage:
  - Data are broken down by England, Wales, Scotland, Northern Ireland, and the UK as a whole, with separate FS estimates and LCM2000 figures.
- Data quality and limitations:
  - LCM2000 statistics are described as uncalibrated in Table 6, requiring calibration against CS2000/FS for robust interpretation.
  - Coastal coverage variability and differences in whether certain intertidal/offshore areas are included affect totals.
  - FS population definitions and potential exclusion of some BHs in Northern Ireland can influence comparability.
  - Tables include numerous footnotes explaining differences, data gaps (n/a), and methodological approaches (bootstrapping, weighting).

## Data Governance and Stewardship Implications

- Provenance and lineage
  - Clear mapping between LCM2000 classifications and CS2000/FS ground-truth data; provenance is essential for repeatable analyses.
- Metadata and documentation
  - Requires thorough metadata describing target classes, subclasses, variants, and cross-walk logic; document calibration status and confidence intervals.
- Interoperability and standards
  - Crosswalks between multiple classification schemes (LCM2000 vs CS2000) necessitate consistent terminology and versioning to support data integration.
- Data quality management
  - Uncalibrated LCM2000 figures and reliance on FS for validation imply ongoing calibration work; governance should track calibration progress, uncertainties, and validation outcomes.
- Update and maintenance
  - Regular updates to classification schemes and field survey methods should be reflected in versioned datasets; coastal and urban-area definitions may require special handling.
- Access and usage considerations
  - Users should consider the 95% CIs and calibration status when applying the data to analyses; provide guidance on when to rely on LCM2000 vs CS2000/FS-derived figures.

## Practical Takeaways for Data Stewards

- Ensure robust metadata accompanying LCM2000-CS2000 crosswalk datasets, including:
  - Definitions of Target Class, Subclass, and Variant levels.
  - Regional breakdowns and UK totals.
  - Calibration status and methods used for aligning LCM2000 to CS2000/FS.
  - Confidence intervals and notes on data gaps or n/a values.
- Maintain clear versioning and change logs for all classifications and crosswalks.
- Preserve the provenance of field survey data and clearly document the basis for any synthetic or aggregated totals.
- Provide guidance on handling coastal variability and urban generalisation in analyses.
- Facilitate reproducibility by sharing the crosswalk logic (mapping tables, bootstrapping approach, weighting schemes) used to generate Tables 8–10.

## Conclusion

- The document provides a comprehensive crosswalk between LCM2000 habitat classifications and CS2000 field survey classifications, with extensive tables detailing area coverage, uncalibrated LCM2000 versus field estimates, and cross-class correspondences.
- It emphasizes data quality considerations, regional variability, and the need for calibration and robust metadata to enable reliable, interoperable use by data stewards managing large-scale habitat datasets.