# Aphid_population_plant_mass.csv

## Overview
- Dataset of plant and aphid population masses collected from Brassica napus plants within Free-Air Diesel and Ozone Enrichment (FADOE) rings.
- Spans two years with three experimental runs (Year, Run).
- Includes measurements of aphid mass, plant mass, and a derived ratio of aphid mass to plant mass.

## Experimental Design and Sampling
- Field locations:
  - 2018: Field of wheat at latitude 51.482853, longitude -0.897749.
  - 2019: Adjacent field at latitude 51.482374, longitude -0.895855.
- Ring-level setup: Each FADOE ring assigned a Ring number.
- Pollutant treatments (four levels): diesel exhaust (D), ozone (O3), diesel exhaust + ozone (D+O3), and control (CON; natural air).
- Aphid inoculation treatments (three levels): 50 aphids, 10 aphids, or 0 aphids per plant.
- Replication across runs:
  - Run 1: 4 Plant_IDs per treatment
  - Run 2: 7 Plant_IDs per treatment
  - Run 3: 4 Plant_IDs per treatment
- Sampling protocol:
  - Plants inoculated at five weeks old.
  - After eight weeks, aphids collected with a pooter and weighed.
  - Plants oven-dried and weighed.
  - Aphid population mass relative to plant mass calculated as Aphid_population_mass_mg_per_g_plant_mass.

## Data Variables and Derived Metrics
- Columns include:
  - Description: textual description field.
  - Year: experimental year.
  - Ring: ring identifier (B).
  - Pollutant: pollutant treatment (D, O3, D+O3, CON).
  - Treatment: aphid inoculation level (50, 10, or 0 aphids).
  - Plant_ID: plant identifier (E).
  - Run: experimental run (F).
  - Aphid_population_mass_g: aphid mass in grams (G).
  - Plant_mass_g: plant mass in grams (H).
  - Aphid_population_mass_mg_per_g_plant_mass: derived ratio (mg per g) (I).

## Spatial and Temporal Context
- Temporal: two-year study with three successive runs.
- Spatial: field locations recorded for each year; field moved from one location in 2018 to an adjacent field in 2019. Coordinates provided for both sites, enabling potential GIS mapping at the field level and linking to Ring, Pollutant, and Treatment factors.

## Reference and Methodology
- Methodology and FADOE configuration detailed in:
  - Ryalls, J.M.W., Langford, B., Mullinger, N.J., Bromfield, L.M., Nemitz, E., Pfrang, C. & Girling, R.D. 2022. Anthropogenic air pollutants reduce insect-mediated pollination services. Environmental Pollution 297, 118847. (doi:10.1016/j.envpol.2022.118847)

## GIS and Visualization Considerations
- Suitable for map-based visualizations by:
  - Pollutant and Treatment categories across Year and Run.
  - Derived aphid-to-plant mass ratio as a continuous variable for spatial comparisons.
  - Ring-level grouping to illustrate intra-field variability (requires ring-to-location mapping if available).
- Potential GIS tasks:
  - Create layers showing Aphid_population_mass_g, Plant_mass_g, and Aphid_population_mass_mg_per_g_plant_mass by treatment and year.
  - Analyze spatial patterns of aphid pressure relative to pollutant exposure.
  - Integrate with field boundaries and any additional spatial attributes for policy or public-facing visuals.