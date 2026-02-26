# Soil microbial community resilience data from Sourhope field experiment site, Scotland, 2001 [NERC Soil Biodiversity Programme]

## Scope and Purpose
- Data collected under the NERC Soil Biodiversity Thematic Programme to understand links between microbial diversity and soil resilience.
- Includes functional resilience metrics under perturbations (heat and copper) and microbial community structure data (DGGE).

## Data Assets
- Two supporting CSV datasets:
  - 1007: Resilience Soil Analysis (P2125_RESILIENCE_SOIL_ANALYSIS.csv) collected November 2001; analyses at Scottish Crop Research Institute, Invergowrie.
  - 1008: Resilience DGGE Analysis (P2125_RESILIENCE_DGGE_ANALYSIS.csv) analyzed at University of Aberdeen.
- Metadata describe sampling design, treatments, and analysis context; includes data dictionaries for each column.

## Experimental Context
- Location: Sourhope field site, upland grassland in the Cheviot hills, southern Scotland.
- Design: Randomised block with five replicate plots; five treatments including untreated control, biocide, N and lime, sewage sludge, and reseeding with Lolium perenne.
- Sampling: November 2001; soil cores collected to 100 mm depth; soils prepared and stored for analysis.
- Treatments details: CaCO3 and NH4NO3 applications, sewage sludge application in 1999–2000, biocide treatment with chlorpyrifos, reseeding of turf.

## Data Schema and Variables
- 1007 Resilience Soil Analysis:
  - Key fields: SAMPLEID, BLOCK, MAIN_PLOT, SUB_PLOT, CELL_X, CELL_Y, SAMPLING_DATE, TREATMENT.
  - Soil properties: pH (CaCl2), NH4_N, NO3_N, MINERAL_N, DOC, FUM_C (microbial biomass C), BASAL_RESPIRATION, QCO2.
  - Functional resilience metrics: RESISTANCE_HEAT, RECOVERY_HEAT, RESILIENCE_HEAT_EXP; RESISTANCE_CU, RECOVERY_CU.
  - Units and data types provided (e.g., mg g-1 soil, ug C g-1 soil h-1, percentages, etc.).
- 1008 Resilience DGGE Analysis:
  - Key fields: SAMPLEID, BLOCK, MAIN_PLOT, SUB_PLOT, CELL_X, CELL_Y, SAMPLING_DATE, TREATMENT.
  - DGGE-derived variables: PC01–PC05 (principal components from DGGE profiles).
- Both datasets include provenance notes and references to the underlying methods.

## Data Processing, Analysis
- Experimental soils bulked and processed with controlled treatments (heat or copper perturbations) to measure CO2 evolution as a proxy for functional capability.
- Calculations include basal respiration, microbial biomass-specific respiration, and metrical indices of resistance, recovery, and resilience under heat and copper stress.
- DGGE data analyzed to produce presence/absence matrices and multivariate PC scores; statistical analyses include ANOVA and principal coordinate analysis with adjustments for gel-to-gel variability.

## Data Quality, Limitations, and Documentation
- Quality control included numeric range checks, formatting checks, and logical integrity checks.
- Datasets subject to quality assurance, but the NERC programme does not warrant accuracy or fitness for a specific use; liability disclaimer applies.

## Access, Usage, and Citation
- Data files are described in Supporting Information and linked to the EIDC catalogue; use should cite the original sources as detailed in the references.
- Primary references include Scott et al. 2003 and related methodological papers; data provenance notes indicate analyses conducted at SRUC Invergowie and University of Aberdeen.

## References
- Key methodological and background sources cited in the documentation (e.g., Griffiths et al., Ritz et al., Kuan et al., Scott et al., Muyzer et al.).