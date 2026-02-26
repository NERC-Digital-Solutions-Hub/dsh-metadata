# Biodiversity and structural data from hedgerow management and rejuvenation experiments in England, 2005-2016

- A comprehensive set of long-running hedgerow experiments in England (2005–2016) focused on how hedgerow management and restoration affect biodiversity and habitat quality.
- Three linked experiments:
  - Experiment 1 (2006–2014): Randomised plots testing effects of hedgerow cutting frequency (annual, biennial, triennial) and timing (autumn vs winter).
  - Experiment 2 (2010–2016): Randomised block design evaluating time of cutting, cutting intensity, and cutting frequency with three sites per treatment, plus three replicates per site.
  - Experiment 3 (2010–2013, rejuvenation + post-treatment management): 12 replicates of rejuvenation treatments (Midlands hedge-laying, Conservation hedge-laying, Wildlife hedging, Circular saw, Coppicing, Control) across five sites, followed by split-plot management (annual vs uncut or 2–3 year cycles).
- Five field sites used across experiments, with species-dominated hedges (hawthorn, blackthorn, or mixed) and one banked hedgerow site; one site (Marsh Gibbon) experienced an operational error in 2014 affecting treatment application.

- Primary data themes and measurements:
  - Vegetation and structure
    - Baseline and follow-up vegetation composition, depth of woody species within hedges, hedge density, and gaps from high-resolution hedge photographs analyzed spectrally.
    - Structural metrics including hedge height/width, gappiness, and area/length of gaps.
  - Flower production and flowering communities
    - Annual counts and percent cover for main woody species (hawthorn, blackthorn, bramble) and associated flowering species.
    - Quadrats and plot-level metrics to convert counts to per-meter hedge-length estimates.
  - Berry availability for wildlife
    - Autumn berry counts and biomass (fresh/dry), subsampling details, and berry weights by species.
  - Pollinators and invertebrates
    - Timed pollinator observations (visitation rates for target flowers) with environmental context (temperature, cloud cover, wind).
    - Invertebrate sampling (beating and guttering) and subsequent taxonomic categorisation; weight measurements for invertebrate groups; Lepidoptera egg surveys for specific species.
  - Hedgerow rejuvenation and regrowth (Experiment 3)
    - Aerial regrowth and basal stool regrowth (shoot counts, lengths, biomass, and gear-specific measurements).
    - Shoot and twig measurements, regrowth height/diameter, and woody biomass partitioning for old vs new growth; seedling regeneration and dead-hedge assessments.
  - Recording and timing
    - Data collected via standardised sheets, transcribed to Excel, then loaded to an Oracle database with extensive QC checks.
    - Visit dates and visit years captured for temporal alignment; historic data include pre-visit-year data with only year recorded.

- Data structure and accessibility:
  - Extensive file set representing repeated measures across experiments and sites. Key files include BaselineSpecies.csv, BaselineParameters.csv, Flowers.csv, Dimensions.csv, Berries.csv, BerriesQuadrats.csv, Pollinators* (various), Invertebrates* (various), Gap.csv, Structure.csv, ShootCount.csv, ShootMeasurements.csv, RegrowthAerial.csv, RegrowthBranch.csv, RegrowthLeaves.csv, RegrowthSeedlings.csv, RegrowthShoots.csv, RegrowthStool.csv, RegrowthTotals.csv, RegrowthWeight.csv.
  - Metadata detailing experimental design, treatment codes, site descriptions, plot identifiers, and measurement units.
  - Unique identifiers combine Experiment, Site, Plot, Aspect, Visit Year, and measurement-specific fields to enable integrated cross-dataset analyses.

- Data quality and governance:
  - Standard protocols used for data collection; expert validation of species lists; anomaly checks during transcription and database import.
  - Historic data included where relevant; some pre-visit-year data exist (only year known for  experiments, where applicable).
  - Missing values acknowledged as operational gaps; notes indicate no systemic data fabrication or fabrication.

- Notable limitations and caveats:
  - 2014 MG site data disrupted by an error causing cessation of some treatments at that site.
  - Some data missing where cutting or rejuvenation could not be applied (e.g., certain years/sites).
  - Data across experiments are harmonised for analysis but originate from multiple protocols and measurement timings; careful alignment needed for cross-experiment comparisons.

- Potential uses for Data Leaders and data teams:
  - System-level data integration across hedgerow management practices to identify best-practice data products for biodiversity outcomes.
  - Cross-site data discovery, gap analysis, and standardisation of metadata to support wider networks of partners.
  - Longitudinal analyses of habitat quality, flora/fauna dynamics, and hedgerow structure in response to management regimes.
  - Replicable data governance and QA workflows for complex ecological data collections, including handling of historic data, missing values, and treatment-code mappings.
  - Development of data products and dashboards for policy colleagues and practitioners to support evidence-based hedgerow management decisions.