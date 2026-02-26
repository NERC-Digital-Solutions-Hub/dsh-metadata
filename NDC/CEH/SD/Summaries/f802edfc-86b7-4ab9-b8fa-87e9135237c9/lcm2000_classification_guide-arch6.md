# LCM2000 Final Report

- The study supports implementation and reporting of the UK Biodiversity Action Plan by aligning Broad Habitats (BHs) with a remote-sensing–based land cover map (LCM2000) and field-survey data (CS2000). It explains how LCM2000 classes map to BHs, Subclasses, Variants, and Target classes, and how map displays are constructed for national/regional use.

## Data sources and structure

- Primary data sources:
  - CS2000 field survey (FS): detailed ground-truth style data collected in 1998–1999 across Britain (569 one-km squares in GB; NI data not yet digitised for testing).
  - LCM2000: thematic classification of spectral data from satellite imagery (late 1990s to 2000–01), designed to map BHs and support broader habitat assessments.
- Classification framework:
  - Broad Habitats (BHs) with Target classes, Subclasses, and Variants.
  - Aggregate classes: simplified 10-class level used for reporting where maps/statistics align with BH aggregations.
- Map display conventions:
  - Colors and aggregation schemes designed to emphasize patterns at national/regional scales, with some Subclasses shown below BH level where useful.

## Data fusion and calibration methods

- GIS workflow:
  - ARC/Info used to generate BH-labeled coverages for all FS squares and corresponding LCM2000 map-sections.
  - 569 correspondence matrices created (one per 1-km square). Three tests:
    - Per-pixel: direct overlay comparisons.
    - Per-segment: FS-dominant segment labels compared with LCM2000 segments.
    - Per-parcel: FS parcels labeled against LCM2000-derived parcel labels.
- Comparison levels and outputs:
  - Correspondences computed at multiple levels: BH, Target class, and Aggregate class.
  - Bootstrapping used to derive 95% confidence limits for correspondence measures.
- Accuracy interpretation:
  - FS is not ground truth; differences arise from resolution, timing, class definitions, and data model gaps.
  - Calibration-focused assessment rather than validation; inter-comparison informs mapping uncertainties.

## Key findings on correspondence and accuracy

- Overall correspondences (GB, across all measures):
  - Per-pixel: ~54% (England/Wales ~60%, Scotland ~44–47% range).
  - Per-segment: ~58% (England/Wales ~64%, Scotland ~47% range).
  - Per-parcel: ~62% (England/Wales ~69%, Scotland ~48% range).
  - Target-class correspondence improves: ~65% (GB, parcel-based), ~73% England/Wales, ~51% Scotland.
- By country and level (highlights):
  - BH-level: Britain ~62%, England/Wales ~64–66%, Scotland ~47–50%.
  - FS captures greater detail than LCM2000 (FS ~0.04 ha MMU vs LCM2000 >0.5 ha MMU) contributing to mismatches.
- Realistic accuracy expectations:
  - Realistic target-class accuracy around 85–87% (based on maximum repeatability of FS ~88% and observed correspondences).
- Notable patterns and causes of mismatch:
  - Small or patchy features (e.g., small woodlands, hedgerows) often fall below LCM2000’s MMU and are misrepresented.
  - Distinctions among semi-natural vs. improved grasslands, neutral/calcareous/acid grasslands, and peat/bog definitions show significant spectral/contextual challenges.
  - Bracken, peat depth (bog distinction), montane definitions, and inland bare ground show substantial classification differences between FS and LCM2000.
  - Coastal BHs and tidal-state variability introduce additional discrepancies and are treated as aggregates for reporting.

## Class-level insights and challenges

- Woodland and arable land:
  - Broadleaved/mixed woodland and coniferous woodland show similar overall cover but lower direct agreement due to small patches and boundary delineation.
  - Arable land vs. grassland misclassifications contribute materially to errors, partly due to rotation farming and spectral confusion.
- Grasslands and semi-natural categories:
  - Neutral, calcareous, and acid grasslands are hard to separate spectrally; many semi-natural swards mapped as neutral by LCM2000.
  - Improved vs. semi-natural grasslands are challenging; field notes indicate management practices influence spectral signatures.
  - Rough grasslands (often derelict or abandoned) present mapping ambiguity; LCM2000 treated many as Neutral grassland.
- Special habitats:
  - Fen, marsh, swamp vs. rush pastures show divergent treatment; LCM2000 tends to underrepresent fen/marsh in some years.
  - Dwarf shrub heath vs. bog distinctions depend on peat depth and contextual peat maps; peat-depth-based corrections affect classifications.
  - Bracken and Montane categories often under-represented or misclassified due to accessibility and sampling intensity.
- Water, built-up areas, and coastal zones:
  - Inland water and standing water mapping aligns reasonably well for larger bodies but smaller/waterways are limited by MMU and width thresholds.
  - Built-up areas are captured with more detail in LCM2000 than FS, leading to mapping differences in urban-rural gradients.

## Change detection and future work

- Change detection needs intelligent approaches beyond satellite data alone to separate real landscape changes from artifact differences.
- The report suggests leveraging FS-derived expectations (Haines-Young et al. 2000) to prioritize plausible changes and inform calibration.
- Ongoing and planned follow-up work:
  - Re-examine LCM2000 bogs and heaths with integrated CS2000 and external datasets.
  - Improve peatland mapping with additional data sources (peat depth, soils, other maps).
  - Develop methods to produce Broad Habitat statistics directly through calibration against field surveys.

## Data products and practical usage for Data Support

- Outputs designed to enable broader data use:
  - BH statistics calibrated against CS2000 field data for robust, country-level reporting.
  - Aggregate-class statistics aligned with LCM2000’s target and BH aggregations for consistent national-scale analysis.
- Practical guidance for data users:
  - Use target-class or aggregate-class outputs for higher accuracy given known BH-level mismatches.
  - Be mindful of resolution differences (FS at parcel-level vs. LCM2000 MMU) when interpreting small features.
  - Apply calibration insights to adjust LCM2000-based estimates of habitat extent, particularly for woodland, grassland, bog, and wetland classes.
- Data integration approach:
  - Combine comprehensive LCM2000 coverage with FS precision to generate comparable HB statistics and improve change analyses.
  - Use the Variant-level BH distinctions where feasible to refine analyses and future reclassification efforts.

## Appendix and conceptual notes

- Appendix I provides a concise review of Broad Habitats and distinguishing features relevant to LCM2000 mapping, highlighting the inherent limitations of remote sensing for fine-scale habitat distinctions and the reliance on contextual data (soil pH, peat depth, land-use history).
- The document emphasizes that precise spectral separation of several semi-natural or peat-related habitats is challenging, and calibration against field surveys is essential for reliable habitat statistics.