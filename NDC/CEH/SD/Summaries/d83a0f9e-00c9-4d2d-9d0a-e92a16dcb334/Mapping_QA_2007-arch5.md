# Mapping Quality Assurance Exercise

## Overview
- Reports on QA of Countryside Survey 2007 data, aiming for high-quality, field-mapped habitat data that can be integrated into a GB geodatabase and analyzed with other national datasets.
- Digital mapping in the field using Surveyor software to reduce interpretation errors and handwriting issues; data uploaded to an interactive wiki for early data checking.
- QA was conducted by visiting survey teams and using standardized QA protocols to assess data accuracy and consistency.

## Data Collection & Standards
- Surveyors used a purpose-built Surveyor package with mandatory fields to collect area/line/point data and to prompt for expected attributes; included visit-status tracking.
- Data checked and guidance provided via an early-access wiki, enabling rapid feedback and guidance for survey design and analysis.
- QA teams conducted field visits to verify adherence to protocols; emphasis on consistent metadata, attribute capture, and timely data sharing.
- All data uploaded to a shared geodatabase; unsurveyed or refused areas excluded prior to analysis to ensure comparability.

## QA Process & Scope
- QA covered mapped data across 23 one-kilometre squares, exceeding prior QA scope and intended to represent square types across GB.
- Refusals and land access issues were accounted for; analyses focused on common surveyed areas between CS and QA datasets.
- QA teams attempted to synchronize surveys in time with field teams to minimize temporal changes in vegetation.

## Analysis Approaches
- 4.1 Direct comparison of aggregate areas/lengths/points for whole squares.
- 4.2 Raster data comparisons: polygons converted to 10 x 10 m raster cells within each 1 km square; dominant Broad Habitat assigned per cell; spatial and amount-based comparisons conducted.
- 4.3 100-point grid: a 10 x 10 grid over each square used to compare Broad Habitat concordance at a fixed resolution; positive vs negative scoring for matches.
- 4.4 Attribute comparisons: reference ID layers created to compare species attributes within matched areas/lines/points.

## Key Findings

### 6.1 Direct comparison of aggregate areas for whole squares
- 81% of squares had Broad Habitat (BH) presence recorded by both CS and QA.
- Mean differences between QA and CS for BH extents were generally small:
  - Most BH: <1–3.5% difference, depending on habitat.
  - Some habitats showed larger variability (e.g., Improved grassland, Dwarf Shrub Heath, Bog, Urban, Neutral/Acid grasslands) suggesting differential allocation between teams.

### 6.2 Comparisons of raster data
- Overall raster agreement across squares averaged around 76%, with a range from ~23% to ~98% depending on square.
- Several squares exhibited notably high concordance (e.g., 364, 488) and some low (e.g., 773, 261, 935, 434).
- Agreement by Broad Habitat per square highlighted where differences arose, e.g., Neutral vs Improved Grassland, Urban vs Grassland, and upland habitat mosaics.

### 6.3 100-point sample grid
- Concordance varied by square; most squares showed reasonable agreement, but some had substantial mismatches:
  - Notable low: square 773 (27–19% range in some tables) and square 261 (around 41–41%).
  - Other squares showed strong concordance (e.g., 364, 359, 364 ~90+%).
- Overall indicated good agreement for many squares but highlighted habitat-definition and mosaic-mapping challenges in others.

### 6.4 Polygon analysis of species attributes
- 1,081 QA polygons and 998 CS polygons spatially matched; 45% of QA polygons had at least one listed species overlapping the matched CS polygon.
- Species concordance varied by Broad Habitat; examples:
  - BH (Broadleaved & Yew Woodland): high match rate (~92.5% of matched polygons).
  - Coniferous woodland: ~88.6% match for species within matched polygons.
  - Improved Grassland showed relatively high match, while Neutral/Acid Grasslands displayed more variability.
- 77% of polygons with a matching species also had a matching BH, indicating species composition influenced Broad Habitat allocation in many but not all cases.
- Polyps (mosaics) and habitat definition complexity contributed to species matching variability.

### 6.5 Lists of commonly recorded species
- Species concordance across spatially matched polygons averaged around 40%, with QA tending to record more species than CS.
- For commonly recorded species (e.g., Lolium perenne, Calluna vulgaris, Molinia caerulea, etc.), there were both matches and discrepancies:
  - Some species showed reasonable agreement (e.g., Lolium perenne; Calluna vulgaris).
  - Others displayed substantial discrepancies (e.g., Eriophorum vaginatum, Pteridium aquilinum, Rhododendron ponticum, etc.), often reflecting field-identification challenges or habitat allocation choices.

## Change Recording and Data Updates
- 2007 allowed more detailed change coding:
  - Real change: a physical change since 1998.
  - Error change: a wrong assignment in the previous map.
  - No change: unchanged since 1998.
- Change coding was complex; some surveyors needed time to adapt.
- Tables show generally good agreement on change coding across habitats and features, though some habitat-specific ambiguities remain (notably with Blanket Bog and related upland habitats).
- Digital data capture enabled in-field verification and updating of change codes, improving data tidiness but adding analytical complexity.

## Data Governance Implications for Data Stewards

- The digital, field-based data collection approach improves data quality and timeliness but requires strong governance around:
  - Consistent habitat definitions and classification rules (e.g., Blanket Bog, Coniferous vs Broadleaved Woodland).
  - Clear guidance for managing mosaics and small-scale heterogeneity, especially in upland areas.
  - Versioning and change-tracking to capture Real vs Error changes and ensure updates propagate across datasets.
  - Metadata standardization and regeneration of BH definitions to support cross-survey comparability.
  - Training and knowledge transfer to minimize user interpretation differences and misclassification.
  - Documentation and governance around use of the Field Handbook updates (e.g., 2007 revisions for Blanket Bog).

- The QA process demonstrated strong alignment between CS and QA teams for many habitat types and features, but highlighted:
  - The impact of habitat definition boundaries on agreement (notably Blanket Bog, Neutral/Improved Grassland, Urban-Grassland distinctions).
  - The challenge of mosaics and fine-scale transitions between habitats, which affect raster and 100-point comparisons.
  - The need for continued calibration of field protocols, especially for upland and machair-like habitats.

- The use of wiki-based QA and a centralized geodatabase supports discoverability and traceability, aligning with data stewardship goals for auditability and reproducibility.

## Recommendations for Future QA & Data Management
- Refine and harmonize habitat definitions, with explicit guidance on problematic edge cases (e.g., Blanket Bog vs Dwarf Shrub Heath, machair, mosaic mapping).
- Strengthen field staff training focused on consistent application of habitat codes, particularly for woodlands and grassland subtypes.
- Improve handling of mosaics and small-scale habitat boundaries in analysis, possibly through enhanced mosaic decomposition guidance or alternative comparison metrics.
- Enhance change-coding workflows with clearer mappings between 1998 and 2007 field data; provide decision trees or guidance for edge cases.
- Maintain and update metadata documentation, ensuring that all habitat definitions, classification criteria, and data-processing steps are versioned and accessible for re-analysis.
- Ensure robust data provenance and lineage in the geodatabase so that QA findings and field changes can be traced and audited by Data Stewards.

- Overall, maintain the publishing mindset: continue to publish and share high-quality, well-documented datasets with clear provenance, consistent standards, and transparent QA reporting to support discovery and reuse.