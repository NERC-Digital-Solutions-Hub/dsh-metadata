# Ozone exposure and physiological responses in Lolium perenne and Trifolium repens under monoculture and mixed-canopy conditions

## Purpose and scope
- Investigates how ozone exposure affects growth and photosynthetic physiology of two pasture species, Lolium perenne (ryegrass) and Trifolium repens (white clover).
- Compares plant performance in monocultures versus mixed cultures to assess competition effects under ozone stress.
- Aims to identify measurable environmental health indicators (biomass, carbon and nitrogen content, and photosynthetic capacity) that could inform monitoring and decision-making.

## Experimental design
- Plant material and origin
  - Lolium perenne and Trifolium repens vegetatively propagated from pasture turf near Edinburgh, UK.
  - Plants originated from different parents and were randomized among competition (monoculture vs mixture) and ozone treatments.
  - Established for ~8 weeks before exposure into experimental pots.
- Setup
  - Large containers (solardomes) with specified dimensions (35.5 cm x 45 cm x 25 cm) and drainage.
  - Each pot contained 12 plants (4 central, 8 surrounding) arranged to create a central turf surrounded by outer plants.
  - Three pots per species per condition (monoculture or mixture) per solardome.

## Treatments and ozone exposure
- Experimental units
  - Four solardomes used for ozone exposure; arranged in a randomized block design.
  - Two domes served as controls (ozone-free air filtered with charcoal); two exposed to ozone with a rural episodic profile.
- Ozone regime
  - Target concentrations: 30 ppb baseline, peaking at 80–100 ppb on days 1–3, with 30 ppb otherwise.
  - Daily cycle: rise from 30 to max over 2 hours, 6 hours at max, then fall back over 2 hours; 30 ppb maintained at other times.
  - Continuous monitoring of ozone every 30 minutes in each dome.
- Exposure duration
  - 12 weeks total, with two harvest periods: 26 July–6 Sept and 7 Sept–16 Oct.

## Harvesting and biomass assessment
- Harvest schedule
  - Two harvest points corresponding to the end of each exposure period.
  - At final harvest, additional layer (0–7 cm) included.
- Layered biomass collection
  - Material categorized by canopy layer: outside pot perimeter, >14 cm above soil, 7–14 cm above soil, and (at final harvest) 0–7 cm.
  - Plant material sorted by species and plant part (T. repens: stolons, flowers, leaves; L. perenne: leaves and stems).
- Drying and weighing
  - Samples dried at 65°C for at least 4 days to determine dry weight.
  - Subsamples of L. perenne leaf material analyzed for carbon and nitrogen content (CHNS analyzer).

## Physiological measurements
- Leaf sampling and aging
  - Measurements focused on representative leaves at different ages (Leaf 1: newest fully expanded; Leaf 2: second newest).
  - Minimum of six leaves per measurement day, matching physiological stage.
- Photosynthetic assessments
  - A-Ci curves: net CO2 assimilation rate (A) vs. substomatal CO2 concentration (Ci) to gauge photosynthetic efficiency and capacity.
  - Light-response (AQ) curves: A vs. photosynthetic photon flux density (PAR) to determine photosynthetic capacity.
  - Instrumentation: CIRAS I with automatic cuvette; constant 1000 μmol m^-2 s^-1 PAR for A-Ci; CO2 steps from 0 to 2000 ppm; similar approach for AQ with PAR steps up to 2000 μmol m^-2 s^-1.
  - Derived parameters: maximum carboxylation velocity (Vc,max) and maximum electron transport rate (Jmax) using standard Farquhar et al. model procedures and linear fits to high Ci data.
- Data processing
  - Use of model equations and empirical adjustments (e.g., I*) to estimate Jmax; average values per plant for comparisons.

## Data and statistical analysis
- Data aggregation
  - Per-solardome mean values used for all statistical analyses.
- Statistical approaches
  - One-way ANOVA (Minitab) to assess ozone effects on Jmax (monoculture vs mixture not directly compared by this test).
  - GLM regression (SPSS) to compare A vs. Ci relationships between treatments.
  - Split-plot and split-split-plot ANOVA (Genstat) with factors: ozone treatment; monoculture vs mixture as subplot; canopy position as sub-subplot for biomass partitioning.
- Data structures and datasets
  - Lolium_and_Trifolium_solardomes_ACi_Curve_data.csv: 220 rows, 7 columns (Species, Leaf number, weeks, Treatment, dome.pot, Ci, A corrected)
  - Lolium_and_Trifolium_solardomes_biomass_data.csv: 16 rows, 6 columns (Harvest, Species, Monoculture or mixture, Ozone treatment, dry weight, standard error)
  - Lolium_and_Trifolium_solardomes_clover_distribution_data.csv: 28 rows, 6 columns (Harvest, Monoculture/mixture, part of canopy, Ozone treatment, dry weight, standard error)
  - Lolium_and_Trifolium_solardomes_Lolium_distribution_data.csv: 32 rows, 6 columns (Harvest, Monoculture/mixture, part of canopy, Ozone treatment, dry weight, standard error)

## Relevance to monitoring frameworks (environmental health monitoring)
- Data quality and governance
  - Emphasizes rigorous data collection protocols (standardized harvesting layers, repeated measures, and calibration of ozone instruments).
  - Requires complete metadata and provenance (treatment, canopy context, harvest times) to ensure traceability.
  - Highlights challenges in data sharing and the need for transparent reporting of underlying data and methods.
- Data availability and access
  - Generates structured datasets (ACi/AQ curves, biomass by canopy layer, C and N content) suitable for long-term monitoring and meta-analyses.
  - Underlines potential barriers to data reuse if metadata are incomplete or formats are heterogeneous.
- Standardization and interoperability
  - Demonstrates clear definitions for experimental treatments, canopy configurations, and measurement protocols, aiding comparability across monitoring programs.
  - The explicit data structures (CSV schemas) support consistent data archiving and reuse.
- Implications for policy and decision-making
  - Provides a framework for linking environmental exposure (ozone) to biological responses (biomass, tissue chemistry, photosynthetic capacity), informing risk assessment and management strategies under air quality policies.
  - Suggests monitoring strategies include multiple life stages (two harvest points), functional readouts (A-Ci, Jmax, Vc,max), and context (monoculture vs mixture) to capture ecosystem-level resilience.

## Practical takeaways for monitoring and decision-making
- When evaluating environmental health, combine exposure metrics (ozone concentration patterns) with organism-level responses (biomass, C/N content) and physiological capacity (A-Ci, Jmax, Vc,max) across relevant life stages.
- Include context of plant competition or canopy structure (monoculture vs mixed) to understand interaction effects under stress.
- Ensure robust data governance: complete metadata, accessible datasets, transparent sharing practices, and consistent data formats to facilitate reuse in policy monitoring and impact assessment.