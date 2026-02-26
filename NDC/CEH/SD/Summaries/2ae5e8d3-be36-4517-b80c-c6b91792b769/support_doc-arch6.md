# Limits to adaptation: Causes and consequences for ecology and ecosystem function

## Overview
- Large-scale mesocosm experiment investigating how genetic diversity and intrinsic plasticity in Daphnia magna affect ecosystem responses to repeated heatwaves.
- Conducted in 42 3000 L mesocosms at Ness Botanical Gardens, UK, with 7 treatments manipulating heatwaves, genetic diversity, and plasticity.
- Data are organized into five downloadable CSV datasets, covering environmental conditions, phenotypic evolution, community composition, and clone-frequency dynamics across time.

## Experimental design (highlights)
- Treatments manipulating heatwave exposure, genetic diversity, and plasticity across mesocosms.
- Two recorded summer heatwaves introduced in specific windows; comparisons made across diversity and plasticity levels.
- Data collected over roughly 2017–2019, enabling analysis of short- and medium-term responses to heat stress.

## Data assets (CSV datasets)

- Data set 1 — Hourly temperature
  - 42 mesocosms, 5-minute temperature measurements at 50 cm depth using sun-protected sensors and data loggers.
  - Heatwaves: two specified periods; some mesocosms designed as heatwave controls (no heatwave).
  - Timeframe: July 2017 – September 2019.
  - File: temp_hourly_Jul17_Sept19.csv (10.8 MB).
  - Key columns: Date.Time, Tank_2 to Tank_50 with hourly/dated temperature values.

- Data set 2 — Environmental parameters
  - Biweekly to monthly environmental measurements across mesocosms, covering treatment, block, and a broad suite of water-quality metrics.
  - Variables include chlorophyll a, oxygen saturation and concentration, pH, conductivity, light transmission (water and surface), nutrient concentrations (DP, DN, NH4, TP, TN), and presence/absence of D. magna.
  - File: ecosystems.bothyrs.csv (164 KB).
  - Includes metadata: mesocosm, date of measurement, and treatment descriptors.

- Data set 3 — Phenotypic evolution
  - Common-garden life-history assays on D. magna across five timepoints (Sept 2017; Mar 2018; Jun 2018; Aug 2018; Oct 2018).
  - Measured nine life-history variables (e.g., age/size at maturity, juvenile/adult growth, offspring metrics, CTmax heat tolerance).
  - Each timepoint samples multiple mesocosms with replicated individuals reared under standard conditions.
  - File: MA1to6data.csv (169 KB).

- Data set 4 — Community data
  - Zooplankton community composition sampled at eight timepoints.
  - Sampling and processing details: depth-integrated water samples, filtration, glycerol storage, microscopic counting and identification to lowest taxonomic level.
  - Taxa include Daphnia species and other microzooplankton; counts provided by mesocosm and timepoint.
  - File: fullComm_CS0added.csv (58 KB).

- Data set 5 — Clone frequency changes
  - Genotyping of D. magna clones at multiple timepoints to track clone-frequency dynamics.
  - Treatments include high plasticity, low plasticity, and maladapted Danish clones; sampling from multiple mesocosms and blocks.
  - Genotyping performed using microsatellite markers; data include timepoint, sample, clone identity, and clone proportion per mesocosm.
  - Files: timepoint-linked clone frequency data (proportions per clone per mesocosm/timepoint).
  - Summary: ~45.5±0.41 genotypes per mesocosm/timepoint; sample coverage varied due to quality.

## Sampling regime and collection
- 42 mesocosms arranged to test interactions between heatwaves, genetic diversity, and plasticity.
- Data collected across multiple domains and frequencies:
  - Temperature: hourly (via 5-minute sensors) with two defined heatwave periods.
  - Environmental parameters: every 2 weeks to months.
  - Phenotypic evolution: five major timepoints across two-year span.
  - Community composition: eight sampling events.
  - Clone frequencies: eight timepoints (with detailed genotyping at select times).
- Data were generated as part of the NERC Highlight grant NE/N016017/1.

## Data quality and provenance
- All data have been checked, verified, and processed for analysis.
- Data are structured in CSV format with clearly defined column descriptions per dataset.
- Experimental metadata (treatment, block, mesocosm, timepoint) accompany measurements to enable reproducible joins across datasets.

## Data structure and formats
- Data are provided as comma-separated values (CSV) across five files:
  - temp_hourly_Jul17_Sept19.csv
  - ecosystems.bothyrs.csv
  - MA1to6data.csv
  - fullComm_CS0added.csv
  - Clone_proportions.csv
- Each dataset includes standard meta-columns (e.g., mesocosm, date/time, treatment, block) plus dataset-specific variables.
- Datasets are designed to be combined for integrated analyses of environmental context, phenotypic responses, community shifts, and genetic dynamics.

## Potential data products and uses (Data Support perspective)
- Self-serve dashboards comparing temperature regimes with phenotypic changes (e.g., CTmax, maturation traits) across treatments.
- Cross-dataset analyses of heatwave exposure versus community composition shifts and clone-frequency dynamics.
- Data transformations to explore genotype-by-environment interactions, plasticity effects, and ecological resilience.
- Time-series visualizations of temperature, water quality, and community trajectories aligned to heatwave events.
- Reports or interactive tools highlighting how genetic diversity and plasticity modulate ecosystem function under thermal stress.

## References
- Geerts AN, Vanoverbeke J, Vanschoenwinkel B, Van Doorslaer W, Feuchtmayr H, Atkinson D, Moss B, Davidson TA, Sayer CD, De Meester L (2015) Rapid evolution of thermal tolerance in the water flea Daphnia. Nature Climate Change, 5: 665-668
- Plaistow SJ, Collin H (2014) Phenotypic integration plasticity in Daphnia magna: an integral facet of G × E interactions. J Evol Biol, 27: 1913-1920