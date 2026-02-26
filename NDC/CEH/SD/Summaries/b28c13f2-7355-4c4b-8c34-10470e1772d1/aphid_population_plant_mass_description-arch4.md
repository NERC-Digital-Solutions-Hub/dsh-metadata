# Aphid_population_plant_mass.csv

## Overview
- Dataset of plant biomass and aphid population masses collected from Brassica napus in Free-Air Diesel and Ozone Enrichment (FADOE) rings.
- Spans two years (2018 and 2019) and includes multiple pollution and aphid treatment combinations to study the effects on aphid mass relative to plant mass.
- Measurements include aphid mass, plant mass, and a derived aphid-to-plant mass ratio.

## Experimental Design and Data Structure
- Field setup: FADOE rings placed in a wheat field; rings were moved to an adjacent field in 2019. Each ring has a numeric identifier.
- Location coordinates:
  - 2018: latitude 51.482853, longitude -0.897749
  - 2019: latitude 51.482374, longitude -0.895855
- Pollutant treatments (four levels): diesel exhaust (D), ozone (O3), diesel exhaust + ozone (D+O3), control (CON; natural air).
- Aphid treatments: inoculation of 50 aphids, 10 aphids, or 0 aphids per plant.
- Replicates and runs: four, seven, and four Plant_ID replicates in the first, second, and third experimental runs, respectively; three experimental runs over the two years.
- Sampling and measurement: aphids collected with a pooter after eight weeks; aphid mass recorded in grams; plants oven-dried and weighed in grams.
- Derived metric: aphid population mass per unit plant mass (Aphid_population_mass_mg_per_g_plant_mass).
- Data columns (A–I): Year (A), Ring (B), Pollutant (C), Treatment (D), Plant_ID (E), Run (F), Aphid_population_mass_g (G), Plant_mass_g (H), Aphid_population_mass_mg_per_g_plant_mass (I).

## Data Provenance and Reference
- FADOE configuration methodology and quality controls described in Ryalls et al. (2022): Anthropogenic air pollutants reduce insect-mediated pollination services. Environmental Pollution, 297, 118847. DOI: 10.1016/j.envpol.2022.118847.

## Data Governance and Quality Considerations for Data Leaders
- Metadata considerations:
  - Document measurement methods (pooter aphid collection; oven-drying protocol) and units (grams for masses; derived mg per g for the ratio).
  - Capture site context, including ring positions, year, and field relocation between years.
  - Clarify treatment definitions for Pollutant and Treatment columns.
- Data integration and reuse:
  - Suitable for analyses of pollutant effects on aphid load relative to host plant mass across years and field conditions.
  - Ensure consistent handling of multiple runs and ring assignments to account for potential confounding from field relocation.
- Data quality and gaps:
  - The description references external methodology for FADOE configuration; ensure the associated metadata links to that documentation for full reproducibility.
  - Be aware of potential variability across runs, rings, and field locations when aggregating or comparing treatments.
- Usage and stewardship:
  - Cite the Ryalls et al. (2022) reference when presenting analyses derived from this dataset.
  - Consider expressing data lineage and transformation steps (raw aphid mass, plant mass, and the derived ratio) to support traceability and re-use in broader data networks.