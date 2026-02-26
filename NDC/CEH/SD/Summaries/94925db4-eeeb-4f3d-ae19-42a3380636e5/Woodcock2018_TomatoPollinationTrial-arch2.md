# Data describing pollination of tomatoes by the bees Bombus terrestris and Lasioglossum spp.

## Overview
- Describes an experimental test of potential over-yielding effects on fruit set and average fruit size for tomato plants in the presence of three pollinator combinations: Bombus terrestris alone; Lasioglossum spp. alone; and an additive combination of both.
- Conducted in 2017 under the CEH Commercial Innovation Fund (National Capability) project NEC06344.

## Experimental design and treatments
- Treatments
  - 1) Bombus terrestris alone (single 30–40 worker colony)
  - 2) Lasioglossum spp. alone (native populations of L. malachurum and L. pauxillum)
  - 3) Additive combination of Bombus terrestris and Lasioglossum spp.
- Field setup
  - Earth Trust, Little Whittenham, UK (Lat 51.633329; Lon -1.1956796)
  - Three 2 × 3 m net cages to hold free-flying bees
  - Lasioglossum spp. populations established in two cages; a third cage near but not covering Lasioglossum nests; B. terrestris colonies introduced in or near cages to create the additive treatment
  - Bee density designed to reflect greenhouse practice; ~4.2 nests m^-2 for Lasioglossum spp.
  - Nets used only during experiment to prevent starving wild Lasioglossum
  - Nectar source provided via caged Asteraceae plants
- Plant material and procedure
  - Tomato variety: Moneymaker
  - Plants transferred from greenhouse to field when flowering stems were present
  - Each plant had two flowering stems: one exposed to pollinators under treatments 1–3; the other bagged as an unrewarded control
  - Experimental batches: batches of five plants per treatment per batch; 4-day exposure per batch, repeated four times
  - Post-exposure, plants returned to greenhouse to mature; assessments occurred when tomatoes reached deep red
  - Flower assessment: each stem typically had multiple flowers; assessments focused on the first five flowers per stem
  - Pollination outcomes measured: number of fruits produced (max 5 per stem) and mass of each fruit

## Data collection and structure
- Primary data file: Woodcock2018_tomatoes.csv
  - Plant-level data describing fruit set and fruit size in response to additive pollinator combinations
- Key data fields (examples)
  - Unique_ID: individual tomato plant (60 discrete levels)
  - Treatment: Bombus (Bombus), Lasiog (Lasioglossum spp.), Bomb_Lasiog (additive)
  - Temporal replication: Batch (4 batches)
  - C_Flow_N, C_Flow_set, C_Prop_set, C_Mass_ave, C1_mass, C2_mass, C3_mass, C4_mass, C5_mass: metrics for the control (no bees)
  - T_Flow_N, T_Flow_set, T_Prop_set, T_Mass_ave, T1_mass_mass, T2_mass_mass, T3_mass_mass, T4_mass_mass, T5_mass_mass: metrics for stems exposed to bees
- Measurements
  - Fruit set per stem (proportion and count), average mass of fruits, and individual fruit masses (up to five per stem)
  - Data collected across four temporal replications with five plants per treatment per batch

## Location, timing, and context
- Conducted April–June 2017
- Location: Earth Trust, Little Whittenham, UK
- Data sit within a broader body of work on bee pollination and crop yields (references cited in dataset metadata)

## Data quality and interoperability notes
- Some stems had fewer than five flowers due to accidental damage; this was accounted for in the dataset as part of the stem-level measurements
- Experimental design includes both controlled (no-pollinator) and pollinator-exposed conditions to enable robust comparisons
- Metadata provides explicit variable descriptions and units, facilitating integration with other datasets and cross-study analyses

## References
- Dag A. (2008) Bee pollination of crop plants under environmental conditions unique to enclosures. J. Apic. Res., 47, 162-165.
- Greenleaf S.S. & Kremen C. (2006) Wild bee species increase tomato production and respond differently to surrounding land use in Northern California. Biological Conservation, 133, 81-87.