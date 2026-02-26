# Data describing pollination of tomatoes by the bees Bombus terrestris and Lasioglossum spp.

## Overview
- Experimental test of potential overyielding effects on fruit set and average fruit size for tomato plants.
- Three pollinator treatment combinations: Bombus terrestris alone, Lasioglossum spp. alone, and an additive combination of Bombus terrestris and Lasioglossum spp.
- No pollinator controls nested within individual tomato plants; field conditions within three cages.
- Conducted in 2017, funded by CEH Commercial Innovation Fund (National Capability) with NERC support.

## Experimental design and methods
- Treatments
  - Bombus terrestris alone (single 30–40 worker colony)
  - Lasioglossum spp. alone (predominantly L. malachurum with some L. pauxillum)
  - Additive combination of Bombus terrestris and Lasioglossum spp. (two Bombus colonies across cages)
- Field setup
  - Three 2 × 3 m net cages at Earth Trust, Little Whittenham (field conditions)
  - Lasioglossum nests established in two cages; a Bombus colony placed in the third cage or allowed to forage in a cage with Lasioglossum nests (Treatment 3 vs Treatment 2)
  - Lasioglossum density ~ 4.2 nest burrows m^-2
  - Nectar sources provided via Asteraceae plants due to tomato flowers lacking nectar
- Plant material and timing
  - Tomato variety: Moneymaker
  - Plants initially grown under greenhouse conditions, then moved to experimental site
  - Each plant stem had multiple flowers; assessments focused on the first 5 matured flowers per stem
- Experimental procedure
  - Batches: 5 plants per treatment per batch, across 4 temporal replications
  - Exposure periods: 4 days per batch, after which plants returned to greenhouse conditions to mature
  - Measurements after maturation: count fruits per stem (max 5 per stem) and mass of each fruit
  - Replication period: April–June 2017
- References for context
  - Greenleaf & Kremen (2006) on wild bee responses to land use
  - Dag (2008) on bee pollination in enclosures

## Data structure and fields
- Dataset: Woodcock2018_tomatoes.csv
- Experimental units: 60 individual tomato plants (Unique_ID, 60 discrete levels)
- Key fields
  - Treatment: additive combinations describing Lasioglossum alone ('Lasiog'), Bombus alone ('Bombus'), and both ('Bomb_Lasiog')
  - Batch/Temporal replication: 4 batches
  - C_Flow_N: number of flowers on a stem under control (no bees)
  - C_Flow_set: number of flowers that set fruit under control
  - C_Prop_set: proportion of control flowers that set fruit
  - C_Mass_ave: average mass of fruits on the stem under control
  - C1_mass … C5_mass: masses of individual fruits under control (may be zero if no fruit)
  - T_Flow_N, T_Flow_set, T_Prop_set, T_Mass_ave, T1_mass_mass … T5_mass_mass: corresponding metrics under treatment with bees
- Data characteristics
  - Units: discrete counts, numerical values, and masses in grams
  - Structure allows per-plant comparisons of fruit set and fruit mass across treatments and temporal batches
  - Some data points may be reduced or missing due to accidental damage (e.g., flowers not maturing or being lost)

## How to use this data
- Primary questions the data can address
  - Do pollinator combinations (single-species vs. additive) affect fruit set and average fruit size compared with no-pollinator control?
  - Is there evidence of overyielding when Bombus terrestris and Lasioglossum spp. are combined?
  - How do nectar provisioning and field cage conditions influence pollination outcomes?
- Analytic approaches
  - Compare C_ vs T_ metrics to quantify pollination effects on fruit set and mass
  - Evaluate differences across the three treatments (Bombus, Lasioglossum, Bomb_Lasiog) and the control
  - Use per-plant data to model yield outcomes (e.g., fruit set rate, mean fruit mass) with batch as a random or fixed effect
  - Assess interaction effects between treatments and temporal replication
- Practical considerations
  - Account for potential damage-related reductions in counts (e.g., fewer than 5 flowers set)
  - Consider field enclosure effects and local variation in bee densities when interpreting results

## Limitations and caveats
- Local field conditions and cage constraints may affect pollination dynamics
- Some data points reflect damaged or missing flowers, influencing counts and masses
- Lasioglossum densities and cage placement could introduce variability between treatments
- The experiment focuses on a specific tomato variety (Moneymaker) and controlled greenhouse-to-field transition

## References
- Dag A. (2008). Bee pollination of crop plants under environmental conditions unique to enclosures. J. Apic. Res., 47, 162-165.
- Greenleaf S.S. & Kremen C. (2006). Wild bee species increase tomato production and respond differently to surrounding land use in Northern California. Biological Conservation, 133, 81-87.

## Provenance and funding
- Authors: Woodcock, B.A. & Pywell, R.F.
- Affiliation: CEH Centre for Ecology & Hydrology, Wallingford, UK
- Funding: CEH Commercial Innovation Fund (National Capability) project NEC06344; Natural Environment Research Council (NERC) support