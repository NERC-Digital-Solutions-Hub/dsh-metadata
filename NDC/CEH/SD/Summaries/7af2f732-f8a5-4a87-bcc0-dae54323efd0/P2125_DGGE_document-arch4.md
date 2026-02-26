# Soil microbial community resilience data from Sourhope field experiment site, Scotland, 2001 [NERC Soil Biodiversity Programme]

- Overview
  - Part of the NERC Soil Biodiversity Thematic Programme (1999 onward) studying soil biota diversity and their functional roles.
  - Field experiment at Sourhope, southern Scotland; aimed to understand links between microbial diversity and soil resilience.
  - 24 projects funded; focus on soil structure, nutrient cycles, and biota from micro- to macro-scale.
  - Supporting Information includes two primary data sets and methodological details for reuse.

- Experimental site and sampling
  - Location: Sourhope Research Station, Cheviot hills, Scotland; randomised block design with five treatments.
  - Treatments: untreated control; biocide application; N and lime application; sewage sludge application; reseeding.
  - Plot details: three replicates per treatment; November 2001 sampling; soils collected to 100 mm depth.
  - Handling: soils field-moist, sieved (4 mm), stored at 4 C; moisture and pH measured; horizon proportions maintained in bulk samples.

- Measurements and properties measured
  - Soil properties: moisture content, pH (CaCl2 extraction), NO3-N, NH4-N, dissolved organic C (DOC); mineral N; microbial biomass C via chloroform fumigation-extraction.
  - Functional tests: soil respiration and soil functional stability using CO2 evolution from grass residue (C:N 20:1); basal respiration and microbial biomass-specific respiration (qCO2).
  - Perturbation experiments: heat stress (40 C for 18 h) and copper stress (CuSO4.5H2O to 1 mg Cu g-1); post-perturbation CO2 tracking for 24 h.
  - Bioavailability/toxicity: soil pore-water extracts tested with lux-marked luminescent E. coli biosensor to assess Cu bioavailability effects.
  - Microbial community structure: DNA extraction from soil; DGGE profiling of 16S rRNA genes to assess community structure.

- Data collection and analysis approach
  - Data collection timeline: multiple sampling days after perturbation (1, 3, 8, 14, 28 days).
  - Data analyses: ANOVA to compare treatments and perturbation responses; functional capability expressed as a percentage of non-perturbed control.
  - DGGE data: presence/absence scoring across band positions; multivariate analysis with principal coordinate analysis (PCO); gel-ran randomization to reduce technical bias.
  - Data integrity: description of randomization and cross-gel comparison methods to address gel-to-gel variation.

- Data structure and content (two main datasets)
  - Dataset 1007: Resilience Soil Analysis
    - Format: CSV; location and processing details provided.
    - Key fields (examples): SAMPLEID, BLOCK, MAIN_PLOT, SUB_PLOT, SAMPLING_DATE, TREATMENT, pH, NH4_N, NO3_N, MINERAL_N, DOC, FUM_C, BASAL_RESPIRATION, QCO2, RESISTANCE_HEAT, RECOVERY_HEAT, RESISTANCE_CU, RECOVERY_CU, etc.
    - Focus: bulked soil analyses across the five treatments; measurements conducted at SRC Institute, Invergowrie.
  - Dataset 1008: Resilience DGGE Analysis
    - Format: CSV; location and processing details provided.
    - Key fields (examples): SAMPLEID, BLOCK, MAIN_PLOT, SUB_PLOT, SAMPLING_DATE, TREATMENT, PC01–PC05 (principal components from DGGE profiles).
    - Focus: DGGE-derived microbial community structure data across treatments.

- Data provenance and access
  - Source: Supporting Information for the project; datasets prepared for sharing via EIDC catalogue record.
  - Data processing origins: analyses and DGGE performed at Scottish Crop Research Institute and University of Aberdeen, respectively.
  - Quality control: numeric range checks, formatting, and logical integrity checks; however, NERC disclaims warranty of accuracy or fitness for use.
  - References and context: multiple foundational methodological and ecological studies cited for data interpretation (e.g., qCO2, DGGE analysis, soil respiration protocols).

- Implications for data governance and reuse (for Data Leaders)
  - Assets and discoverability: well-documented, multi-parameter soil data linked to a clearly defined field experiment; two complementary datasets (chemical/biological function and community structure) enhance reusability.
  - Metadata richness: extensive description of sampling design, treatments, measurement methods, and data fields supports interpretation and integration with other datasets.
  - Data standards and integration: explicit field definitions and data column mappings facilitate harmonisation with other soil-biodiversity or resilience datasets.
  - Gaps and considerations: data reflect a single time-point sampling event (November 2001) with follow-up perturbation experiments; no ongoing updates indicated; ensure clear licensing and liability notes are observed.
  - Potential collaboration opportunities: data could support cross-study analyses of microbial diversity and resilience, inform meta-analyses, and contribute to broader soil-health monitoring programs; supports ideas of co-ownership and pooled data products.

- References and further reading (selected)
  - Foundational methods and related studies on soil biodiversity, microbial biomass, soil respiration, and DGGE analysis cited to contextualize data interpretations.