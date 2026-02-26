# LCM2000: Calibration and Assessment of Broad Habitats in Great Britain

## Overview and purpose
- Aimed to support the UK Biodiversity Action Plan by mapping Broad Habitats (BHs) across the UK.
- LCM2000 is a thematic classification of satellite-derived spectral data, designed to distinguish BHs and provide context from external datasets.
- Classifications are organized into Target classes, Subclasses, and Variants, with Aggregate (10-class) levels for reporting that align with BH groupings.
- Map displays balance reliability with pattern visibility; some rare BHs are aggregated at regional/national scales.

## Data structure and classification
- BHs are mapped indirectly via spectral and contextual read-across to Target classes; Subclasses and Variants provide finer detail where feasible.
- Distinctions among BHs and LCM2000 classes can differ; nomenclature and read-across rules guide interpretation.
- Map-display classes reflect practical reporting needs; Subclasses may be shown below BH level when useful and accurate.
- Coastal, boundary/linear features, and some small patches are treated specially or aggregated due to resolution limits.

## Calibration with CS2000 field survey
- CS2000 field survey collected data in 569 one-kilometre squares across Great Britain (1998–1999; NI data not yet digital for testing).
- Field data are detailed but not treated as “ground truth”; an independent QA study reported 88% repeatability for primary codes used to create BH labels.
- Calibration approach vs validation: inter-comparison used to calibrate LCM2000 against CS2000, acknowledging resolution and timing differences.

## Methodology and assessments
- ARC/Info GIS workflow produced BH-labeled map sections for direct comparison with CS2000 squares.
- Three main tests:
  - Per-pixel: direct overlay differences across 25 m pixels.
  - Per-segment: compare LCM2000 segment dominance against CS2000 class.
  - Per-parcel: compare CS2000 parcels with LCM2000-derived labels.
- Correspondences evaluated at multiple thematic levels:
  - BH level (with some features generalized or excluded)
  - Target class level
  - Aggregate class level
- Confidence estimates created via bootstrapping (95% interval estimates) for GB, England/Wales, and Scotland.

## Key results: overall accuracy and patterns
- Per-pixel correspondence (BH level): GB 54% (95% CI 53–56%), England/Wales 60% (58–62%), Scotland 44% (40–47%).
- Per-segment correspondence (BH level): GB 58% (57–60%), England/Wales 64% (62–66%), Scotland 47% (43–50%).
- Per-parcel correspondence (BH level): GB 62% (60–64%), England/Wales 69% (67–72%), Scotland 48% (44–52%).
- Target-class correspondence (per-parcel): GB 65%, England/Wales 73%, Scotland 51% (differences largely due to bog-heath confusion and upland mapping challenges).
- Aggregate-class results show closer alignment to CS2000, illustrating better agreement when broad groupings are used.

## Habitat-specific findings and issues
- Broadleaved/mixed woodland and Coniferous woodland: overall woodland area similar between LCM2000 (6.3%, 5.8%) and CS2000; many small woodlands fall below LCM2000’s minimum mappable unit (MMU), causing misalignments with CS2000 classifications.
- Arable and horticultural land: LCM2000 ~23.4% vs CS2000 ~21.5%; about 70% of LCM2000 arable matches CS2000 arable; some confusion with grassland and improved grassland due to rotation and spectral similarity.
- Improved vs semi-natural grasslands: ~20% of CS2000 Improved grassland is mapped as semi-natural by LCM2000; grassland classification is sensitive to management and spectral signature.
- Neutral, Calcareous, and Acid grasslands: difficult to separate spectrally; peat depth and soil pH context used in corrections, but there is a general poor match without integrating soil/mgmt data.
- Bracken, Dwarf shrub heath, Bogs: notable differences due to BH definitions and spectral/peat depth criteria; bog mapping relies on peat-depth context and can diverge from field-based definitions.
- Fen, marsh, swamp and related wetland types: FS records more extensive occurrence than LCM2000; rush pastures can be inconsistently categorized between datasets.
- Montane and Inland bare ground: altitude-based callbacks and peat/rock distinctions complicate alignment; inland bare ground often associated with urban context in CS2000 but mapped differently in LCM2000.
- Water (inland): generally mapped with a >0.5 ha threshold; standing water often aligns with CS2000, but smaller water bodies are excluded in LCM2000 calculations.
- Built up areas and coastal habitats: urban open spaces and vegetation heterogeneity captured differently; coastal BHs are small and often aggregated for national/regional displays.
- Boundary and linear features: CS2000 captures many linear features; LCM2000 did not target these as BHs, contributing to systematic differences in calibration.

## Change detection and future directions
- Detecting landscape changes between 1990 and 2000 is challenging with satellite data alone due to resolution, timing, and class-definition differences.
- Proposed approach: combine LCM2000 with CS2000 and FS-based change indicators; use intelligent, pattern-based methods to distinguish real changes from classification errors.
- Future work includes generating Broad Habitat statistics through direct calibration against field data, refining variant-level distinctions, and integrating multiple data sources for improved accuracy.

## Practical implications for GIS work
- LCM2000 provides broad, nationwide coverage with consistent 25 m-scale mapping, suitable for map-based products and regional analyses, but with acknowledged accuracy limitations at finer class levels.
- For policy or planning applications requiring precise habitat boundaries or small patches, use caution and consider integrating field data (CS2000/FS) and ancillary soil or management information.
- Aggregate BHs offer more reliable outputs for reporting, while individual Target/Subclass/Variant distinctions should be used with awareness of spectral/field-consultation limitations.

## Appendix highlights
- Table 2 maps LCM2000 Variants to BHs with color codes, illustrating how specific spectral variants relate to broad habitat groupings.
- Appendix I reviews distinguishing features and limitations for each Broad Habitat, emphasizing spectral ambiguity, peat-depth contexts, soil pH corrections, and the challenge of remotely sensing certain semi-natural or management-influenced swards.