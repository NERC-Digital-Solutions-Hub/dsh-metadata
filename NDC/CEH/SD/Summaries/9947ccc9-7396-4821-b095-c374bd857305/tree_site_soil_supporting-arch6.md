# Soil, site and tree characteristics for acute oak decline (AOD) symptomatic and non-symptomatic oak in three UK woodlands, southern England, 2016

## Purpose and scope
- Dataset from a study linking Acute Oak Decline (AOD) symptoms with local-scale environmental factors.
- Focuses on interactions between tree, site context, and soil properties at a local scale.
- Managed across three UK oak woodlands with 60 sampled trees (symptomatic and non-symptomatic).

## Data files and structure
- Three CSV files:
  - Tree_characteristics.csv
  - Site_characteristics.csv
  - Soil_characteristics.csv
- Tree_characteristics.csv includes: coordinates (latitude/longitude), species classification (morphometric and genetic), tree dimensions (height, DBH, crown dimensions), crown condition, rooting depth, AOD symptom status.
- Site_characteristics.csv includes: site name, 0-20 m and 20-40 m basal area, depth to gleying, compound topographic index, tree social status.
- Soil_characteristics.csv includes: sample depth, AOD status, soil texture fractions (clay, silt, sand), organic matter, pH, total carbon and nitrogen, extractable nutrients (nitrate/nitrite, ammonium, Olsen P), cation exchange capacity, exchangeable cations (Al, Ca, Fe, K, Mg, Mn, Na), bulk density; with detailed measurement methods and units.
- Missing values coded as 'nd' where applicable.

## Spatial and temporal coverage
- Spatial: three oak woodlands in England (Monks Wood, Cambridgeshire; Writtle Forest, Essex; Stratfield Brake, Oxfordshire). Tree-level latitude-longitude coordinates provided.
- Temporal: field observations and samples collected July–November 2016 (single time point).

## Data collection and methods
- Field measurements follow standard forest mensuration and crown condition protocols; recording tree social status.
- Soil site context: soil pit (0.8 m) near each tree; depth to gleying measured using Munsell chart; micro-topography mapped along radial transects; Topographic Wetness Index calculated.
- Soil sampling: eight samples per depth (5–15 cm and 40–50 cm) per tree, pooled into depth-specific composites; samples air-dried (except field-moist for mineral N analysis).
- Laboratory analyses:
  - Organic matter by loss on ignition; pH in water.
  - Particle-size distribution by laser granulometry (clay, silt, sand).
  - Total carbon and nitrogen by CN analyzer.
  - Exchangeable cations (Al, Ca, Fe, K, Mg, Mn, Na) by BaCl2 extraction with ICP-OES.
  - Olsen P by extraction; mineral N (nitrate + nitrite and ammonium) by 1 M KCl extraction with colorimetric analysis.
  - Bulk density from dried soil.
- Replication and quality control: technical replication (various tests), instrument calibration, blanks, and use of reference materials; adjustments for measurements below detection limits (LOD/2) where needed.
- Leaf morphometry and genetics: five leaves per tree for morphometric classification and Sequenom SNP analysis to determine species (Quercus robur, Quercus petraea, or hybrids).

## Experimental design
- Sites: Monks Wood, Stratfield Brake, Writtle.
- Sampling: 60 trees total (3 sites × 20 trees). At each site, 10 AOD-symptomatic and 10 asymptomatic trees.
- Symptom identification: presence of bleeding stem cankers on the lower stem; asymptomatic trees selected randomly with >20 m separation from symptomatic trees.

## Quality control and data handling
- Detailed instrument calibration, blanks, and replication records documented for each measurement type.
- Cross-site data provenance and unit consistency maintained; missing values noted as 'nd'.
- Sample and site identifiers (Tree_ID, Site) ensure traceability across all three data files.

## Practical uses and access
- Enables self-serve exploration of relationships between AOD symptoms, tree/site context, and soil properties.
- Supports site-specific and cross-site analyses of local drivers of AOD progression.
- Data underpin a pre-print study on local-scale site and soil factors in AOD.

## Miscellaneous
- Pre-print basis: Shaw et al., The cause-effect conundrum of local-scale site and soil factors in acute oak decline (AOD). DOI: https://doi.org/10.1101/2025.01.24.634765
- Method references provided for standard procedures (forest mensuration, crown assessment, soil analysis, leaf morphometrics, and SNP-based species identification).