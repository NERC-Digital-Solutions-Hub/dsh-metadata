# LCM2000: Calibration and Assessment of Broad Habitat Mapping

- Purpose and context
  - Supports UK Biodiversity Action Plan by mapping Broad Habitats (BH) across the UK using LCM2000, a thematic classification of satellite imagery augmented with external datasets.
  - Aims to describe BHs, Target classes, Subclasses, and Variants, and to provide aggregate classes for reporting when maps align with BH concepts.
  - Distinguishes BHs to assist broad land-cover assessments relevant to policy, land management, and public data products.

- Classification framework
  - BHs are described by a hierarchy: Broad Habitats (BHs) with Target classes, Subclasses, and Variants; Aggregate classes are used for reporting when needed.
  - LCM2000 classes (bold) map to BHs (italic) and can be aggregated to align with BH categories for analysis and display.
  - Differences in definitions and nomenclature reflect practical mapping trade-offs; some BHs are treated at subclass or variant levels for utility.

- Data and sources
  - LCM2000 uses spectral data from satellite imagery, with contextual external data to refine classification.
  - Field survey CS2000 (FS) data provide detailed, ground-level information used to assess and calibrate LCM2000 (not ground truth).
  - FS data cover 569 one-kilometre squares; some NI data not yet digital; FS repeatability about 88% for primary codes.

- Methodology and calibration
  - Calibration approach (not validation): compare FS and LCM2000 to understand correspondences and adjust interpretations.
  - GIS workflow: ARC/Info used to create BH-labeled coverages for all FS squares and equivalent LCM2000 map sections; produced 569 correspondence matrices (one per 1 km square).
  - Three main tests of correspondence:
    - Per-pixel: direct overlay comparisons (sensitive to resolution and MMU differences).
    - Per-segment: compare LCM2000 segments to FS-dominant classes.
    - Per-parcel: compare FS parcels to LCM2000-derived parcel labels.
  - Correspondence analyses conducted at multiple thematic levels:
    - BH level (excluding boundaries and rivers/streams)
    - Generalised urban levels (to match FS urban mapping)
    - Target class level
    - Aggregate class level
  - Confidence estimation: bootstrapping used to derive 95% confidence intervals for correspondence measures.

- Key results: agreement metrics
  - Per-pixel correspondence (GB-wide): ~54% (95% CI 53–56%); England & Wales ~60% (58–62%); Scotland ~44% (40–47%).
  - Per-segment correspondence: GB ~58% (57–60%); England & Wales ~64% (62–66%); Scotland ~47% (43–50%).
  - Per-parcel correspondence: GB ~62% (60–64%); England & Wales ~69% (67–72%); Scotland ~48% (44–52%).
  - BH-level across Britain (per-parcel): ~62% (range 60–64%) with England & Wales ~69% (67–72%), Scotland ~48% (44–52%).
  - Target class level (weighted, parcel-based): GB ~65%; England & Wales ~73%; Scotland ~51%.
  - Overall interpretation: FS field data and LCM2000 differ due to resolution (MMU: FS ~0.04 ha vs LCM2000 >0.5 ha), timing differences (FS mainly 1998 vs imagery 1998–2001), and class-definition differences; per-pixel results are most sensitive to these factors.

- Class-level insights and considerations
  - Broadleaved/mixed woodland and Coniferous woodland: overall area similar, but FS shows more small woodlands (often below LCM2000’s minimum mapping unit) appearing as grassland or arable in LCM2000.
  - Arable and horticultural land: LCM2000 often overestimates relative to FS due to small features and misclassifications with grassland; some confusion between arable and built-up land.
  - Improved vs semi-natural grassland: FS more often identifies semi-natural/Improved distinctions than LCM2000; roughly 20% of FS Improved grassland recorded as semi-natural by LCM2000.
  - Neutral, Calcareous, and Acid grasslands: spectral separation is difficult; soil pH and liming practices influence classification, leading to poor matches without contextual corrections.
  - Bracken, dwarf shrub heath, fen/marsh/swamp, bogs: significant classification challenges; peat depth and context dramatically influence bog vs heath distinctions.
  - Montane and Inland bare ground: low FS counterparts; altitude and context-based rules in LCM2000 can misclassify some montane and inland bare areas.
  - Coastal BHs (Supralittoral/Littoral): small and often near resolution limits; intertidal areas and context ( tide state) complicate mapping, treated as aggregates for reporting.

- Change detection and longitudinal use
  - Detecting landscape change between 1990 and 2000 is challenging with satellite-based mapping alone due to resolution, timing, and classification differences.
  - Intelligent, pattern-based approaches are recommended to separate true change from error (e.g., using prior FS data and known change trends).
  - Calibration results highlight under- and over-estimates in 2000, informing change analyses and interpretation.

- Data products and next steps
  - The final report (mid-March release) will detail calibration procedures and present Broad Habitat statistics derived from direct calibration against field survey data.
  - Outputs aim to combine LCM2000’s broad coverage with FS’s precision in recognizing habitats, enabling robust BH statistics for policy and planning.
  - Further follow-up work planned to re-examine BHs (e.g., bogs and heaths) with integrated LCM2000, FS, and external data sources.

- Practical implications for data support and product development
  - Data integration: the need to align field survey data (FS) with satellite classifications (LCM2000) across differing resolutions, times, and classification schemes.
  - Data products: develop user-friendly BH statistics, Target-class level outputs, and aggregate-class summaries; provide documentation on reading maps, variants, and the read-across between BHs and LCM2000 classes.
  - Quality and caveats: communicate that FS is not ground truth; mapping accuracy varies by class, geography, and scale; emphasize the importance of context when interpreting results.
  - Future enhancements: refine classification for problematic habitats (neutral/calcareous/acid grasslands, bogs, bracken), leverage variant-level distinctions, and explore improved peatland and coastal mappings.