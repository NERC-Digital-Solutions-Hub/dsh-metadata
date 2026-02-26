# Life history data from insects in a host-parasitoid interaction under a range of humidity and heat stress conditions

## Overview
- A lab-based data resource on life history parameters for a host insect (Plodia interpunctella) and its parasitoid (Venturia canescens).
- Experiments examined responses under two humidity levels (high 60.8% RH; low 32.5% RH) and heat stress at 38°C.
- Heat stress applied at 4th or 5th larval instars for 0, 6, or 72 hours.
- Missing data are labeled NA due to sample loss or mortality.

## Collection and experimental design
- Single-generation, full-factorial lab study with 2 × 2 × 2 × 3 design:
  - Parasitism: parasitized vs unparasitized larvae
  - Humidity: high vs low
  - Larval stage at heat exposure: 4th vs 5th instar
  - Heat-stress duration: 0, 6, 72 hours
- Each treatment combination includes 2025 observations.
- Host eggs were reared in 25-well plates at 28°C; humidity manipulated via saturated NaCl for high humidity.
- Parasitism induced by exposing early 4th instar larvae to a newly emerged parasitoid.
- Life-history outcomes tracked until adulthood; body size measured as mid-femur and hind tibia lengths using microscopy and imaging software.
- Data were digitized and checked for accuracy.

## Nature and units of recorded values
- Data recorded per individual host or parasitoid with fields covering timing, survival, development, and morphology.
- Common units:
  - Dates (YYYYMMDD)
  - Durations in hours
  - Measurements in millimeters (mm)
  - Binary outcomes (1 = yes, 0 = no)
- Two linked data records per organism: host.csv and parasitoid.csv.

## Details of data structure

- host.csv
  - Plate_id, Id
  - Humidity (H = high, NH = low)
  - Parasitism (H = host alone, HP = parasitized)
  - Duration (0, 6, 72)
  - Stage (L4, L5)
  - Eggtransfer_date
  - Survivived2L4 (1/0)
  - Pupate (1/0)
  - Hostpupate_date
  - Host emergence, Hostemerge_date
  - Hostdead_date
  - Host_sex (M/F)
  - Midfemur, Rearfemur (mm)

- parasitoid.csv
  - Plate_id, Id
  - Humidity (H, NH)
  - Interaction (H-P for parasitized)
  - Duration (0, 6, 72)
  - Stage (L4, L5)
  - Eggtransfer_date
  - Survivived2L4 (1/0)
  - Parasited_date
  - Parasitism (1/0)
  - Pupate
  - Hostpupate_date
  - Hostemerge/Wasp_emerge
  - Emerge_date
  - Dead_date
  - Wasp_size (hind tibia length, mm)
  - Midfemur, Rearfemur (mm)
  - Host_sex.if.applicable

## Quality control
- Full-factorial design (2 × 2 × 2 × 3) with 2025 observations per treatment combination.
- The dataset comes from a long-running model system used for over 20 years in the research group.
- Missing values (NA) arise from sample loss or non-applicable conditions (e.g., mortality before a given measurement).

## Data accessibility and structure
- Files:
  - host.csv: life-history traits for unparasitized hosts
  - parasitoid.csv: life-history traits for parasitized hosts/wasp outcomes
- Data types include dates, durations, categorical indicators, and morphometric measurements, enabling linkage between host and parasitoid outcomes by Plate_id and Id.

## GIS-relevant considerations and potential use
- Although collected in a controlled lab setting, the structured, multi-factor design provides parameters (survival, development, body size) that can be integrated with environmental layers (humidity, temperature maps) for spatially explicit modeling of host–parasitoid dynamics.
- Potential visualizations include:
  - Heat-stress and humidity effects on survival and body size
  - Stage-specific responses under parasitized vs unparasitized conditions
- Note: The data are not spatial by themselves; GIS applications would require coupling with environmental/spatial datasets or modeling frameworks.

## Limitations and caveats
- Lab-based and single-generation; may not capture field-level spatial heterogeneity or longer-term dynamics.
- Missing data labeled NA; interpretation should consider potential biases from non-random sample loss (e.g., mortality under heat stress).

## Summary of usage
- Use host.csv and parasitoid.csv to analyze how humidity, heat-stress duration, and parasitism status affect survival, development timing, and body size across 4th and 5th instars.
- Integrate with GIS-ready environmental data to explore spatially informed host–parasitoid models or risk assessments under varying humidity and temperature scenarios.