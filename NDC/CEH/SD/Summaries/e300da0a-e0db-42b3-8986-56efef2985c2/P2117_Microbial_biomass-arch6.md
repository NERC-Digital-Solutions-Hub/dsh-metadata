# Microbial biomass measurements from an upland grassland liming experiment [NERC Soil Biodiversity Programme] Johnson, D., Leake, J. R., & Read, D. J. University of Sheffield

## Overview
- Part of the NERC Soil Biodiversity Thematic Programme (launched 1999) aiming to understand soil biodiversity and functional roles in ecological processes across 24 projects.
- Focus of this dataset: soil microbial biomass carbon (Cmic), basal respiration, and metabolic quotient (qCO2) measured in an upland grassland liming experiment at Sourhope.
- Output derived from Project 2117: “The effect of mycorrhizal mycelium on the diversity, biomass and functioning of soil microbial communities and its role in carbon and nutrient cycles.”
- Measurements cover two soil horizons (FH and Ah) under four treatments (control, lime, N, lime + N) across 20 turfs arranged in a randomized block design.
- Data theme: supports analysis of microbial activity and biomass in relation to liming and nitrogen fertilization, contributing to broader soil biodiversity and biogeochemistry research.

## Study site and experimental design
- Location: Sourhope field site, upland grassland, Kelso, Scotland (NGR NT 854196; ~500 m a.s.l.).
- Plot design: 20 turfs (40 cm x 25 cm x 20 cm) from experimental plots (20 m x 12 m) in a 5-block x 4-treatment completely randomized design.
- Treatments:
  - Control
  - Lime (CaCO3)
  - Nitrogen (N)
  - Lime + Nitrogen (N + lime)
- Soil and vegetation context: long-term pasture prior to experiment; acid brown earths with pH 4.5–5.0; ~40% clay in the 2 mm fraction; plant community largely AM-mycorrhizal.
- Management: lime and N applied annually in April/May; plots mown six times per summer; clippings removed.

## Measurements and methods
- Horizons analyzed: FH and Ah.
- Basal respiration: measured with a sealed Respicond automated respirometer; 4 cm diameter soil cores incubated at 22°C; 8-hour logging with 30-minute intervals.
- Microbial biomass carbon (Cmic): determined by substrate-induced respiration; 10 g soil, glucose added (10 mg g dwt-1) in 2 mL water; maximum respiration rate within the first 4 hours used to calculate Cmic.
- Metabolic quotient (qCO2): calculated as basal respiration divided by Cmic.
- Seedling perturbation: described process to study rapid AMF responses (context for methodological sensitivity).
- Data provenance: field site Sourhope; sample labeling and horizon designation follow Scott et al. (2003) and related supporting information.

## Data outputs and schema (Dataset 1081)
- File: Soil microbial biomass 1.0 (P2117_SOIL_MICROBIAL_BIOMASS_1.csv)
- Key fields:
  - SAMPID: Unique sample identifier (text)
  - SAMPLE_DATE: Sampling date (date)
  - BLOCK: Block number (1–5) (numeric)
  - MAIN_PLOT: Main plot label (A–F) (text)
  - HORIZON: Horizon sampled (FH or Ah) (text)
  - TREATMENT: Plot treatment (Control, Lime, N, Lime+N) (text)
  - CMIC: Microbial biomass carbon (mg C per g soil dry weight) (numeric)
  - BASAL: Basal respiration rate (mg CO2 per g soil dwt per hour) (numeric)
  - QC02: Metabolic quotient (mg CO2 per g Cmic per hour) (numeric)
- Notes: Measurement units specified; data types provided; consistent with the described methods.

## Quality control and reliability
- Quality control steps included numeric range checks, formatting conformity, and logical integrity checks.
- Important caveat: NERC cannot guarantee the accuracy or fitness of the data for a given use; data are provided with no liability for use or interpretation.
- Users should consider the experimental context (liming and N treatments, horizon differences, block structure) when integrating with other datasets or building dashboards.

## References and related materials
- Anderson J.P.E. & Domsch K.H. (1978). A method for quantitative measurement of microbial biomass in soils.
- Anderson T.-H. & Domsch K.H. (1993). Metabolic quotient for CO2 (qCO2) as an activity parameter.
- Johnson, D., Leake, J.R., & Read, D.J. (2005). Liming and nitrogen fertilization effects on phosphatase activities, microbial biomass, and mycorrhizal colonisation.
- R. Scott et al. (2003). SOURHOPE FIELD DATA HANDBOOK 2003. Supporting information.
- Usher et al. (2006). Understanding biological diversity in soil: UK Soil Biodiversity Research Programme.

## Data use and potential applications
- Suitable for dashboards or pivot tables comparing Cmic, basal respiration, and qCO2 across treatments and horizons.
- Enables exploration of the impact of liming and nitrogen on soil microbial functioning within upland grassland ecosystems.
- Can be combined with related soil biodiversity datasets from the Sourhope site for broader analyses of soil biogeochemical processes.