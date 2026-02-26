# The combined effect of microplastic exposure (biodegradable PBAT and conventional PET) and seawater inundation on the coastal terrestrial plant Plantago coronopus

## Overview
- Lab-based ecotoxicological dataset on Plantago coronopus, measuring mortality, growth, reproductive output, necrosis, and photosynthetic efficiency under microplastics and seawater inundation over 64 days.
- Supported by the BIO-PLASTIC-RISK project; grant NE/V007556/1.
- Comprises two CSV files: Plantago_data.csv and Plantago_data_necrosis.csv.

## Experimental design
- Factorial design: 3 levels of microplastic exposure (none, conventional PET, biodegradable PBAT) × 2 levels of seawater inundation (no inundation, inundation).
- 10 plants per treatment, yielding 60 plants total (6 treatment groups).
- Growth conditions: seeds grown in John Innes Seed Sowing Compost, later moved to plastic-contaminated compost with ≤300 μm plastics; PET or PBAT plastics used as relevant treatments.
- After 35 days, plants flooded to pot height with artificial seawater (72 hours at 34‰), then grown for 24 more days in a controlled growth chamber at 15°C with 18:6 light:dark cycle.

## Datasets and key variables
- Plantago_data.csv
  - plast_treatment: plastic exposure type (no_plastic, conventional_plastics, biodegradable_plastics)
  - inundation_treatment: seawater treatment (no_inundation, inundation)
  - Survived: plant mortality (0 = dead, 1 = alive)
  - shoots_grams: dry mass of shoots (g)
  - roots_grams: dry mass of roots (g)
  - root_to_shoot_ratio: dry root-to-shoot ratio
  - scapes: number of flower scapes produced per plant

- Plantago_data_necrosis.csv
  - plant_id: unique plant-treatment identifier
  - plastics_treatment: plastic exposure type
  - inundation_treatment: seawater treatment
  - duration: duration in weeks (W1–W9)
  - necrosis: percentage of necrotic tissue (scored visually)

- Data tables referenced as Table 2 and Table 3 in the accompanying documentation describe variable names and meanings.

## Data collection and quality control
- Seawater prepared to 34‰ (Instant Ocean®), checked with a salinity meter; stored in a sealed container at growth chamber temperature to prevent plant cold shock.
- Necrosis scored visually by a single consistent observer.
- Tissues separated into envelopes, oven-dried at 50°C for 96 hours to a constant mass for root/shoot measurements.
- Plants immersed in seawater to pot height within their specific treatment groups to prevent cross-contamination.
- Instrumentation: Sartorius balance (4 decimal places) calibrated with standard weights.

## Data usage and GIS relevance
- Although not geographic, data are suitable for map-based visualization by aggregating plant-level results to treatment categories (e.g., survival rates, biomass, necrosis progression) across microplastic types and inundation conditions.
- Potential GIS-style outputs include:
  - categorical maps or dashboards showing treatment groups and associated outcomes
  - time-enabled visuals for necrosis progression (weeks) aligned with treatment axes
  - spatially explicit summaries if experimental staging locations or replicate positions are later georeferenced

## Reference
- Courtene-Jones et al (2024), The combined effect of microplastic exposure (biodegradable PBAT and conventional PET) and seawater inundation on the coastal terrestrial plant Plantago coronopus, Environmental Pollution, 124573. https://doi.org/10.1016/j.envpol.2024.124573