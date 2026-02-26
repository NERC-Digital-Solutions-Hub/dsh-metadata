# Aphid_population_plant_mass.csv

## Overview
- Dataset of plant and aphid population masses for Brassica napus plants within Free-Air Diesel and Ozone Enrichment (FADOE) rings.
- Sampling occurred over two years (2018 and 2019) across four pollutant treatments and varying aphid inoculation levels, with three experimental runs.

## Experimental Design and Collection
- Field setup: FADOE rings distributed within a field of wheat in 2018 (latitude 51.482853, longitude -0.897749) and moved to an adjacent field in 2019 (latitude 51.482374, longitude -0.895855).
- Treatments:
  - Pollutants: diesel exhaust (D), ozone (O3), diesel exhaust + ozone (D+O3), control (CON; natural air).
  - Aphid inoculation: 50 aphids, 10 aphids, or 0 aphids per plant (Treatment Column).
- Experimental structure:
  - Four, seven, and four replicate plants for Run 1, Run 2, and Run 3, respectively.
  - Three experimental runs conducted over the two-year period.
- Measurements after eight weeks:
  - Aphids collected with a pooter and weighed (Aphid_population_mass_g).
  - Plants oven-dried and weighed (Plant_mass_g).
  - Derived metric: Aphid_population_mass_mg_per_g_plant_mass (aphid mass per unit plant mass).

## Data Columns (Mapping)
- Year (Run) — Column A
- Ring — Column B
- Pollutant — Column C
- Treatment — Column D
- Plant_ID — Column E
- Run — Column F
- Aphid_population_mass_g — Column G
- Plant_mass_g — Column H
- Aphid_population_mass_mg_per_g_plant_mass — Column I

## Data and Methods Notes
- The dataset uses full FADOE configuration methodology and quality control as described in the referenced study [1].
- The primary reference for the FADOE setup is Ryalls et al. 2022 (Environmental Pollution, 297, 118847). DOI: 10.1016/j.envpol.2022.118847.

## Usage Considerations
- Temporal and spatial variation: data span two years with field relocation; analysis should account for year and field/location effects.
- Data integration: designed to enable cross-treatment comparisons of aphid mass relative to plant mass across pollutant exposures.
- Data quality and provenance: methodology details and quality control are documented in the cited reference.