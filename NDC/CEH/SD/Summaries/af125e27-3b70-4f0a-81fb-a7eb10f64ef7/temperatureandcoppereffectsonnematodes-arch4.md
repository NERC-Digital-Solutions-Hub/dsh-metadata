# Temperature and copper effects on the nematode Caenorhabditis elegans

## Overview
- Metadata-backed dataset describing how temperature and copper exposure affect Caenorhabditis elegans (N2 Bristol).
- Associated with the journal paper on variable temperature stress and sensitivity to additional chemical stressors.
- Dataset hosted with the NERC Environmental Information Data Centre; includes explicit variable definitions, units, and data structure.

## Experimental design and organism
- Organism: C. elegans (N2 Bristol), cultured on nematode growth medium (NGM) agar with E. coli OP50, in darkness at 20°C.
- Acclimation: Cultures acclimatized at selected test temperatures for several generations before experiments.
- Synchronization: Adults laid eggs at test temperatures; eggs hatched and offspring grown to L4 stage for testing.
- Temperature regimes:
  - Steady temperatures: 8, 12, 16, 20, 24°C.
  - Variable regimes: daily fluctuations of ±4°C (ranges 8–16, 12–20, 16–24°C; averages 12, 16, 20°C) and ±8°C within 8–24°C (average 16°C); temperature change rate = 4°C/hour.
- Copper exposure: CuCl2 added to NGM; concentrations 0, 1, 3, 8, 20, 40 mg Cu/L.
  - Copper batches prepared every ~5 days to minimize immobilization.
  - Synchronization and exposure conducted on copper-spiked plates with E. coli; eggs laid and hatched on exposure plates.
- Experimental units and replication:
  - 12 replicates per treatment (24°C control and certain variable regimes had 36 replicates).
  - 8°C regime had limited availability, resulting in 6–12 worms per treatment.
  - Each test worm moved to fresh wells daily; one worm per well in 12-well plates after hatch.

## Data collected and variables
- Timing and reproduction:
  - Time to first egg laid (TFE) and daily egg production tracked throughout reproductive and senescent phases until death.
  - Fertile eggs and hatched juveniles counted as offspring; infertile eggs excluded from brood size.
- Morphometrics:
  - Body length measured at the L4 larval stage using microscopy and imaging software (Length in micrometers).
- Copper exposure assessment:
  - Copper content measured in water fraction of agar at 1 and 5 days to distinguish dissolved vs agar-bound copper using graphite furnace AAS; quality control with blanks, spikes, and NIST reference material.
- Data structure:
  - Temperatureandcoppereffectsonnematodes.csv with columns:
    - Plate, Replicate, Cu, Day, Length, Offspring
  - Additional metadata on treatments (temperature, variation, plate randomization) included in the dataset description.

## Analysis and modeling
- Statistical tests:
  - One-way ANOVA with Tukey post hoc for brood size, lifespan, and maximal length for non-Cu-exposed groups.
  - Analyses performed in R (version 2.12.0).
- Growth and reproduction modeling:
  - Average cumulative egg production modeled with a three-parameter log-logistic sigmoid function: y = d / [1 + (x/e)^b].
  - Derived metrics:
    - e (time to half-maximum eggs)
    - d (maximum cumulative eggs)
    - b (slope parameter)
  - Time to first egg (TFE) calculated from the model (x when y = 1/d); standard errors provided by the DRC package.

## Data quality, provenance, and accessibility
- provenance:
  - Data generated from controlled acclimated cultures and synchronized cohorts; experimental conditions documented (temperatures, copper concentrations, transfer schedule).
  - Copper analysis included quality controls and reference materials to ensure validity.
- metadata and discoverability:
  - Clear explanations of each variable, units, and measurement methods; randomization and plate-level design noted.
  - Data file and accompanying metadata enable reuse for cross-study comparisons, meta-analyses, or harmonization with similar datasets.

## Relevance for Data Leaders
- Demonstrates a fully documented data lifecycle: acquisition, processing, storage, annotation, and analysis-ready structure.
- Provides standardized units, explicit variable definitions, and replicable experimental design—facilitating data integration across networks and studies.
- Highlights practical challenges and considerations for data governance: data provenance, quality controls (especially for chemical exposure data), and modeling outputs with transparent assumptions.