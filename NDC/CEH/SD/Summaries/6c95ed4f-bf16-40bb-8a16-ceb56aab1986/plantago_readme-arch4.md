# The combined effect of microplastic exposure (biodegradable PBAT and conventional PET) and seawater inundation on the coastal terrestrial plant Plantago coronopus

## Overview
- 64-day, lab-based ecotoxicological study on Plantago coronopus exposed to microplastics and seawater inundation.
- Factorial design: microplastics (none, conventional PET, biodegradable PBAT) × seawater inundation (present, absent).
- 10 plants per treatment; growth in John Innes compost; plastics ≤300 μm; artificial seawater exposure following 35 days of growth.
- Measurements include mortality, growth (root and shoot mass), root:shoot ratio, and flower scapes; time-course necrosis data collected for each plant.

## Datasets Included
- Plantago_data.csv
  - Variables: plastics_treatment, inundation_treatment, Survived (0 dead, 1 alive), shoots_grams, roots_grams, root_to_shoot_ratio, scapes (number of flower scapes).
- Plantago_data_necrosis.csv
  - Variables: plant_id, plastics_treatment, inundation_treatment, Duration (weeks W1–W9), necrosis (percentage necrotic tissue).

## Experimental Design and Procedures
- Design: 3 (microplastics) × 2 (seawater inundation) factorial.
  - Microplastics: no_plastic, conventional_plastics (PET), biodegradable_plastics (PBAT).
  - Inundation: no_inundation, inundation.
- Setup: 10 plants per treatment group; plants grown from seed and acclimated in John Innes Seed Sowing Compost, then transferred to plastic-contaminated compost.
- Plastic materials: PET (conventional) and PBAT (biodegradable) milled to ≤300 μm.
- Inundation event: after 35 days, plants flooded with artificial seawater (34‰) for 72 hours, then drained and grown for an additional 24 days.
- Environment: growth chamber at 15°C with 18:6 h light:dark cycle.

## Measured Variables and Data Files
- Plantago_data.csv
  - plastcs_treatment: no_plastic, conventional_plastics, biodegradable_plastics
  - inundation_treatment: no_inundation, inundation
  - Survived: 0 = dead, 1 = alive
  - shoots_grams: dry mass of shoots (g)
  - roots_grams: dry mass of roots (g)
  - root_to_shoot_ratio: calculated ratio
  - scapes: number of flower scapes produced
- Plantago_data_necrosis.csv
  - plant_id: unique plant-treatment identifier
  - plastics_treatment: as above
  - inundation_treatment: as above
  - Duration: weeks (W1–W9)
  - necrosis: percentage of necrotic tissue (visual scoring)

## Quality Control, Instrumentation, and Data Integrity
- Seawater: Instant Ocean salt, prepared to 34‰, salinity checked, stored to equilibrate temperature.
- Necrosis scoring: performed by the same observer for consistency.
- Tissue processing: above- and below-ground tissues separated, oven-dried at 50°C for 96 hours, dry masses recorded.
- Cross-contamination prevention: treatments kept distinct to avoid contamination between plastics and inundation groups.
- Instrumentation: Sartorius balance (four decimal places) for precise mass measurements.

## Data Provenance and Citation
- Associated with Courtene-Jones et al. (2024), The combined effect of microplastic exposure (biodegradable PBAT and conventional PET) and seawater inundation on the coastal terrestrial plant Plantago coronopus, Environmental Pollution, 124573. DOI: https://doi.org/10.1016/j.envpol.2024.124573

## Data Stewardship Considerations for Data Leaders
- Structure and metadata clarity: clear coding for treatment groups and consistent variable naming facilitate discoverability and reuse.
- Multiple data files with complementary time-series data (necrosis) support longitudinal analyses.
- Documentation of experimental design and QA steps aids reproducibility and integration with broader datasets.
- Potential gaps: explicit data on photosynthetic efficiency mentioned in background but not enumerated in data files; consider harmonizing metadata to capture all measured endpoints.