# Topsoil invertebrate model estimates [Countryside Survey]

- What the dataset is
  - Model-based estimates of mean values for topsoil invertebrates (0–8 cm depth) across Great Britain, including Total Catch, Mite:springtail ratio, Number of broad taxa, and Shannon diversity index.
  - Derived from 947 cores collected in 2007 across 256 1 km × 1 km squares; supports comparisons across habitat/parent material combinations.
  - Uses data from 1978, 1998, and 2007 modeled with a mixed-model approach; habitat and parent material characteristics are derived from Land Cover Map 2007 and the British Geological Survey Soil Parent Material Model 2009.

- Spatial coverage and reference
  - Spatial units: 256 Great Britain squares, each 1 km × 1 km.
  - Coordinate system: OSGB 1936 / British National Grid (EPSG:27700).

- Data attributes and GIS integration
  - Core attributes (examples): 
    - LCM_CLASS (derived from LCM2007)
    - DOM_GRAIN (dominant grain size from Soil PMM)
    - SOIL_GROUP (soil texture category)
    - CATCH_98 / CATCH_07 (mean total invertebrates for 1998/2007)
    - TAXA_98 / TAXA_07 (mean number of broad taxa for 1998/2007)
    - RATIO_98 / RATIO_07 (mites:springtails ratio for 1998/2007)
    - SHAN_98 / SHAN_07 (Shannon diversity index for 1998/2007)
    - SE fields: CATCH_98SE, CATCH_07SE, TAXA_98SE, TAXA_07SE, RATIO_98SE, RATIO_07SE, SHAN_98SE, SHAN_07SE
  - Model outputs are means by habitat/parent material combinations; some combinations have insufficient sample sizes and thus no estimates for those cells.
  - Data are tied to habitat and soil predictors (LCM2007 and Soil PMM), enabling GIS-based classification and thematic mapping.

- Modeling and data generation
  - Estimates produced by modeling dominant habitat and dominant parent material characteristics from LCM2007 and PMM, selecting the parent material characteristic that minimises AIC.
  - Not all areas have data (e.g., urban and littoral rock are not sampled by Countryside Survey).

- Collection, processing, and quality control
  - Sampling: 4 cm diameter × 8 cm long cores; vegetation removed; litter layer left; cores extracted in the field and kept intact.
  - Extraction: dry Tullgren method; invertebrates identified to broad taxa (taxonomic level 1) and counted.
  - Quality control: periodic reassembly and re-identification by a second staff member to assess potential operator error; discrepancies resolved and recorded.

- Data limitations and considerations
  - Areas not sampled by CS have no associated data.
  - Some habitat/parent material combinations have insufficient sample sizes, limiting estimate availability for those cells.
  - Model-based estimates depend on the accuracy of LCM2007 and Soil PMM inputs; uncertainties are reflected in provided standard error fields.

- References and supporting documents
  - Emmett et al. 2008, 2010; Scott 2008; Morton's Land Cover Map 2007 documentation; Soil Parent Material Model references.
  - Key technical reports: Countryside Survey Technical Reports on soils and statistical analyses.