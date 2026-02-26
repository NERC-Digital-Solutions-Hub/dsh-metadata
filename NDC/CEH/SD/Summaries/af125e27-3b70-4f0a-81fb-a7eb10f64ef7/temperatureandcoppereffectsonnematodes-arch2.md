# Temperature and copper effects on the nematode Caenorhabditis elegans

- Aim
  - Assess how constant and variable temperature regimes, together with copper exposure, affect Caenorhabditis elegans life-history traits and copper bioavailability; provide a standardized dataset for evaluating environmental health and policy-relevant stress responses.

- Organism and culture context
  - Species: Caenorhabditis elegans (N2 Bristol strain)
  - Cultured on nematode growth medium (NGM) agar with E. coli OP50
  - Darkness and acclimatization: grown in darkness at 20°C, acclimatized over several generations to selected test temperatures
  - Regular transfer of culture material to fresh NGM plates weekly

- Experimental design and conditions
  - Temperature regimes
    - Constant: 8, 12, 16, 20, 24°C
    - Variable: daily fluctuations of ±4°C; ranges 8–16°C (avg 12°C), 12–20°C (avg 16°C), 16–24°C (avg 20°C)
    - Extended variability: daily fluctuations of ±8°C in 8–24°C range (avg 16°C)
    - Temperature change rate: 4°C per hour
  - Copper exposure
    - Copper concentrations in agar: 0, 1, 3, 8, 20, 40 mg Cu/L
    - Copper supplied as CuCl2 in demineralized water; copper stock prepared (2 g Cu/L)
    - Fresh copper-spiked batches prepared every five days to limit immobilization in agar
  - Cohort preparation and replication
    - Synchronized cohorts: adults laid eggs on copper-spiked plates at test temperatures; eggs incubated to hatch
    - 12 replicates per treatment; several control treatments with 24–36 replicates
    - Some 8°C tests had fewer worms per treatment (6–12) due to availability
  - Measurements and sampling
    - Daily transfers to fresh wells; observations tracked reproduction and survival
    - Key traits:
      - Time to first egg (TFE)
      - Daily egg production; total offspring (fertile eggs + hatched larvae)
      - Body length measurements from L4 stage onward
    - Termination: when the last worm dies (no further data recorded)

- Copper analysis and bioavailability
  - Copper content measured in water fraction of agar and as agar-bound copper
  - Sampling times: 1 day and 5 days after production
  - Analytical method: graphite furnace AAS (with blanks, spiked references, and NIST standard reference material for QA)

- Data structure and file details
  - Dataset: temperatureandcoppereffectsonnematodes.csv
  - Key variables/columns
    - Plate: TC-plate number; treatment randomization by plate
    - Replicate: replicate number
    - Cu: copper concentration in mg/L
    - Day: day after eggs laid
    - Length: body length in micrometers (µm); measured from L4 stage
    - Offspring: number of fertile eggs and larvae counted (zero if none)
  - Termination indicator: data ends when the last worm dies

- Analysis and modelling approaches
  - Statistical tests
    - One-way ANOVA with Tukey post hoc (R version 2.12.0)
  - Reproductive growth modelling
    - Cumulative egg production modeled with a three-parameter log-logistic sigmoid:
      y = d / (1 + (x/e)^b)
      - d: maximum number of eggs
      - e: time to half-maximum eggs
      - b: slope parameter
    - Time to first egg (TFE) derived by solving for x when y = 1/d
    - Parameter estimation and standard errors provided via the DRC package in R
  - Software
    - R (v2.12.0) and DRC package for dose–response modelling

- Relevance to environmental monitoring and data practices
  - Demonstrates standardized methodology for environmental stressor studies (temperature variability and chemical exposure)
  - Emphasizes data quality assurance, synchronization, and transparent data structure
  - Includes explicit metadata and analytical workflows to support reuse and cross-study comparability
  - Addresses copper bioavailability considerations relevant to environmental risk assessments

- Notes on context and scope
  - Copper concentrations used exceed typical uncontaminated surface water and soil pore water levels, but are comparable to polluted soil pore waters
  - Study links temperature stress with possible altered sensitivity to chemical stressors, informing assessments of combined stressors in natural environments