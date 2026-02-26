# CSLCM/Final

## Aim and context
- Purpose: support implementation, reporting, and decision-making under the UK Biodiversity Action Plan (BAP) by using Broad Habitats (BHs) to cover the full range of UK habitats.
- LCM2000: a thematic classification of satellite spectral data, designed to map BHs with context from external datasets; outputs can be aggregated to BHs, Target classes, Subclasses, and Variants, with Aggregate 10-class levels for reporting.
- Calibration objective: assess how well LCM2000 corresponds to CS2000 field survey data (CSLCM/Final) and develop BH statistics from LCM2000 with field-survey precision.

## Data sources and classification framework
- Data types:
  - LCM2000: satellite-derived spectral classes refined with context data.
  - CS2000 field survey (FS): detailed 1998–1999 ground-truth style data used for calibration.
  - External datasets (e.g., peat maps) and context corrections.
- Classification levels:
  - Broad Habitats (BHs) with associated Target classes and Subclasses.
  - Variants: finer spectral/contextual components.
  - Aggregate classes: simplified 10-class level aligning with BH aggregations for reporting.
- Map displays: cartographic conventions to balance reliability and pattern visibility; some BHs aggregated for national/regional plots.

## Methodology and calibration approach
- Objectives:
  - Measure correspondences between CS2000 FS and LCM2000 to assess map accuracy at multiple thematic levels.
  - Calibrate LCM2000 to FS to enable BH cover-statistics comparable to FS data.
- Tests and comparisons:
  - Per-pixel: direct overlay of FS vs. LCM2000.
  - Per-segment: LCM2000 segment labels vs. FS-dominant FS class.
  - Per-parcel: FS parcels labeled against LCM2000-derived parcel classes.
- Correspondence levels (GB, England&Wales, Scotland) evaluated across:
  - BH-level (excluding boundaries/linear features and rivers/streams),
  - Target-class level,
  - Aggregate-class level.
- Confidence: bootstrap-based 95% confidence limits to quantify variation in correspondence.

## Key results and interpretation
- Overall correspondence (by level, GB and regions):
  - Per-pixel (BH level): GB 54% (CI 53–56%), England&Wales 60% (CI 58–62%), Scotland 44% (CI 40–47%).
  - Per-segment: GB 58% (57–60%), England&Wales 64% (62–66%), Scotland 47% (43–50%).
  - Per-parcel: GB 62% (60–64%), England&Wales 69% (67–72%), Scotland 48% (44–52%).
  - Target-class level (parcels): GB 65% (overall), England&Wales 73%, Scotland 51%.
- Observations:
  - Mismatches arise from FS vs. LCM2000 differences in spatial resolution, survey timing, and class definitions.
  - The 0.5 ha > 0.04 ha MMU mismatch and the 25 m pixel grid contribute to systematic differences, particularly for small patches.
  - Segmentation and labeling adjustments (FS mosaic vs. LCM2000 segmentation) affect outcomes, especially in complex landscapes (e.g., woodlands, arable vs. grassland).
- Habitat-specific insights:
  - Broadleaved/mixed and Coniferous woodland: similar cover, but small woodlands frequently fall below LCM2000’s minimum mapping unit, causing mismatches with FS.
  - Arable and horticultural land: LCM2000 generally aligns with FS but some misclassification between arable and grassland or improved vs. semi-natural grasslands occurs.
  - Semi-natural grasslands, neutral/calcareous/acid grasslands: spectral separation is challenging; significant differences attributed to management, derelict swards, and peat/soil context corrections.
  - Bracken, fen/marsh/swamp, bogs: substantial discrepancies linked to peat depth criteria, context maps, and differing field definitions; peat depth and soil acidity masks drive classifications.
  - Montane, inland bare ground, coastal BHs: distinct interpretation issues (altitude-based thresholds, peat-related bog delineation, coastal masking, and marine-perimeter complexities).
- Accuracy perspective:
  - FS is not ground truth; 88% repeatability for FS primary codes limits definitive accuracy.
  - LCM2000 is estimated to achieve around 87% accuracy at the Target-class level; overall, about 72% of maximum potential accuracy when accounting for FS limitations and MMU differences.

## Change detection and future directions
- Change detection with satellite data alone is unlikely to achieve the precision needed for robust landscape-change inference.
- An intelligent, integrated approach is recommended:
  - Use historical FS data (e.g., 1990, 1998) to guide interpretation of differences.
  - Combine calibration insights with new data to distinguish real change from classification or data-product error.
- Planned follow-up:
  - Full details of image selection, processing, classification, and calibration in the Final Report.
  - Direct calibration to generate Broad Habitat statistics, leveraging FS precision with LCM2000's coverage.

## Data governance, metadata, and practical considerations for monitoring frameworks
- Data sharing and transparency:
  - Public sharing of underlying data is a recurring barrier; governance processes needed to facilitate open data while respecting constraints.
- Metadata and data quality:
  - Shortcomings in metadata impede verification; adding metadata and robust data management at source is essential.
- Data accessibility and silos:
  - Silos within/between organizations hinder data flow; efforts to foster data integration and governance are critical.
- Data timeliness and updates:
  - Keeping data up to date is a recognized challenge; timely data updates are necessary to maintain relevance for monitoring and decision-making.

## Appendix highlights: Broad Habitat distinctions and mapping challenges
- Key mapping issues and distinguishing features for BHs versus LCM2000 mappings:
  - Woodland (Broadleaved/mixed, Coniferous): spectral classification often struggles with small stands and variable canopy, leading to underrepresentation or misclassification.
  - Arable vs Improved vs Semi-natural grasslands: spectral signals can be ambiguous; contextual/field data improve distinctions but remain imperfect.
  - Neutral, Calcareous, and Acid grasslands: no consistent spectral signature; reliance on soil acidity and peat context is necessary but imperfect.
  - Bracken, Dwarf shrub heath, Fen/marsh/swamp, Bog: complex habitat definitions; peat depth, indicator species, and local context influence classification outcomes.
  - Inland bare ground and Coastal habitats: confusion with urban/industrial contexts and sublittoral/coastal distinctions; resolution and contextual corrections affect accuracy.
  - Boundary/linear features: not targeted by LCM2000 at the BH level; FS captures these more completely, influencing calibration results.
- Practical implication:
  - Detailed BH definitions and region-specific considerations are essential for accurate interpretation, calibration, and subsequent BH statistics generation.

## Conclusions for monitoring framework authors
- LCM2000 provides broad, nationwide habitat coverage but requires careful calibration against high-quality field data to produce reliable BH statistics.
- Calibration reveals systematic differences driven by resolution, timing, and classification definitions; these must be accounted for in monitoring frameworks.
- An integrated approach that combines FS-like ground-truth insights with satellite-derived maps, plus robust metadata, data governance, and transparent data sharing, will enhance the usefulness of BH metrics for policy evaluation and decision-making.
- Change detection should be pursued with intelligent, data-integrated strategies that leverage historical survey data to separate real landscape change from product errors.