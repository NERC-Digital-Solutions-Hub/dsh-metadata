# ReadMe file for AutumnCH4Flux.csv

## Overview
- CH4 flux measurements from a humic gleysol in unimproved grazing land, Carneddau mountains, Snowdonia National Park, Wales, UK.
- Treatments: control (no urine), artificial sheep urine, and nitrate + glucose.
- Sampling occurred after treatment application on 25/10/2017 and continued for 45 days.
- Sheep were excluded from plots from 15/05/2017 to avoid recent excretion confounding data.
- Location: 556 m above sea level; coordinates provided; data collected with automated GHG monitoring.

## Experimental Design
- Randomised block design with four treatments.
- Chamber-based measurements; each chamber has a base area of 0.25 m2 and dimensions 50 cm x 50 cm x 15 cm (L x W x H).
- Treatments analyzed over a 45-day period following application.

## Treatments
- Control: no urine application.
- Artificial sheep urine (ArtUrine): urine applied in triplicate discrete patches inside the chamber; each patch delivers 1120 kg N ha-1; 200 ml artificial urine applied per patch over 100 cm2 soil surface.
- C and N (nitrate and glucose): 106 kg N ha-1 and 213 kg C ha-1; 1 L of nitrate + glucose solution applied across a 40 cm x 40 cm square inside the chamber.

## Data Collection and Instruments
- Emissions monitored with an automated greenhouse gas monitoring system (Queensland University of Technology) using a SRI 8610 GC.
- Sampling cadence: eight flux measurements per chamber per day (1-hour chamber closure; four gas samples per closure period); calibration standard analyzed after every fourth sample.
- Data capture period corresponds to high-frequency flux data; not raw gas concentration data.
- Quality assurance involved inspecting raw data files and GC chromatograms for anomalies and removing problematic data.

## Data Structure and Variables
- Chamber data: four treatments with multiple chambers/plots; headers specify treatment and chamber/plot identifiers.
- Timestamp format: dd/mm/yy hh:mm.
- Days: time relative to treatment (pre- or post-treatment).
- CH4 flux columns: B to M (eight flux measurements per chamber per day) expressed as µg CH4-C m-2 h-1.
- Treatment codes: Control, ArtUrine (artificial urine), CandN (nitrate and glucose).
- Primary metadata includes chamber basal area (0.25 m2) and chamber dimensions.

## Quality Assurance and Data Provenance
- Data represent quality-assessed flux measurements (not raw gas concentrations).
- Documentation notes authorship acknowledgment for reused/reproduced data.
- Data headers and treatment identifiers are provided to support traceability and reproducibility.

## Context and Notes
- The study assesses CH4 flux responses to urine and nitrate+glucose inputs in a 고 respective pasture soil context.
- Geographic and temporal context provided to enable alignment with related datasets and potential meta-analyses.

## Data Usage Considerations for Analysis
- Suitable for correlation analyses between treatments and CH4 flux, as well as time-series modelling over the 45-day post-treatment window.
- Potential integration with environmental or management covariates if available.
- Important to reference the data origin and ensure proper acknowledgment of authors when reusing.