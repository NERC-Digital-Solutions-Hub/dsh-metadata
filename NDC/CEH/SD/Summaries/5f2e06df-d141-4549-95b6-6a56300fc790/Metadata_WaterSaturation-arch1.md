# Mathematically modelled daily water saturation profiles for sites on the Namoi River floodplain in south-east Australia, at different distances from the river.

## Overview
- Dataset of daily, vertically-resolved soil water saturation profiles (0–10 m depth) at six sites near the Namoi River floodplain, across two locations (Old Mollee and Yarral East) at varying distances from the river.
- Generated with a physically-based hydrological model (HaughFlow) to simulate subsurface moisture dynamics in a hydraulically connected floodplain system.
- Intended to support analysis of how proximity to the river influences subsurface saturation over time.

## Data and model details
- Model: HaughFlow (Fortran90) using coupled 1D vertical Richards equation (vadose zone) and 1D lateral Boussinesq equation (phreatic zone); two-way coupling between vadose and phreatic zones.
- Outputs: time series of soil-water saturation profiles at specified depths and distances from the river.
- Spatial discretisation: 944 grid points across 10 m depth, at half-grid intervals.
- Temporal discretisation: daily outputs.
- Inputs driving the model: river stage levels, climate parameters, and soil properties.
- Data format: outputs originally in unformatted files, converted to formatted CSV files for ease of use.
- Related figures/files: Data correspond to figures in Evans et al. (2018).

## Variables and outputs
- Depth: measured in metres from ground surface.
- Water saturation: proportion of pore space filled with water, ranging from 0 to 1; reported with seven decimals.
- Output grid: vertical profiles from surface down to 10 m depth; daily time series.

## Spatial and temporal coverage
- Locations and sites:
  - Old Mollee: 50 m, 140 m, 320 m from the river.
  - Yarral East: 40 m, 110 m, 290 m from the river.
- Time frames:
  - Old Mollee: Figure 6 datasets run 01 July 2011 – 30 June 2015.
  - Yarral East: Figure 6 datasets run 01 Jan 2013 – 30 June 2015.
  - Old Mollee Figure 7: 01 Jan 2004 – 31 Dec 2016 (alternative climate inputs).
- File naming: datasets are linked to figures in Evans et al. (2018); example files include Figure6a_OldMollee50m_WaterSaturation.csv, Figure6b_YarralEast40m_WaterSaturation.csv, etc.

## Calibration and validation
- Calibration target: water table levels at Yarral East 290 m site for the year 2013.
- Resulting soil properties (calibrated): saturated hydraulic conductivity = 5.756 m/day; drainage = 0.01568 m/day.

## Site locations
- Latitude/longitude (decimal degrees) and Australian Height Datum (AHN) elevations:
  - Old Mollee 50 m: -30.254, 149.681; AHN 202.25
  - Old Mollee 140 m: -30.254, 149.682; AHN 204.37
  - Old Mollee 320 m: -30.254, 149.684; AHN 203.82
  - Yarral East 40 m: -30.237, 149.671; AHN 202.98
  - Yarral East 110 m: -30.236, 149.671; AHN 202.84
  - Yarral East 290 m: -30.234, 149.671; AHN 202.02

## Data access and references
- Data were modelled as part of a PhD project funded by the Natural Environment Research Council and the National Trust.
- Primary reference: Evans, C.M., Dritschel, D.G., and Singer, M.B., 2018, "Modelling subsurface hydrology in floodplains", Water Resources Research.
- Outputs: converted to accessible formatted CSVs from original unformatted model outputs; intended to facilitate reuse in further analyses and cross-site comparisons.