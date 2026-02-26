# Soil microbial community resilience data from Sourhope field experiment site, Scotland, 2001 [NERC Soil Biodiversity Programme]

## Overview
- Purpose: Investigate the link between microbial diversity and soil resilience within the NERC Soil Biodiversity Thematic Programme.
- Location: Sourhope field site, Cheviot hills, southern Scotland (upland grassland; Sourhope Series soil).
- Experimental design: Randomised block with five treatments; three replicate plots per treatment; sampling conducted in November 2001.
- Scope: Comprehensive study of soil biota and functional processes across multiple soil components (microbial biomass, carbon and nitrogen cycles, community structure).

## Experimental design and treatments
- Treatments:
  - Untreated control
  - Biocide application (Dursban chlorpyriphos)
  - N and lime application (600 g CaCO3 m^-2 y^-1 and 24 g NH4NO3 m^-2 y^-1)
  - Sewage sludge application
  - Reseeding with Lolium perenne
- Plot setup: Five main plots with three replicates per treatment.
- Sampling details: Soils collected from 100 mm depth; litter and surface vegetation removed; soils sieved (4 mm) and stored field-moist at 4°C prior to analysis.
- Environment and measurements: Soil moisture and pH measured; soil horizons preserved in analyses.

## Measurements and biological endpoints
- Soil properties (start of experiment):
  - pH (CaCl2 extraction), NH4-N, NO3-N, Mineral N, DOC, microbial biomass C (fum C).
- Soil respiration and functional stability:
  - Carbon mineralisation rate via CO2 evolution from grass-amended soils after perturbations.
  - Perturbations: heat (40°C for 18 h) and copper (CuSO4.5H2O to 1 mg Cu g^-1).
  - Basal respiration and microbial biomass-specific respiration calculated.
- Bioassay for Cu toxicity:
  - Soil pore water extracts tested with luminescent E. coli HB101 (pUCD607) biosensor.
  - Cu-amended vs. unamended soils; luminescence measured (RLU) to assess copper bioavailability and microbial response.
- Microbial community structure:
  - DNA extraction and DGGE profiling of 16S rRNA genes; analysis via presence/absence and DGGE banding patterns.
- Data handling and timing:
  - Functional capability assessed at 1, 3, 8, 14, and 28 days post-perturbation.

## Data analysis
- Functional resilience metrics:
  - CO2 evolution of perturbed soils as a percentage of non-perturbed, grass-amended soil.
- DGGE data:
  - Convert to presence/absence; analyze with principal coordinate analysis (PCO); ANOVA on PCO scores.
  - Randomisation across gels to minimize bias; only comparisons within the same gel.
- Tools:
  - ANOVA (Genstat for Windows v7); PCO analyses as described; methodological references included.

## Data sets (data products)
- Dataset 1007: Resilience Soil Analysis
  - Soil analyses on bulked samples from control, sewage, biocide, N+lime, and reseeded plots (Nov 2001).
  - Analyzed at Scottish Crop Research Institute, Invergowrie, Dundee.
  - Included fields: SAMPLEID, BLOCK, MAIN_PLOT, SUB_PLOT, CELL_X, CELL_Y, SAMPLING_DATE, TREATMENT, pH, NH4_N, NO3_N, MINERAL_N, DOC, FUM_C, BASAL_RESPIRATION, QCO2, RESISTANCE_HEAT, RECOVERY_HEAT, RESILIENCE_HEAT_EXP, RESISTANCE_CU, RECOVERY_CU, etc.
- Dataset 1008: Resilience DGGE Analysis
  - DGGE analysis of bulked soil samples (Nov 2001) with same plot metadata.
  - Included fields: SAMPLEID, BLOCK, MAIN_PLOT, SUB_PLOT, CELL_X, CELL_Y, SAMPLING_DATE, TREATMENT, PC01–PC05 (principal components of DGGE profiles).

## Data structure and accessibility
- Data provided as two CSV files with detailed column descriptions and standardized metadata, aligned with Sourhope Field Data Handbook references (Scott et al., 2003).
- Datasets enable linking soil chemical properties, microbial activity, copper tolerance, and microbial community structure to treatments and resilience outcomes.

## Quality control and limitations
- Quality assurance steps performed (numeric range checks, formatting, logical integrity).
- NERC provides no warranty on data accuracy or fitness for purpose; liability disclaimer for data use.

## References and context
- Methodological and contextual references include: Anderson & Domsch (1993); Griffiths et al. (2001); Kuan et al. (2006); Muyzer et al. (1993); Ritz et al. (1992); Scott et al. (2003); and related foundational works.