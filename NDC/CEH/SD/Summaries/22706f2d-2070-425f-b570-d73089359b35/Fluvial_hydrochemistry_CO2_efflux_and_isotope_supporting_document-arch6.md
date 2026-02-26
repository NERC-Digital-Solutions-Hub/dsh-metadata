# Fluvial hydrochemistry, CO2  efflux and delta   13 C-Dissolved inorganic carbon data for the Houzhai Catchment, Southwest China, 2016-2018

## Overview
- Dataset from the NERC-funded project addressing CO2 efflux in karst-fluvial systems, focusing on the Houzhai catchment in SW China.
- Measurements include: CO2 efflux rate (F_CO2), water velocity, temperature, pH, dissolved oxygen (DO), electrical conductivity (EC), total alkalinity (TA), dissolved inorganic carbon (DIC), calculated pCO2 from DIC (pCO2_DIC) and TA (pCO2_TA), and stable isotope composition of DIC (δ13C-DIC).
- Sampling cadence: monthly at most sites, with some intensive monitoring during rainfall events.
- Data object: a single CSV (flux_and_13C_data) with 19 columns; site details are provided in Table 1.

## Study area and site information
- Houzhai catchment: ~73.4 km², Guizhou Province, China; humid subtropical monsoon climate; ~1140 mm annual precipitation; ~20.1°C average temperature.
- Geology: Middle Triassic limestones and dolomite.
- Monitoring sites include streams, springs, sinkholes, and standing water bodies (reservoirs/ponds); Table 1 lists site IDs, coordinates (latitude/longitude), and site types (e.g., Spring, Sinkhole, Stream, Reservoir).

## Sampling and analytical methods
- CO2 flux: measured via floating chamber (volume 0.0028 m³) over 4 minutes, with three repeats; F_CO2 calculated from CO2 accumulation rate using a standard equation.
- Flow velocity: depth-averaged mean velocity (ū) measured with an impeller flow meter; depth-based averaging scheme depends on water depth.
- Water chemistry: at deployment, measure temperature (T) and pH in situ; collect water samples within 15 minutes to determine [DIC], δ13C-DIC, and TA (headspace method for DIC; titration for TA). pCO2 estimated from DIC via pH and temperature (pCO2_DIC) and from TA (pCO2_TA).
- Quality control: calibration with three isotopically distinct DIC standards; standard every 10 samples to correct instrument drift; methods align with Waldron et al. 2014 and Zhang et al. 2017 references.

## Data structure and content
- File: flux_and_13C_data.csv with 19 columns:
  - Sequence, ID, Type, Date, Time
  - F-CO2_, F_sd (mean CO2 flux and standard deviation from 3 repeats)
  - TA, T, pH, EC, DO, Water_depth, Flow_velocity
  - DIC, DIC_TA, pCO2_DIC, pCO2_TA, d13C-DIC
- Units:
  - F-CO2 and related flux parameters: μmol m⁻² s⁻¹
  - TA, DIC: mmol L⁻¹
  - T: °C; pH: unitless; EC: μS cm⁻¹; DO: mg L⁻¹
  - Water_depth and Flow_velocity: m and m s⁻¹
  - d13C-DIC: ‰ (per mil)
- pCO2 values are derived quantities (from DIC and TA data) as described.

## Usage and context
- Enables analysis of CO2 efflux from karst-influenced river systems, DIC dynamics, and isotope-based source and process interpretation.
- Suitable for creating self-serve data products (dashboards, charts) and integrating with broader hydrological data.
- Supports comparative analysis across site types (springs, sinkholes, streams, reservoirs) and temporal variability (monthly vs. rainfall-driven events).

## Data quality and references
- Explicit QC procedures for CO2 flux and DIC/δ13C measurements; instrument drift corrections and calibration standards documented.
- References: Waldron et al. 2014 (DIC isotope measurement accuracy) and Zhang et al. 2017 (contextual hydrological insights in karst catchments).

## Table 1 site metadata (sample)
- Provides site IDs with precise latitude and longitude and site type (e.g., Spring, Sinkhole, Stream, Reservoir), enabling spatial mapping and site-based analyses.