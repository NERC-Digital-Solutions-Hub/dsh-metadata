# Life history data from insects in a host-parasitoid interaction under a range of humidity and heat stress conditions

## Overview
- Lab-based, single-generation study on a host (Plodia interpunctella) and its parasitoid (Venturia canescens).
- Investigates how humidity (high 60.8% RH vs low 32.5% RH) interacts with heat stress exposure at 4th or 5th larval instar.
- Heat stress durations include 0, 6, and 72 hours.
- Data collected as life history parameters; missing data are recorded as NA due to sample loss or mortality.

## Collection and generation method
- Full-factorial design: parasitized vs unparasitized, high vs low humidity, 4th vs 5th instar, and heat-stress duration (0, 6, 72 hours).
- 2025 observations per treatment combination.
- Methods:
  - Host eggs individually placed in 25-well plates; incubated at 28℃ with controlled humidity.
  - Parasitized larvae created by exposing early 4th instar to a newly emerged parasitoid; unparasitized controls maintained separately.
  - Heat stress applied by transferring plates to 38℃ incubators.
  - Hosts monitored daily until adulthood; adults measured for body size and recorded.
- Body size measurements: mid-femur length and hind tibia length via microscope and imaging software.
- Data are digitized and quality-checked.

## Nature and units of recorded values
- Data organized by individual with multiple treatment and trait measurements.
- Recorded columns include date, days, and millimeters (mm) for body measurements.
- Two CSV files:
  - host.csv: life history traits for unparasitized larvae with variables such as Plate_id, Id, Humidity, Parasitism, Duration, Stage, Eggtransfer_date, Survived2L4, Pupate, Hostpupate_date, Host emergence, Hostemerge_date, Hostdead_date, Host_sex, Midfemur, Rearfemur.
  - parasitoid.csv: life history traits for parasitized larvae with variables such as Plate_id, Id, Humidity, Interaction, Duration, Stage, Eggtransfer_date, Survived2L4, Parasited_date, Parasitism, Pupate, Hostpupate_date, Hostemerge/Wasp_emerge, Emerge_date, Dead_date, Wasp_size, Midfemur, Rearfemur, Host_sex.if.applicable.
- Units:
  - Date fields: YYYYMMDD
  - Duration: hours
  - Size fields: millimeters (mm)

## Quality control
- Experimental design is 2 × 2 × 2 × 3 (parasitism, humidity, larval stage, duration) with 2025 observations per treatment.
- The study system has been in use for over 20 years within the research group, supporting methodological consistency.
- Data were transformed to digital format with accuracy checks.

## Details of data structure
- host.csv:
  - Plate_id, Id, Humidity, Parasitism, Duration, Stage, Eggtransfer_date, Survived2L4, Pupate, Hostpupate_date, Host emergence, Hostemerge_date, Hostdead_date, Host_sex, Midfemur, Rearfemur.
- parasitoid.csv:
  - Plate_id, Id, Humidity, Interaction, Duration, Stage, Eggtransfer_date, Survived2L4, Parasited_date, Parasitism, Pupate, Hostpupate_date, Hostemerge/Wasp_emerge, Emerge_date, Dead_date, Wasp_size, Midfemur, Rearfemur, Host_sex.if.applicable.