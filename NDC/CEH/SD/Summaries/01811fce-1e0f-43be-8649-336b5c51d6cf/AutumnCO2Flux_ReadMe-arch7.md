# ReadMe file for AutumnCO2Flux.csv

## Overview
- Describes CO2 flux measurements from a controlled, replicated field experiment in Snowdonia, Wales.
- Data intended for GIS-style mapping and spatial analysis of gas flux responses to treatments.

## Location and setting
- Site: unimproved grazing land in the Carneddau mountains, Snowdonia National Park, Wales, UK.
- Elevation: 556 m above sea level.
- Coordinates provided: 53°22'N, 3°95'W.
- Study design: randomised block experiment with defined plots/chambers.

## Experimental treatments and design
- Treatments (n = 4 replicates per treatment):
  - Control: no urine application.
  - ArtUrine: artificial sheep urine applied in triplicate discrete patches inside the chamber (each patch: 200 ml artificial urine over 100 cm2 soil area; N application rate = 1120 kg N ha-1).
  - CandN: nitrate and glucose treatment (1 L solution applied across a 40 × 40 cm square inside the chamber; 106 kg N ha-1 and 213 kg C ha-1).
- Treatment application date: 25/10/17.
- Monitoring period: 45 days post-treatment.
- Experimental units: chambers with a basal area of 0.25 m2; dimensions 50 cm × 50 cm × 15 cm (L × W × H).

## Data collection and instrumentation
- Monitoring system: automated greenhouse gas monitoring system (Queensland University of Technology) with a LI-COR LI-820.
- Measurements: eight flux measurements per chamber per day; 1 h chamber closure per measurement; four gas samples analyzed per 1 h closure; calibration standard analyzed after every fourth gas sample with GC.
- Data type: high-frequency, quality-assessed flux data (not raw gas concentration data).

## Data content and headers
- Flux metric: CH4 fluxes reported as mg CO2-C m-2 h-1 (note potential inconsistency in CH4 label vs CO2-C unit; interpret as given).
- Time stamps: Timestamp in format dd/mm/yy hh:mm.
- Time reference: Days indicates time relative to treatment (pre- or post-treatment).
- Columns B–M: flux values for each chamber/plot corresponding to treatments (Control, ArtUrine, CandN).

## Data quality and quality assurance
- QA steps: inspection of raw data files and GC chromatograms for anomalies; removal of data if necessary (e.g., interference in gas peaks).
- The dataset comprises quality-assessed flux data rather than raw concentrations.

## Data structure implications for GIS
- Spatial attributes: treatment type, chamber/plot identifiers, and corresponding flux measurements.
- Temporal attributes: timestamp and Days relative to treatment allow spatiotemporal mapping of flux dynamics.
- Suitable for map-based visualization of treatment effects and high-frequency flux trends.
- Be mindful of potential labeling confusion (CH4 label with CO2-C units) when integrating with other datasets.

## Provenance and usage notes
- Authors must be acknowledged if data are reused or reproduced.
- Data may be spread across multiple files or require careful parsing to align metadata with flux values.