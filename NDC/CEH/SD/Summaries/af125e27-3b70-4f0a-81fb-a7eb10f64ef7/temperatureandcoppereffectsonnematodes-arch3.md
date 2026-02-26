# Temperature and copper effects on the nematode Caenorhabditis elegans

## Overview
- Investigates how temperature and copper exposure affect Caenorhabditis elegans (N2 Bristol) biology.
- Data collected June–October 2013; experiments conducted under constant and variable temperature regimes with copper spiked into nematode growth medium (NGM) agar.

## Experimental design and exposures
- Organism and culture: C. elegans maintained on NGM agar with E. coli OP50 in darkness at 20°C; acclimated for several generations at selected test temperatures.
- Temperature regimes: 
  - Constant: 8, 12, 16, 20, 24°C.
  - Variable: daily fluctuations of ±4°C (ranges 8–16°C, 12–20°C, 16–24°C) and ±8°C (range 8–24°C) with average temperatures 12, 16, and 20°C respectively; rate of temperature change at 4°C per hour.
- Copper exposures: 0, 1, 3, 8, 20, 40 mg Cu/L in agar; copper stock prepared as CuCl2 in water and added to liquid NGM.
- Experimental setup: 
  - Synchronized cohorts derived from acclimated adults; eggs laid during exposure window (4–6 hours depending on temperature).
  - Offspring raised on copper-spiked plates; one worm per well in 12-well plates; controls with higher replication.
  - Daily transfers to fresh copper-spiked plates; observations recorded through reproductive and senescence stages until death.
- Replication: Usually 12 worms per treatment; 24°C constant, 8–16°C, 8–24°C, and 16–24°C had 36 replicates; 8°C had 6–12 worms per treatment due to availability.

## Measurements and endpoints
- Growth: body length measured at L4 larval stage using imaging software.
- Reproduction: daily offspring counts (fertile eggs and hatched larvae); infertile eggs excluded from brood size; end of reproduction marked by death.
- Timing: time to first egg laid (TFE) derived from brood production data via a sigmoid model.
- Data kept in a structured format with explicit event timing and outcomes.

## Copper analysis and bioavailability
- Water fraction copper measured 1 and 5 days after production to distinguish dissolved vs agar-bound copper.
- Analysis performed with graphite furnace AAS; quality controls included blanks, spiked references, and a NIST standard reference material (NIST 1577c).

## Data structure and documentation
- Dataset file: temperatureandcoppereffectsonnematodes.csv with columns:
  - Plate (randomised treatment plates)
  - Replicate
  - Cu (mg/L in agar)
  - Day (days after egg laying)
  - Length (µm)
  - Offspring (count of fertile eggs and larvae; zero where none)
- Death is indicated by absence of data beyond last observed measurement.

## Data analysis and modelling
- Statistical tests: one-way ANOVA with Tukey post hoc analyses (R v2.12.0).
- Growth and reproduction modelling: average cumulative egg production modeled with a three-parameter log-logistic sigmoid:
  - y = d / (1 + (x / e)^b)
  - d = maximum eggs, e = time to half-maximum, b = slope
- Derived metrics: time to first egg (TFE) estimated from the model; standard errors provided by the DRC package in R.
- Software tools: R 2.12.0 and DRC package.

## Implications for monitoring and data governance
- Demonstrates a structured approach to linking environmental stressors (temperature and copper) with organism responses (growth, reproduction, survivorship).
- Highlights the importance of:
  - Clear metadata and data structure to enable reuse and verification (plate, replicate, Cu, Day, Length, Offspring).
  - Rigorous QA/QC for chemical analyses and sample handling to assess bioavailability (dissolved vs agar-bound copper).
  - Data sharing and public availability of underlying data to support transparency and reproducibility.
- Challenges relevant to monitoring frameworks:
  - Ensuring complete and high-quality metadata; avoiding data silos; public sharing of datasets with appropriate governance.
  - Managing data transformation needs and maintaining up-to-date, well-documented datasets for long-term decision-making.