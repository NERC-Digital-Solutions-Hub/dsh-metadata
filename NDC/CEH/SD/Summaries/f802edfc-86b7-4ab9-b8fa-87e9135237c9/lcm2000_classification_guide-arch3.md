# LCM2000 Final Report

## Background and purpose
- LCM2000 is a thematic, satellite-based land cover classification designed to map Broad Habitats (BHs) to support the UK Biodiversity Action Plan.
- BHs are defined by JNCC; LCM2000 aims to distinguish BHs where possible, using Target classes, Subclasses, Variants, and aggregate 10-class reporting when appropriate.
- The mapping balances spectral information with contextual data from external datasets; some BH distinctions are challenging or not possible at the 1 km resolution.
- The report emphasizes the need to clarify and standardise data definitions, aggregation, and communication of results for monitoring purposes.

## Data and classification structure
- BHs are mapped via a hierarchical system: Broad Habitats, with Target classes, Subclasses, and Variants; aggregate classes are used for reporting where needed.
- Spectral (imaging) data are combined with contextual information; mismatches between BH definitions and spectral/read-across to Target classes are common in several habitat types (e.g., bogs, neutral/calcareous/acid grasslands).
- Some BHs are small or fragmented (e.g., woodland stands under minimum mappable unit), leading to differences between field data and map representations.
- Coastal and boundary/linear features are treated differently due to resolution and definitional constraints; some features are aggregated for display and reporting.

## Calibration data and methods
- CS2000 field survey data (CSLCM) provided a basis to assess LCM2000 map accuracy and calibrate BH statistics. It covered 569 one-kilometre squares in GB (1998–1999; NI data not digital yet).
- CS2000 data are not “ground truth” but provide a calibration framework; an independent QA study showed 88% repeatability for primary FS codes.
- Three main comparison modes were used:
  - Per-pixel comparisons (overlay of FS and LCM2000)
  - Per-segment comparisons (dominant FS class within LCM2000 segments)
  - Per-parcel comparisons (FS parcels vs. LCM2000-derived labels)
- Confidence limits were estimated with bootstrapping to produce 95% ranges for correspondence estimates.

## Calibration results and accuracy
- Overall correspondence (GB) varies by level and country:
  - Per-pixel: ~54% (GB); ~60% England/Wales; ~44% Scotland
  - Per-segment: ~58% (GB); ~64% England/Wales; ~47% Scotland
  - Per-parcel: ~62% (GB); ~69% England/Wales; ~48% Scotland
  - Target class level (higher agreement): ~65% GB (parcel); ~73% England/Wales; ~51% Scotland
- BH-level correspondence is affected by several factors:
  - Resolution differences: FS uses finer detail; LCM2000 MMU is 0.5 ha vs FS ~0.04 ha
  - Time differences between surveys (FS mainly 1998; LCM2000 1998–2001)
  - Definitions and class boundaries misalignments between FS and LCM2000
  - Misclassification across large class groups (arable vs grassland; improved vs semi-natural grassland; bogs vs heath)
- Segment-based classification improves agreement relative to pixel-based assessments but still reflects segmentation and resolution constraints.
- Overall, LCM2000 is estimated to achieve around 87% accuracy at the Target class level (considering constraints and FS repeatability limits).

## Class-level findings and issues
- Broadleaved/mixed woodland and coniferous woodland show similar total cover but limited direct agreement in field vs map due to under-recording of small woodlands and misalignment of boundaries.
- Arable and horticultural land: LCM2000 often overestimates relative to FS due to mapping of small features and rotation differences; partial misclassification between arable and grassland is a contributor.
- Improved vs semi-natural grassland: FS tends to distinguish between semi-natural and improved swards; LCM2000 often records rough grass as Neutral grassland, causing substantial differences in some areas.
- Neutral, calcareous, and acid grasslands: spectral data struggle to consistently separate these; spectral masking by soil acidity reduces discrimination accuracy.
- Bracken, dwarf shrub heath, bogs (deep peat), fen/marsh/swamp, montane habitats, inland bare ground: significant mismatches driven by spectral limitations, peat-depth context, altitude-based rules, and contextual corrections. Some distinctions (e.g., peat depth for bogs) led to conservative estimates and potential misclassifications.
- Coastal BHs and water-related habitats: small, often near-resolution limits; aggregation is used for reporting; intertidal areas present particular mapping challenges.
- Boundary and linear features: not targeted by LCM2000 as distinct BHs; field data capture these, but they are excluded from calibration at the BH level.

## Change detection
- Detecting landscape change between 1990 and 2000 requires high precision beyond satellite mapping alone; segment-based approaches differ from 1990 raster products.
- Real changes likely exist but are hard to separate from data/product differences.
- A more intelligent, blended approach is recommended, using earlier FS data (e.g., Haines-Young et al. 2000) to guide interpretation of mapped differences.
- Future work includes integrating LCM2000 with FS and external datasets to better quantify changes and calibrate Broad Habitat statistics.

## Implications for monitoring frameworks
- Calibrating broad habitat statistics through direct comparison with field surveys enables leveraging the comprehensive coverage of LCM2000 with the precision of field observations.
- Data governance considerations:
  - The need for consistent metadata, transparent definitions, and documented calibration procedures to support reproducibility and comparability over time.
  - Data sharing and openness remain important, even when public release poses challenges; aggregation and variant-level detail can help balance utility with accessibility.
- Methodological guidance for monitoring programs:
  - Use aggregated BHs or Target classes when high-resolution class-level accuracy is not achievable.
  - Apply multi-level validation (pixel, segment, parcel) to understand where accuracy is adequate for monitoring needs.
  - Be cautious with time-lag effects and MMU differences when interpreting change over time.
  - Consider integrating additional datasets and contextual information to improve discrimination among biologically similar habitats.
- Recommendations for future iterations:
  - Re-examine bogs, heath, montane, and peat-related classes with integrated LCM2000, FS, and external peat/soil data.
  - Enhance knowledge-based corrections to bridge FS-LCM2000 differences.
  - Develop direct calibration workflows to produce Broad Habitat statistics grounded in field observations.

## Appendix I: Broad Habitats and distinguishing features (LCM2000 mapping)
- Provides detailed notes on each Broad Habitat category and the practical limitations of distinguishing them via spectral data, including:
  - Broadleaved/mixed woodland and coniferous woodland distinctions
  - Arable vs horticultural and the role of seasonal imagery
  - Improved vs semi-natural grasslands and the influence of management
  - Neutral, calcareous, and acid grasslands and soil pH masking
  - Bracken, dwarf shrub heath, fen/marsh/swamp, bogs, Montane, and Inland bare ground
  - Coastal habitats, standing water, rivers/streams, and urban/built-up areas
- Emphasizes that some spectral distinctions are not robust at 1 km scale and that context, peat depth, altitude, and other ancillary data are critical for improving accuracy.