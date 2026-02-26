# Life history data from insects in a host-parasitoid interaction under a range of humidity and heat stress conditions

## Overview
- Data resource on life history parameters for a host insect (the Indian meal moth, Plodia interpunctella) and its parasitoid (Venturia canescens).
- Experimental conditions: high humidity (60.8% RH) vs low humidity (32.5% RH) and heat stress exposure at 38°C.
- Stress durations: 0, 6, or 72 hours; host stages tested: 4th or 5th instar.
- Single-generation lab study; aims to understand how humidity modifies stage-specific responses to heat stress.
- Missing data denoted as NA due to sample loss or mortality during heat stress.

## Collection and design
- Lab study with a full-factorial design: parasitism (parasitized vs unparasitized) × humidity (high vs low) × larval stage (L4 vs L5) × duration of heat stress (0, 6, 72 hours) → 2 × 2 × 2 × 3 = 24 treatment combinations.
- Each combination includes 2025 observations.
- Procedure:
  - Host eggs placed in 25-well plates; incubated at 28°C under specified humidity.
  - Parasitized larvae created by exposing early 4th instar larvae to adult parasitoids; unparasitized larvae serve as controls.
  - Heat stress applied by transferring plates to a 38°C incubator.
  - Daily monitoring until adult emergence; adults collected for body size measurements.
- Measurements:
  - Body size proxy: mid-femur length and hind tibia length, measured with a Nikon DS-5 M camera and NIS-element software.
  - Data digitized and quality-checked.

## Data structure and content
- Two CSV files:
  - host.csv: life history traits for unparasitized larvae.
    - Key variables: Plate_id, Id, Humidity (H/NH), Parasitism (H/HP), Duration (0/6/72), Stage (L4/L5), Eggtransfer_date, Survived2L4, Pupate, Hostpupate_date, Host emergence, Hostemerge_date, Hostdead_date, Host_sex, Midfemur, Rearfemur.
  - parasitoid.csv: life history traits for parasitized larvae.
    - Key variables: Plate_id, Id, Humidity (H/NH), Interaction (H-P), Duration, Stage, Eggtransfer_date, Survived2L4, Parasited_date, Parasitism, Pupate, Hostpupate_date, Hostemerge/Wasp_emerge, Emerge_date, Dead_date, Wasp_size, Midfemur, Rearfemur, Host_sex.if.applicable.
- Data units:
  - Dates in YYYYMMDD format.
  - Lengths in millimeters (mm).
  - Duration in hours.
- NA used where applicable (e.g., not surviving to a life stage, or non-applicable measurements).

## Quality control and provenance
- Factorial design validated by structure: 2 × 2 × 2 × 3 with robust replication.
- Large sample size per treatment (2025 observations) and long-term use of this model organism within the research group (>20 years) support reliability.
- Data were digitized, transformed, and checked for accuracy; detailed metadata and definitions accompany the CSVs to support clarity and reuse.

## Reuse considerations for data leaders
- Clear keys for linking records across datasets via Plate_id and Id enable integration with other datasets or longitudinal studies.
- Standardized variable definitions and units support interoperability and cross-institution collaborations.
- Useful for analyses of host-parasitoid interactions under environmental stressors (humidity and heat), stress physiology, and developmental timing.
- Considerations:
  - Handle missing data (NA) due to mortality or non-applicability.
  - Ensure consistent interpretation of Parasitism indicators and date fields across analyses.
  - Leverage the documented data structure to integrate with broader data governance and data-sharing practices.