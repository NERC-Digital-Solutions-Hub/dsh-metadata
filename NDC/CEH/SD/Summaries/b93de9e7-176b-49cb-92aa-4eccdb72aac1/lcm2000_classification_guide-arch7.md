LCM2000 Final Report

- Purpose and scope
  - Develop Broad Habitat (BH) framework to support UK Biodiversity Action Plan (BAP) reporting.
  - Use LCM2000 as a thematic, satellite-derived classification that can be complemented by external datasets to better reflect terrestrial, freshwater, and coastal habitats.
  - Provide map displays and statistics at multiple aggregation levels, aligning spectral target classes and Subclasses with BHs where possible.
  - Distinguish Target classes, Subclasses, and Variants, while offering aggregated 10-class levels for reporting.

- Classification framework
  - Broad Habitats (BHs) are core categories describing large-scale habitat types.
  - LCM2000 classes are spectral-derived and mapped consistently across the UK; Target classes and Subclasses refine BHs where feasible, with Variants capturing finer details (e.g., specific crops, management states).
  - Relationship notes
    - Target classes and Subclasses aim to match BHs, but exact equivalence can differ due to definitions and data sources.
    - Aggregate classes combine Target/Subclass information to align with BHs for reporting.
  - Map display conventions
    - Cartographic choices balance reliability with pattern visibility.
    - National/regional displays aggregate rare/dissected classes; Subclass and Variant levels may be shown where useful.

- Data and calibration approach
  - CS2000 field survey data used to assess and calibrate LCM2000 against ground-truth-like information.
  - 569 one-kilometre squares sampled in GB (549 in 1998, remainder in 1999); NI data not yet digitally available for testing.
  - Calibration rather than strict validation due to differences in resolution, timing, and field vs. remote-sensing classification approaches.
  - ARC/Info vector mapping prepared for each square; comparisons produced matrices at several thematic levels:
    - Per-pixel: direct overlay comparisons.
    - Per-segment: segment-dominant FS class vs. LCM2000 segmentation.
    - Per-parcel: FS parcels vs. LCM2000-derived parcel labels.
  - Confidence estimation via bootstrapping to generate 95% intervals for correspondence measures.

- Key results and accuracy indicators
  - Overall correspondence (GB) at BH level
    - Per-pixel: ~54% (95% CI 53–56%)
    - Per-segment: ~58% (CI 57–60%)
    - Per-parcel: ~62% (CI 60–64%)
  - England & Wales
    - Per-pixel: ~60% (CI 58–62%)
    - Per-segment: ~64% (CI 62–66%)
    - Per-parcel: ~69% (CI 67–72%)
  - Scotland
    - Per-pixel: ~44% (CI 40–47%)
    - Per-segment: ~47% (CI 43–50%)
    - Per-parcel: ~48% (CI 44–52%)
  - Target class level (parcels)
    - GB: ~65% (higher when aggregating urban/generalisation differences)
    - England & Wales: ~73%
    - Scotland: ~51%
  - General interpretation
    - Per-pixel measures are the most variable due to resolution and boundary issues.
    - Parcel- and Target-class-level correspondences improve as spatial resolution differences are mitigated by aggregation.
    - The 225 m–500 m scale generalization and MMU differences (FS ~0.04 ha vs LCM2000 >0.5 ha) contribute significantly to mismatches.
  - Overall assessment
    - LCM2000 is estimated to capture Target classes at about 85–87% accuracy relative to the best possible given data constraints; accuracy improves at aggregate/Target levels compared with strict BH-level per-pixel matches.

