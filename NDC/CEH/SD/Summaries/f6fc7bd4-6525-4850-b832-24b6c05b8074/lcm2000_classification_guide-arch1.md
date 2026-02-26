CENTRE FOR ECOLOGY AND HYDROLOGY (NATURAL ENVIRONMENT RESEARCH COUNCIL) Project. T02083j5/C00878 CSLCM/Final

## Background and Objective
- LCM2000 is a thematic classification of spectral data from satellite imagery aiming to map Broad Habitats (BHs) across the UK to support the UK Biodiversity Action Plan.
- BH framework (developed by JNCC) encompasses terrestrial, freshwater, and coastal habitats; LCM2000 maps BHs and associated land-cover details where possible.
- The mapping uses spectral classes that can be combined into thematic components and aggregated into various schemes; BHs are the primary target, with additional details captured as Subclasses and Variants when feasible.
- Map displays use a national/regional scale with aggregated displays to balance reliability and pattern visibility; some rare or highly dissected classes are merged for clarity.

## Broad Habitats and LCM2000 Classes
- Spectral Target Classes are mapped into Subclasses and Variants; alignment with BHs is sought but not always exact, due to differences in definitions and practical mapping limits.
- Variants represent thematic components of Target Classes and Subclasses; aggregate classes combine Target Classes and Subclasses to a 10-class level for reporting.
- Spectral-context mismatches can occur (e.g., Bog vs. Dwarf shrub heath; neutral vs. calcareous vs. acid grasslands); some land-cover types are difficult to distinguish spectrally, requiring contextual or ancillary data.
- Specific BHs (e.g., Bracken, Fen/Marsh/Swamp, Montane, Inland Bare Ground, Coastal BHs) present notable mapping challenges and are treated with appropriate aggregations or special handling in maps and statistics.
- Coastal and inland-water classifications are aggregated or simplified at national scales due to relatively small extents and resolution limits; linear features and boundaries are treated differently (FS data include them; LCM2000 does not target them as BHs).

## Map Display Classes
- Cartographic conventions emphasize reliability and pattern visibility; some BHs are aggregated (e.g., inter-tidal and supra-littoral components) to suit map resolution.
- Subclasses may be shown where useful, such as Dense/Open Dwarf Shrub Heath, Saltmarsh, and Urban/Developed components.
- The display and reporting use both BH nomenclature and corresponding LCM2000 classes, with consistent mapping to support interpretation.

## CS2000 Field Survey (FS) and Calibration Purpose
- CS2000 FS data provide a basis to assess LCM2000 quality and to calibrate LCM2000 to produce BH cover statistics equivalent to FS outputs.
- FS covered 569 one-kilometre squares in GB (1998-1999; NI data not yet digital for testing) and recorded much more detail than LCM2000.
- FS is not ground truth; an independent QA study showed 88% repeatability for primary FS codes used to derive BH labels.
- The calibration approach compares FS vs LCM2000 across per-pixel, per-segment, and per-parcel levels to understand correspondence and guide calibration.

## GIS Operation and Tests
- ARC/Info coverage files were created for all 569 FS squares and equivalent LCM2000 map-sections; 569 correspondence matrices were produced (one per 1-km square).
- Three main tests:
  - Per-pixel: direct overlay comparisons to capture all spatial differences.
  - Per-segment: LCM2000 segment labels vs. FS-dominant FS class for each segment.
  - Per-parcel: FS parcels vs. LCM2000-derived parcel labels.
- Correspondences were analyzed at multiple thematic levels:
  - BH level (excluding some features like boundaries and rivers/streams)
  - Generalised urban vs. non-urban distinctions
  - Target class level
  - Aggregate class level (close matches with FS)

## Confidence Limits for Measures of Correspondence
- A bootstrapping procedure estimated 95% confidence intervals for correspondence across GB, England/Wales, and Scotland.
- Overall GB results (example figures):
  - Per-pixel: ~54% correspondence (CI ~53–56%)
  - Per-segment: ~58% (CI ~57–60%)
  - Per-parcel: ~62% (CI ~60–64%)
