# Soil microbial community resilience data from Sourhope field experiment site, Scotland, 2001 [NERC Soil Biodiversity Programme]

## Overview and purpose
- Supporting Information for the project “What is the link between microbial diversity and soil resilience?”
- Part of the NERC Soil Biodiversity Thematic Programme (1999), focusing on understanding soil biota diversity and their functional roles in key ecological processes.
- Data provide measures of soil productivity, community composition, and microbial function under various treatments to assess microbial resilience and functional stability.

## Experimental site and design
- Location: Sourhope field site, Cheviot hills, southern Scotland (grid reference NT854196).
- Site characteristics: upland grassland with a Brown Forest soil; Festuca ovina-Agrostis capillaris-Galium saxatile vegetation.
- Experimental design: randomized block with five replicate plots; three plots sampled per treatment in November 2001.
- Treatments: untreated control; biocide; N and lime addition; sewage sludge application; reseeding with Lolium perenne.
- Sampling and preparation: soils collected to 100 mm depth; field moisture kept; samples air-dried and sieved; soils composed from horizon fractions to maintain original horizon volumes.

## Measurements and properties
- Soil properties measured at the start: soil moisture, pH (CaCl2 method), NO3-N, NH4-N, dissolved organic carbon (DOC), microbial biomass C (via chloroform fumigation-extraction), mineral N.
- Functional soil stability and respiration: carbon mineralisation rate measured via decomposition of standardized grass residues; perturbations included heat (40°C) and copper (CuSO4.5H2O) treatments; control soils left unperturbed.
- Basal respiration and microbial activity: CO2 evolution recorded; microbial biomass-specific respiration calculated (CO2 evolved per mg microbial C per hour).
- Bioavailability and toxicity: soil pore water extracted and tested with a lux-marked E. coli biosensor to assess copper bioavailability and microbial response.
- Microbial community structure: DNA extraction from soil followed by DGGE of 16S rRNA genes to profile bacterial community structure; presence/absence of bands analyzed.

## Data analysis approaches
- Functional resilience metrics: CO2 evolution after perturbation (heat and Cu) relative to non-perturbed controls; resistance, recovery, and resilience quantified for both heat and copper stresses.
- Statistical analyses: ANOVA for each sampling time point; DGGE data analyzed with presence/absence matrices, followed by principal coordinate analysis (PCO) and ANOVA on PCO scores.
- Data handling: randomization across gels to reduce batch effects; comparisons made within the same gel to avoid bias.
- Data interpretation aims: link between microbial diversity, functional stability, and resilience to perturbations.

## Data files and structure
- Dataset reference 1007: Resilience Soil Analysis (P2125_RESILIENCE_SOIL_ANALYSIS.csv)
  - Contents: soil analyses from control, sewage, biocide, N+lime, and reseeded plots (Nov 2001).
  - Key fields: SAMPLEID, BLOCK, MAIN_PLOT, SUB_PLOT, CELL_X, CELL_Y, SAMPLING_DATE, TREATMENT, pH, NH4_N, NO3_N, MINERAL_N, DOC, FUM_C (microbial biomass C), BASAL_RESPIRATION, QCO2, RESISTANCE_HEAT, RECOVERY_HEAT, RESILIENCE_HEAT_EXP, RESISTANCE_CU, RECOVERY_CU, etc.
  - Units and descriptions provided for each variable and measurement method.
- Dataset reference 1008: Resilience DGGE Analysis (P2125_RESILIENCE_DGGE_ANALYSIS.csv)
  - Contents: DGGE profiling results from the same plots.
  - Key fields: SAMPLEID, BLOCK, MAIN_PLOT, SUB_PLOT, CELL_X, CELL_Y, SAMPLING_DATE, TREATMENT, PC01–PC05 (principal components from DGGE profiles).
  - Data reflect DGGE-derived community structure analyses.

## Data quality, governance, and availability
- Quality control: numeric range checks, formatting, and logical integrity checks applied.
- Data provenance: includes QA procedures; NERC does not guarantee accuracy or suitability for specific uses and disclaims liability for data use.
- Metadata and openness: detailed field descriptions, units, and data definitions included to support data reuse and governance; notes demand for data openness and transparent sharing of underlying data.

## Relevance for monitoring frameworks and policy decisions
- Practical measures for environmental health monitoring:
  - Functional resilience metrics: resistance, recovery, and resilience under heat and copper perturbations.
  - Functional stability assessment via CO2 evolution and microbial biomass-related respiration parameters.
  - Bioavailability and toxicity assessment through soil pore-water assays with a biosensor.
  - Microbial community structure profiling (DGGE) to relate diversity patterns to functional responses.
- Data structure and metadata alignment:
  - Comprehensive dataset schema with explicit field definitions, units, and sampling metadata; supports integration into monitoring dashboards and metadata standards.
  - Public sharing of underlying data and associated QA processes aligns with open data and governance expectations, though subject to dataset-specific restrictions.
- Practical challenges and considerations for monitoring authors:
  - Complex datasets requiring transformation and harmonization for cross-site comparisons.
  - Managing data silos and ensuring timely access to datasets (as highlighted in typical monitoring challenges).
  - Need for clear communication of complex results (functional metrics, resilience concepts) to policymakers.

## References and context
- Key references for methods and analyses (e.g., qCO2, DGGE analysis, and resilience concepts) provided to support interpretation and methodological replication.
- Related data-handling handbook and sources cited for data structure and analysis approaches (Scott et al., 2003; Griffiths et al., 2001; Muyzer et al., 1993; Ritz et al., 1992; Usher et al., 2006).