# The combined effect of microplastic exposure (biodegradable PBAT and conventional PET) and seawater inundation on the coastal terrestrial plant Plantago coronopus

- Overview
  - Laboratory ecotoxicology dataset assessing how microplastics (PBAT and PET) and seawater inundation jointly affect Plantago coronopus over 64 days.
  - Supported by the BIO-PLASTIC-RISK project; data accompany a peer-reviewed article in Environmental Pollution (2024).

- Experimental design
  - 3 x 2 factorial design: microplastic exposure (none, conventional PET, biodegradable PBAT) × seawater inundation (no inundation, inundation).
  - 10 plants per treatment group.
  - Plants grown in compost, contaminated with specified plastics, then subjected to a seawater inundation step.
  - Inundation protocol: 35 days of plastic exposure, followed by 72 hours of inundation with artificial seawater (34‰), then 24 more days of growth.
  - Growth conditions: controlled growth chamber at 15°C with 18:6 h light:dark cycle.

- Measured/ecotoxicological endpoints
  - Mortality (survival status; 0 = dead, 1 = alive) recorded throughout.
  - Necrosis (visual percentage necrotic tissue) measured weekly (Plantago_data_necrosis.csv).
  - Biomass metrics at termination: root mass, shoot mass, root-to-shoot ratio (root_to_shoot_ratio).
  - Reproductive output: number of flower scapes produced per plant.

- Data files and variables
  - Plantago_data.csv
    - plastics_treatment: no_plastic, conventional_plastics (PET), biodegradable_plastics (PBAT)
    - inundation_treatment: no_inundation, inundation
    - Survived: mortality status (0 = dead, 1 = alive)
    - shoots_grams: dry mass of shoots (g)
    - roots_grams: dry mass of roots (g)
    - root_to_shoot_ratio: calculated dry root-to-shoot ratio
    - scapes: number of flower scapes produced per plant
  - Plantago_data_necrosis.csv
    - plant_id: unique plant-treatment identifier
    - plastics_treatment: as above
    - inundation_treatment: as above
    - Duration: duration in weeks (W1–W9)
    - necrosis: percentage of necrotic tissue over time (weekly scores)

- Quality control, instrumentation, and data handling
  - Seawater simulation: Instant Ocean® marine salt, prepared to 34‰, verified with salinity meter; prepared one day prior; stored in growth chamber to prevent cold shock.
  - Necrosis scoring: performed by a single researcher to ensure consistency.
  - Tissue processing: above- and below-ground tissues separated, oven-dried at 50°C for 96 hours, then weighed to compute root:shoot ratio.
  - Cross-contamination prevention: plants immersed to pot height in treatment-specific groups; no cross-contact between plastics treatments.
  - Lab instrumentation: Sartorius balance with four decimal places; calibrated with standard weights.

- Data accessibility and citation
  - Datasets accompany the article: Courtene-Jones et al. 2024, The combined effect of microplastic exposure (biodegradable PBAT and conventional PET) and seawater inundation on the coastal terrestrial plant Plantago coronopus, Environmental Pollution, 124573. DOI: https://doi.org/10.1016/j.envpol.2024.124573

- Relevance for monitoring frameworks
  - Provides a structured, multi-stressor dataset linking specific plastic types and environmental inundation to ecotoxicological outcomes in a coastal plant.
  - Demonstrates a clear schema for documenting experimental design, endpoints, and metadata (variable descriptions, units, and treatment identifiers) suitable for environmental health monitoring datasets.
  - Highlights practical data governance considerations (metadata clarity, data sharing, and provenance) that monitoring frameworks must address to enable data integration, replication, and policy-relevant analyses.