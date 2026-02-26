# Data describing pollination of tomatoes by the bees Bombus terrestris and Lasioglossum spp.

## Overview and purpose
- Describes an experimental test of how three pollinator treatments affect tomato fruit set and average fruit size:
  - Bombus terrestris alone
  - Lasioglossum spp. alone
  - A combination of B. terrestris and Lasioglossum spp.
- Conducted in 2017 under field conditions using net cages at Earth Trust, Little Whittenham; part of a CEH Commercial Innovation Fund project (Project NEC06344).

## Experimental design and methods
- Treatments and setup
  - Three foraging treatments within field cages (2 × 3 m) to hold free-flying bees.
  - B. terrestris: single colony (30–40 workers) in one cage; a second B. terrestris colony used in another cage to forage within Lasioglossum cages (Treatment 3).
  - Lasioglossum spp.: natural populations (Lasioglossum malachurum and L. pauxillum) established in two cages.
  - Densities chosen to be additive, reflecting greenhouse practice.
- Plant material and setup
  - Tomato variety: Moneymaker.
  - Controlled greenhouse-grown plants, pollinators excluded until transfer to experimental site.
  - Each plant stem had multiple flowers; assessments focused on the first five flowers to mature on each stem.
  - Two flowering stems per plant: one exposed to pollinators per treatment; one bagged to prevent pollination (control).
- Replication and timeline
  - Batches: five plants per treatment per batch, across four temporal batches.
  - Exposure period: four days per batch, after which plants returned to greenhouse to mature.
  - Measurements at maturity: number of fruits per stem (maximum 5) and mass of each fruit.
- Additional context
  - To provide nectar for pollinators (tomatoes produce no nectar), a small quantity of Asteraceae nectar sources was caged near the plants.

## Data collected and structure
- Plant-level data collected on fruit set and fruit size in response to pollinator treatments.
- Key variables (as described in the dataset metadata)
  - Unique_ID: plant-level identifier
  - Treatment: category (Lasiogloss, Bombus, or Bomb_Lasiog)
  - Batch: temporal replication (4 batches)
  - C_Flow_N, C_Flow_set, C_Prop_set, C_Mass_ave: control (no bees) flowering and fruit-set metrics
  - C1_mass ... C5_mass: masses of up to five control fruits
  - T_Flow_N, T_Flow_set, T_Prop_set, T_Mass_ave: corresponding metrics under bee exposure
  - T1_mass_mass ... T5_mass_mass: masses of up to five fruits under bee exposure
- Data dictionary/metadata
  - The dataset includes a comprehensive CSV metadata file: Woodcock2018_tomatoes.csv
  - Variables include units (Discrete, Numerical, Categorical), descriptions, and notes on data collection (e.g., some stems had fewer than 5 flowers due to damage; some fruit masses may be zero if no fruit set).

## Provenance and references
- Authors: Woodcock, B.A. and Pywell, R.F.
- Affiliation: NERC Centre for Ecology & Hydrology, Wallingford, UK
- Funding: CEH Commercial Innovation Fund (National Capability), Project NEC06344
- References:
  - Dag A. (2008) Bee pollination of crop plants under environmental conditions unique to enclosures.
  - Greenleaf S.S. & Kremen C. (2006) Wild bee species increase tomato production and respond differently to surrounding land use.

## Data quality, caveats, and considerations for reuse
- Quality considerations
  - Some plants had fewer than five flowers; there are instances where fruit counts or masses are zero if no fruit set.
  - Experimental conditions (cage environments, nectar provisioning) and potential variability in Lasioglossum populations may influence results.
- Harmonization and interoperability
  - A detailed data dictionary is provided, supporting clear interpretation of each variable and units; essential for cross-study integration.
  - Names and coding of treatments and batches should be consistently applied when aggregating datasets from multiple sources.
- Licensing and sharing
  - The document does not specify licensing terms; confirm data usage terms with the data creators if re-sharing or integration into other repositories.

## Governance and stewardship implications
- Metadata completeness is strong for discoverability and reuse; maintain alignment between the data and its metadata if updates occur.
- Ensure consistent species naming, treatment coding, and unit definitions across related datasets.
- Preserve provenance information (authors, affiliation, funding) for attribution and audit trails.
- Consider attaching or linking to the data dictionary within a data catalogue entry to support downstream data stewards and users.