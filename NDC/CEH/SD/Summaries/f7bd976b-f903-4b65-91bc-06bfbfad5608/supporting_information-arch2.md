# Life history data from insects in a host-parasitoid interaction under a range of humidity and heat stress conditions

## Overview
- Dataset of life history parameters for a host (Plodia interpunctella) and its parasitoid (Venturia canescens) under two humidity levels and simulated heat stress.
- Humidity: high (~60.8% RH) vs. low (~32.5% RH).
- Heat stress: applied at the 4th or 5th instar for 0, 6, or 72 hours.
- Single-generation lab experiment to assess how humidity modifies stage-specific responses to heat stress.
- Missing data represented as NA due to sample loss or mortality.

## Collection/generation method
- Lab study using a full-factorial, single-generation design.
- Host eggs placed individually in 25-well plates; incubated at 28°C under either high or low humidity (achieved with saturated NaCl for high humidity).
- Parasitized larvae created by exposing early 4th instar larvae to a newly emerged adult parasitoid; unparasitized larvae used as controls.
- Heat stress applied by transferring plates to a 38°C incubator under corresponding humidity conditions.
- Hosts monitored daily until an adult emerged; body sizes measured via microscopy (mid-femur and hind tibia lengths) using Nikon camera/software.
- Data digitized and quality-checked.

## Nature and units of recorded values
- Data organized in two CSV files: host.csv and parasitoid.csv.
- Each record includes date, duration, stage, and body-size measurements, with treatment indicators.
- Host data variables include: Plate_id, Id, Humidity, Parasitism, Duration, Stage, Eggtransfer_date, Survival to L4, Pupate, Hostpupate_date, Host emergence, Hostemerge_date, Hostdead_date, Host_sex, Midfemur, Rearfemur.
- Parasitoid data variables include: Plate_id, Id, Humidity, Interaction, Duration, Stage, Eggtransfer_date, Survivived2L4, Parasited_date, Parasitism, Pupate, Hostpupate_date, Hostemerge/Wasp_emerge, Emerge_date, Dead_date, Wasp_size, Midfemur, Rearfemur, Host_sex.if.applicable.
- Units: dates (YYYYMMDD), durations in hours, body lengths in mm; NA used where not applicable.

## Quality control
- Full-factorial design: 2 (parasitism) × 2 (humidity) × 2 (larval stage) × 3 (heat-stress duration).
- Each treatment combination contains 2025 observations.
- Longstanding laboratory system (>20 years) used as a model organism.

## Details of data structure
- Files: host.csv (life-history traits for unparasitized larvae) and parasitoid.csv (life-history traits for parasitized larvae).
- Key measured outcomes: survival to 4th instar, pupation, emergence; dates of developmental milestones; sex when applicable; body-size measurements (midfemur, rearfemur).
- Data contain explicit treatment identifiers and timing information for downstream analyses.

## Access and applicability for environmental monitoring
- Standardized, well-documented dataset suitable for integration with environmental stress datasets.
- Enables analysis of how humidity and heat stress jointly influence host and parasitoid life-history traits.
- Clear variable definitions and formats support QA, reproducibility, and portal-based data sharing.