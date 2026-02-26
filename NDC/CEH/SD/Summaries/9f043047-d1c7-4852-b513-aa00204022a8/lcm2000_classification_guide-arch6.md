# LCM2000 Final Report

## Overview and aims
- UK Biodiversity Action Plan framework uses Broad Habitats (BHs) to describe UK habitats; LCM2000 maps terrestrial, freshwater, and coastal BHs using satellite-derived spectral data augmented by external datasets.
- Aim to distinguish BHs where possible, with Subclasses and Variants providing finer detail beyond BHs; aggregate classes are used for reporting.
- Map displays are designed for national/regional views, prioritising reliability and pattern visibility over the rarest, most dissected classes.

## Classification framework and map display
- BHs: broad habitat categories (e.g., Broadleaved woodland, Coniferous woodland, Arable land, Grasslands, Fen/marsh/swamp, etc.).
- Target classes and Subclasses: thematic refinements within BHs; Variants capture finer spectral/contextual distinctions (e.g., crop types, grassland management).
- Aggregate classes: simplified 10-class level used for reporting when close to BH aggregations.
- Map displays: standardized colors and naming; some BHs aggregated or split at Subclass/Variant levels to reflect utility and accuracy at national scales.

## Data sources and GIS workflow
- CS2000 field survey: 569 one-kilometre squares (549 in 1998, remainder in 1999); far more detailed in the field than LCM2000.
- Ground truth limitations: FS not ground truth; 88% repeatability for primary codes; upland boundaries difficult to map reproducibly; calibration focuses on inter-comparison rather than true validation.
- Data products: ARC/Info GIS coverage with BH labels; alignment matrices created per 1 km square; comparisons staged at multiple thematic levels.

## Calibration, comparisons, and confidence
- Three main comparison modes:
  - Per-pixel: overlay without structural adjustments; highlights spatial differences.
  - Per-segment: LCM2000 segments vs FS dominant class.
  - Per-parcel: FS parcels vs LCM2000-derived parcel labels.
- Confidence limits via bootstrapping (95% ranges) across GB, England/Wales, and Scotland.
- Key results (approximate, weighted bootstrapped):
  - Per-pixel: GB ~54%; England/Wales ~60%; Scotland ~44%.
  - Per-segment: GB ~58%; England/Wales ~64%; Scotland ~47%.
  - Per-parcel: GB ~62%; England/Wales ~69%; Scotland ~48%.
  - Target class level generally higher: GB ~65% (per parcel); England/Wales ~73%; Scotland ~51%.
- Overall, LCM2000 mapping reflects substantial, but not perfect, correspondence with CS2000 at multiple levels; differences stem from resolution (MMU), timing, class definitions, and survey errors.

## Accuracy interpretation and limitations
- The correspondence measures are not a direct measure of LCM2000 accuracy; FS is not ground truth, and methodological differences influence results.
- FS repeatability (88%) indicates a ceiling for achievable agreement; LCM2000 performance is about 72% of that potential when considering the data structures.
- Main drivers of mismatch:
  - Field vs satellite resolution (FS finer than LCM2000 25 m parcels vs FS parcel boundaries).
  - Time differences between surveys (FS mostly 1998 vs imagery 1998–2001 for LCM2000).
  - Class definition differences and mapping generalisations (e.g., MMU, urban/suburban distinctions).
- Estimated realistic accuracy at Target class level around 85% (c. 87% in some assessments); at BH level lower due to boundary issues and aggregation.

## Change detection
- Detecting landscape change between 1990 and 2000 is challenging; changes are likely small and confounded by error rates.
- A straightforward satellite-only approach is insufficient for robust change detection; intelligent, pattern-based approaches using FS data (1990/1998) and known change directions are recommended.
- Future work includes integrating CS2000 with FS and other data to better separate change from error, and direct calibration for Broad Habitat statistics.

## Habitat-level findings and notable issues
- Broadleaved/mixed vs Coniferous woodland: similar total cover, but small woodlands (below 0.5 ha) often omitted by LCM2000, causing mismatches with FS classifications.
- Arable and horticultural land: LCM2000 often overestimates relative to FS due to inclusion of small features; misclassification between arable and built-up areas exists.
- Improved vs semi-natural grassland: FS distinguishes management-driven improvements more readily; LCM2000 often maps some Improved grassland as Neutral grassland due to spectral similarities.
- Neutral, Calcareous, and Acid grasslands: semi-natural swards hard to separate spectrally; peat depth and soil pH context are critical for distinguishing these categories.
- Bracken, Dwarf shrub heath, Fen/marsh/swamp, Bog: significant mapping differences arise from the interpretation of peat depth and moss/vascular plant indicators; peat depth (>0.5 m) strongly influences bog vs heath assignment.
- Montane habitats and Inland bare ground: altitude-based definitions and context influence accuracy; inland bare ground is sometimes misclassified as urban features.
- Water bodies: Inland water mapping aligns with FS for standing water >0.5 ha, but coastal intertidal areas and narrow water bodies are variably represented; coastal BHs generally contribute little to overall accuracy.
- Built-up areas and coastal habitats: FS treats urban land differently (more continuous) than LCM2000, leading to differences in area estimates and spatial distribution.

## Outputs, applications, and follow-up
- The project aims to produce Broad Habitat statistics calibrated against field surveys to enable the use of LCM2000’s wide coverage with field-level precision for habitat quantification.
- Follow-up work includes re-examining bogs and heath classifications with integrated data (FS, peat maps, soil pH), and refining Variant-level distinctions (e.g., rough grassland vs improved) to improve consistency.
- Appendix I and the final report provide deeper technical detail on class definitions, spectral distinctions, and the limitations of remote sensing for fine habitat distinctions.

## Appendix I: Broad Habitats—distinguishing features and limitations
- Highlights the challenge of using remote sensing to distinguish many Broad Habitats (e.g., fine distinctions within woodlands, grassland management, bogs vs. dwarf shrub heath, and peat depth effects).
- Emphasizes the role of contextual data (soil chemistry, peat depth maps, land-use history) in improving classification accuracy.
- Describes recommended approaches to improve accuracy, including knowledge-based corrections and integrating multiple data sources.