- England & Wales generally higher than Scotland:
  - Per-pixel: 60% (CI ~58–62%)
  - Per-parcel: 69% (CI ~67–72%)
  - Per-segment: 64% (CI ~62–66%)
  - Scotland typically lower (e.g., per-pixel ~44%, per-parcel ~48%, per-segment ~47%)
- Differences arise from FS’s finer original resolution, time differences, class-definition differences, and survey errors; higher-level Target class and aggregate-level correspondences are larger than BH-level matches.

## LCM2000 Assessments at Class Level
- Assessments are aggregated by Land Class (GB, England/Wales, Scotland) and presented for:
  - Broadleaved/mixed woodland and Coniferous woodland: UK cover around 6.3% (LCM2000) vs 6.2% (FS); direct agreement lower (roughly 44%) due to MMU limits (FS records many small woodlands; LCM2000's 0.5 ha MMU excludes many small patches).
  - Arable and horticultural land: LCM2000 ~23.4% vs FS ~21.5%; misclassifications often occur between arable and improved grassland or between arable and built-up areas.
  - Improved grassland: ~25.7% (LCM2000) vs FS ~25.8%; generally well-classified, but distinguishing from semi-natural grassland is challenging; about 20% of FS-improved grassland is recorded by LCM2000 as semi-natural.
  - Semi-natural grasslands, Neutral/Calcareous/Acid grasslands: difficult to separate; issues stem from spectral similarity, soil pH masking, and management practices; LCM2000 uses a peat-depth-based approach to differentiate bog from dwarf shrub heath, but this can underrepresent peatlands relative to FS.
  - Bracken, Dwarf shrub heath, Fen/marsh/swamp, Bogs (deep peat): substantial mis-match due to classification differences (peat-depth control, indicator species, and spectral limitations).
  - Montane habitats, Inland bare ground, Water (inland), Built-up areas and gardens: varying degrees of agreement; water bodies of >0.5 ha generally well-mapped, but inland bare ground is often overrepresented in LCM2000 due to thresholding and urban context treatment.
  - Coastal habitats (supra-littoral and littoral): treated as aggregates for reporting; coastal mapping is constrained by small extent and resolution.
  - Boundary and linear features: not targeted by LCM2000 as distinct BHs; FS retains them as discrete features.

## LCM2000 Accuracy
- The stated correspondence is not a direct accuracy measure since FS is not ground truth; differences arise from resolution, data structure, timing, and class definitions.
- At BH level, per-parcel correspondence is ~63.4% (GB), reflecting exclusions of Boundary/linear features and rivers/streams and FS generalisations.
- Estimated potential maximum accuracy is around 87% for Target classes; overall target-class accuracy around ~85% is considered realistic given the data limitations.
- Key drivers of mismatch:
  - 25 m parcel grid vs FS’s finer detail
  - FS MMU of >0.04 ha vs LCM2000 MMU of >0.5 ha
  - Temporal differences between field surveys (1998) and satellite imagery (1998–2001)
  - Inherent differences in classification schemes and context

## Change Detection
- Detecting landscape changes between years is challenging with satellite data alone due to limited precision and inherent classification differences.
- Real 1990–2000 changes likely exist but are small and often obscured by errors.
- An intelligent approach is recommended: leverage FS change measures (e.g., 1990 vs. 1998) and known change patterns to distinguish true change from classification error.
- Calibration results highlight under- and over-estimates in 2000 that should inform change analyses, and ongoing work will integrate LCM2000 with FS and additional data sources.

## Data and Appendix Notes
- Full methodological details, image selection, class definitions, pre-processing, and calibration are documented in the Final Report (mid-March release referenced).
- Table 2 maps LCM2000 Variants to BHs with color codes; Appendix I provides a concise review of Broad Habitats and distinguishing features in relation to LCM2000 mapping.
- The study emphasizes the need for integrated analysis and future refinement using LCM2000 data in combination with field survey data to improve broad habitat statistics and mapping accuracy.