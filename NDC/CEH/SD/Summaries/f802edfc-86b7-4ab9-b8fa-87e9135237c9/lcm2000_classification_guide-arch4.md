CENTRE FOR ECOLOGY AND HYDROLOGY (NATURAL ENVIRONMENT RESEARCH COUNCIL) Project. T02083j5/C00878 CSLCM/Final

## Overview and purpose
- Aids implementation and reporting under the UK Biodiversity Action Plan (BAP) by framing Broad Habitats (BHs) across the UK.
- LCM2000 provides a thematic, satellite-based classification designed to map widespread terrestrial, freshwater, and coastal BHs, with external data added to refine spectral classifications.
- Aims to distinguish BHs, define Target classes and Subclasses, and support reporting through aggregated class levels.

## Classification approach and data structure
- LCM2000 combines spectral data with external context to classify BHs, forming Target classes and Subclasses, with Variants as spectral components.
- BHs are mapped consistently but with some compromises on accuracy; Subclasses may be shown below BH level when useful.
- Aggregate classes consolidate Target/Subclass data to 10-class levels for reporting; map displays use cartographic simplifications to emphasize patterns and avoid over-detail.

## Display, mapping, and calibration context
- Map displays use standardized colors; some rare BHs are aggregated for national/regional plots.
- Calibration against CS2000 field survey (CSLCM/Final) used CS2000 FS data to assess map accuracy and to calibrate BH statistics.
- FS data (569 one-km squares in GB; 1998–1999) provide detailed field observations but are not “ground truth” due to resolution and timing differences.

## Validation and calibration methodology
- Three main tests to compare CS2000 FS with LCM2000:
  - Per-pixel comparisons (direct overlay; sensitive to resolution/time differences and class definitions).
  - Per-segment comparisons (dominant FS class within LCM2000 segments).
  - Per-parcel comparisons (FS parcels vs LCM2000-derived parcel labels).
- Correspondence assessed at multiple thematic levels:
  - BH level (with some features generalized or omitted).
  - Target class level.
  - Aggregate class level (closest match to BH aggregations).
- Confidence limits estimated with bootstrapping to produce 95% ranges.

## Key accuracy findings
- Per-pixel correspondence (Britain): 54% (95% CI 53–56%); England & Wales: 60% (CI 58–62%); Scotland: 44% (CI 40–47%).
- Per-segment correspondence: GB 58% (CI 57–60%); England & Wales 64% (CI 62–66%); Scotland 47% (CI 43–50%).
- Per-parcel correspondence: GB 62% (CI 60–64%); England & Wales 69% (CI 67–72%); Scotland 48% (CI 44–52%).
- BH-level vs Target-class performance:
  - BH-level maps show more mis-match due to resolution and boundary effects.
  - Target class correspondence higher: GB 65% (parcels); England & Wales 73%; Scotland 51%.
- Overall, LCM2000 aligns more closely with FS at the Aggregate/Target class level; per-pixel results are the most variable.

## Main drivers of mismatch and limitations
- Resolution and minimum mapping unit:
  - FS observations often capture parcels < 0.5 ha; LCM2000 MMU is > 0.5 ha, causing mismatches for small features.
- Temporal differences:
  - FS mainly 1998; LCM2000 images from 1998–2001; date differences contribute to mismatches.
- Class-definition differences:
  - Distinctions between BHs and Target classes, and confusion among grassland types (neutral, calcareous, acid) and rough grasslands.
- Spectral/Contextual limitations:
  - Some habitats (e.g., bogs, peat-depth effects, montane, inland rock) are difficult to separate spectrally or contextually at 1-km resolution.
- Actual mapping gaps:
  - Boundary/linear features and some small-scale urban/rural elements are not targeted consistently by LCM2000.

## Habitat-specific mapping insights
- Woodlands: broadleaved/mixed and coniferous woodland show general agreement, but small woods are often omitted or misclassified due to MMU.
- Grasslands: improved vs semi-natural grasslands hard to separate; rough grasslands often treated as neutral grassland in LCM2000.
- Fen, marsh, swamp; bogs; heath and montane habitats present notable distinction challenges; peat depth and soil pH influence classifications.
- Water and coastal habitats: standing water and inland water acceptable at >0.5 ha; coastal BHs are small and less reliably mapped at 1-km resolution.
- Built-up areas: LCM2000 differentiates between suburban/rural developed and continuous urban, whereas FS treats urban land more generally, affecting cross-class correspondence.

## Change detection and future work
- Detecting landscape change with satellite data alone is limited; requires intelligent approaches that incorporate prior1 field data (FS) and known change patterns.
- Calibration results indicate under- and over-estimates that should be accounted for in change analyses.
- Future work includes integrating LCM2000 with FS and external datasets to refine Broad Habitat statistics and improve change-detection capabilities.

## Data usage and governance implications for Data Leaders
- LCM2000 provides broad, continental-scale habitat mapping with wide coverage but with acknowledged limitations in accuracy at fine scales.
- For data strategy:
  - Use LCM2000 for high-level monitoring and trend analyses, with explicit caveats about resolution-driven errors and class-definition ambiguities.
  - Leverage calibration insights to quantify uncertainty and to improve aggregations used for reporting (Target/Aggregate levels).
  - Integrate FS-inspired data where possible to improve confidence in habitat statistics and support change detection.
- Recommendations for data management:
  - Maintain clear metadata about resolution, MMU, date range, and BH/Target/class definitions.
  - Track known biases (e.g., underestimation of peat/bog areas, rough grassland classifications) to inform interpretation and decision-making.
  - Consider higher-resolution or multi-temporal data to enhance detection of smaller features and to refine specific BH distinctions.
  - Foster integration with external datasets and field surveys to improve accuracy and utility for policy and planning.

## Appendix and mapping context (high-level)
- Appendix I outlines distinguishing features and limitations for each Broad Habitat class relative to LCM2000 mapping, including notes on woodland types, arable/grassland distinctions, and challenges in semi-natural vs improved grasslands, wetland classifications, and coastal habitats.
- Table 2 demonstrates mapping codes and color mappings linking LCM2000 variants to BHs for visualization.