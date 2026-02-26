# Authors must be acknowledged if data are re-used or reproduced. The data corresponds to CH4 emissions measured from control (no urine) artificial and real sheep urine applied to an orthic podzol within a semiimproved upland grassland at Henfaes Research Station, Abergwyngregyn, North Wales (270 m a.s.l.; 53°13'N, 4°0'W) in autumn, 2016. Emissions were monitored from plots based on a randomised block experimental design.

## Overview
- High-frequency CH4 emission data collected from plots with three treatments: Control, artificial urine, and real urine.
- Experimental design: randomized block.
- Aimed at enabling map-based visualization and spatial analysis of emissions across treatments and plots.

## Study site and design
- Location: Henfaes Research Station, Abergwyngregyn, North Wales (53°13'N, 4°0'W), altitude 270 m above sea level.
- Habitat: semi-improved upland grassland on orthic podzol soil.
- Plot layout: randomized block design for treatment assignment.
- Chamber specifications: each chamber with a basal area of 0.25 m²; dimensions 50 cm × 50 cm × 15 cm (L × W × H).

## Data collection and methods
- Instrumentation: automated greenhouse gas monitoring system using LI-COR LI-820.
- Measurement cadence: eight flux measurements per chamber per day.
  - Each measurement cycle includes a 1-hour chamber closure period.
  - Four gas samples analyzed per 1-hour closure period.
  - Calibration standard analyzed after every fourth gas sample entering the GC.
- Target gas: CH4 emissions (data described as flux measurements; note: data headers reference CO2 fluxes, see Data content).
- Data period: emissions data from the period analyzed by the automated system (high-frequency data).

## Data content and structure
- Data represent quality-assessed flux data rather than raw gas concentrations.
- Data headers:
  - Timestamp: dd/mm/yy hh:mm
  - Columns B–M: CO2 fluxes expressed as mg CO2-C m⁻² h⁻¹
  - Treatments encoded in headers: Control, ArtUrine (artificial urine), Urine (real urine)
- Spatial and temporal resolution suitable for GIS applications, with explicit treatment and chamber/plot identifiers.

## Quality assurance and data processing
- QA procedures include inspection of raw data files and GC chromatograms for anomalies.
- Anomalous data or interference (e.g., gas peak interference) are removed as needed.
- Data provided are filtered quality-assessed flux values, not raw concentration data.

## GIS applicability and considerations
- Suitable for map-based visualization of emission fluxes by treatment and plot over time.
- Consider data standard inconsistencies (document notes CH4 emissions in text but data headers reference CO2 fluxes) when integrating with other datasets.
- Data may combine measurements at different resolutions; plan for harmonization when merging with other layers.
- Important to align timestamps with other spatial datasets to support temporal analyses (e.g., daily vs. high-frequency intervals).
- Ensure attribution to authors when reusing data.

## Attribution and reuse notes
- Authors must be acknowledged if data are reused or reproduced.