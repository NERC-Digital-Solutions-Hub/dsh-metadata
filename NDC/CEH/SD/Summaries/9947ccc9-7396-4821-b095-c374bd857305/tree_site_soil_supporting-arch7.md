# Soil, site and tree characteristics for acute oak decline (AOD) symptomatic and non-symptomatic oak in three UK woodlands, southern England, 2016

- Purpose and scope
  - Dataset from a study on the relationship between Acute Oak Decline (AOD) symptoms and local-scale environmental factors.
  - Focuses on interactions between tree, soil, and site characteristics at a fine spatial scale to inform AOD understanding.
  - Aims to support GIS-based visualization and spatial analysis of AOD drivers.

- Data structure (three CSV files)
  - Tree_characteristics.csv: individual tree measurements and identity, spatial coordinates, AOD status, species classification (morphometric and genetic), and tree dimensions.
  - Site_characteristics.csv: site-level context around each tree (e.g., distance to gleying, basal area in surrounding rings, topographic index, social class).
  - Soil_characteristics.csv: soil properties by tree and depth (5-15 cm and 40-50 cm), including texture fractions, organic matter, pH, total C and N, mineral N, Olsen P, cation exchange properties, bulk density, and extractable cations.

- Spatial and temporal coverage
  - Spatial: three oak woodlands in England — Monks Wood (Cambridgeshire), Writtle Forest (Essex), Stratfield Brake (Oxfordshire).
  - Temporal: one sampling campaign conducted July–November 2016; single time point per tree/soil/leaf.

- Sampling design and selection
  - 60 trees total: 3 sites × 20 trees/site (10 AOD symptomatic and 10 asymptomatic per site).
  - Symptomatic status identified by bleeding canker lesions on the lower stem; asymptomatic trees selected at least 20 m away from symptomatic trees.

- Data collection and measurement methods
  - Tree and site measurements
    - Standard forest mensuration procedures for height, DBH, crown dimensions; crown density reduction; tree social status (dominant to dying).
    - Soil pit (0.8 m) near each tree to measure rooting depth and depth to gleying (Munsell-based assessment).
    - Micro-topography measured along eight radial transects; Topographic Wetness Index calculated (Sørensen et al., 2006).
    - Basal area computed for 0-20 m and 20-40 m surrounding the tree (relascope method).
  - Soil sampling and analysis
    - Eight soil samples per depth (5–15 cm and 40–50 cm) per tree, composite per depth.
    - Sample processing: air-dried and sieved (<2 mm) for most analyses; field-moist sub-sample stored at 4 °C for mineral N analysis.
    - Analyses include: organic matter by LOI; pH; particle size distribution (clay, silt, sand); Total C and N; extractable mineral N (KCl); Olsen P; cation exchange capacity; extractable cations (Al, Ca, Fe, K, Mg, Mn, Na); bulk density.
    - Instrumentation and quality control details (replicates, calibration, reference materials) documented (as per Table 4 in the source).
  - Leaf morphometry and species confirmation
    - Five leaves per tree analyzed morphometrically to classify as Quercus robur, Quercus petraea, or a hybrid (morphometric method) and confirmed by genetic SNP analysis (Sequenom).
  - Data quality considerations
    - Technical replication provided for key measurements (e.g., LOI, pH, particle size, Total C/N, Olsen P, mineral N, exchangeable cations).
    - Handling of below-detection-limit values (e.g., half the LoD used in calculations for certain extracts).

- Variable highlights by file
  - Tree_characteristics.csv
    - Tree_ID, Site, GPS coordinates (Latitude/Longitude), AOD_symptom_status, species classifications (morphometric leaves and DNA-based), tree dimensions (Height, DBH, Crown Width EW/NS), Crown_density_reduction, Root_depth_cm.
  - Site_characteristics.csv
    - Site, Tree_ID, AOD_symptom_status, Depth_to_Gleying_cm, Basal_Area_0_20m, Basal_Area_20_40m, Compound_topographic_index, Social_class.
  - Soil_characteristics.csv
    - Tree_ID, Site, Sample_depth (5–15 cm or 40–50 cm), OM_%, pH, Clay_%, Silt_%, Sand_%, TotalC_%, TotalN_%, NitrateN_mgkg, AmmoniumN_mgkg, OlsenP_mg/kg, CEC_mmolc/kg, ExchangeableAl_mgkg, ExchangeableCa_mgkg, ExchangeableFe_mgkg, ExchangeableK_mgkg, ExchangeableMg_mgkg, ExchangeableMn_mgkg, ExchangeableNa_mgkg, Bulkdensity_gcm3.
    - Notes on method detection limits, and instrument-specific replication/calibration details included.

- Temporal and methodological scope
  - Leaf, soil, and tree measurements integrated to examine local-scale site and soil factors contributing to AOD.
  - Uses standardized field protocols, multiple analytical techniques, and QA procedures to enable reproducibility and GIS-ready spatial analyses.

- Potential GIS applications
  - Georeferenced tree-level data enables mapping of AOD status against soil properties, site context, and micro-topography.
  - Supports spatial analysis of AOD drivers: soil texture/chemistry, depth to gleying, basal area, and topographic index around each tree.
  - Data suitable for linking with environmental layers and for visualization of spatial patterns at stand-scale.

- Related references and provenance
  - Dataset underpinning a pre-print study: The cause-effect conundrum of local-scale site and soil factors in acute oak decline (AOD) with DOI: 10.1101/2025.01.24.634765.
  - Methodological references for field measurements and soil analyses (Hamilton 1975; Lakatos et al. 2014; Sørensen et al. 2006; Olsen et al. 1954; USEPA 2000; and others).