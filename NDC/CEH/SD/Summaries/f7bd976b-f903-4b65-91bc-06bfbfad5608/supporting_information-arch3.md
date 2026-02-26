# Life history data from insects in a host-parasitoid interaction under a range of humidity and heat stress conditions

## Overview
- A lab-based, single-generation life-history dataset exploring how humidity and heat stress influence host (Plodia interpunctella) and parasitoid (Venturia canescens) interactions.
- Measures life-history traits for both unparasitized hosts and parasitized hosts under high (60.8% RH) and low (32.5% RH) humidity, with heat stress exposure at the 4th or 5th instar for 0, 6, or 72 hours.
- Missing data are marked as NA due to sample loss or mortality.

## Study design and collection methods
- Full-factorial design: parasitism (parasitized vs unparasitized) × humidity (high vs low) × larval stage (4th vs 5th instar) × duration of heat stress (0, 6, 72 hours).
- Each treatment combination comprises 2025 observations.
- Host eggs reared individually in 25-well plates at 28°C; humidity manipulated using saturated NaCl for high humidity.
- Parasitized hosts created by exposing early 4th instar larvae to a newly emerged adult parasitoid.
- Heat stress applied by transferring plates to 38°C incubators with corresponding humidity levels.
- Daily monitoring until adult emergence; body size measured via mid-femur and hind tibia lengths using microscopy and imaging software.
- Data recorded in two csv files (host.csv and parasitoid.csv) with detailed event dates and life-history outcomes.

## Data structure and key variables

- host.csv (life-history traits for unparasitized larvae)
  - Plate_id, Id, Humidity, Parasitism, Duration, Stage
  - Eggtransfer_date, Survivived2L4, Pupate, Hostpupate_date
  - Host emergence, Hostemerge_date, Hostdead_date
  - Host_sex, Midfemur, Rearfemur
  - Additional fields track timing and survival milestones (e.g., Pupate_date, Hostemerge_date)

- parasitoid.csv (life-history traits for parasitized larvae)
  - Plate_id, Id, Humidity, Interaction (H-P), Duration, Stage
  - Eggtransfer_date, Survivived2L4, Parasited_date, Parasitism
  - Pupate, Hostpupate_date, Hostemerge/Wasp_emerge, Emerge_date
  - Dead_date, Wasp_size, Midfemur, Rearfemur, Host_sex.if.applicable

- Units and timing
  - Dates are recorded as YYYYMMDD; durations in hours; body measurements in millimeters.

## Measurements and units
- Life-history endpoints for hosts and parasitoids:
  - Survival to key stages (e.g., Survivived2L4, Hostemerge, Wasp_emerge)
  - Development milestones (Pupate, Hostpupate_date, Emerge_date)
  - Size metrics (Midfemur, Rearfemur; Wasp_size for parasitoids)
  - Sex information when applicable
- Temporal data captured via specific event dates; all measurements in mm or date format as noted.

## Quality control and data management
- Conducted as a controlled, model-organism lab system with long-standing use in the research group.
- Each treatment combination has a large, explicit replication (2025 observations).
- Data integrity checked during measurement; NA values used for non-occurring events (e.g., mortality before a stage).
- Clear documentation of data structure and variable definitions within the two CSV files.

## Strengths and limitations for policy monitoring
- Strengths:
  - Rich, stage- and condition-specific life-history data under controlled, repeatable conditions.
  - Clear factorial design enabling isolation of humidity, heat stress, parasitism, and developmental stage effects.
  - Comprehensive variable definitions and standardized measurements facilitate comparability and potential aggregation in monitoring frameworks.
- Limitations:
  - Lab-based, single-generation study; may not capture multi-generational or field-condition variability.
  - Data reflect controlled environments and may require cautious extrapolation to real-world ecological monitoring.
  - Absence of an explicit external metadata file beyond in-file variable descriptions; may require parsing to align with broader data governance standards.

## Implications for environmental health monitoring
- Enables assessment of how humidity and heat stress interact to alter host–parasitoid dynamics, which is relevant for climate-health risk assessments and pest management policies.
- Provides a blueprint for designing monitoring datasets with factorial manipulations to disentangle environmental drivers on insect life histories.
- Supports meta-analyses and model parameterization for predicting responses to climate variability in host–parasitoid systems.
- Highlights practical data governance considerations (data sharing, metadata clarity, standardized units) that are pertinent to implementing monitoring frameworks.