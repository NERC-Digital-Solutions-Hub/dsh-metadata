# Aphid_population_plant_mass.csv

## Overview
- Dataset of plant and aphid masses collected from Brassica napus in Free-Air Diesel and Ozone Enrichment (FADOE) rings.
- Sampling occurred over two years (2018–2019) with three experimental runs.
- Rings were placed in a field of wheat (two field locations between 2018 and 2019) and subjected to four pollutant treatments: diesel exhaust (D), ozone (O3), diesel exhaust plus ozone (D+O3), and control (CON).
- Each ring housed two replicate rings per pollutant treatment across the study area.
- Aphid inoculation levels on plants were 50, 10, or 0 aphids, to create varying aphid pressure.
- After eight weeks, aphids were collected, weighed, and plant masses were measured; the key outcome is aphid population mass relative to plant mass.

## Experimental design and collection
- Experimental settings: Full-Air Diesel and Ozone Enrichment (FADOE) rings embedded in an agricultural field; two fields used across years with specified coordinates.
- Treatments:
  - Pollutants: D, O3, D+O3, CON (natural air)
  - Aphid inoculation: 50 aphids, 10 aphids, or 0 aphids
- Replication:
  - In the first, second, and third experimental runs, there were four, seven, and four plant replicates per treatment, respectively.
  - Two rings per pollutant treatment within the field in each year.
- Timing:
  - Plants inoculated when five weeks old.
  - Aphids collected after eight weeks.
- Measurements:
  - Aphid population mass per plant: Aphid_population_mass_g
  - Plant mass: Plant_mass_g (oven-dried)
  - Derived metric: Aphid_population_mass_mg_per_g_plant_mass
- Field locations:
  - 2018: latitude 51.482853, longitude -0.897749
  - 2019: latitude 51.482374, longitude -0.895855
- Reference methodology: FADOE configuration and quality control described in Ryalls et al. 2022 (Environmental Pollution 297, 118847).

## Data columns and variables
- Year (A)
- Ring (B)
- Pollutant (C): D, O3, D+O3, CON
- Treatment (D): aphid inoculation level (50, 10, or 0)
- Plant_ID (E)
- Run (F): experimental run number (1st, 2nd, 3rd)
- Aphid_population_mass_g (G): total aphid mass collected
- Plant_mass_g (H): dry plant mass
- Aphid_population_mass_mg_per_g_plant_mass (I): derived aphid mass per unit plant mass

## Data structure and scope
- Multi-year, multi-run design with replication per pollutant treatment and aphid inoculation level.
- Spatial context provided by coordinates; rings moved between fields between years.
- Data are prepared for analysis of how air pollutants influence aphid mass relative to plant biomass, with potential to model interactions between pollutant type, aphid inoculation level, year, and ring effects.

## Potential analyses and considerations
- Compare aphid mass relative to plant mass across pollutant treatments (D, O3, D+O3, CON).
- Assess influence of aphid inoculation level (50, 10, 0) on aphid/plant mass ratio within and across treatments.
- Examine year-to-year consistency and potential spatial effects (ring-level variation).
- Control for plant biomass by using the derived Aphid_population_mass_mg_per_g_plant_mass as the primary response.
- Consider hierarchical structure (Ring nested within Pollutant treatment; Run effects) and potential data gaps across runs.

## Reference
- Ryalls, J.M.W., Langford, B., Mullinger, N.J., Bromfield, L.M., Nemitz, E., Pfrang, C. & Girling, R.D. 2022. Anthropogenic air pollutants reduce insect-mediated pollination services. Environmental Pollution 297, 118847. (doi:10.1016/j.envpol.2022.118847).