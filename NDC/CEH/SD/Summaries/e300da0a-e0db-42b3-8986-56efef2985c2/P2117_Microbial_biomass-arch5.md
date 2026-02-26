# Microbial biomass measurements from an upland grassland liming experiment [NERC Soil Biodiversity Programme] Johnson, D., Leake, J. R., & Read, D. J. University of Sheffield

## Overview
- Part of the NERC Soil Biodiversity Thematic Programme (established 1999) focused on understanding soil biodiversity and the functional roles of soil organisms in carbon and nitrogen cycles.
- Datasets measure soil microbial biomass carbon (Cmic), basal respiration rate, and metabolic quotient (qCO2) from an upland grassland liming experiment at Sourhope, UK.
- Data outputs come from a project examining the effects of lime and nitrogen on soil microbial activity and AM fungal associations; linked to the project titled “The effect of mycorrhizal mycelium on the diversity, biomass and functioning of soil microbial communities and its role in carbon and nutrient cycles.”

## Study site and experimental design
- Location: Sourhope field site, upland grassland in Kelso, Scotland (NGR NT 854196; altitude ~500 m a.s.l.); soils are acid brown earths (pH 4.5–5.0) with ~40% clay in the 2 mm fraction.
- Experimental setup: Twenty turfs (40 cm x 25 cm x 20 cm) taken from experimental plots (20 m x 12 m) arranged in a 5-block x 4-treatment completely randomized design.
- Treatments: Control, lime (CaCO3, 39% Ca; 0.6 kg m^-2), nitrogen (NH4NO3, 12 g m^-2), and lime + nitrogen.
- Management: Site fenced, excluded from grazing since 1999; harvested clippings removed; turfs maintained outdoors at Sheffield Experimental Gardens.
- Plant community: 24 higher-plant species, 21 AM-mycorrhiza-forming; vegetation classified as U4d in the British National Vegetation Classification.
- Soil details: Old Red Sandstone-derived soils; 500 m altitude; root/soil disturbance minimized for microbiological measurements.

## Measurements and methods
- Microbial biomass carbon (Cmic) and basal respiration:
  - Basal respiration measured with a sealed system using Respicond automated respirometer; intact soil cores (4 cm diameter) split into FH and Ah horizons; incubated at 22°C with 30-minute measurements over 8 hours.
  - Cmic determined by substrate-induced respiration: 10 g soil incubated at 22°C after glucose addition (10 mg g dwt^-1), with respiration recorded every 20 minutes; the maximum rate within the first 4 hours used to calculate Cmic.
  - Metabolic quotient (qCO2) calculated as basal respiration divided by Cmic.
- Seedling manipulation:
  - Agrostis capillaris L. seeds sterilized and germinated; seedlings introduced into turfs for 10 days to study rapid AMF responses before cessation of perturbation.
- Data captured in Reference 1081 dataset (P2117_SOIL_MICROBIAL_BIOMASS_1.csv) with fields including SAMPID, SAMPLE_DATE, BLOCK, MAIN_PLOT, HORIZON (FH or Ah), TREATMENT, CMIC, BASAL, and QC02.

## Data structure and metadata
- Data outputs and structure:
  - SAMPID: unique sample identifier; SAMPLE_DATE: date of sampling; BLOCK: block number (1–5); MAIN_PLOT: plot letter (A–F); HORIZON: soil horizon (FH or Ah); TREATMENT: applied treatment; CMIC: soil microbial biomass carbon (mg C g soil dwt^-1); BASAL: basal respiration rate (mg CO2 g soil dwt^-1 h^-1); QC02: metabolic quotient (mg CO2 g Cmic^-1 h^-1).
- Documentation and references:
  - Related publications and data handbooks cited (e.g., SOURHOPE FIELD DATA HANDBOOK 2003) and prior work on liming, nitrogen fertilization, phosphatase activities, and AMF colonization.

## Data quality, limitations, and governance
- Quality control: Numeric range checks, formatting checks, and logical integrity checks implemented.
- Documentation: Dataset accompanied by a data dictionary and historical references; The dataset is part of a broader program with multiple linked studies.
- Limitations and liability:
  - NERC QA procedures were applied, but data are not warranted for accuracy or fitness for a particular use; no liability accepted for data use.
  - Data sharing and interpretation should acknowledge potential limitations (disclosure risks, proprietary issues, or embargoes) and refer to accompanying handbooks and publications for context.

## Access, usage, and related materials
- Data linked to the Sourhope Field Data Handbook and related project records; useful for analyses of soil microbial biomass, respiration, and carbon/nitrogen cycling under liming and nitrogen treatments.
- Researchers should consult referenced literature for methodological details and context; dataset appears to be intended for integration into larger soil biodiversity and ecosystem functioning analyses.