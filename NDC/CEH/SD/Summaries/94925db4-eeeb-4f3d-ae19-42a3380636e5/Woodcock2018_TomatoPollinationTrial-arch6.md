# Data describing pollination of tomatoes by the bees Bombus terrestris and Lasioglossum spp.

## Overview
- Describes an experimental test of pollinator effects on tomato fruit set and average fruit size.
- Three pollinator treatment combinations: Bombus terrestris alone, Lasioglossum spp. alone, and an additive combination of B. terrestris and Lasioglossum spp.
- Field-based experimental design with controlled cage setups to compare pollination outcomes.

## Experimental setup
- Location: Earth Trust, Little Whittenham, UK (Latitude 51.633329; Longitude -1.1956796).
- Habitat: Three net cages (2 × 3 m) placed to hold free-flying bees.
- Plant material: Tomato plants (var. Moneymaker) grown under greenhouse conditions, then transferred to field cages.
- Duration: April–June 2017; 4-day exposure periods repeated across four temporal batches.
- Pollinator management: 
  - B. terrestris provided as a 30–40 worker colony (two cages involved; one cage with a colony, one without for the additive treatment).
  - Lasioglossum spp. nests (L. malachurum and L. pauxillum) established in cages; density broadly equivalent across cages (~4.2 nest borrows m^-2).
  - Netting used to exclude pollinators from a control stem on each plant.
- Nectar provision: Asteraceae plants caged to provide nectar since tomato flowers produce no nectar.

## Treatments and pollination conditions
- Treatment 1: Bombus terrestris alone.
- Treatment 2: Lasioglossum spp. alone.
- Treatment 3: Bombus terrestris + Lasioglossum spp. additive combination (reflecting likely greenhouse practice).

## Data collection and structure
- Experimental units: Individual tomato plants (with multiple stems per plant; assessments focused on the first 5 flowers per stem that matured).
- Within-plant design: For each plant, one stem open to pollination (treatment) and one stem protected (control) with a net bag.
- Replication: Batches of five plants per treatment per temporal batch; four batches in total.
- Measurements captured in Woodcock2018_tomatoes.csv include:
  - Plant and treatment identifiers: Unique_ID, Treatment, Batch.
  - Control (no bees) metrics:
    - C_Flow_N: Number of flowers on stems in control.
    - C_Flow_set: Number of flowers that set fruit in control.
    - C_Prop_set: Proportion of flowers that set fruit in control.
    - C_Mass_ave: Average mass of fruits on the stem in control.
    - C1_mass to C5_mass: Mass of individual fruits on the control stem (up to five fruits; may be zero if not set).
  - Treatment (with bees) metrics:
    - T_Flow_N: Number of flowers on stems when exposed to bees.
    - T_Flow_set: Number of flowers that set fruit when exposed to bees.
    - T_Prop_set: Proportion of flowers that set fruit when exposed to bees.
    - T_Mass_ave: Average mass of fruits on the stem when exposed to bees.
    - T1_mass_mass to T5_mass_mass: Mass of individual fruits when exposed to bees (up to five fruits; may be zero if not set).
  - Categorical and numeric data: Units and descriptions provided for each variable; 60 discrete levels for Unique_ID; 4 temporal batches; 3 treatment levels.
- Key notes on data collection:
  - Average flowering per stem: around 7.5 flowers per stem (range 3–12).
  - Some stems had fewer than 5 flowers assessed due to damage.
  - Some units reflect control conditions vs. treatment exposure to bees.

## Dataset provenance and references
- Authors: Woodcock, B.A. and Pywell, R.F.
- Affiliation: NERC Centre for Ecology & Hydrology, Wallingford, UK.
- Funding: CEH Commercial Innovation Fund (National Capability) via Natural Environment Research Council (Project NEC06344).
- Field site and date range: Earth Trust, Little Whittenham; Apr–Jun 2017.
- Related literature: Greenleaf & Kremen (2006); Dag (2008).

## Potential uses and considerations
- Compare yield components across pollinator treatments (fruit set proportion, fruit mass) to assess pollination efficiency and potential overyielding effects.
- Analyze how bee presence (additive combination) affects fruit set versus single-pollinator treatments.
- Explore relationships between floral resource (flowering on stems) and fruit outcomes, using C_ and T_ variables.
- Consider data structure for meta-analysis: plant-level data with paired control vs treatment stems, across four temporal batches.
- Data quality considerations:
  - Some missing or zero-valued fruit masses when no fruit was set.
  - Differences between control and treated stems within the same plant, enabling within-plant comparisons.

## Access and file details
- Primary dataset file: Woodcock2018_tomatoes.csv
- Data columns detail: clearly defined for control and treatment measurements, enabling self-contained analysis of fruit set and mass under three pollination scenarios.