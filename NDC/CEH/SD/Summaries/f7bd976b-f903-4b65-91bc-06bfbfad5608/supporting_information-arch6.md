# Life history data from insects in a host-parasitoid interaction under a range of humidity and heat stress conditions

## Overview
- Dataset of life history parameters for a host (Plodia interpunctella) and its parasitoid (Venturia canescens) under varying humidity and heat stress.
- Humidity conditions: high (60.8% RH) or low (32.5% RH).
- Heat stress applied at 4th or 5th instar larvae for durations of 0, 6, or 72 hours.
- Single-generation lab experiment; missing data denoted as NA due to sample loss or mortality under heat stress.

## Collection/generation method
- Lab study with a full-factorial design monitoring a single generation of host and parasitoid life history.
- Host eggs placed in 25-well plates; hosts reared at 28°C with humidity manipulated via saturated salt solution.
- Parasitism manipulated by exposing early 4th instar larvae to parasitoids (parasitized) or not (unparasitized).
- Heat stress applied by transferring plates to an incubator at 38°C with the designated humidity.
- Daily monitoring until emergence of adult host or parasitoid; body size measured via mid-femur and hind tibia lengths using microscopy and image software.
- Data cleaned and converted to digital format.

## Nature and Units of recorded values
- Data include date, days, and measurements in millimeters (mm) across treatments.
- Two CSV files store the data: host.csv for unparasitized larvae and parasitoid.csv for parasitized larvae.

## Quality control
- Experimental design: 2 × 2 × 2 × 3 (parasitism, humidity, larval stage, duration of heat stress).
- Each treatment combination comprises 2025 observations.
- The design has been used for over 20 years, indicating robust, established lab methodology.

## Details of data structure
- host.csv: life history traits for unparasitized larvae with variables such as:
  - Plate_id, Id, Humidity (H or NH), Parasitism (H or HP), Duration (0, 6, 72), Stage (L4 or L5),
  - Eggtransfer_date, Survivived2L4, Pupate, Hostpupate_date, Host emergence, Hostemerge_date, Hostdead_date,
  - Host_sex, Midfemur, Rearfemur.
- parasitoid.csv: life history traits for parasitized larvae with variables such as:
  - Plate_id, Id, Humidity (H or NH), Interaction (H-P), Duration, Stage,
  - Eggtransfer_date, Survivived2L4, Parasited_date, Parasitism, Pupate, Hostpupate_date,
  - Hostemerge/Wasp_emerge, Emerge_date, Dead_date, Wasp_size, Midfemur, Rearfemur,
  - Host_sex.if.applicable.
- Units and dates:
  - Dates use YYYYMMDD format.
  - Length measurements in millimeters (mm).

## How this data supports data exploration and product development (Data Support perspective)
- Enables combining host and parasitoid life-history data to study interaction outcomes under stress.
- Suitable for creating self-serve analyses and dashboards around survival rates, development timing, and body size across treatments.
- Can be enriched with external datasets (e.g., environmental conditions, additional life stages) to broaden policy or operational insights.
- Clear documentation of variables, units, and data structure facilitates data reuse, quality assurance, and reproducible analyses.
- NA values clearly indicate missing measurements due to mortality or loss, which should be accounted for in analyses.