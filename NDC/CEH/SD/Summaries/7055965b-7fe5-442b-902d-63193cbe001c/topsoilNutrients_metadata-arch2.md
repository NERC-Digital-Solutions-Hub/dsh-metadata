# Topsoil nutrient model estimates [Countryside Survey]

- Data scope
  - Topsoil nutrient data for 0–15 cm depth: total nitrogen (N) concentration (%), C:N ratio, and Olsen-Phosphorus (P) (mg/kg).
  - Based on 2007 data: 1024 cores for total N, 1054 cores for Olsen-P from 256 1 km × 1 km squares across Great Britain.
  - Habitat and parent-material–level mean estimates derived from CS data from 1978, 1998, and 2007 using a mixed-model approach.

- Modelling approach
  - Means modelled by dominant habitat (from Land Cover Map 2007) and dominant parent material (PMM 2009).
  - Parent material characteristic used: Dominant grain size (DOM_GRAIN). N concentration and C:N ratio also linked to DOM_GRAIN; Olsen-P to DOM_GRAIN.
  - The PMM characteristic chosen to minimise AIC in each model.
  - Limitations: Urban and littoral rock areas are not sampled by Countryside Survey; some habitat/PM combinations have insufficient sample sizes.

- Outputs and structure
  - Estimated mean values for selected habitat–parent material combinations.
  - Data attributes include: LCM_CLASS, LCM_NUMBER, DOM_GRAIN, SOIL_GROUP, CACO3_RANK, NCONC_98/07, CN_98/07, OLSEN_98/07, and corresponding standard errors (e.g., NCONC_98SE, TOTN_07SE, CN_07SE, OLSEN_07SE).
  - Spatial reference: OSGB 1936 / British National Grid (EPSG:27700).

- Data collection and methods
  - Experimental design: 1024 plots in 2007; 1110 plots in 1998; about 75% of 2007 plots also sampled in 1998; Olsen-P measured in 1068 plots in 2007 (65% overlap with 1998).
  - Sampling method: 15 cm long by 5 cm diameter cores collected per field protocol (Emmett et al. 2008).
  - Analytical methods:
    - Total N: measured with a total elemental analyser (CEH Lancaster UKAS SOP3102).
    - Olsen-P: extracted with 0.5 M NaHCO3 (pH 8.5) and determined colorimetrically using molybdenum blue with dialysis to reduce interference (air-dried, <2 mm sieved soil).
  - Quality control: Adherence to Defra/NERC Joint Codes of Practice.

- Related references and supporting documents
  - Emmett et al. 2008, 2010 (Soils Manual; Soils Report from 2007).
  - Scott 2008 (Statistical Report).
  - Mortom et al. 2011 (Land Cover Map 2007 data).
  - Additional CS outputs and PMM material references (BGS Soil Parent Material Model).