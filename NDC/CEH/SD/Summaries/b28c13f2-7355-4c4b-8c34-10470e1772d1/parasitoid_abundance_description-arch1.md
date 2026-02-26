# Description, Experimental Design and Collection

- This dataset captures the abundance of parasitic wasps (parasitoids) on sticky traps placed among Brassica napus plants within Free-Air Diesel and Ozone Enrichment (FADOE) rings.
- Focus is on two parasitoid groups: Diaeretiella rapae and other parasitoids, collected across two years under various pollution and aphid-treatment conditions.

## Overview

- Sampling occurred over two years (Year) in FADOE rings assigned to pollution treatments and aphid-infestation levels.
- Primary aim is to quantify how environmental pollutants and aphid management influence parasitoid communities on Brassica napus.

## Experimental Design

- Location:
  - 2018: field of wheat at latitude 51.482853, longitude -0.897749.
  - 2019: adjacent field at latitude 51.482374, longitude -0.895855 (rings moved).
- Experimental units:
  - FADOE rings; each ring allocated to one of four pollutant treatments:
    - D: diesel exhaust
    - O3: ozone
    - D+O3: diesel exhaust plus ozone
    - CON: control (natural air)
- Aphid treatment (applied when plants were five weeks old):
  - 50 aphids
  - 10 aphids
  - 0 aphids (no infestation)
- Replication and timing:
  - One sticky trap placed on a stick within groups of Brassica napus plants.
  - Each run comprised a different arrangement of plants: four, seven, and four replicate plants for runs 1, 2, and 3, respectively.
  - The experiment was repeated three times (three runs) over the two years.
- Trap collection:
  - Traps collected at seven weeks, then again after a week (week eight).
  - Traps stored at -20 °C prior to processing.

## Data Collected and Measurements

- Parasitoids counted from sticky traps and identified under a microscope.
- Two outcome categories:
  - D_rapae_counts: number of Diaeretiella rapae parasitoids per trap.
  - Others_counts: number of other parasitoids per trap.
- Pooling:
  - Abundances from traps collected at week seven and week eight were pooled for each: Treatment, Ring, and Year.
- Proportion calculated:
  - Percentage_D_rapae: percentage of total counted parasitoids that were D. rapae.
- Data columns (as described in the dataset):
  - Year
  - Ring (ring identifier)
  - Pollutant (D, O3, D+O3, CON)
  - Treatment (aphid infestation level: 50, 10, or 0 aphids)
  - Run (experimental run 1, 2, or 3)
  - D_rapae_counts
  - Others_counts
  - Percentage_D_rapae
- Additional context:
  - Full methodological details and quality control are described in the referenced configuration methodology.

## Variables and Dataset Structure

- Key variables:
  - Year: experimental year (2018 or 2019)
  - Ring: numeric ring identifier
  - Pollutant: categorical treatment (D, O3, D+O3, CON)
  - Treatment: aphid infestation level (50, 10, 0)
  - Run: experimental run number (1, 2, or 3)
  - D_rapae_counts: count of Diaeretiella rapae
  - Others_counts: count of other parasitoids
  - Percentage_D_rapae: proportion of D. rapae among parasitoids
- Spatial/temporal context:
  - Field location changed between years; two distinct sites are represented by the Year and associated coordinates.

## Data Processing and Pooling

- Abundances are pooled across weeks 7 and 8 within each Treatment, Ring, and Year.
- The dataset presents aggregated counts and calculated percentages to enable comparison across pollutants, aphid treatments, and runs.

## Quality Control and Reference

- Parasitoids were identified under a microscope following quality control procedures described in the FADOE methodology.
- Reference methodology for the FADOE configuration:
  - Ryalls, J.M.W., Langford, B., Mullinger, N.J., Bromfield, L.M., Nemitz, E., Pfrang, C. & Girling, R.D. 2022. Anthropogenic air pollutants reduce insect-mediated pollination services. Environmental Pollution 297, 118847. (doi:10.1016/j.envpol.2022.118847)

## Potential Uses and Considerations for Analysis

- Suitable analyses:
  - Examine correlations between pollutant exposure and D. rapae abundance or proportion.
  - Assess effects of aphid infestation level on parasitoid community composition.
  - Model counts using Poisson or negative binomial frameworks, with Year, Ring, Pollutant, Treatment, and Run as factors.
  - Explore interactions between pollutant type and aphid treatment across rings and years.
- Considerations:
  - Two-field change and year-to-year differences may introduce spatial and temporal confounding.
  - Pooling across weeks 7 and 8 provides aggregate counts; temporal dynamics within weeks are not captured.
  - Data scale and accessibility limitations noted in typical data-analytic contexts, including cross-dataset harmonization and metadata richness. 

## Reference

- Ryalls, J.M.W., Langford, B., Mullinger, N.J., Bromfield, L.M., Nemitz, E., Pfrang, C. & Girling, R.D. 2022. Anthropogenic air pollutants reduce insect-mediated pollination services. Environmental Pollution 297, 118847. (doi:10.1016/j.envpol.2022.118847).