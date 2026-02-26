# The combined effect of microplastic exposure (biodegradable PBAT and conventional PET) and seawater inundation on the coastal terrestrial plant Plantago coronopus

## Overview
- Dataset of ecotoxicological measurements for Plantago coronopus over 64 days, examining the combined effects of microplastics and seawater inundation.
- Supported by the BIO-PLASTIC-RISK project (NERC grant NE/V007556/1).
- Includes two CSV files: Plantago_data.csv and Plantago_data_necrosis.csv.
- Related publication: Courtene-Jones et al. (2024), Environmental Pollution.

## Experimental design
- Lab-based, factorial design: 3 microplastic treatments × 2 seawater inundation levels.
  - Microplastic treatments: none, conventional plastics (PET), biodegradable plastics (PBAT).
  - Seawater treatments: no inundation, inundation.
- 10 plants per treatment combination (total replicates per cell = 10).
- Plant material and plastics:
  - Plants grown from seed in John Innes seed sowing compost.
  - After 3 months, transferred to compost containing plastics at 0.02 g/kg (<300 µm).
  - PET particles ≤300 µm; PBAT pellets milled to ≤300 µm.
- Inundation protocol:
  - After 35 days, replicates flooded to pot height with artificial seawater (34‰ salinity) for 72 hours, then drained and grown 24 more days.
- Growth conditions: growth chamber at 15°C with 18:6 h light:dark cycle.

## Measurements and datasets
- Ecotoxicological endpoints (Plantago_data.csv):
  - Plastics treatment: no_plastic, conventional_plastics (PET), biodegradable_plastics (PBAT).
  - Inundation treatment: no_inundation, inundation.
  - Survived: mortality status (0 = dead, 1 = alive).
  - Shoots_grams: dry mass of shoots (g).
  - Roots_grams: dry mass of roots (g).
  - Root_to_shoot_ratio: calculated ratio.
  - Scapes: number of flower scapes produced per plant.
- Necrosis over time (Plantago_data_necrosis.csv):
  - plant_id: unique plant identifier.
  - Plastics_treatment: no_plastic, conventional_plastics, biodegradable_plastics.
  - Inundation_treatment: no_inundation, inundation.
  - Duration: weeks during the experiment (W1–W9).
  - Necrosis: percentage of necrotic tissue (visual scoring).

## Data quality, handling, and instrumentation
- Water chemistry:
  - Artificial seawater prepared to 34‰ using Instant Ocean salt; salinity verified with a salinity meter.
  - Prepared 1 day prior to use; stored in a sealed container to prevent plant cold shock.
- Necrosis scoring:
  - Visually scored; the same individual performed scoring for consistency.
- Tissue processing:
  - Above- and below-ground tissues separated; oven-dried at 50°C for 96 hours to constant mass before weighing for root:shoot.
- Lab equipment:
  - Sartorius balance calibrated to four decimal places.

## Data usability and analytical potential
- Suitable for:
  - Analyzing main effects and interaction effects of microplastic type and seawater inundation on plant survival, biomass partitioning, and reproductive output (scapes).
  - Modeling time-resolved necrosis and its relation to mortality and biomass metrics.
  - Comparing toxicity and growth responses across plastic types (none, PET, PBAT) under inundation vs. non-inundation.
- Data provenance:
  - Two structured datasets with explicit variable descriptions (Tables 2 and 3 in the original documentation) to support reproducibility and dataset discovery.
- Practical considerations:
  - Lab-scale, controlled-environment conditions; extrapolation to field contexts should be done with caution.
  - Provides critical metadata to enable combining with other datasets or meta-analyses, including clear treatment codes and measurement units.

## Reference to accompanying publication
- Courtene-Jones et al. (2024), The combined effect of microplastic exposure (biodegradable PBAT and conventional PET) and seawater inundation on the coastal terrestrial plant Plantago coronopus, Environmental Pollution. DOI: https://doi.org/10.1016/j.envpol.2024.124573