# Data describing pollination of tomatoes by the bees Bombus terrestris and Lasioglossum spp.

## Overview
- Experimental dataset examining how three pollinator treatments affect tomato fruit set and average fruit size.
- Field-delivered bee pollination experiments conducted in 2017 under CEH funding.
- Aimed at understanding pollination-driven yield differences across pollinator assemblages.

## Experimental design
- Treatments:
  - 1) Bombus terrestris alone (a single 30–40 worker colony).
  - 2) Lasioglossum spp. alone (L. malachurum and L. pauxillum present).
  - 3) Additive combination of Bombus terrestris and Lasioglossum spp. (Bombus colony foraging in Lasioglossum cages).
- Setup:
  - Three cages (2 × 3 m nets) at Earth Trust, Little Whittenham, with field conditions and nectar supplementation using Asteraceae plants to provide nectar for bees.
  - Density: Lasioglossum nests at approximately 4.2 ± 0.8 nests/m2; Bombus colonies introduced as described for treatments.
  - Control: Within each plant, one flowering stem exposed to pollinators (treatments 1–3) and one stem bagged as control.
  - Experimental blocks: Batches of five plants per treatment per temporal replication, with four temporal replicates (4 days per replicate).
  - Tomato variety: Moneymaker; plants moved from greenhouse to cages when flowering; greenhouse pollinator-exclusion prior to exposure.
- Timeline: April–June 2017.

## Data collected (structure and scope)
- Plant-level measurements focusing on pollination outcomes:
  - Fruit set and mass per stem, under both pollinator-exposed and control conditions.
  - Maximums per stem (up to 5 fruits) across observations.
- Temporal replication: 4 batches.
- Spatial context: Field cages within a single site (Earth Trust); coordinates provided for location.
- Data file: Woodcock2018_tomatoes.csv, with detailed metadata for each variable.

## Variables and data fields (key components)
- Unique_ID: Individual tomato plant code (60 discrete levels).
- Treatment: Categorical, describing Lasioglossum, Bombus, or Bombus_Lasiogloss (3 levels).
- Batch: Temporal replication (Discrete, 4 levels).
- C_Flow_N: Number of flowers on control stems (no bees) per stem (numerical, integer; some values adjusted due to damage).
- C_Flow_set: Number of flowers on control stems that set fruit (per stem).
- C_Prop_set: Proportion of control flowers that set fruit.
- C_Mass_ave: Average mass of fruits per control stem.
- C1_mass … C5_mass: Mass of fruit 1 to 5 on control stems (grams; may be zero if no fruit).
- T_Flow_N: Number of flowers on stems when exposed to bees.
- T_Flow_set: Number of flowers that set fruit under bee exposure.
- T_Prop_set: Proportion of flowers that set fruit under bee exposure.
- T_Mass_ave: Average mass of fruits per stem under bee exposure.
- T1_mass_mass … T5_mass_mass: Mass of each fruit 1–5 under bee exposure (grams; may be zero if no fruit).

## Spatial and temporal context for GIS
- Location details: Earth Trust, Little Whittenham, UK; coordinates provided (Latitude 51.633329, Longitude -1.1956796).
- Four temporal replication batches conducted at the same field site.
- Cage layout and proximity among Lasioglossum populations and Bombus colonies described, enabling potential spatial mapping of treatments and outcomes.

## Data quality, uncertainties, and limitations
- Some stems had fewer than 5 flowers due to damage; variable C_Flow_N values.
- Lasioglossum species identification relied on available field populations; potential sampling variability.
- Tomato provides no nectar, necessitating artificial nectar supplementation, which may influence bee foraging behavior.
- Experimental design includes controls (bagged stems) to isolate pollination effects; cage-based setup may introduce enclosure effects.
- Data per plant and per fruit allow granular analysis but require careful handling of zeros (no fruit) in mass fields.

## Provenance and references
- Authors: Woodcock, B.A. and Pywell, R.F. (NERC Centre for Ecology & Hydrology, Wallingford, UK).
- Funding: CEH Commercial Innovation Fund (National Capability), Project NEC06344.
- Related references: Dag (2008); Greenleaf & Kremen (2006).

## GIS-focused use opportunities
- Create spatial maps of fruit set and fruit mass by treatment across the three cages, with the site’s geolocation as a base layer.
- Visualize treatment effects over time using the four temporal batches.
- Combine with environmental layers (soil, microhabitat, surrounding land use) to assess context of pollination outcomes.
- Build a data product that supports policy or client-facing visualization of pollination services by bee assemblages.