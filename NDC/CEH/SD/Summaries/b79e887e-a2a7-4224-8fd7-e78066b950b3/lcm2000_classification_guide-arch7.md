# LCM2000 Final Report

- Provides a comprehensive overview of the LCM2000 project, its Broad Habitat (BH) framework, classification scheme, calibration with CS2000 field survey data, and assessments of map accuracy and change detection.
- Aims to support UK biodiversity planning by mapping widespread terrestrial, freshwater, and coastal BHs, and to relate spectral classifications to user-relevant land-cover categories.

## Background and aims

- UK Biodiversity Group adopted Broad Habitats to cover the range of UK habitats; LCM2000 aimed to map widespread BHs using satellite-derived spectral data with external context where possible.
- The classification combines spectral classes into thematic components, then into BHs, Target classes, Subclasses, and Variants; aggregate classes (10-class level) align with BH aggregations for reporting.
- The study emphasizes consistent UK-wide mapping, while allowing detailed subclass and variant distinctions for broader usability.

## Broad Habitats and LCM2000 classification

- BHs are defined conceptually; Target classes are the nearest consistently mappable matches from spectral data; Subclasses and Variants refine those classifications where feasible.
- Map displays generally present Target classes; Subclasses and Variants may be shown where useful and separable.
- Key relationships:
  - BHs map to broader habitat types (e.g., Broadleaved woodland, Coniferous woodland, Arable and horticulture).
  - Subclasses/Variants capture finer distinctions (e.g., Bracken, Open dwarf shrub heath, Wet/dry bog, Neutral vs Calcareous grasslands).
  - Aggregate 10-class level provides a practical basis for national/regional reporting where exact BH matches are challenging.
- Several habitat types present mapping and interpretation challenges (e.g., Wet/dry bog vs dwarf shrub heath, Neutral vs Calcareous vs Acid grasslands, rough grasslands).

## Map display conventions

- Cartographic display uses colors designed for national/regional plots; some rare or highly disaggregated BHs are aggregated for readability.
- Coastal BHs are largely aggregated, with some Subclasses distinguished where useful.
- Distinctions between BHs are constrained by resolution (1 km imagery), with some BHs treated as aggregates for display and analysis.

## Calibration with CS2000 field survey data

- CS2000 field survey tested LCM2000 against ground-based observations to:
  - Assess correspondences and map-accuracy in a broad sense
  - Calibrate LCM2000 to FS data to derive BH cover statistics comparable to field surveys
- CS2000 sampled 569 one-kilometre squares (1998: 549; 1999: remainder); FS data are more detailed but not direct ground truth.
- Key outcome: calibration, not validation; recognition that upland boundaries are difficult to map reproducibly.

## GIS operation and tests

- Arc/Info coverage files were created for all 569 CS2000 squares and equivalent LCM2000 map sections.
- Three main tests for correspondence:
  - Per-pixel: direct overlay without structural adjustments
  - Per-segment: LCM2000 segment labels compared to FS-dominant FS class
  - Per-parcel: FS parcels labeled against LCM2000-derived parcel labels
- Correspondences calculated at multiple thematic levels:
  - BH level (excluding Boundaries/linear features and some rivers/streams)
  - Generalised urban vs non-urban mapping
  - Target class level
  - Aggregate class level
- Bootstrapping used to estimate 95% confidence limits for correspondence measures.

## Confidence and results

- Overall correspondence is not a ground-truth accuracy measure (FS is not ground truth); differences arise from resolution, timing, class definitions, and data structure.
- By region and level:
  - Per-pixel (BH level): GB 54% (CI 53–56%); England & Wales 60% (58–62%); Scotland 44% (40–47%).
  - Per-parcel: GB 62% (60–64%); England & Wales 69% (67–72%); Scotland 48% (44–52%).
  - Per-segment: GB 58% (57–60%); England & Wales 64% (62–66%); Scotland 47% (43–50%).
  - Target class level: GB 65%; England & Wales 73%; Scotland 51%.
- FS repeatability about 88%; LCM2000 performance is assessed as ~72% of maximum potential given data differences and MMU contrasts.
- Key causes of mismatch:
  - FS higher spatial resolution vs 25 m pixels in LCM2000
  - Time differences between FS (1998/1999) and LCM2000 imagery (1998–2001)
  - Differences in class definitions and practical mapping constraints
  - Minimum mapping unit (MMU) differences (FS >0.04 ha vs LCM2000 >0.5 ha)
- Overall, LCM2000 is believed to record Target classes with roughly 87% success; around 85% accuracy at the Target class level is a realistic expectation.

## Habitat-by-habitat findings and discussion

- Broadleaved/mixed woodland and Coniferous woodland: similar UK cover, but direct BH-level agreement is lower due to small woodland patches and MMU effects; coniferous woodland shows higher direct correspondence (70%).
- Arable and horticultural land: LCM2000 slightly overestimates relative to FS; misclassifications between arable, horticultural, grassland, and built-up areas occur, partly due to rotation timing and spectral ambiguity.
- Improved grassland vs semi-natural grassland: LCM2000 generally recognises improved grassland, but distinctions between improved and semi-natural are challenging; around 20% of FS-improved grassland is mapped as semi-natural by LCM2000.
- Semi-natural grasslands, bracken, fens, marshes, and bogs: greatest classification challenges; significant differences largely driven by peat-depth (bog) criteria and spectral masking; many rough grasslands are grouped into Neutral grassland by LCM2000, while FS distinguishes improved roughness.
- Bracken and Montane/Inland bare ground: bracken often underrepresented in imagery; montane and inland bare ground show discrepancies due to altitude-based definitions and detection limits; peat depth deeply influences bog vs heath classification.
- Water bodies and built-up areas: inland water mapped with >0.5 ha threshold; standing water and canals often conflated with other classes; built-up areas show heterogeneity (urban cores vs vegetated open spaces) and are divided into Continuous urban and Suburban/rural developed categories.
- Coastal BHs: supralittoral and littoral zones are small and often below resolution; treated as aggregates for reporting, with less reliability at pixel-level separation.

## Data structure and table references

- Table 2 maps LCM2000 class Variants to Broad Habitats, including color schemes and alpha-numeric codes. This demonstrates the detailed crosswalk between spectral/variant classes and BHs used for reporting and analysis.
- Appendix I (Brief review of Broad Habitats) provides distinguishing features and notes on practical mapping limitations for a wide range of BHs (e.g., woodland, grasslands, bracken, bogs, fens, heath, water, and urban/built-up types).

## Change detection and future work

- Detecting landscape changes between LCMGB 1990 and LCM2000 is anticipated to be challenging due to small overall changes and higher error rates.
- Satellite-based mapping alone cannot guarantee consistent change detection; intelligent, integrated approaches are proposed (e.g., using FS trends (Haines-Young et al. 2000) to guide interpretation, and calibrating change evidence against known patterns).
- Calibration results identify under- and over-estimations that should inform change analyses; future work aims to improve BH statistics through direct calibration against field data and integration with external datasets.

## Appendix I: Distinguishing features (high-level)

- Broad Habitat distinctions (e.g., broadleaved/mixed woodland, coniferous woodland, arable, improved vs neutral grassland, bogs, heaths, fen/marsh, water, urban, coastal) are difficult to resolve spectrally at 1 km resolution.
- In many cases, auxiliary context (soil, peat depth, pH, land-use history) is necessary to distinguish otherwise spectrally similar classes.
- Specific notes on problematic areas (e.g., bogs on deep peat, neutral vs calcareous vs acid grasslands, rough grasslands, and bracken) inform potential refinements and follow-up data integration.