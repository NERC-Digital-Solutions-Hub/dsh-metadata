# Temperature and copper effects on the nematode Caenorhabditis elegans

## Dataset overview
- Metadata accompanying the dataset linked to the journal paper "Temperature and copper effects on the nematode Caenorhabditis elegans" with DOI and NERC Environmental Information Data Centre reference.
- Dataset appears as temperatureandcoppereffectsonnematodes.csv, with detailed variable definitions and units.
- Focus: how temperature regimes and copper exposure affect C. elegans growth, reproduction, and size, including analysis-ready measurements and copper speciation.

## Experimental design and organisms
- Organism: Caenorhabditis elegans (N2 Bristol) from the C. elegans Genetics Centre.
- Culture conditions: grown on nematode growth medium (NGM) agar, fed E. coli OP50, in darkness at 20°C; acclimated for several generations at selected test temperatures before experiments.
- Synchronization and cohort generation: adults laid eggs on copper-spiked NGM; eggs hatch and develop to L4 stage before transfer to individual wells for measurements.
- Time frame: data collected between June and October 2013.

## Treatments and exposure conditions
- Temperature regimes:
  - Steady: 8, 12, 16, 20, 24°C.
  - Variable: daily fluctuations of ±4°C at 8-16°C (12°C avg), 12-20°C (16°C avg), 16-24°C (20°C avg); and ±8°C at 8-24°C (16°C avg).
  - Temperature change rate: 4°C per hour.
- Copper exposure: copper concentrations in agar of 0, 1, 3, 8, 20, 40 mg Cu/L.
- Copper stock: CuCl2 in demineralized water (2 g Cu/L); refreshed batches every five days to minimize copper immobilization in agar.
- Replication: generally 12 replicates per treatment; controls (24°C constant, 8-16°C, 8-24°C, 16-24°C) with 24–36 replicates; 8°C sometimes had 6–12 worms per treatment due to availability.

## Measurements and data collected
- Life-history and growth:
  - Daily transfers to fresh wells; record time to first egg laid (TFE) and daily offspring production.
  - Length measurements: body length (micrometers) taken at the L4 stage using Nikon microscopy and imaging software.
- Offspring counts: fertile eggs and hatched larvae counted; infertile eggs excluded from brood size.
- Data timing: measurements continued through reproductive and senescence until death (probed non-responsiveness).
- Copper speciation analysis: copper content in water fraction measured 1 and 5 days after production to distinguish dissolved vs. agar-bound copper via graphite furnace AAS; included blanks, spikes, and NIST standard reference material for validation.

## Data structure and variable definitions
- File: temperatureandcoppereffectsonnematodes.csv
- Key columns:
  - Plate: TC-plate number; randomization by plate.
  - Replicate: replicate number.
  - Cu: copper concentration in mg/L.
  - Day: days after egg laying.
  - Length: body length in micrometers.
  - Offspring: number of fertile eggs and larvae; zeros indicate no offspring.
- Additional notes:
  - Measurements began at L4 stage; data row is removed after death (orange area indicates end).
  - End of experiment when last worm died.

## Data analysis and modelling
- Statistical tests:
  - One-way ANOVA with Tukey post hoc analysis (R version 2.12.0) to compare temperature treatment effects on brood size, lifespan, and maximal length in non-Cu-exposed nematodes.
- Modelling of reproductive output:
  - Cumulative egg production modeled with a three-parameter log-logistic sigmoid: y = d / (1 + (x/e)^b).
  - Parameters:
    - d: maximum total eggs.
    - e: time to half-maximum egg production.
    - b: slope parameter.
  - Derived metric: time to first egg (TFE) obtained by solving x where y = 1/d; standard errors provided via the DRC package in R.
  
## Data quality and reuse considerations
- Quality control:
  - Use of synchronized cohorts and acclimation to each temperature regime to reduce non-treatment variability.
  - Regular copper analysis to assess bioavailable copper fractions.
  - Blanks, spike checks, and reference materials to ensure copper measurement accuracy.
- Data accessibility and re-use:
  - Comprehensive metadata and explicit unit definitions (e.g., Length in micrometers, Cu in mg/L, Day in days) to facilitate reuse.
  - Randomization and replication details documented (plate and replicate identifiers) to support robust secondary analyses.

## Practical notes for data users
- Understand the experimental context (temperature trajectories and copper exposure) before re-analysis.
- When reusing the data, refer to the detailed column definitions and experimental setup to correctly align observations with treatments.
- The provided modelling framework (log-logistic) can be applied or extended to explore temperature-copper interaction effects on reproductive timing and output.