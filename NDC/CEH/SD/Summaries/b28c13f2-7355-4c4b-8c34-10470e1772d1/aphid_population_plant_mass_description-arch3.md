# Aphid_population_plant_mass.csv

## Overview
- Dataset from Brassica napus plants in Free-Air Diesel and Ozone Enrichment (FADOE) rings.
- Aims to relate aphid population mass to plant mass under different air pollutant treatments, across two years and multiple experimental runs.

## Experimental Design and Sampling
- Two-year study (2018–2019) with two field locations rotated between years.
- FADOE rings assigned to four pollutant treatments: diesel exhaust (D), ozone (O3), diesel exhaust plus ozone (D+O3), and control (CON; natural air).
- Plants inoculated with aphids at three levels: 50 aphids, 10 aphids, or none (0).
- Replication: 4, 7, and 4 plant replicates for the first, second, and third experimental runs, respectively.
- After eight weeks, aphids were collected with a pooter and weighed; plants were oven-dried and weighed.
- Derived metric: aphid_population_mass_mg_per_g_plant_mass (aphid population mass relative to plant mass).

## Location and Temporal Coverage
- Field location in 2018: latitude 51.482853, longitude -0.897749; moved to a adjacent field in 2019: latitude 51.482374, longitude -0.895855.
- Measurements taken over three experimental runs across two years.

## Data Variables and Structure
- Key variables:
  - Aphid_population_mass_g
  - Plant_mass_g
  - Aphid_population_mass_mg_per_g_plant_mass
  - Identifier columns: Year, Ring, Pollutant, Treatment, Plant_ID, Run
- Data are linked to each FADOE ring and pollutant treatment, with aphid inoculation level as part of the treatment design.

## Methods and Data Provenance
- Aphids collected using a pooter; plant masses determined by oven drying.
- Full details of the FADOE configuration and quality control are described in the referenced methodology document.
- Methodology reference: Ryalls et al. 2022 (Anthropogenic air pollutants reduce insect-mediated pollination services).

## Relevance for Monitoring Frameworks
- Provides a multi-year, replicated dataset linking biotic (aphid populations) and plant responses under environmental stressors (pollutants).
- Supports assessment of environmental health measures related to insect-plant interactions under pollutant exposure.
- Demonstrates integration of field experiments, treatment randomization, replication, and derived metrics for policy-relevant monitoring.

## Data Governance, Metadata, and Accessibility Considerations
- Metadata quality is implied by the need to describe the FADOE configuration; explicit metadata gaps may exist and require explicit provenance notes.
- Sharing underlying data and derived metrics is important for transparency and reproducibility, aligned with data governance best practices.
- Potential barriers noted in monitoring frameworks include data accessibility, metadata completeness, and the need to transform data formats for use.

## Reference
- Ryalls, J.M.W., Langford, B., Mullinger, N.J., Bromfield, L.M., Nemitz, E., Pfrang, C. & Girling, R.D. 2022. Anthropogenic air pollutants reduce insect-mediated pollination services. Environmental Pollution 297, 118847.