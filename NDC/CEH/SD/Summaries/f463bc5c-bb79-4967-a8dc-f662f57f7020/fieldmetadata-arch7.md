# Long-term multisite Scots pine trial, Scotland: field phenotypes, 2013-2020

- Purpose and scope
  - A field-phenotype dataset for Scots pine (Pinus sylvestris) across three field sites in Scotland, capturing growth and phenology from 2013 to 2020.
  - Seed material from 21 native populations (10 trees per population) collected in 2007; families defined as offspring from the same mother tree.

- Spatial context
  - Seed origin: James Hutton Institute, Aberdeen (57.133214, -2.158764).
  - Field sites (transplanted in 2012): Yair (FS, south Scotland), Glensaugh (FE, east Scotland), Inverewe (FW, west Scotland).
  - Field sites coordinates:
    - FS (Yair): 55.603625, -2.893025
    - FE (Glensaugh): 56.893567, -2.535736
    - FW (Inverewe): 57.775714, -5.597181

- Experimental design
  - Planting scheme: randomized blocks, 3 m x 3 m spacing; guard row around block perimeters.
  - Each block contains one individual from each of eight of the 10 families per 21 populations (168 trees per site).
  - Some family replacements occurred due to insufficient trees at FS (9 replacements with other families from the same population).
  - Nursery origins prior to field planting:
    - FS: all trees raised in NG (except some local exceptions)
    - FE: mostly raised in NE; others locally in NE or NG
    - FW: cohorts raised in NW (290), NG (132), and NE (82)
  - Number of blocks: FS and FE have four blocks each; FW has three blocks.

- Measurements and timeframe
  - Growth measurements:
    - Height: end-of-growing-season measurements per year (FE and FW: 2013–2020; FS: 2014–2020)
    - Basal stem diameter: end-of-growing-season measurements (FE and FW: 2013–2020; FS: 2020)
  - Phenology assessments: spring 2015–2019 (2020 not possible due to COVID-19 restrictions)
  - Data captured at the tree level across sites with annual resolution

- Data file and schema (FieldTraits.txt)
  - Key fields and groupings:
    - PopulationCode, Description: population identifier and description
    - Family: family code (siblings from the same mother tree)
    - FieldSite: site code (FE, FS, FW) with corresponding site names
    - FieldCode: unique code for each tree (Inverewe 5001–5672, 6001–6004, 7001–7672; others NA if not transplanted)
    - Block: randomised block code (FE: A/B/C/D; FS: A–D; FW: A–D)
  - Growth metrics by year (7th–14th growing seasons):
    - HA13–HA20: Height in mm
    - HI13–HI20: Height increment per year (mm)
    - DA13–DA20: Base stem diameter (mm)
    - DI14–DI20: Base stem diameter increment (mm)
  - Budburst and phenology measures:
    - BD15–BD20: Duration of budburst (days from stage 4 to stage 6)
    - BT15_4, BT15_5, BT15_6 (and similarly for 2016–2019): Time to reach budburst stages 4, 5, 6 or days since 31 March 2015 for each stage
  - Units and data types:
    - Height and diameter: millimeters (mm)
    - Time metrics: days
  - Note on data quality:
    - Most populations represented at all sites, with 9 replacements at FS due to insufficient trees from some populations
    - COVID-19 restricted phenology data collection in 2020

- Practical GIS relevance
  - Spatial arrangement and coordinates enable mapping of field sites and tree-level data integration with spatial layers.
  - Longitudinal measurements across multiple sites support spatial-temporal analyses of growth and phenology across environmental gradients.
  - Clear site-specific metadata (FieldSite, FieldCode, Block) facilitates linking phenotypic data to precise planting units for GIS workflows.