# Soil microbial community resilience data from Sourhope field experiment site, Scotland, 2001 [NERC Soil Biodiversity Programme]

## Overview
- Part of the NERC Soil Biodiversity Thematic Programme (1999–2001) studying soil biodiversity and ecosystem function at Sourhope, Scotland.
- Aimed to understand both diversity of soil biota and functional roles in key ecological processes; involved 24 projects examining soil structure, nutrient cycles, and microfauna/meso- and macro-fauna.

## Experimental site and sampling
- Location: Sourhope field site, Cheviot hills, southern Scotland; grid reference NT8545019630.
- Site characteristics: upland grassland, 309 m above sea level; Brown Forest soil (Sourhope Series); predominant vegetation is Festuca ovina-Agrostis capillaris-Galium saxatile.
- Experimental design: randomised block with five replicate plots; three replicates per treatment sampled in November 2001.
- Treatments:
  - Untreated (control)
  - Biocide application (Dursban 4, chlorpyriphos)
  - N and lime application (600 g CaCO3 m^-2 y^-1 and 24 g NH4NO3 m^-2 y^-1)
  - Sewage sludge application (101 m^-2 in 1999; 201 m^-2 in 2000)
  - Reseeding (Lolium perenne) after turf removal in May 1999
- Sampling: three replicate plots per treatment; soils collected to 100 mm depth; field-moist handling and controlled laboratory preparation to maintain horizon ratios; soils sieved and stored at 4 °C prior to analysis.

## Soil properties measured
- At start: bulked soil analyses including pH (1:5 soil-CaCl2), NH4-N, NO3-N, mineral N, DOC, and microbial biomass C (fumC via chloroform fumigation-extraction).
- Colorimetric analyses for nitrate/nitrite and ammonium after 1 M KCl extraction; measurements performed with a segmented-flow autoanalyser.
- Additional handling: moisture content (105 °C) and maintenance of horizon proportions in homogenised samples.

## Soil respiration and functional stability
- Primary functional metric: rate of carbon mineralisation (short-term decomposition of plant residues) measured via CO2 evolution.
- Perturbations and protocol:
  - Heat perturbation: soils amended and heated to 40 °C for 18 h, then incubated at 15 °C; CO2 quantified by GC-TCD.
  - Copper perturbation: soils amended with CuSO4 to 1 mg Cu g^-1; CO2 evolution measured subsequently.
  - Non-stressed controls: unamended soils with corresponding treatments.
- Metrics:
  - Basal respiration (24 h CO2 from unamended soil)
  - Microbial biomass-specific respiration (CO2 evolved per unit microbial C)
  - Functional resistance and recovery under heat and Cu stress
  - Resilience (logarithmic fit) over 28 days after perturbation

## Bioassay of soil pore water and copper toxicity
- Lux-marked luminescent biosensor Escherichia coli (HB101) used to assess copper bioavailability effects.
- Soil pore water extracts prepared from Cu-amended soils, spiked to 1000 mg Cu kg^-1, then diluted to obtain optimal biosensor response.
- Luminescence measured (relative light units, RLU) after 15 minutes to infer copper bioavailability and community response.

## Microbial community structure
- DNA extraction from 0.5 g soil; PCR amplification of 16S rRNA genes; DGGE profiling.
- DGGE analysis performed to capture community structure shifts across treatments; samples run on 15 h gels.

## Data analysis
- Functional data: analysis of variance (ANOVA) in Genstat; functional capability expressed as a percentage of non-perturbed control for each sampling day after perturbation.
- DGGE data: band presence/absence scored; patterns analyzed by principal coordinate analysis (PCoA); ANOVA on PCoA scores.
- Quality control for DGGE: randomisation of lanes; comparisons made within same gel to avoid gel-to-gel bias.

## Data structure and content
- Dataset 1007: Resilience Soil Analysis (P2125_RESILIENCE_SOIL_ANALYSIS.csv)
  - Columns include: SAMPLEID, BLOCK, MAIN_PLOT, SUB_PLOT, CELL_X, CELL_Y, SAMPLING_DATE, TREATMENT, pH, NH4_N, NO3_N, MINERAL_N, DOC, FUM_C, BASAL_RESPIRATION, QCO2, RESISTANCE_HEAT, RECOVERY_HEAT, RESILIENCE_HEAT_EXP, RESISTANCE_CU, RECOVERY_CU, etc.
  - Purpose: soil analyses on bulked samples from control, sewage, biocide, N+lime, and reseeded plots (Nov 2001); analyses conducted at Scottish Crop Research Institute.
- Dataset 1008: Resilience DGGE Analysis (P2125_RESILIENCE_DGGE_ANALYSIS.csv)
  - Columns include: SAMPLEID, BLOCK, MAIN_PLOT, SUB_PLOT, CELL_X, CELL_Y, SAMPLING_DATE, TREATMENT, PC01–PC05 (principal components from DGGE profiles).
  - Purpose: DGGE analysis of bulked soil samples (16S rRNA gene profiling) from the same plot treatments; analyses performed at University of Aberdeen.

## Data quality and usage statements
- Quality control: numeric range checks, formatting controls, and logical integrity checks applied.
- Limitations: despite QA procedures, data accuracy cannot be guaranteed by NERC; the programme disclaims liability for data fitness or outcomes from their use.

## References and further reading
- Includes methodological and contextual references for qCO2, soil respiration, DGGE, and the Sourhope field data handbook, among others, detailing measurement techniques and prior analyses related to soil biodiversity and function.