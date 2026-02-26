# Temperature and copper effects on the nematode Caenorhabditis elegans

## Overview
- Dataset and accompanying metadata study how temperature and copper exposure affect reproduction, growth, and survival in C. elegans (N2 Bristol strain).
- Experimental design spans constant and variable temperature regimes with copper concentrations to assess interactive stress effects.
- Data support analyses of reproductive output (offspring, time to first egg), growth (body length), and lifespan, with copper quantified in water fraction of the growth medium.

## Experimental design
- Organism and culture: C. elegans (N2 Bristol) cultured on nematode growth medium (NGM) agar with E. coli OP50 in darkness at 20°C prior to acclimation.
- Acclimation: Worms acclimatized through several generations at chosen test temperatures for reliability.
- Temperature regimes: Constant exposures at 8, 12, 16, 20, 24°C; variable temperature regimes with daily fluctuations of ±4°C (ranges 8–16, 12–20, 16–24°C; 12°C, 16°C, 20°C averages) and ±8°C (range 8–24°C; 16°C average).
- Temperature change rate: 4°C per hour.
- Copper exposures: CuCl2 added to NGM to achieve 0, 1, 3, 8, 20, 40 mg Cu/L agar (high concentrations relative to uncontaminated environments; comparable to polluted soils/pore waters).
- Cohort generation: Synchronized cohorts created from adults laid eggs within a 4–6 hour window (shortened to 4 hours at most temperatures, 6 hours at 8°C to increase egg output). Offspring hatched and grown to L4 stage on copper-spiked plates.
- Experimental unit and replication: One worm per well in 12-well plates; 12 replicates per treatment; control regimes included with 24°C constant, 8–16°C, 8–24°C, and 16–24°C (36 replicates). The 8°C test often had 6–12 worms per treatment.
- Transfer and observation: Daily transfers to fresh plates; daily counts of offspring and observation of development and death; reproduction and senescence tracked until death.
- Food and environment consistency: Fresh batches of copper-spiked NGM produced every five days to limit copper immobilization in the agar.

## Data and variables
- File: temperatureandcoppereffectsonnematodes.csv.
- Key columns and meanings:
  - Plate: TC-plate number; randomization by plate.
  - Replicate: Replicate number.
  - Cu: Copper concentration in mg/L agar.
  - Day: Day after the eggs were laid.
  - Length: Body length in micrometers (measured from L4 stage onward).
  - Offspring: Number of fertile eggs and hatched larvae; infertile eggs excluded.
- Temperature and variation: Distinguish constant versus variable temperature treatments; include average temperature and variation details.
- Time frame for data collection: Exposures and measurements conducted during June–October 2013.
- Growth and reproduction endpoints: Growth trajectory (length), daily offspring production, and cumulative egg production over time.

## Measurements and data processing
- Growth measurement: Body length measured at the L4 larval stage using Nikon DS-Fi1 camera and Nikon NIS Elements Imaging Software 3.2.
- Reproduction: Daily transfer allowed counting of time to first egg and daily egg production; total offspring counted until death.
- Data handling: Fertile eggs and hatched juveniles counted as offspring; visibly infertile eggs excluded.
- Copper bioavailability: Copper content in the water fraction measured at 1 and 5 days post-production to distinguish dissolved copper from agar-bound copper.

## Copper analysis and quality assurance
- Analytical method: Graphite furnace AAS (Perkin Elmer Zeeman 5100) with blanks, spiked references, and NIST 1577c bovine liver standard to ensure validity.
- Quality controls differentiate dissolved copper from copper bound to agar, informing bioavailability considerations.

## Statistical analysis
- Temperature treatment effects on brood size, lifespan, and maximal length (non-Cu exposed) tested with one-way ANOVA and Tukey post hoc comparisons using R version 2.12.0.
- Reproductive dynamics: 3-parameter log-logistic sigmoid model fitted to average cumulative egg production over time using R and the DRC package.
  - Model: y = d / (1 + (x / e)^b), where d is maximum egg production, e is time to half-maximum production, b relates to slope.
  - From the model, time to first egg (TFE) estimated by solving x when y equals 1/d; standard errors provided by the DRC package.

## Data access and provenance
- Metadata is from the NERC Environmental Information Data Centre.
- Associated journal reference: Variable temperature stress in the nematode Caenorhabditis elegans (Maupas) and its implications for sensitivity to an additional chemical stressor.
- Dataset DOI: 10.5285/af125e27-3b70-4f0a-81fb-a7eb10f64ef7.

## Potential uses and caveats for analysts
- Suitable for exploring temperature–copper interactions on C. elegans reproduction, growth, and survival.
- Potential to build predictive models of brood size, TFE, and length under combined thermal and chemical stress.
- Consider scale limitations: laboratory conditions, high copper concentrations, and specific strains/species; results may not generalize to natural environments without caution.
- Data structure and metadata enable integration with other datasets and reproducible analysis, with careful attention to units (µm for length, mg/L for Cu, days for reproduction timing).