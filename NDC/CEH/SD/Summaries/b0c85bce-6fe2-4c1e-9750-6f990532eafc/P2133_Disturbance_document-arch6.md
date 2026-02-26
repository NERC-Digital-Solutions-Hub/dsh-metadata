# Plant and soil animal diversity measurements from a disturbance and nitrogen addition experiment in an upland grassland site [NERC Soil Biodiversity Programme]

- Summary of purpose: Provides data from the NERC Soil Biodiversity Programme at Sourhope to study how disturbance and nitrogen addition affect plant diversity, soil microarthropods (mites and Collembola), and aboveground biomass in an upland grassland.
- Key topics covered: plant species abundance, microarthropod abundance and diversity, aboveground biomass, and relationships among diversity, biomass, and function under a crossed gradient of disturbance and nitrogen treatments.

## Study site and experimental design

- Location: Sourhope, Cheviot Hills, Southeast Scotland, UK; semi-improved upland grassland at ~350 m altitude.
- Climate/soil: ~1117 mm annual rainfall; humic brown Sourhope soil; dominant plant types listed.
- Experimental layout: five replicated blocks; within each block, five replicated and randomly positioned experimental areas (3 m × 3 m) receiving a crossed gradient of nitrogen addition (0, 60, 120, 180, 240 kg N ha-1) and disturbance (0%, 25%, 50%, 75%, 100% ground cover disturbed).
- Plot design details: continuous 5 × 5 grid (0.5 m2 sub-plots) with buffer zones; nitrogen applied February 2000 and April 2001; disturbance induced December 1999 and December 2000.
- Sampling periods: plant and soil measurements taken on 1–18 August 2000 and 20–23 August 2001.

## Sampling and data collection

- Plant diversity: assessed on sampling dates using point quadrats; metrics include Shannon Wiener diversity index (H), evenness (J), and cumulative species richness (R).
- Functional diversity (belowground): indices calculated for predatory vs. non-predatory mites; overall microarthropod diversity (mites + Collembola) also quantified.
- Aboveground productivity: plots mown to 6 cm, samples dried to obtain biomass.
- Soil cores: three cores per 0.5 m2 plot (3 cm diameter × 5 cm depth) collected for microarthropods; cores combined for analysis.
- Identification: Collembola identified; mites identified to major taxonomic groups where possible.
- Data scope: counts of mites and Collembola (2000 and 2001 for total counts); species-level data collected for 2001.

## Data structure and files

- Four comma-separated value (CSV) files provide the data:
  - Dataset 1047: Matrix plant species abundance data 2000
    - File: P2133_MATRIX_SURVEY2000.csv
    - Key fields: SAMPLING_DATE, BLOCK, MAIN_PLOT, MATRIX_POSITION, DISTURBANCE, NITROGEN, SPECIES, COUNT
  - Dataset 1048: Matrix plant species abundance data 2001
    - File: P2133_MATRIX_SURVEY2001.csv
    - Key fields: SAMPLING_DATE, BLOCK, MAIN_PLOT, MATRIX_POSITION, DISTURBANCE, NITROGEN, SPECIES, COUNT
  - Dataset (MPOD; matrix microarthropod data) within this suite
    - File: P2133_MATRIX_MPOD.csv
    - Key fields: YEAR, BLOCK, MAIN_PLOT, MATRIX_POSITION, DISTURBANCE, NITROGEN, PLANT_BIOMASS, MITES, COLLEMBOLA
  - Dataset 1045: Microarthropod species abundance, 2001
    - File: P2133_MATRIX_MPOD_SPECIES.csv
    - Key fields: YEAR, BLOCK, MAIN_PLOT, MATRIX_POSITION, DISTURBANCE, NITROGEN, SPECIES, COUNT
- Notes on fields: datasets document sampling dates, experimental treatment levels, plot geometry, and per-sample measurements (plant species counts, aboveground biomass, microarthropod counts and species).

## Data quality and limitations

- Quality assurance: numeric range checks, formatting conformity, and logical integrity checks performed.
- Limitations: data are subject to QA procedures but not guaranteed for accuracy or fitness for a specific use; liability disclaimer applies for use of data.
- Related documentation: Users may refer to the SOURHOPE FIELD DATA HANDBOOK (2003) and Usher et al. (2006) for context and methods.

## References and related resources

- Begon, Harper, Townsend (1996) Ecology: Individuals, Populations and Communities
- Burke & Grime (1996) An experimental study of plant community invasibility
- Cole, Buckland, Bardgett (2008) Influence of disturbance and nitrogen addition on plant and soil animal diversity in grassland
- Hopkin (2000) A key to the springtails of Britain and Ireland
- Krantz (1978) A Manual of Acarology
- Related data and methodological resources: SOURHOPE FIELD DATA HANDBOOK 2003; Usher et al. (2006) Applied Soil Ecology
- Site and project records: Project 2133, The relationship between diversity, biomass and function of soil microarthropod communities; Sourhope field data references via EIDC catalogue