# Mapping Quality Assurance Exercise

- Purpose and context
  - Document reports on the 2007 Countryside Survey digital mapping QA exercise, evaluating the transition from paper/digitised maps to field-based digital mapping for habitats and landscape features.
  - Aims to ensure data are high quality, compatible with previous approaches, and suitable for integration into a national geodatabase for rapid analysis alongside other spatial datasets.
  - Key motivations: reduce interpretation subjectivity, improve data clarity, enable early QA via an interactive wiki, and test QA across multiple scales.

- Data, tools and workflow
  - Field data collected with Surveyor software in the 2007 survey; mandatory fields and prompts for feature types; integrated visit status tracking.
  - Immediate upload to a wiki for early data checks by both surveyors and CS staff; Quality Control teams reviewed protocols early in the survey.
  - Data management employed a central geodatabase; unsurveyed or refused areas excluded prior to analysis; two comparable datasets created (CS survey data and QA data) for common surveyed areas using mask overlays.

- QA methodology and approaches
  - Direct comparison at aggregate level: proportions of Broad Habitat (BH) types per 1 km square; team-by-team comparison (CS vs QA).
  - Raster comparison: convert polygons to a 10,000-cell (10 m x 10 m) raster per square, determine dominant BH per cell, and compare QA vs CS raster layers; sample with a resolution grid to assess absolute area and spatial agreement.
  - 100-point grid comparison: overlay a 10x10 grid within each square, compare BH presence at matched points to derive concordance and mis-matches.
  - Attribute comparison: match reference IDs to compare species and other attributes between QA and CS datasets.
  - Linear and point feature analysis: additional methods (buffering lines to 5 m; matching point features) to enable robust cross-checks of land-use themes and habitat codes.
  - Change recording: new digital “change” field to capture real changes, error changes, and no change; analysis of agreement on change coding across habitats, lines, and points.

- Extent and coverage
  - QA mapping covered 23 one-km squares, sampled to reflect different land classes; access refusals limited the surveyed area but common areas were analyzed for comparability.

- Key findings: data quality and agreement
  - Overall habitat extent agreements
    - In 81% of CS vs QA square comparisons, the same Broad Habitat was recorded by both teams.
    - Mean differences in BH proportions were typically small: under 1% for 13 BHs; 1–2% for 5 BHs; under 3.5% for the remaining two. Notable potential issues identified for Improved and Acid Grassland, Dwarf Shrub Heath, Bog, Urban, and Sub-littoral sediment.
  - Raster data agreement
    - Across squares, raster BH agreement ranged widely, with an overall average around 76%, but high conformity in some squares (e.g., 364: 98%, 488: 94%) and notable discordance in others (261: 49%, 773: 23%).
    - Per-square BH concordance table showed varying agreement by habitat type, with some misclassifications concentrated in upland and mixed mosaics, and machair-related neutral/grassland issues in Scotland.
  - 100-point concordance
    - Most BH/PH codes showed good concordance, but several squares exhibited notable mismatches (e.g., 261: 41%, 773: 19% concordance).
    - Overall, 76–78% concordance observed across many squares, with some squares showing higher concordance (e.g., 364: ~96%) and others lower (e.g., 773: ~19%).
  - Polygon-based species attributes
    - About 45% of QA polygons had at least one listed species matching the CS polygon at the same location (excluding mosaics).
    - Species concordance varied by habitat type; woodland and Improved Grassland showed higher matching species rates; upland and mosaicked polygons tended to show lower concordance.
    - The concordance for listed species within spatially matched polygons hovered around 40%, with QA data generally recording more species than CS.
  - Points and linears
    - Point-feature habitat codes were well aligned between QA and CS, though some confusion occurred between woodland/forest codes due to legacy coding practices.
    - Linear features showed a high level of consistency in land-use themes; a small number of mismatches were expected (e.g., fence vs wall).
    - Aggregate lengths for linear features generally matched well; some differences occurred in specific land-use themes.
  - Change recording
    - Change coding generally aligned with QA guidelines; some complexities persisted in habitat-related change interpretation.
    - The digital workflow enabled more in-field verification and the potential to update incorrect previous maps, with overall positive alignment between CS and QA change codes.

- Notable issues and interpretation
  - Blanket Bog: major definitional disagreements between QA and CS due to evolving 2007 field handbook revisions and debates on peat/vegetation delineations; this produced significant mismatches, particularly in upland squares (e.g., 773, 991, 1034).
  - Neutral vs Improved Grassland: overlapping species and gradient issues led to some misallocation between these two habitats; no clear bias toward QA or CS in most cases.
  - Woodland classification: complexity in distinguishing Broadleaf vs Coniferous woodland; discrepancies often related to historical definitions and back-allocations in earlier surveys.
  - Upland mosaics: small-scale mosaics of BH types complicated exact matches between QA and CS; mosaics were disaggregated for analysis, which could introduce mismatches.
  - Machair habitats: local Scotland-specific machair vegetation on sand dunes caused anomalies in the sand-dune habitat comparisons, underscoring landscape- and locality-driven recording challenges.
  - Species-level concordance: overall species-level agreement lower than habitat-level agreement, reflecting the difficulty of assigning a single dominant species in biodiverse areas; Lolium perenne showed relatively higher concordance due to dominance in swards.

- Change management and GIS implications
  - The digital field approach (Surveyor + wiki QA) substantially improved data completeness, consistency, and the ability to verify and update data against prior maps.
  - Findings highlight the importance of continuous refinement of habitat definitions, particularly for Blanket Bog, upland mosaics, and grassland boundaries.
  - Training and clearer field handbook guidance are critical to reduce misclassification between similar broad habitats and to improve cross-team consistency.
  - The QA exercise demonstrates that GIS-based QA can effectively flag discrepancies, guide data standardization, and inform improvements to data products for policy, client, and public audiences.

- Conclusions and takeaways for GIS practice
  - Digital mapping and integrated QA workflows dramatically enhance data quality and timeliness for map-based GIS products.
  - While overall agreement between surveyors and QA teams is high for most habitat types and feature classes, certain upland and transitional habitats require ongoing definition refinement and targeted training.
  - The exercise confirms the value of multiple QA approaches (aggregate, raster, 100-point, and attribute-based) to comprehensively assess spatial data quality.
  - The experience underscores the need for robust data standards, clear habitat definitions, and recognition of landscape-scale variability when interpreting fine-scale maps in GIS applications.