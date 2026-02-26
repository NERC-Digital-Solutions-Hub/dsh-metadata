# ReadMe file for SpringCH4Data.csv

## Overview
- CH4 emissions data from plots treated with control (no urine), artificial urine (ArtUrine), and real sheep urine (Urine).
- Experimental context: orthic podzol soil within a semi-improved upland grassland at Henfaes Research Station, North Wales.
- Study design: randomised block experiment conducted in spring 2016.
- Data represent quality-assessed CH4 flux measurements, not raw gas concentrations.

## Location, soil, and design
- Location: Henfaes Research Station, Abergwyngregyn, North Wales (53°13'N, 4°0'W), elevation ~270 m above sea level.
- Soil/landscape: orthic podzol on semi-improved upland grassland.
- Experimental design: randomised block with multiple plots to compare treatments.

## Data collection and instruments
- Instrumentation: automated greenhouse gas monitoring system linked to a SRI 8610 GC.
- Flux measurement cadence: eight flux measurements per chamber per day.
- Timing: 1-hour chamber closure periods with four gas samples analyzed per closure period.
- Calibration: standard calibration after every fourth gas sample.
- Chamber dimensions: 50 cm x 50 cm x 15 cm; basal area = 0.25 m2.
- Data type: flux data post-quality assurance (not raw concentration data).

## Data structure and content
- Timestamp format: dd/mm/yy hh:mm.
- Flux data: columns B to M contain CH4 fluxes expressed as mg CH4-C m-2 h-1.
- Metadata in headers: treatment (Control, ArtUrine, Urine) and chamber/plot identifiers.

## Treatments and metadata
- Treatments included in the dataset:
  - Control (no urine)
  - ArtUrine (artificial urine)
  - Urine (real sheep urine)
- Header information encodes treatment and chamber/plot numbers for spatial referencing.

## Quality assurance and data quality
- QA procedures: visual inspection of raw data files and GC chromatograms for anomalies; anomalous data removed if necessary.
- Data provided represent quality-assessed flux values rather than raw gas concentrations.

## Temporal and spatial applicability for GIS
- Temporal scope: spring 2016 measurements; multiple observations per day per chamber.
- Spatial context: designed around a randomized block layout; data are suitable for mapping spatial patterns of CH4 flux by treatment and block, subject to chamber/location availability.
- Units are per area (mg CH4-C m-2 h-1), facilitating comparison across plots and integration with other GIS layers.

## Usage notes and attribution
- Authors must be acknowledged if data are reused or reproduced.
- Data are suitable for GIS visualisations and spatial analyses of CH4 flux under different urine treatments, with caveats about potential missing values due to QA steps and the lack of per-chamber geographic coordinates in the readme.