# The combined effect of microplastic exposure (biodegradable PBAT and conventional PET) and seawater inundation on the coastal terrestrial plant Plantago coronopus

## Overview
- Dataset from a lab-based ecotoxicology study on Plantago coronopus over 64 days.
- Investigates the combined effects of microplastic exposure (three levels: no plastic, conventional PET, biodegradable PBAT) and seawater inundation (with/without) in a 3 × 2 factorial design.
- 10 plants per treatment, totaling 6 treatment groups.
- Measured outcomes include mortality, biomass partitioning (root and shoot masses), root:shoot ratio, and number of flower scapes; time-resolved data on necrosis is available.

## Data files included
- Plantago_data.csv
  - Variables:
    - plastics_treatment: no_plastic, conventional_plastics, biodegradable_plastics
    - inundation_treatment: no_inundation, inundation
    - Survived: mortality (0 = dead, 1 = alive)
    - shoots_grams: dry mass of shoots (g)
    - roots_grams: dry mass of roots (g)
    - root_to_shoot_ratio: calculated ratio
    - scapes: number of flower scapes produced
- Plantago_data_necrosis.csv
  - Variables:
    - plant_id: unique plant-treatment identifier
    - plastics_treatment: as above
    - inundation_treatment: as above
    - Duration: duration in weeks (W1–W9)
    - necrosis: percentage of necrotic tissue (visual score)

## Experimental design and methods
- Factorial design: 3 microplastic treatments × 2 inundation treatments.
- Treatments: no_plastic, conventional_plastics (PET), biodegradable_plastics (PBAT); no_inundation, inundation.
- Sample size: 10 plants per treatment (n = 60 total plants).
- Growth conditions: plants grown from seed in John Innes Seed Sowing Compost; after 3 months transferred to plastic-contaminated compost with specified microplastics concentrations (0.02 g/kg, <300 μm). 
- Inundation step: after 35 days, selected replicates flooded to pot height with artificial seawater for 72 hours (34‰ salinity), then drained and grown for 24 more days.
- Environmental conditions: growth chamber at 15°C with 18:6 h light:dark cycle.

## Measurements and data collection
- Ecotoxicological measures:
  - Mortality (visual) recorded throughout the experiment.
  - Necrosis (visual scoring) recorded over time (necrosis.csv).
  - Biomass: dry mass of shoots and roots measured at termination.
  - Biomass allocation: root:shoot ratio calculated from dry masses.
  - Reproductive output: number of flower scapes produced per plant.
- Necrosis data: weekly percentages from W1 to W9, enabling time-resolved analysis.

## Quality control and data integrity
- Seawater prepared at 34‰ using Instant Ocean salt; salinity checked with a meter; prepared one day prior and stored sealed to maintain conditions.
- Necrosis scored by the same assessor to ensure consistency.
- Tissue separation and drying: roots and shoots dried separately at 50°C for 96 hours to constant mass for accurate biomass and root:shoot calculations.
- Cross-contamination minimized by immersing plants to pot height within treatment groups.
- Equipment: calibrated Sartorius balance (4 decimal places) used for mass measurements.

## Data usage and context
- Data accompany the research output: Courtene-Jones et al. (2024), The combined effect of microplastic exposure (biodegradable PBAT and conventional PET) and seawater inundation on the coastal terrestrial plant Plantago coronopus, Environmental Pollution, 124573. DOI: https://doi.org/10.1016/j.envpol.2024.124573
- Suitable for analyses of interaction effects between microplastic type and seawater inundation on plant survival, growth, and necrosis, as well as for time-series assessments of necrotic tissue development.

## Relevance for data use and potential analyses
- Allows examination of:
  - How microplastic type (none, PET, PBAT) interacts with seawater inundation to affect mortality and biomass allocation.
  - Whether biodegradable PBAT differs from conventional PET in ecotoxicological impact under inundation.
  - Temporal pattern of necrosis and its relation to treatment conditions.
- Clear variable definitions and units support reproducibility and integration with other datasets or dashboards.