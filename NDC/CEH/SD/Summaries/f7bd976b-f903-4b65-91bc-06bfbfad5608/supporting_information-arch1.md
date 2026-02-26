# Life history data from insects in a host-parasitoid interaction under a range of humidity and heat stress conditions

## Objective and scope
- A data resource documenting life history parameters for a host, Plodia interpunctella (Indian meal moth), and its parasitoid, Venturia canescens.
- Examines how humidity interacts with heat stress to affect stage-specific responses during a single generation.
- Humidity manipulated at high (60.8%) or low (32.5%) relative humidity; heat stress applied at 38°C for 0, 6, or 72 hours.
- Heat stress applied to hosts in 4th or 5th instar; includes both parasitized and unparasitized hosts.

## Organisms and experimental design
- Hosts: Indian meal moth eggs reared individually in 25-well plates, either unparasitized or parasitized by a newly emerged parasitoid.
- Parasitoids: Venturia canescens exposed to parasitized hosts.
- Design: full-factorial experiment with four factors:
  - Parasitism: parasitized vs unparasitized
  - Humidity: high vs low
  - Larval stage when heat stress is applied: 4th vs 5th instar
  - Duration of heat stress: 0, 6, 72 hours
- Replication: 2 × 2 × 2 × 3 design, with 2025 observations per treatment combination.
- Duration and scope: data collected over a single generation; model organism used by the research group for over two decades.
- Data collection environment: laboratory incubators at controlled temperatures; humidity manipulated using saturated salt solutions; plates moved to 38°C incubator for heat stress.

## Data collection and measurements
- Measurements taken as hosts and parasitoids progress through life stages, including survival and development milestones.
- Host metrics:
  - Survival to 4th instar, pupation, and emergence
  - Dates for key events (Eggtransfer_date, Hostpupate_date, Hostemerge_date, Hostdead_date)
  - Morphometrics (Midfemur, Rearfemur) in mm
  - Sex (Host_sex)
- Parasitoid metrics:
  - Parasitism confirmation (Parasited_date, Parasitam, i.e., observation of cocking behavior)
  - Survival to 4th instar, emergence of host/parasitoid, and related dates (Parasited_date, Hostemerge/Wasp_emerge, Emerge_date, Dead_date)
  - Morphometrics (Wasp_size, Midfemur, Rearfemur) in mm
  - Host sex if applicable (Host_sex.if.applicable)
- Data types and units:
  - Dates in YYYYMMDD format
  - Durations in hours
  - Sizes in millimeters (mm)
  - Other descriptors as categorical codes (e.g., Humidity: H = high, NH = low; Stage: L4, L5)

## Data files and structure
- Two CSV files:
  - host.csv: life history traits for each unparasitized larva
    - Key columns include Plate_id, Id, Humidity, Parasitism, Duration, Stage, Eggtransfer_date, Survivived2L4, Pupate, Hostpupate_date, Host emergence, Hostemerge_date, Hostdead_date, Host_sex, Midfemur, Rearfemur, among others
  - parasitoid.csv: life history traits for each parasitized larva
    - Key columns include Plate_id, Id, Humidity, Interaction, Duration, Stage, Eggtransfer_date, Survivived2L4, Parasited_date, Parasitism, Pupate, Hostpupate_date, Hostemerge/Wasp_emerge, Emerge_date, Dead_date, Wasp_size, Midfemur, Rearfemur, Host_sex.if.applicable, among others
- Data structure details include:
  - Plate_id identifies the 25-well plate used
  - Id provides unique individual identifiers
  - Across both files, date and size fields are provided with clear units
  - NA used where data are missing due to mortality or non-applicability

## Quality control and provenance
- Fully factorial experimental design with extensive replication per treatment
- Laboratory model system with long-term use (20+ years) in the research group, supporting reliability and comparability
- Data were digitized with accuracy checks to ensure measurement integrity

## Potential analyses and applications
- Assess how humidity modulates host and parasitoid responses to heat stress across developmental stages
- Explore correlations between survival, development timing, and morphological traits under different environmental conditions
- Build predictive models (e.g., logistic or survival analyses) for stage-specific outcomes and emergence success
- Integrate host and parasitoid data to study interaction dynamics under environmental stress
- Use as a reproducible data resource with metadata for data sharing and cross-study comparisons

## Considerations and limitations
- Missing data (NA) reflect mortality events or non-applicability at certain life stages
- Findings are based on a laboratory, single-generation setup and may not fully generalize to natural environments
- Some fields are condition-specific (e.g., parasitism status, stage at stress) and require careful alignment when integrating host and parasitoid datasets
- Data formatting and variable naming differences between host and parasitoid files necessitate careful merging when performing joint analyses