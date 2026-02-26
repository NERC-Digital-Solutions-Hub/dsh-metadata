# Soil, site and tree characteristics for acute oak decline (AOD) symptomatic and non-symptomatic oak in three UK woodlands, southern England, 2016

- Purpose: A dataset from a field study investigating how local-scale tree, soil, and site factors relate to Acute Oak Decline (AOD) symptoms in three UK woodlands (Monks Wood, Writtle Forest, Stratfield Brake) during 2016. It supports exploring interactions between tree health, soil properties, and site context at the individual-tree level.

- Data files and structure:
  - Tree_characteristics.csv
    - Includes: site name, unique Tree_ID, geographic coordinates (latitude/longitude), AOD symptom status (symptomatic vs asymptomatic), species classification (morphometric leaves and DNA-based haplotype), and tree biometric measures (height, DBH, crown dimensions, crown density reduction, rooting depth).
  - Site_characteristics.csv
    - Includes: site name, Tree_ID linkage, AOD symptom status, local context metrics (depth to gleying), stand structure (basal area within 0-20 m and 20-40 m), compound topographic index, and tree social status (dominant to dying).
  - Soil_characteristics.csv
    - Includes: Tree_ID and Site, sample depth (5-15 cm or 40-50 cm), and soil properties (organic matter, pH, particle size fractions, total carbon and nitrogen, mineral N (nitrate, ammonium), Olsen P, cation exchange capacity, exchangeable cations (Al, Ca, Fe, K, Mg, Mn, Na), and bulk density). Various fields note method detection limits and replication specifics.

- Data collection and quality control:
  - Field design: Three sites; targeted sampling of 10 symptomatic and 10 asymptomatic trees per site (60 trees total). Symptomatic status identified by bleeding stem canker presence; asymptomatic trees selected at random directions (>20 m away from a symptomatic tree).
  - Measurements and sampling:
    - Tree and site context: standard forest mensuration methods; crown condition monitoring; sociometric status; soil pit excavated near each tree; rooting depth and depth to gleying measured.
    - Site context: eight radial soil micro-topography transects; Topographic Wetness Index calculated; basal area measured with relascope.
    - Soil sampling: eight samples per depth per tree (5-15 cm and 40-50 cm), pooled to one composite per depth per tree; samples air-dried and analyzed for physical and chemical properties.
  - Laboratory analyses and QA:
    - Organic matter by loss on ignition; pH in water; particle-size distribution by laser granulometry; total C and N by elemental analyzer; exchangeable cations by BaCl2 extraction with ICP-OES; Olsen P by Olsen method; mineral N by 1M KCl extraction with colorimetric analysis.
    - Technical replicates specified for each test; calibration and reference materials documented; handling of values below detection limits (LoD/2) noted for some extracts.
  - Documentation and provenance:
    - Detailed instrument usage, blanks, calibrations, and reference materials recorded (e.g., LOI, pH meter, Malvern Mastersizer, Skalar SAN++ analyzer, ICP-OES).
    - Data aligned with a related preprint on local-scale site and soil factors in AOD.

- Spatial and temporal scope:
  - Spatial: three woodlands in southern England; tree-level coordinates provided for all sampled trees.
  - Temporal: single field campaign from July to November 2016; all measurements taken at one time point per tree/site during that period.

- Variables and data integration considerations:
  - AOD status is consistent across tree- and site-level records.
  - Species determination combines morphometric leaf analysis and genetic SNP-based confirmation.
  - Site-context variables (basal area, depth to gleying, topographic index) enable cross-analysis with soil properties and tree health.
  - Soil data are depth-specific (5–15 cm and 40–50 cm) and include comprehensive chemical and physical properties, enabling depth-resolved analyses.

- Recommended analyses and downstream uses:
  - Correlational and regression analyses linking AOD symptom status to soil properties, topography, and surrounding stand structure.
  - Multilevel modelling to account for tree-level measurements nested within sites, incorporating species identity (morphometric and genetic) as a factor.
  - Integration of leaf morphometrics and genetic data to explore species identity and hybridization in relation to AOD susceptibility.
  - Spatial analysis leveraging coordinates to examine micro-site patterns of AOD in relation to depth to gleying and Topographic Wetness Index.
  - Meta-analyses or replication checks using the provided QC and replication details to assess data reliability.

- Access notes and references:
  - Associated preprint: The cause-effect conundrum of local-scale site and soil factors in acute oak decline (AOD). DOI: https://doi.org/10.1101/2025.01.24.634765
  - Key methodological references cover forest mensuration, crown condition assessment, leaf morphometrics, genetic species identification, soil analysis methods, and data handling practices for environmental datasets.