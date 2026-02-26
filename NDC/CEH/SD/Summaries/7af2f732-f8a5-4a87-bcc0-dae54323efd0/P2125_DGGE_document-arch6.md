# Soil microbial community resilience data from Sourhope field experiment site, Scotland, 2001 [NERC Soil Biodiversity Programme]

## Overview
- Part of the NERC Soil Biodiversity Thematic Programme (established 1999) studying soil biota diversity and ecosystem processes at Sourhope, Scottish Borders.
- Aimed to understand links between microbial diversity, community structure, and soil resilience/functional stability.
- Experimental site: Sourhope field station, upland grassland in the Cheviot hills, Scotland; randomized block design with five treatments.

## Experimental design and sampling
- Treatments (three replicate plots per treatment): untreated control, biocide application, N and lime application, sewage sludge application, reseeding.
- Sampling in November 2001; soils collected from randomised plots to 100 mm depth.
- Soil handling: field-moist storage, sieved to remove litter and fauna, soils kept at 4 °C prior to analysis.
- Soil moisture and pH measured; horizon-specific mixing preserved when homogenizing samples.

## Data collection and analysis methods

- Soil properties
  - Measurements: microbial biomass carbon (fumigation-extraction), NO3-N, NH4-N, dissolved organic carbon (DOC), pH (1:5 soil CaCl2), bulked samples.
  - Extraction and analysis: 1M KCl extracts; colorimetric determinations; standard methods cited.

- Soil respiration and functional stability
  - Carbon mineralisation assessed via CO2 evolution from 10 g soil amended with plant residues; perturbations included heat (40 °C) and copper (CuSO4) treatments.
  - Basal respiration computed from 24 h CO2; microbial biomass-specific respiration derived from CO2 per unit microbial C.
  - Functional resistance and recovery measured across time after perturbation (1, 3, 8, 14, 28 days).

- Bioassay of soil pore water and acute Cu toxicity
  - Pore water extracts tested with lux-marked Escherichia coli HB101 to assess copper bioavailability effects on microbial response.
  - Soils amended with copper, incubated 28 days, then luminescence read as relative light units (RLU) to gauge copper impact.

- Microbial community structure
  - DNA extracted from 0.5 g subsamples; 16S rRNA genes amplified and DGGE analyzed to profile community structure.
  - Patterns analyzed via presence/absence scoring, then principal coordinate analysis (PCO).

- Data analysis
  - ANOVA (Genstat) used for treatment effects and temporal sampling.
  - DGGE data analyzed with PCO; gel-running randomized to reduce lane bias; same-gel comparisons only.

## Datasets and data structure

- Dataset reference 1007: Resilience Soil Analysis (P2125_RESILIENCE_SOIL_ANALYSIS.csv)
  - Source: soil analyses on bulked samples from control, sewage, biocide, N+lime, and reseeded plots (November 2001).
  - Analyses conducted at Scottish Crop Research Institute (Invergowrie, Dundee).
  - Key fields include SAMPLEID, BLOCK, MAIN_PLOT, SUB_PLOT, CELL_X, CELL_Y, SAMPLING_DATE, TREATMENT, pH, NH4_N, NO3_N, MINERAL_N, DOC, FUM_C, BASAL_RESPIRATION, QCO2, RESISTANCE_HEAT, RECOVERY_HEAT, RESILIENCE_HEAT_EXP, RESISTANCE_CU, RECOVERY_CU, with explicit units and data types.

- Dataset reference 1008: Resilience DGGE Analysis (P2125_RESILIENCE_DGGE_ANALYSIS.csv)
  - Source: DGGE analysis of bulked soil samples (November 2001); analyses at University of Aberdeen.
  - Key fields include SAMPLEID, BLOCK, MAIN_PLOT, SUB_PLOT, CELL_X, CELL_Y, SAMPLING_DATE, TREATMENT, PC01–PC05 (principal components from DGGE profiles); data describe bacterial community structure patterns.

## Data quality, provenance, and usage notes

- Quality control
  - Numeric range checks, formatting validation, and logical integrity checks implemented.
  - Datasets subject to QA but NERC does not warrant accuracy or fitness for a specific use; data provided with liability disclaimer.

- Provenance and references
  - Methods and analyses align with cited literature (Griffiths et al.; Kuan et al.; Simpson et al.; Scott et al. 2003; etc.).
  - Data linked to the Sourhope Field Data Handbook (2003) and related methodological papers.

## Usage and potential applications

- Enables analyses of how microbial biomass, soil chemistry, and functional stability respond to different treatments and perturbations.
- Supports exploration of links between microbial community structure (DGGE patterns) and functional resilience metrics (heat and copper perturbations).
- Provides a structured, machine-readable data foundation for dashboards or self-service exploration of soil resilience indicators.
- Useful for meta-analyses on soil biodiversity and ecosystem function within managed grassland systems.

## References and further reading (selected)

- Anderson, T.H., Domsch, K.H. (1993). Metabolic quotient for CO2 (qCO2).
- Griffiths, B.S. et al. (2001, 2006). Biodiversity-ecosystem function relationships and resilience.
- Kuan, H.L. et al. (2006). Functional resilience of microbial communities to stresses.
- McCaig, A.E. et al. (2001); Muyzer, G. et al. (1993). DGGE approaches for microbial community profiling.
- Ritz, K. et al. (1992); Wheatley, R.E. et al. (1989). Soil microbial biomass and nutrient extraction methods.