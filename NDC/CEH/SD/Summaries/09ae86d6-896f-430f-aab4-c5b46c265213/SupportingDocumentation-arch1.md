# Stable isotope values for 108 water samples collected in the Gandak River Basin, in Bihar, India are presented

## Overview
- 108 water samples collected between February 2017 and February 2019 from surface water, groundwater, and rainfall in the Gandak River Basin, Bihar, India.
- Accompanying values for specific electrical conductivity (SEC) provided for most samples.
- Isotopic analysis focused on deuterium (dD) and oxygen-18 (d18O) using mass spectrometry at British Geological Survey laboratories (UK).
- Data collected as part of the CHANSE (Coupled Human And Natural Systems Environment) project.

## Variables and data structure
- Key fields include:
  - sample_date: date the sample was taken
  - d18O VSMOW2 (‰): oxygen-18 concentration relative to VSMOW
  - dD VSMOW2 (‰): deuterium concentration relative to VSMOW
  - SEC uS/cm: specific electrical conductivity
- Each entry also includes:
  - BGS Sample identifier or Lab Code
  - For missing values, fields are left blank

## Site locations and sampling details
- Sources represented include:
  - River Gandak (surface water)
  - Groundwater from boreholes, tube wells, and hand pumps
  - Canals and canal-related water
  - Rainfall and rainwater samples
- Data entries provide:
  - lat/long coordinates (geographic location)
  - surface_elevation_mOD (meters above mean datum)
  - source_depth_m (well depth or depth to water)
  - Source_use (e.g., domestic, irrigation, temple, nursery)
  - Notes on sampling context (e.g., time pumped before sampling, proximity to canals, presence of bubbles in flow, water use)
- Sample identifiers vary across datasets (e.g., 13965-0001, 13966-0001, 14466-0001, 1A, S1, CHPat01, NIGL_001, etc.), reflecting multiple collection campaigns or datasets integrated in the release.
- Many entries include qualitative details about sampling conditions and water usage (e.g., “pumped 5–15 mins before sampling,” “drilled more than 20 years ago,” “good tasting water,” “tastes of iron”).

## Data provenance and scope
- Isotopic measurements conducted at BGS laboratories (UK); SEC measurements at the sampling site.
- Data contributed as part of the CHANSE project, with metadata designed to support data discovery and reuse.

## Potential analyses and use cases for analysts
- Identify water source signatures and potential mixing between river, groundwater, and rainfall inputs.
- Compare d18O and dD values to infer recharge pathways and evaporation effects across different source types (surface water vs groundwater vs rainfall).
- Assess spatial patterns by linking isotopic compositions with precise locations, depths, and land-use context.
- Explore relationships between isotopic ratios and SEC as a proxy for water origin and quality.
- Use temporal coverage (2017–2019) to examine seasonal or yearly variations in water sources and isotopic signatures.

## Limitations and caveats
- Some entries have missing depth (source_depth_m) and/or elevation data.
- Sampling contexts vary (e.g., pumping before sampling, proximity to canals, variable field conditions) which may influence isotopic or conductivity readings.
- Large dataset with multiple sub-collections; ensure consistent cross-dataset alignment when performing integrated analyses.
- Data are descriptive of sampling events and locations; explicit statistical analyses or model outputs are not provided within this document.