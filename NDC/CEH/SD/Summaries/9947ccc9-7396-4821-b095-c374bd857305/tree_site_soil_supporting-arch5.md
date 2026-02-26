# Soil, site and tree characteristics for acute oak decline (AOD) symptomatic and non-symptomatic oak in three UK woodlands, southern England, 2016

## Overview
- A dataset from a study of how local-scale tree, site, and soil factors relate to Acute Oak Decline (AOD) in three UK woodlands (Monks Wood, Writtle Forest, Stratfield Brake) during 2016.
- Aimed at understanding interactions between tree and soil properties and their potential role in AOD onset and progression.
- Data types cover tree characteristics, site context, and soil properties, collected from 60 trees (10 symptomatic and 10 asymptomatic per site).

## Dataset structure and content
- File set (CSV format):
  - Tree_characteristics.csv: tree-level measurements and identifiers.
  - Site_characteristics.csv: site context around each sampled tree.
  - Soil_characteristics.csv: soil physical and chemical properties around each tree.
- Variables and units are described in the accompanying data dictionary within the document:
  - Tree-level variables include location (latitude/longitude), AOD symptom status, species classification (morphometric leaves and genetic SNP confirmation), tree dimensions (height, DBH), crown dimensions, crown density reduction, and rooting depth.
  - Site/context variables include depth to gleying, basal areas (0–20 m and 20–40 m), compound topographic index, and tree social status.
  - Soil variables include texture fractions (clay, silt, sand), organic matter, pH, total carbon and nitrogen, mineral N (nitrate and ammonium), Olsen P, cation exchange capacity, and exchangeable cations (Al, Ca, Fe, K, Mg, Mn, Na), soil bulk density, and sampling depth.
- Missing values are indicated by "nd"; some measurements below detection limits are represented as LoD/2 where applicable.
- Spatial coverage: three oak woodlands in England with tree coordinates provided in Tree_characteristics.csv.
- Temporal coverage: single field season (July–November 2016), one measurement point per tree.

## Data collection, processing, and quality control
- Field measurements followed established forestry protocols:
  - Tree measurements and crown condition using standard forest mensuration methods; crown density reduction recorded as a percentage.
  - Soil pits excavated near each tree (0.8 m deep) to assess rooting depth and depth to gleying; micro-topography measured along radial transects; topographic wetness index calculated.
  - Basal area estimated within 0–20 m and 20–40 m surrounding each tree.
- Soil sampling and laboratory analyses:
  - Eight soil samples per depth (5–15 cm and 40–50 cm) per tree, pooled to one composite per depth per tree.
  - Analyses included LOI for organic matter, pH (in water), particle size distribution (via a laser granulometer), total C and N (CN analyzer), extractable nutrients (N and P) and exchangeable cations (BaCl2 extraction with ICP-OES analysis), and Olsen P.
  - Replication and calibration details:
    - Technical replication: multiple repetitions for LOI, pH, particle size, C/N, and cations.
    - Blanks and calibration materials used for QA (e.g., standards for pH, CN, Olsen P, and cation analyses).
  - In cases where extract measurements fell below detection limits, values were substituted with half the detection limit (as per USEPA guidance).
- Biological analyses for species identification:
  - Leaves collected from each tree (five per tree) for morphometric analysis and genetic SNP-based species confirmation.
  - Morphometric approach followed Kremer et al. (2002); genetic typing used Sequenom with SNPs (Guichoux et al. 2013).
- Experimental design:
  - 3 sites × 20 trees per site = 60 trees total.
  - At each site: 10 symptomatic (bleeding canker) and 10 asymptomatic trees selected; asymptomatic trees chosen at least 20 m away from symptomatic trees using a randomized bearing method.
- Instrumentation and QA details are documented (calibration standards, blanks, replication counts, and reference materials) to support data quality and reproducibility.

## Temporal and spatial context
- Temporal: Measurements and sampling occurred within July–November 2016 at a single time point per tree.
- Spatial: The study sites are Monks Wood (Cambridgeshire), Writtle Forest (Essex), and Stratfield Brake (Oxfordshire); precise tree coordinates are provided in Tree_characteristics.csv.

## Data governance and use considerations for Data Stewards
- Data are organized into thematically distinct files with a clear linkage via Tree_ID (project-specific code), enabling traceability across tree, site, and soil data.
- Comprehensive data dictionary in the dataset description (including units and data capture methods) supports consistent reuse and integration with other datasets.
- Provenance is documented through detailed collection and analysis methods, instrumentation, and QA procedures, aiding data quality assessment and reproducibility.
- Acknowledges association with a pre-print publication and cites extensive methodological references for traceability and potential replication.
- Potential reuse considerations:
  - Ensure consistent interpretation of AOD_symptom_status and other categorical indicators across datasets.
  - Respect the indicated missing value conventions and detection-limit substitutions when performing analyses.
  - Maintain linkage via Tree_ID to support cross-table joins and site-specific analyses.

## Limitations and caveats
- One-time-point sampling per tree within a single season; temporal dynamics beyond this window are not captured.
- The sampling frame focuses on three woodlands and 60 trees, which may limit generalizability to broader regions or other oak stands.
- Some measurements are near or below detection limits; substitution rules are described and should be applied consistently in analyses.

## Related resources and references
- Dataset underpinning pre-print: The cause-effect conundrum of local-scale site and soil factors in acute oak decline (AOD). DOI: https://doi.org/10.1101/2025.01.24.634765
- Core methodological references for field and laboratory procedures (forestry measurements, crown assessment, soil analysis, particle size, CN analysis, cation exchange, Olsen P, mineral N, and QA practices).
- Species identification references: Kremer et al. (2002) for leaf morphometrics; Guichoux et al. (2013) for SNP-based genetic classification.
- Instrumentation and analysis references for soil properties and QA practices (e.g., USEPA guidance for data handling below detection limits).