# CSLCM/Final

- Background and aims
  - UK Biodiversity Action Plan framework uses Broad Habitats (BHs) to cover UK habitats; LCM2000 maps terrestrial, freshwater and coastal BHs by spectral data, supplemented with external datasets.
  - LCM2000 creates Target classes, Subclasses and Variants that align with BHs where possible, acknowledging differences in definitions and read-across between BHs and LCM2000 classifications.
  - Purpose includes providing broad habitat maps and enabling data integration for wider use, with aggregate classes used for reporting.

- Broad Habitats and LCM2000 classes
  - LCM2000 is a satellite-image–based thematic classification; BHs are the conceptual habitat categories, while LCM2000 classes are spectral/contextual proxies.
  - Relationships among Target classes, Subclasses and Variants are mapped, with some BHs approximated where exact matches are not feasible.
  - Map displays balance reliability and pattern visibility; some rare or small BHs are aggregated for national/regional plots.

- Map display and data structure
  - Display uses a 10-class aggregation aligned with BHs for reporting, while retaining some Subclass detail where useful.
  - Coastal and interior features are treated as aggregates due to small size or resolution limits; Boundaries and linear features are excluded as distinct BHs in calibration.

- CS2000 field survey (FS) and calibration approach
  - CS2000 FS data (569 one-kilometre squares in GB; 1998–1999) provide detailed land-cover information but are not “ground truth.”
  - Calibration objectives: assess map-accuracy and calibrate LCM2000 to FS to derive BH cover statistics from nationwide LCM2000 data.
  - Calibration method involved three tests across squares:
    - Per-pixel comparisons (overlays, high-resolution differences).
    - Per-segment comparisons (dominant FS class within LCM2000 segments).
    - Per-parcel comparisons (FS parcels vs LCM2000-derived labels).
  - Confidence limits were produced via bootstrapping (95% ranges) across GB, England/Wales, and Scotland.

- Key calibration outcomes (level of correspondence)
  - BH-level correspondence (per-pixel): GB ~54%; England/Wales ~60%; Scotland ~44%.
  - Segmented-level correspondence (LCM2000 segments vs FS): GB ~58%; England/Wales ~64%; Scotland ~47%.
  - Parcel-level correspondence (FS parcels vs LCM2000 labels): GB ~62%; England/Wales ~69%; Scotland ~48%.
  - Target-class level correspondence generally higher than BH level; overall, around 65% (GB) to 73% (England/Wales) depending on method; Scotland lower due to upland and bog-heath mapping difficulties.
  - The FS and LCM2000 differences arise from resolution differences, survey timing, class definitions, and measurement uncertainties; aggregate class results align more closely.

- LCM2000 assessments at class level
  - Woodland (Broadleaved/mixed and Coniferous) shows similar areal shares, but exact mapping differs due to minimum mapping unit (0.5 ha) and small woodlands being underrepresented in LCM2000.
  - Arable and horticultural land: LCM2000 ~23–23.4%; FS ~21.5%; misclassifications occur between arable and grassland, and between arable and built-up areas.
  - Improved grassland vs semi-natural grassland: substantial overlap and misclassification (~20% FS improved mapped as semi-natural by LCM2000); distinguishing management practices remains challenging spectrally.
  - Neutral, Calcareous and Acid grasslands: spectral separation is difficult; rough grasslands treated differently in FS and LCM2000, causing notable discrepancies.
  - Bracken, fen/marsh/swamp, bog, montane, inland bare ground: substantial classification challenges due to spectral similarity, peat-depth considerations, and context (peatland vs heath).
  - Water bodies (inland): LCM2000 shows standing water and canals as a near-identical estimate but excludes smaller water bodies; boundaries with rivers/streams are not consistently captured at 1 km resolution.
  - Built-up areas and gardens: LCM2000 maps urban heterogeneity (Suburban/rural development and Continuous urban) more explicitly than FS, which treated urban land more generally.
  - Coastal habitats (supra-littoral and littoral): small, near-resolution-scale; often treated as aggregates; inter-tidal areas are inconsistently captured due to imaging timing.
  - Boundary and linear features: not targeted as BHs in LCM2000; FS captures many of these as linear features.

- LCM2000 accuracy
  - FS is not ground truth; differences reflect resolution, data models, and timing.
  - Estimated practical accuracy at Target class level is around 85% (best-case), with per-parcel alignment around 72% of maximum theoretical repeatability (FS repeatability ~88%).
  - Key mis-match drivers: 25 m map parcels vs field detail; FS parcel size (>0.04 ha) vs LCM2000 minimum mapping unit (>0.5 ha); survey year differences; and generalization in the LCM2000 MMU.

- Change detection
  - Detecting landscape change between 1990 and 2000 is challenging with satellite data alone due to small magnitudes of change and residual errors.
  - An intelligent approach is proposed: combine FS historical change directions with LCM2000 calibration to identify plausible changes and distinguish them from classification errors.
  - The forthcoming Final Report will detail methods for integrating field-based change signals with calibrated LCM2000 outputs.

- Appendix and mapping crosswalk
  - Appendix I provides a crosswalk of LCM2000 Variants to Broad Habitats, with detailed notes on distinguishing features and spectral limitations.
  - The mapping framework emphasizes caution in interpreting BH definitions and cross-walks, especially for peat depth, rough grasslands, bogs, montane habitats, and coastal zones.

- Overall takeaway for monitoring analysts
  - LCM2000 provides comprehensive nationwide BH mapping with standardized outputs, but accuracy varies by habitat type and is constrained by resolution and timing differences with field surveys.
  - Calibration against CS2000 FS yields important insights into where LCM2000 aligns with field data and where improvements are needed, especially for fine-scale or spectrally subtle habitats.
  - For policy monitoring and environmental health assessments, target-class level estimates are most reliable, with recognition of limitations in upland, bog, peatland, and some semi-natural grassland distinctions.
  - Change detection requires integrated, intelligence-driven approaches that leverage both field data and calibrated remote-sensing outputs.