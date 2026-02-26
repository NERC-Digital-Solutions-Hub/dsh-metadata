# Aphid_population_plant_mass.csv

## Overview
- Dataset from Brassica napus plants in Free-Air Diesel and Ozone Enrichment (FADOE) rings.
- Two-year study collecting plant and aphid masses; includes a computed aphid-to-plant mass ratio.
- Aims to support data governance through documented experimental design, metadata, and measurement details.

## Experimental Design and Data Collection
- FADOE rings located in a field of wheat; coordinates provided for 2018 and 2019, with rings moved to an adjacent field in 2019.
- Pollution treatments (Pollutant): diesel exhaust (D), ozone (O3), diesel exhaust + ozone (D+O3), and control (CON; natural air); four rings per treatment.
- Aphid inoculation treatments (Treatment): 50 aphids, 10 aphids, or 0 aphids per plant.
- Replication: 4 plants in Run 1, 7 plants in Run 2, and 4 plants in Run 3 (three experimental runs over two years).
- Measurements after eight weeks:
  - Aphid_population_mass_g: aphid mass collected from plants (grams).
  - Plant_mass_g: oven-dried plant mass (grams).
  - Aphid_population_mass_mg_per_g_plant_mass: aphid mass relative to plant mass (mg per g plant mass).
- Full details of the FADOE configuration and quality control are described in the referenced methodology document.

## Data Columns / Variables
- Year: year of sampling (2018 or 2019).
- Ring: FADOE ring identifier.
- Pollutant: pollution treatment (D, O3, D+O3, CON).
- Treatment: aphid inoculation level (50, 10, or 0).
- Plant_ID: plant replicate identifier.
- Run: experimental run (1, 2, or 3).
- Aphid_population_mass_g: aphid mass in grams.
- Plant_mass_g: plant mass in grams.
- Aphid_population_mass_mg_per_g_plant_mass: computed metric (mg aphid per g plant mass).

## Temporal and Spatial Coverage
- Timeframe: across two years (2018 and 2019).
- Location: field-based study with rings in 2018 at specified coordinates, moved to adjacent field in 2019; precise latitude/ longitude provided for each year.

## Data Quality, Provenance, and Access
- Methodology and quality control are described in the cited reference (Ryalls et al. 2022).
- Data provenance includes explicit experimental design details (ring assignments, treatments, replication, run structure) and measurement procedures (pooter collection, weighing, oven drying).
- Potential governance considerations: ensure consistency of units across years, maintain linkage between Year, Ring, Pollutant, Treatment, and Run, and preserve the computed Aphid_population_mass_mg_per_g_plant_mass value for reuse.

## Reuse and Governance Considerations
- Use for assessing effects of air pollutants and aphid-plant interactions; consider experimental factors (Pollutant, Treatment) and their interactions.
- Ensure proper attribution to methodology source for full experimental context and quality controls.
- Consider supplementing with metadata on data collection times, measurement instruments, and any field condition notes to improve interoperability and reuse.
- Data may be impacted by field relocation between years; account for potential spatial confounding when analyzing year effects.