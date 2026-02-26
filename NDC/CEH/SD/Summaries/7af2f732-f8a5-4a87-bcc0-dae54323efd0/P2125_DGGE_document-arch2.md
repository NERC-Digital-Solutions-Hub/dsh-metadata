# Soil microbial community resilience data from Sourhope field experiment site, Scotland, 2001 [NERC Soil Biodiversity Programme]

## Purpose and programme context
- Part of the NERC Soil Biodiversity Thematic Programme (established 1999) to understand soil biodiversity and the functional roles of soil organisms.
- Aimed to link microbial diversity with soil resilience and ecosystem processes through a large field experiment at Sourhope, Scotland.
- 24 projects funded to study soil structure, carbon and nitrogen cycles, and roles of micro-/meso-/macro-fauna across diverse ecological processes.

## Experimental site and design
- Location: Sourhope Research Station, Rigg Foot, Cheviot hills, southern Scotland; upland grassland with Brown Forest soil.
- Site characteristics: 309 m above sea level; Festuca ovina- Agrostis capillaris-Galium saxatile vegetation.
- Experimental design: randomised block with five replicate plots; three replicates sampled per treatment in November 2001.
- Treatments: untreated control; biocide application; N and lime application; sewage sludge application; reseeding.
- Sampling: soils collected to 100 mm depth; field-moist handling, stored at 4°C; soil moisture and pH measured; horizon proportions preserved in sample homogenates.
- Plot management specifics: N and lime inputs (CaCO3 and NH4NO3) and sewage sludge application details; reseeded plots had indigenous turf removed and Lolium perenne introduced.

## Measurements and assays
- Soil properties measured on bulked samples:
  - pH (CaCl2 method), NH4-N, NO3-N, mineral N, and dissolved organic carbon (DOC).
  - Microbial biomass carbon (fumC) via chloroform fumigation-extraction.
- Soil respiration and functional stability:
  - Carbon mineralisation assessed using grass litter with a 20:1 C:N ratio.
  - Perturbations: heat (40°C for 18 h) and copper (CuSO4.5H2O to 1 mg Cu g-1); controls without perturbation.
  - CO2 evolution measured over time; microbial biomass-specific respiration calculated.
  - Basal respiration and resistance/recovery to heat and Cu stress quantified as percent of non-stressed control; resilience modeled over 28 days.
- Bioassay for copper bioavailability:
  - Soil pore water extracts tested with lux-marked E. coli HB101 biosensor; Cu-amended and unamended soils tested across a Cu gradient (0.1–2 mg/L).
  - Luminescence measured to assess bioavailability effects on microbial response.
- Microbial community structure:
  - DNA extraction from 0.5 g soil; PCR amplifications of 16S rRNA genes; DGGE profiling to assess community structure.
  - DGGE data analyzed via presence/absence scoring and principal coordinate analysis (PCO).
- Data analysis methods:
  - ANOVA (Genstat) to compare treatments and timepoints.
  - For DGGE: PCO scores analyzed by ANOVA; randomisation across gels to mitigate gel-bias.

## Data and analyses
- Two datasets included:
  - 1007: Resilience Soil Analysis (P2125_RESILIENCE_SOIL_ANALYSIS.csv)
    - Bulk soil analyses from control, sewage, biocide, N+lime, and reseeded plots (Nov 2001).
    - Variables include SAMPLEID, BLOCK, MAIN_PLOT, SUB_PLOT, sampling date, TREATMENT, pH, NH4-N, NO3-N, MINERAL_N, DOC, FUM_C, BASAL_RESPIRATION, QCO2, RESISTANCE_HEAT, RECOVERY_HEAT, RESILIENCE_HEAT_EXP, RESISTANCE_CU, RECOVERY_CU.
  - 1008: Resilience DGGE Analysis (P2125_RESILIENCE_DGGE_ANALYSIS.csv)
    - DGGE profiles from the same plots; includes SAMPLEID, block/plot details, sampling date, TREATMENT, and principal component scores PC01–PC05.
- Data structure and preparation:
  - Fields include sample identifiers, plot details, sampling date, treatment, and multiple chemical, biological, and functional measurements.
  - Data prepared and analyses conducted with reference to established methodologies (e.g., Griffiths et al., Ritz et al., Scott et al.).

## Quality control and limitations
- Quality assurance steps include numeric range checks, formatting checks, and logical integrity checks.
- Data are subject to QA procedures, but no warranty of accuracy; no liability for use or fitness for a particular purpose.
- Data capture reflects a snapshot from November 2001 and specific plot treatments; interpretation should consider site-specific conditions and experimental perturbations.

## Relevance for environmental monitoring and policy
- Provides standardized, multi-dimensional data to assess soil microbial resilience to perturbations (heat, copper) and management practices (biocide, N+lime, sewage sludge, reseeding).
- Enables cross-dataset integration: combines chemical, microbial activity, community structure, and functional resilience metrics.
- Supports monitoring frameworks by offering clear, comparable outputs (e.g., resistance/recovery metrics, DGGE-based community shifts) across treatments and time.
- Highlights opportunities to combine with other datasets to enhance value and facilitate broader access to underlying data.