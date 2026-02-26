# Microbial biomass measurements from an upland grassland liming experiment [NERC Soil Biodiversity Programme]

- Purpose and context
  - Part of the NERC Soil Biodiversity Thematic Programme (established 1999) focused on understanding soil biota diversity and functional roles in key ecological processes.
  - Large field experiment at Sourhope, Scotland, with 24 funded projects studying soil structure, processes (carbon and nitrogen cycles), and biota across micro-, meso-, and macro-fauna.
  - This document reports microbial biomass measurements (Cmic), basal respiration, and enzyme-related activity from the Sourhope site to link microbial function with soil processes and plant-microbial interactions.

- Study design and data collected
  - Site and treatments: upland grassland turfs (40 cm x 25 cm x 20 cm) from Sourhope, arranged in a 5-block x 4-treatment, completely randomized design: control, lime, nitrogen (N), and lime + N. Lime applied at 0.6 kg m-2; N applied as NH4NO3 at 12 g m-2; site mown and clippings removed; 40-year fertiliser-free prior history.
  - Soil horizons analyzed: FH (partly mineral) and Ah (ap horizon) horizons.
  - Measurements:
    - Basal respiration rates of soil microbial communities using a sealed respirometer (Respicond).
    - Microbial biomass carbon (Cmic) determined by substrate-induced respiration (glucose addition) with measurements used to compute Cmic.
    - Metabolic quotient (qCO2) calculated as basal respiration divided by Cmic.
  - Method details: intact soil cores incubated at 22°C; respiration recorded at frequent intervals (every 20–30 minutes) over several hours; Cmic derived from peak respiration following glucose addition.
  - Plant and microbial context: common bent grass (Agrostis capillaris) used for some procedures; the plant community includes AM-mycorrhizal associations; soils are acid brown with ~40% clay in the 2 mm fraction.

- Dataset: Soil microbial biomass 1.0 (CSV)
  - File: P2117_SOIL_MICROBIAL_BIOMASS_1.csv (Measurement of microbial biomass carbon and basal respiration rates in soil from control, limed, nitrogen and limed plus nitrogen treatments from the FH and Ah horizons)
  - Key fields:
    - SAMPID: unique sample identifier
    - SAMPLE_DATE: date of sampling
    - BLOCK: block number (1–5)
    - MAIN_PLOT: main plot letter (A–F)
    - HORIZON: soil horizon sampled (FH or Ah)
    - TREATMENT: soil treatment applied (control, lime, N, lime+N)
    - CMIC: microbial biomass carbon (mg C g soil dry weight-1)
    - BASAL: basal respiration rate (mg CO2 g soil dry weight-1 h-1)
    - QC02: metabolic quotient (mg CO2 g Cmic-1 h-1)
  - Data types: SAMPID (text), SAMPLE_DATE (date), BLOCK (number), MAIN_PLOT (text), HORIZON (text), TREATMENT (text), CMIC (numeric), BASAL (numeric), QC02 (numeric)
  - Notes: dataset adheres to a standardized structure aligned with Scott et al., 2003 and linked to the Sourhope Field Data Handbook (2003); supports traceability to experimental design and treatment schemes.

- Data quality, governance, and provenance
  - Quality control: numeric range checks, formatting conformity, and logical integrity checks performed.
  - Limitations: while QA procedures apply, the data are not warranted for accuracy or fitness for any particular use; no liability accepted by NERC for data use.
  - Provenance and references: data originate from the Sourhope field site; linked to multiple publications and the Sourhope Field Data Handbook (2003); broader contextual references include Johnson et al. (2005), Usher et al. (2006), and related soil biodiversity literature.
  - Accessibility and metadata: dataset described with explicit metadata fields and data descriptions; associated references and supporting information available through relevant catalogues (e.g., EIDC) and Scott et al. 2003.

- Relevance for monitoring frameworks
  - Demonstrates capturing functional microbial health indicators (Cmic, basal respiration, qCO2) across treatments to evaluate soil health and ecosystem processes.
  - Highlights data governance needs for environmental monitoring: standardized data schemas, clear metadata, treatment-plot mapping, horizon specificity, and data provenance.
  - Illustrates potential barriers to reuse in monitoring contexts: reliance on site-specific methodological details, need for thorough metadata (e.g., horizon definitions, measurement protocols), and explicit data-use liabilities.
  - Provides a concrete example of linking long-term experimental design with measurable microbial functional indicators, useful for informing data collection standards, quality assurance, and transparent data sharing in environmental health monitoring.