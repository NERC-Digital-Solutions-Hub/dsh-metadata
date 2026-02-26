# Temperature and copper effects on the nematode Caenorhabditis elegans

## Metadata and dataset association
- Dataset metadata accompany a dataset titled Temperature and copper effects on the nematode Caenorhabditis elegans and are associated with the journal paper Variable temperature stress in the nematode Caenorhabditis elegans (Maupas) and its implications for sensitivity to an additional chemical stressor.
- Key metadata fields and units include:
  - Temperature: average test temperature (degrees Celsius), Variation (degrees Celsius) around the average
  - Plate: test plate number; Replicate: replicate number
  - Cu (mg/L): copper concentration in agar; Day: day after eggs are laid
  - Length ('m) Day 'n' (micrometers): body length on the test day
  - Offspring (count): number of offspring
- Data file: temperatureandcoppereffectsonnematodes.csv (columns include Plate, Replicate, Cu, Day, Length, Offspring, among others)
- Data provenance: processed and analyzed using R (versions around 2.12.0); datasets recorded June–October 2013; copper content measured in water fraction vs agar-bound copper; analyses included blanks and reference materials (e.g., NIST 1577c)

## Experimental design
- Organism and culture
  - Caenorhabditis elegans (N2 Bristol) cultured on NGM agar with E. coli OP50; maintained in darkness at 20°C
  - Cultures acclimated at selected test temperatures for several generations (minimum two weeks) prior to experiments
- Temperature regimes
  - Constant temperatures: 8, 12, 16, 20, 24°C
  - Variable temperature scenarios: daily fluctuations of ±4°C (ranges 8–16, 12–20, 16–24°C; means 12, 16, 20°C respectively) and ±8°C (range 8–24°C; mean 16°C)
  - Temperature changes at 4°C per hour
- Copper exposure
  - Copper (CuCl2) added to NGM agar to achieve 0, 1, 3, 8, 20, 40 mg Cu/L
  - Stock solution prepared (2 g Cu/L) and mixed into molten agar; new batches produced every five days to minimize copper immobilization
- Cohort preparation and exposure
  - Synchronized cohorts produced from adults laid eggs on copper-spiked plates; eggs hatch and develop to L4 on copper-spiked plates
  - One worm per well in 12-well plates with copper-spiked NGM and E. coli; control groups included with 24°C constant, 8–16°C, 8–24°C, and 16–24°C regimes
  - Replication: 12 worms per treatment, 24–36 for certain controls; some 8°C treatments had 6–12 worms due to availability
- Data collection
  - Daily transfers to fresh wells; monitoring continues through reproductive and senescence stages until death
  - Measurements:
    - Time to first egg laid (TFE)
    - Daily egg production (brood size)
    - Lifespan (death determined by lack of response)
    - Body length measurements using microscopy and imaging software
  - Offspring counted as fertile eggs and larvae; infertile eggs excluded from brood size
- Copper analysis
  - Copper content measured in water fraction one and five days after production to distinguish dissolved vs. agar-bound copper
  - Analytical method: graphite furnace AAS with blanks, spike references, and NIST reference material

## Data structure and content
- Data file name: temperatureandcoppereffectsonnematodes.csv
- Key columns and definitions
  - Plate: randomized plate number
  - Replicate: replicate number
  - Cu: copper concentration in mg/L in agar
  - Day: day after eggs laid
  - Length: body length in micrometers (measured from L4 stage onward)
  - Offspring: count of fertile eggs and larvae; zero if none
- Termination: experiment ends when the last worm dies (end of data region)
- Data organization supports per-worm longitudinal tracking across days and copper treatments

## Analysis and statistics
- Temperature effects on brood size, lifespan, and maximal length (non-Cu exposed) assessed by one-way ANOVA with Tukey post hoc tests (R 2.12.0)
- Cumulative egg production modeled with a three-parameter log-logistic sigmoid:
  - y = d / [1 + (x / e)^b]
  - d: maximum number of eggs produced
  - e: time when half the maximum eggs are produced
  - b: slope parameter
  - x: time
  - y: accumulated eggs
- Time to first egg (TFE) estimated by solving the model for y = 1/d; standard errors provided by the DRC package in R

## Quality assurance, provenance, and limitations
- Data collection window and replication strategies documented; synchronized cohorts used to ensure comparability
- Copper measurements included quality controls (blanks, spiked references, standard reference material)
- Batch preparation of NGM every five days to maintain copper bioavailability
- The highest copper concentrations are substantially above typical environmental levels, which may affect ecological relevance and transferability of results

## Reuse considerations for Data Stewards
- Metadata completeness supports discoverability: explicit units, explanations, and data structure details
- Clear association with a journal article and dataset DOI enhances traceability and citation
- Documentation of experimental conditions (temperature regimes, copper concentrations, culture methods) facilitates reproducibility and cross-study integration
- Consider potential interoperability improvements when dealing with non-interoperable legacy formats or heterogeneous systems across studies with large datasets