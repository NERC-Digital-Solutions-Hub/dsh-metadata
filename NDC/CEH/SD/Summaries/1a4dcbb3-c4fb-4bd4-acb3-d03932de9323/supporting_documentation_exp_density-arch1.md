# Supporting documentation for the experiment manipulating local population density

## Overview
- Location and species: Wytham Woods, Oxfordshire, UK; great tits, blue tits, marsh tits, and nuthatches.
- Goal: manipulate local population density around selective feeders to study effects on bird visitation; collect RFID-based visitation data to identify correlations and inform predictive analyses.
- Tagging and identification: birds captured (winter or spring), fitted with metal BTO rings and plastic PIT tags; visits recorded when tagged birds landed on perches with RFID antennas.
- Data collection period: January–March 2021; six-week experimental manipulation following ~2-week pre-experiment baseline.

## Experimental design
- Feeder setup: eight sites, each with two selective feeders (one access hole, RFID-enabled perch). Feeders approximately 100 m apart; sunflower seeds provided.
- Experimental vs control sites:
  - Experimental: six sites (1B, 1H, 2C, 6A, 7C, 7H) with one feeder assigned to high-density treatment and the other to low-density treatment.
  - Control: two sites (4G, 6G) used to monitor baseline conditions without density manipulation.
- Density manipulation logic:
  - Based on pre-experiment visitation, the feeder with more visits could be assigned to high-density or low-density treatment at three sites; the assignment was reversed at the other three sites.
  - At all birds with substantial prior presence (≥100 visits during the pre-experimental period), 20% were randomly selected to the low-density treatment and excluded from accessing the high-density feeder.
  - Effectively, low-density feeders restricted access to the 20% subset, while high-density feeders allowed access to all PIT-tagged birds, except the 20% subset.
- Timeline and maintenance:
  - Pre-experiment phase to establish baseline visitation.
  - Experimental manipulation lasting six weeks.
  - Feeders checked and refilled every 2–3 days; performance and data collection monitored regularly.

## Data collection and variables
- Primary dataset: a single CSV containing feeder visitation data with the following fields:
  - date, time, logger (feeder identifier)
  - Bto.ring (individual bird identity)
  - Site (experimental site designation)
  - period (pre/during experiment)
  - treatment ( feeder-level assignment: low/high/c1/c2 for control sites)
  - id.treatment (bird-level assignment: low/high/control)
  - Bto.species.code (greti = great tit, bluti = blue tit, marti = marsh tit, nutha = nuthatch)

## Roles and logistics
- Field team: data collection conducted by Keith McMahon, Sam Croft, and Kristina Beck.
- Purpose of data: enable analysis of how local density manipulation affects visitation patterns, with considerations of species differences and site-specific factors.

## Analytical opportunities and considerations
- Potential analyses:
  - Compare visitation frequency and patterns between high-density and low-density treatments within and across sites.
  - Assess whether effects differ by species or by individual exposure level (id.treatment).
  - Examine pre- vs during-experiment changes to establish causal inferences about density manipulation.
  - Explore temporal patterns (date/time) and feeder-level variation.
- Data quality and scope considerations:
  - Baseline establishment via 2-week pre-experiment phase to inform treatment assignment.
  - Randomization at the individual level (20% subset) to mitigate selection bias for low-density exposure.
  - Data integration across sites and treatments possible due to consistent CSV structure and metadata (site, period, treatment, id.treatment, species).
- Limitations and caveats:
  - The manipulations are site- and individual-level with potential confounding factors (e.g., behavioral differences among species, local habitat variation).
  - Control sites (4G, 6G) provide baseline comparisons but do not implement density manipulation.

## Key takeaways for analysts
- The dataset enables evaluation of how restricting access to feeders (local density manipulation) influences visitation behavior across multiple small passerine species.
- The design includes baseline (pre-experiment) and treatment (during experiment) periods, allowing difference-in-differences-like analyses.
- Rich metadata supports cross-species and cross-site comparative analyses, with clear bifurcation between feeder-level treatment and individual bird-level treatment.