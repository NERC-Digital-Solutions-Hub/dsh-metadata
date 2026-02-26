# The combined effect of microplastic exposure (biodegradable PBAT and conventional PET) and seawater inundation on the coastal terrestrial plant Plantago coronopus

## Overview
- Lab-based ecotoxicological dataset examining mortality, growth, reproduction, necrosis, and photosynthetic-related metrics of Plantago coronopus under microplastic exposure and seawater inundation.
- 3 x 2 factorial design: microplastic exposure (no_plastic, conventional_plastics PET, biodegradable_plastics PBAT) and seawater inundation (no_inundation, inundation).
- 10 plants per treatment; total duration of 64 days.
- Supported by NERC BIO-PLASTIC-RISK project (grant NE/V007556/1).
- Dataset comprises two CSV files: Plantago_data.csv and Plantago_data_necrosis.csv, with accompanying publication: Courtene-Jones et al. (2024), Environmental Pollution.

## Data files and contents
- Plantago_data.csv
  - plastics_treatment: type of plastic exposure (no_plastic, conventional_plastics, biodegradable_plastics)
  - inundation_treatment: seawater treatment (no_inundation, inundation)
  - Survived: mortality (0 = dead, 1 = alive)
  - shoots_grams: dry mass of shoots (g)
  - roots_grams: dry mass of roots (g)
  - root_to_shoot_ratio: calculated dry root:shoot ratio
  - scapes: number of flower scapes produced per plant
- Plantago_data_necrosis.csv
  - plant_id: unique plant-treatment identifier
  - plastics_treatment: as above
  - inundation_treatment: as above
  - Duration: duration in weeks (W1–W9)
  - necrosis: percentage of necrotic tissue (visually scored)

## Experimental design and methods
- 64-day study with two key phases:
  - Initial 35 days: plants grown with specified plastic treatments in contaminated compost with <300 μm plastics.
  - Following 72-hour seawater inundation (34‰ salinity) at pot height, then 24 more days of growth.
- Growth conditions: 15°C, 18:6 h light:dark cycle.
- Plastic materials: conventional PET powder (≤300 μm) and PBAT pellets (≤300 μm), plus a no_plastic control.
- Replication: 10 plants per treatment combination.
- Measurements:
  - Mortality (visual) and necrosis (visual) tracked over time.
  - Final biomass metrics: root and shoot masses, root:shoot ratio.
  - Reproductive output: number of flower scapes.
  - Necrosis data captured as weekly percentages (necrosis.csv).

## Quality control and data integrity
- Seawater: Instant Ocean® marine salt, prepared to 34‰; salinity checked and equilibrated prior to use.
- Consistency in necrosis scoring: the same observer performed all necrosis assessments.
- Tissue processing: above- and below-ground tissues dried at 50°C for 96 hours to constant mass before weighing.
- Cross-contamination prevention: plants immersed in seawater only within their designated plastic treatment groups.
- Instrumentation: Sartorius balance calibrated with standard weights (four decimal places).

## Data governance, provenance, and access
- Data are linked to a peer‑reviewed publication and include explicit methodological detail to support reproducibility.
- DOI and link to the Environmental Pollution article provided for citation and data provenance.
- Data formats: CSV files; clear variable naming and unit conventions in the accompanying variable dictionaries (Tables 2 and 3 in the dataset documentation).
- Licensing and reuse rights not specified in the provided text; users should verify data licensing and citation requirements via the associated publication and repository.

## Reuse considerations for data stewards
- Discoverability: dataset is accompanied by a formal publication and includes descriptive metadata (treatment types, duration, measured outcomes).
- Interoperability: clearly defined categorical treatments and standardized measurement units, enabling integration with other ecotoxicology datasets.
- Documentation quality: includes data dictionaries (variable descriptions), experimental design details, and quality-control notes; consider exporting into a machine-readable metadata schema (e.g., DataCite, Dublin Core) for broader cataloging.
- Limitations to note:
  - Laboratory conditions may limit ecological extrapolation; study uses a single plant species.
  - Sample size is modest (n=10 per treatment), which may affect statistical power.
  - Licensing details are not stated and should be clarified for future reuse.
- Suggested governance actions:
  - Attach a machine-readable metadata record and a clear data usage license.
  - Maintain versioning and provide citation guidance aligned with the associated publication.
  - Include any updates or corrections from the data providers to support ongoing discovery and reuse.