- Detailed findings by habitat type (representative notes)
  - Woodlands
    - Broadleaved/mixed woodland: similar area estimates between LCM2000 and FS, but direct agreements are limited due to small stands often falling below LCM2000’s minimum mapping unit (MMU); small trees/copses may be mapped as non-woodland elsewhere.
    - Coniferous woodland: higher direct correspondence; blocks are larger and more distinct; overall coverages similar.
  - Arable and horticultural land
    - LCM2000 slightly higher overall; ~70% of LCM2000 arable corresponds to FS arable; confusion with grassland/Improved grassland and rotation differences can cause misclassifications.
  - Grasslands
    - Improved vs semi-natural grasslands: FS often maps improved grassland where LCM2000 sees semi-natural or neutral grasslands; roughly 20% of FS improved grassland is mapped as semi-natural by LCM2000.
    - Neutral, Calcareous, and Acid grasslands: difficult to separate spectrally; soil acidity (pH) maps used as a contextual correction, but spectral limitations persist.
  - Rough grasslands, bracken, fen/marsh, bogs
    - Distinctions among Neutral/Calcareous/Acid grasslands, and between bogs and dwarf shrub heath, are challenging; peat depth and context are critical controls in LCM2000.
    - Bracken is treated as a subclass feature rather than a BH target; field data often show bracken on open ground that may be misclassified spectrally.
    - Fen, marsh, and swamp: FS records more extensive occurrence than LCM2000; rush pastures influence spectral signatures and are handled differently in the two datasets.
  - Heath and montane
    - Dwarf shrub heath vs bogs: bogs (deep peat) defined by peat depth (>0.5 m) and indicator species; spectral signals alone are insufficient for robust separation.
    - Montane habitats: altitude-based criteria used to define montane; field accessibility limits representation, leading to underestimation in some areas.
  - Inland bare ground and water features
    - Inland bare ground: LCM2000 tends to include some urban bare ground as part of inland bare ground; FS treats these differently, affecting comparability.
    - Water (inland): LCM2000 uses a >0.5 ha threshold and width criteria; standing water and canals are mapped with some constraints, yielding close totals for standing water when compared with FS.
  - Coastal and boundary features
    - Coastal BHs (Supralittoral and Littoral) are small relative to land cover and are generally aggregated for reporting; tidal state and coastal masking add complexity to comparisons.
    - Boundary and linear features: FS records these extensively, but LCM2000 excludes them as distinct BHs in calibration due to resolution and the scope of satellite mapping.

- Change detection and monitoring
  - Detecting landscape changes between 1990 and 2000 is challenging with satellite data alone due to resolution and classification differences.
  - A segment-based approach shows differences from the 1990 raster product; BH-level classifications constrain direct comparability.
  - Suggested path: use intelligent, pattern-based approaches that incorporate FS historical data to identify plausible changes and separate them from classification errors; calibration results help identify under- or over-estimations to inform change analyses.
  - Ongoing work planned to integrate LCM2000 with FS and external datasets to improve broad-habitat statistics and detection of meaningful landscape changes.

- Practical implications for GIS specialists
  - Use aggregation: rely on Aggregate Target/ BH alignments for reporting and national statistics where precision at the 1 km or parcel level is limited.
  - Leverage Variant-level details when patterns are needed (e.g., specific crops, urban vegetation, or rough grassland nuances) but be mindful of spectral/temporal limitations.
  - Be aware of data scale and resolution mismatches: 25 m pixels in CS2000 vs 1 km squares in FS; MMU differences can drive mismatches in small habitat patches.
  - Apply context-based corrections where possible (e.g., soil pH maps to help distinguish Neutral/Calcareous/Acid grasslands; peat-depth context for bogs).
  - Recognize that certain habitat classes (bogs, montane, inland bare ground, bracken) have persistent definitional and mapping challenges that may require follow-up integration with field data.

- Future directions and recommendations
  - Re-examine bogs and peatland mappings with integrated data sources (FS, peat-depth maps, national peatland mapping) to improve accuracy of deep-peat bog classifications.
  - Further refine buffering by Subclass Variants where it adds practical value for users, while maintaining stability at the Aggregate BH level.
  - Continue development of change-detection methodologies that blend FS patterns with LCM2000 outputs to distinguish real landscape changes from dataset artefacts.
  - Publish calibration details and broad-habitat statistics through the integrated Final Report, with additional data products aligned to user needs.

- Appendices and supplementary references
  - Appendix I: Brief review of Broad Habitats with distinguishing features relevant to LCM2000 mapping.
  - Table 2: Mapping of LCM2000 Variants to Broad Habitats, including alpha-codes and color representations (used for map production and user interpretation).
  - Note: Full methodological details, image selection, classification procedures, and calibration steps are provided in the Final Report and accompanying materials.