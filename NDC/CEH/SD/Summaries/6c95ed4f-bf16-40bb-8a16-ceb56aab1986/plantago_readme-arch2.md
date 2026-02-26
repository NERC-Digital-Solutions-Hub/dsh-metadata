# The combined effect of microplastic exposure (biodegradable PBAT and conventional PET) and seawater inundation on the coastal terrestrial plant Plantago coronopus

- Overview
  - Ecotoxicological dataset on Plantago coronopus over 64 days
  - Investigates mortality, growth (root and shoot mass), necrosis, and reproductive output under microplastic exposure and seawater inundation
  - Supported by NERC BIO-PLASTIC-RISK project
  - Data accompany a published study: Courtene-Jones et al. 2024, Environmental Pollution

- Experimental design
  - Lab-based, 3 x 2 factorial design
    - Microplastic exposure: none (NP), conventional PET, biodegradable PBAT
    - Seawater inundation: no inundation (NI), inundation (I)
  - 10 plants per treatment
  - Plant preparation: seeds grown to mature plants, then transferred to plastic-contaminated compost with 0.02 g/kg plastic (<300 μm)
  - Plastic types and sizes: PET powder and PBAT pellets milled to ≤300 μm
  - Flooding: after 35 days, 72-hour inundation with artificial seawater (34‰), then 24 more days
  - Conditions: growth chamber at 15°C, 18:6 h light:dark

- Data files and structure
  - Plantago_data.csv
  - Plantago_data_necrosis.csv

- Variables in Plantago_data.csv
  - plastics_treatment: type of plastic exposure (no_plastic, conventional_plastics PET, biodegradable_plastics PBAT)
  - inundation_treatment: seawater exposure (no_inundation, inundation)
  - Survived: plant mortality (0 = dead, 1 = alive)
  - shoots_grams: dry shoot mass (g)
  - roots_grams: dry root mass (g)
  - root_to_shoot_ratio: calculated dry root to shoot ratio
  - scapes: number of flower scapes produced per plant at the end

- Variables in Plantago_data_necrosis.csv
  - plant_id: unique plant-treatment identifier
  - plastics_treatment: type of plastic exposure
  - inundation_treatment: seawater exposure
  - Duration: duration in weeks (W1–W9)
  - necrosis: percentage of necrotic tissue (visual score)

- Quality control and methods
  - Seawater: Instant Ocean salt, prepared to 34‰, salinity checked with salinity meter
  - Necrosis scoring: performed by the same individual for consistency
  - Tissue processing: roots and shoots separated, oven-dried at 50°C for 96 hours to constant mass
  - Cross-contamination prevention: plants immersed to pot height in treatment-specific groups
  - Instrumentation: Sartorius balance (four decimal places), calibrated with standard weights

- Data use and interpretation for environmental monitoring
  - Standardized ecotoxicological endpoints (mortality, necrosis, biomass allocation, and reproductive output) under multiple stressors
  - Enables assessment of combined impacts of microplastics and seawater inundation on coastal vegetation
  - Datasets designed for storage and sharing in monitoring portals, with clear metadata and variable definitions

- Provenance and reference
  - Data accompany Courtene-Jones et al. (2024), The combined effect of microplastic exposure (biodegradable PBAT and conventional PET) and seawater inundation on the coastal terrestrial plant Plantago coronopus, Environmental Pollution, DOI: https://doi.org/10.1016/j.envpol.2024.124573

- Relevance to environmental monitoring challenges
  - Aligns with aims to verify data quality, use standardized methods, and present outputs in clear formats
  - Demonstrates (and can be integrated with) broader environmental health datasets by combining multiple stressor data and enabling access to underlying measurements
  - Provides a concrete example of a controlled, repeatable dataset suitable for trend analysis and cross-study comparability in ecosystem risk assessments