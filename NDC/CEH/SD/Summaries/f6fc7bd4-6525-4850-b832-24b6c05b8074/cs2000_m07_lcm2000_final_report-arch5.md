# Table 1. Broad Habitats and their relation to LCM2000 Target classes, Subclasses and Variants (the Suclasses are shown in their map display colours)

- Purpose: Describe how Broad Habitats relate to LCM2000 Target Classes, Subclasses, and Variants, including color mappings used in map displays.
- Content scope: Links between Habitat types (e.g., Broad-leaved woodland, Coniferous woodland, Arable & horticultural, Grassland types, Bracken, Dwarf shrub heath, Fen/marsh/swamp, Bog, various water/rock/shore categories) and their LCM2000 classifications (Target Class, Subclasses, Variants).
- Application: Provides a framework for interpreting LCM2000 outputs against habitat concepts used in field surveys and mapping displays.

## Data and tables summarized

- Table 5: LCM2000 and FS coverage
  - Presents area (km2) for Subclasses from LCM2000 and Aggregate classes (bold) from LCM2000 and field survey (FS) across the UK and constituent countries.
  - Examples of large category coverments include:
    - Broad-leaved/mixed/yew woodland
    - Coniferous woodland
    - Arable cereals and Arable & Horticultural
    - Improved grassland and Other grassland groups
    - Built up areas and gardens
    - Mountain habitats, Fen/marsh/swamp, Bog, Bracken, Dwarf shrub heath, and various coastal/shoreline classes
  - Countries shown: England, Wales, Scotland, Northern Ireland, and UK totals.
  - Notes: LCM2000 vs FS differences, coastal coverage variability, and how totals depend on population definitions used in FS.

- Table 6: LCM2000 cover (uncalibrated) for Broad Habitats (BHs) with 95% CIs from FS
  - Provides country-level and GB-wide comparisons of LCM2000 estimates vs field survey (FS) estimates.
  - Examples of matched classes (UK LCM2000 vs FS Low/High ranges):
    - Broadleaved/mixed and yew woodland: UK LCM2000 = 15,259; FS Low = 12,750; FS High = 16,670
    - Coniferous woodland: UK LCM2000 = 12,879; FS Low = 10,672; FS High = 16,808
    - Arable & Horticulture (GB total): LCM2000 = 56,638; FS Low = 47,944; FS High = 57,036
    - Improved grassland (GB total): LCM2000 = 50,024; FS Low = 50,536; FS High = 59,104
  - Notes: FS values are missing for some regions; coastal coverage variability and differences in FS population definitions affect comparisons; table uses bootstrapped, weighted estimates across 40 Land Classes with 95% CIs.

## Validation and correspondence insights

- Table 8–10: Summary correspondence matrices (per 1,000; weighted, bootstrapped)
  - Compare LCM2000 with CS2000 field survey squares in Great Britain and in England & Wales.
  - Present broad-habitat level correspondences and finer target/subclass levels.
  - Indicate level of agreement and transfer patterns (e.g., urban generalisation, BH-level mappings, and cross-class relationships).
  - Footnotes provide explicit mappings between CS2000 and LCM2000 codes for various habitat types (e.g., Coniferous woodland, Broadleaved woodland, Arable & horticulture, Improved grassland, Bracken, Dwarf shrub heath, Fen, bog, etc.).
  - Key takeaway: There is substantive alignment in many broad categories but notable differences in several classes, especially where urban/generalised mapping or coastal definitions influence classification.

- Methodological note
  - The validation uses bootstrapping and stratification by 40 Land Classes to generate confidence estimates.
  - FS (field survey) data provide ground-truth baselines for calibration and assessment of LCM2000 accuracy.
  - Differences between LCM2000 and CS2000 FS outputs are discussed, including urban generalisation effects and coastal/intertidal coverage variability.

## Practical implications for Data Stewards

- Data provenance and lineage
  - LCM2000 versus CS2000: maintain clear lineage, definitions, and versioning of target classes, subclasses, variants, and BH-level mappings.
  - Document calibration status (unCalibrated vs Calibrated) and how confidence intervals were derived.

- Metadata and semantics
  - Provide explicit definitions for Target Class, Subclass, Variant, and BH-level; annotate any generalisations (e.g., urban generalisation) and coastal area considerations.
  - Include methodology notes on bootstrapping, sampling strata (40 Land Classes), and how weights were applied.

- Data quality and uncertainty
  - Report 95% CIs and clearly label data as calibrated/uncalibrated; highlight regions with missing FS values (e.g., NI in Table 6) and areas with coastal coverage caveats.
  - Keep track of differences between LCM2000 and field-survey results to inform users about potential biases in habitat area estimates.

- Data governance and sharing
  - Version control for datasets (LCM2000 vs CS2000 mappings; updated classifications; urban/generalisation adjustments).
  - Data portals should present both raw LCM2000 outputs and calibrated/validated results, with clear notes on confidence and regional caveats.
  - Maintain crosswalks between CS2000 and LCM2000 classifications to support reuse in comparative studies and policy analyses.

- Data usability and dissemination
  - Provide user-friendly summaries of major habitat areas and their uncertainties (e.g., UK totals for key classes like broadleaf woodland, coniferous woodland, arable, grassland groups).
  - Include guidance on how to use the correspondences in Tables 8–10 for translating CS2000 field observations to LCM2000 classifications and vice versa.

- Operational considerations
  - Address disparities across the UK nations (England, Wales, Scotland, NI) and how NI data gaps affect national totals.
  - Highlight the impact of coastal/intertidal delineations on class areas and subsequent analyses or decisions.

## Bottom-line takeaway for Data Stewards

- The document presents a comprehensive linkage and validation framework between LCM2000 habitat classifications and CS2000 field surveys, with detailed area statistics by class and country, plus robust validation through bootstrap-informed confidence intervals and cross-walks between classification schemes.
- For governance and stewardship, critical actions include maintaining transparent metadata, versioned crosswalks, clear documentation of calibration status and uncertainties, and accessible, well-annotated data products that note regional and coastal caveats to support reliable discovery, sharing, and reuse.