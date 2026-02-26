# CSLCM/Final

## Overview and Aim
- Support UK Biodiversity Action Plan by presenting a framework of Broad Habitats (BHs) across Great Britain.
- Create a thematic land-cover map (LCM2000) from satellite imagery, enhanced with external contextual data.
- Provide a structure (BHs, Target classes, Subclasses, Variants) to enable consistent mapping, reporting, and interoperability.
- Establish a calibration approach to relate LCM2000 outputs to the CS2000 field survey data for improved habitat statistics.

## Data and Classification Structures
- BHs: Broad Habitat categories (e.g., Broadleaved/mixed woodland, Coniferous woodland, Arable and horticulture, Improved grassland, Neutral/Calcareous/Acid grasslands, Bracken, Fen/marsh/swamp, Bogs, Montane, Inland rock, Built-up areas, Coastal habitats, etc.).
- LCM2000 classes: Spectral/land-cover classes that map to BHs, with Target classes, Subclasses, and Variants for finer distinctions.
- Aggregate class level: Simplified 10-class abstraction used for reporting where BHs align closely with aggregated categories.
- Map displays: Cartographic choices balance reliability and pattern visibility; some small or rare BHs are aggregated for national/regional plots.

## Data Collection and Processing
- CS2000 field survey (FS): 569 one-kilometre squares (549 in 1998, others in 1999); much more detailed than LCM2000; not ground truth but used for calibration.
- Inter-comparison approach designed around calibration (not validation) due to differences in resolution and timing.
- GIS workflow: ARC/Info-based datasets created for FS squares and LCM2000 map sections; generated correspondence matrices for per-pixel, per-segment, and per-parcel comparisons.

## Calibration and Quality Assessment
- Confidence limits via bootstrapping to estimate 95% ranges for correspondence across GB, England/Wales, and Scotland.
- Key correspondence findings (by level and region):
  - BH level (per-pixel): GB 54%, England/Wales 60%, Scotland 44%.
  - Per-segment: GB 58%, England/Wales 64%, Scotland 47%.
  - Per-parcel: GB 62%, England/Wales 69%, Scotland 48%.
  - Target class level generally higher than BH level across methods.
  - Aggregated class level: closer matches between LCM2000 and FS.
- Observed patterns:
  - Per-pixel is the most sensitive to spatial resolution and feature boundaries.
  - Larger, well-defined features (e.g., coniferous woodland) show higher concordance; small woodlands often fall below the LCM2000 minimum mappable unit (MMU) and are misrepresented.
  - Urban and arable classifications show confusions (e.g., grassland vs arable, urban vs non-urban), partly due to spectral similarities and seasonal effects.
  - Fen, marsh, swamp and peatland (bog) delineations are particularly challenging; peat-depth masks influenced bog mapping, sometimes underestimating bog extent relative to FS.
  - Montane, bracken, dwarf shrub heath, and coastal/boundary features present complex distinctions that are not consistently captured at 1 km scale.
- Overall interpretation:
  - LCM2000 achieves notable agreement with field-derived classifications at broader aggregated levels, but is not a direct substitute for field surveys.
  - Realistic accuracy at the Target class level is around 87% potential (given underlying limitations), with practical per-class accuracy lower due to scale, timing, and definitional differences.

## Change Detection
- Between LCMGB 1990 and LCM2000 changes were likely small and frequently confounded by error.
- Satellite-only mapping limits detection of real landscape changes; a more intelligent approach is needed.
- Proposed approach: combine FS (1990, 1998) change trajectories with LCM2000 outputs to identify probable changes and distinguish them from classification or data-product errors.
- Future work: development of calibration-based change detection to improve reliability.

## Practical Implications for Data Stewardship
- Data provenance and versioning:
  - LCM2000 is a satellite-derived, broad-scale dataset calibrated against detailed field data (CS2000). Document calibration steps, version numbers, and data lineage.
- Metadata and classifications:
  - Explicit mapping between BHs, Target classes, Subclasses, and Variants; document any re-interpretations or future refinements (e.g., rough grasslands, peat depth assumptions).
- Accuracy and uncertainty:
  - Report that accuracy is not ground truth; acknowledge MMU differences, temporal mismatch, and class-definition disparities.
  Provide region-specific and class-specific accuracy notes to inform data users about reliability and applicability for their analyses.
- Updates and interoperability:
  - Plan for iterative improvements by integrating FS data and external datasets; maintain interoperability with UK biodiversity frameworks and other land-cover standards (e.g., CORINE-derived corrections).
- Change analysis governance:
  - Any change-detection outputs should be treated with caution; use calibration-informed approaches to attribute observed changes to real landscape dynamics versus data artifacts.
- Documentation and accessibility:
  - Provide thorough documentation of classification schemes, calibration methodology, and the rationale for aggregations; ensure data are discoverable and usable by researchers, policy makers, and data managers.

## Appendix and Classification Details (Highlights)
- Appendix I outlines distinguishing features and limitations of BHs relative to LCM2000 mapping, including challenges distinguishing neutral/calcareous/acid grasslands, peat depth’s role in bog classification, and the complexities of shrub/heath and coastal habitats.
- The report emphasizes that certain BH distinctions (e.g., grassland types, rough vs improved, bracken, peat-associated bogs) require contextual information beyond remote sensing and may necessitate knowledge-based corrections.