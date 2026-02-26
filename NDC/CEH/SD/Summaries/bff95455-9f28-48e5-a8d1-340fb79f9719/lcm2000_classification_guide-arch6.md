# LCM2000 Final Report

- Purpose and context
  - Part of the UK Biodiversity Action Plan effort to map Broad Habitats (BHs) using the LCM2000 satellite-derived thematic classification.
  - Aimed to contribute to habitat assessment by mapping terrestrial, freshwater, and coastal BHs, while also recording detailed land-cover information where possible.
  - Calibration exercise: compare LCM2000 outputs with CS2000 field survey data to calibrate BH statistics and improve end-user data products (maps, tables, self-serve tools).

- Data sources and classifications
  - LCM2000: spectral-class based map with thematic components that can be aggregated into BHs, Target classes, Subclasses, and Variants.
  - CS2000 field survey (FS): detailed, higher-resolution ground data (~569 1-km squares in GB; 549 in 1998, 1999 in GB; NI data not digitally available yet).
  - Key concepts:
    - BHs: Broad Habitat classifications (e.g., Broadleaved woodland, Coniferous woodland, Arable/grassland, Improved/Neutral/Calcareous/Acid grassland, Bracken, Dwarf shrub heath, Fen/marsh/swamp, Bog, Water, Montane, Inland rock, Built-up areas, Coastal BHs).
    - Target classes and Subclasses: spectral/ contextual classifications that map to BHs where possible; Variants capture finer distinctions.
    - Aggregate classes: 10-class level used for broad reporting to align with BH aggregations.
  - Display and reporting: map displays use cartographic conventions; some rare/dissected classes are aggregated to maintain legibility at national/regional scales.

- GIS workflow and calibration approach
  - Data alignment: ARC/Info GIS used to create BH-labeled coverage for all FS squares and LCM2000 map sections; produced 569 correspondence matrices (one per 1-km square).
  - Comparison modes:
    - Per-pixel: direct overlay of FS vs. LCM2000 at 25 m pixels (captures fine spatial differences).
    - Per-segment: FS-dominant class comparison within LCM2000 segments.
    - Per-parcel: FS parcels compared to LCM2000-derived parcel labels.
  - Thematic levels for correspondence:
    - BH level (excluding boundaries/linear features and some rivers/streams due to resolution).
    - Target class level and Aggregate class level (where FS generalisation is applied to urban areas and other features).
  - Confidence estimates: bootstrapping used to compute 95% confidence limits for correspondence across GB, England/Wales, and Scotland.

- Key results and accuracy findings
  - Per-pixel correspondence (GB BH level): 54% (95% CI 53–56%); England & Wales 60% (58–62%); Scotland 44% (40–47%).
  - Per-segment correspondence (GB BH level): 58% (57–60%); England & Wales 64% (62–66%); Scotland 47% (43–50%).
  - Per-parcel correspondence (GB BH level): 62% (60–64%); England & Wales 69% (67–72%); Scotland 48% (44–52%).
  - Target class correspondence (parcels): GB 65% (overall); England/Wales 73%; Scotland 51% (lower due to upland bog-heath issues).
  - Overall interpretation: the FS data are higher resolution and differ in timing and definitions; this results in non-trivial mismatches, especially at the BH level.
  - LCM2000 accuracy perspective:
    - Segments vs FS parcels show about 63.4% basic correspondence at BH level; around 72% of maximum potential given FS repeatability of 88%.
    - Estimated realistic Target-class accuracy around 85–87% (not exceeding FS repeatability), implying robust usefulness for many applications despite known discrepancies.
  - Notable sources of mismatch:
    - Differences in spatial resolution (25 m parcels vs FS field-level detail; FS measured >0.04 ha parcels, LCM2000 MMU >0.5 ha).
    - Time differences between FS (mostly 1998) and LCM2000 imagery (1998–2001).
    - Class-definition and interpretation differences (e.g., arable vs. urban, improved vs. semi-natural grassland, peat/bog distinctions).
    - Difficulties distinguishing certain semi-natural swards (neutral/calcareous/acid grasslands) using spectral data alone.
    - Peat depth criteria and peatland mapping affecting Bogs vs Heath classifications; Montane and Inland bare ground complexities.
  - Specific habitat mapping challenges:
    - Arable vs horticultural land and confusion with Improved grassland.
    - Semi-natural vs improved grasslands; Neutral/Calcareous/Acid grasslands differentiation limitations.
    - Bracken detection and seasonal visibility (May imagery bias).
    - Fen/marsh/swamp vs rush pastures on floodplains; peat depth control for bog vs heath.
    - Coastal BHs (supra-littoral and littoral) are small, often below resolution; inter-tidal areas cause variability with FS.
  - Built-up areas vs open spaces: FS treated urban land differently, leading to FS maps containing elements (woodland, grassland, water) that LCM2000 does not map as discrete BHs.

- Change detection and future work
  - Change detection between LCMGB 1990 and LCM2000 is challenging; satellite data alone are insufficient for consistent detection at national scale.
  - The study endorses an intelligent, pattern-based approach to distinguish true change from errors, leveraging FS historic data (e.g., Haines-Young et al. 2000) and calibration results.
  - Future work (beyond production phase) aims to integrate LCM2000 with FS and external datasets to improve Broad Habitat statistics and enable robust change analyses.

- Outputs, data products, and impact for data use
  - Direct calibration enables generation of BH statistics from LCM2000’s comprehensive national coverage, informed by the field-validated precision of CS2000.
  - Outputs include mapped BHs, Target-class and Aggregate-class statistics, and potential early prototypes for end-user self-serve data products.
  - The documented calibration framework provides a pathway to improve data products, communicate uncertainties, and refine classifications over time.

- Appendix and classification detail (maps and descriptors)
  - Appendix I provides a concise review of Broad Habitats and their distinguishing features relative to LCM2000 mapping, highlighting:
    - The limitations of remote sensing in capturing fine-grained woodland structure, boundaries, and certain semi-natural grassland distinctions.
    - The role of context data (soil pH, peat depth, land use history) in differentiating habitats (e.g., Neutral vs Calcareous vs Acid grasslands, bogs, and heath).
    - The mapping rationale for various BHs, including peat-related corrections, and notes on the regional variability of classifications.

- Relevance for data-support work
  - Demonstrates a rigorous, multi-resolution data integration workflow (field survey + satellite-derived classification) with formal calibration to produce reliable data products.
  - Highlights the importance of documenting uncertainty, choosing appropriate comparison levels (BH, Target, Aggregate), and using bootstrapping to quantify confidence.
  - Provides concrete examples of data challenges when harmonizing thematic classifications across datasets with different resolutions, timings, and definitions.
  - Offers a model for generating standardized, user-friendly data outputs (maps and statistics) that can be consumed by non-specialist stakeholders, while signaling underlying limitations and uncertainties.