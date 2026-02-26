# High-resolution ammonia concentration data from Queensberry experimental site in Sri Lanka (2022)

## Overview
- Field experiment conducted in 2022 at Queensberry Estate, central Sri Lanka, to investigate effects of elevated atmospheric ammonia on forest vegetation, bryophytes, lichens, and soil.
- Ammonia release is triggered by wind conditions to study plume movement within the canopy.
- Data capture includes NH3 release parameters, environmental conditions, and concentration downwind.

## Data collection and experimental design
- Site: tropical sub-montane forest, coordinates 6.9693° and 80.5911°, altitude 1645 m.
- Release system: three parallel PVC tubes (20 m length, 110 mm OD) with holes along their length; NH3 diluted by a central airflow.
- NH3 supply: 6.35 mm stainless steel line with a mass flow controller and solenoid valve to gate release based on wind direction and speed thresholds (0.3–10 m/s; wind targets 5–75° and 185–255° relative to monitoring quadrats).
- Campaign objective: optimize release rates to achieve target NH3 enhancement concentrations and characterize lateral/vertical plume movement within the canopy.
- Downwind measurement point: Picarro G2123 NH3/H2O analyser located ~10 m downwind on the northeastern sector.

## Measurement system and sampling
- Concentration measurements at four heights: 0.5, 1.0, 1.5, and 2.5 m above ground.
- Sampling system: custom-designed manifold with four 5.5 m PTFE inlets; automated LabVIEW control.
- Sampling cadence: 2 minutes per height; total sampling across heights conducted sequentially.
- Inlet conditioning: heated to ~40°C ±3°C to minimize adsorption/desorption delays; continuous purge flow between sampling phases (7 to 12 standard L/min).
- Data logging: NH3 concentrations recorded at 10 Hz and averaged to 0.016 Hz.
- Data integrity: heating may cause minor volatilisation of NH4NO3 aerosol; background expected to be relatively stable.

## Data structure and content
- Dataset size: 14,094 measurements across 6 parameters.
- Data format: CSV file with detailed metadata columns:
  - Timestamp, Timestamp details (instrument, manufacturer, etc.)
  - NH3_status: status of NH3 release (codes indicating ON/OFF/valve states)
  - NH3_flow: flow rate source (slpm, MFC, etc.)
  - Wind_speed: measurement source (Below-canopy, instruments)
  - Wind_direction: measurement source (Below-canopy, Vaisala, etc.)
  - NH3_conc: NH3 concentration downwind (ppb) with instrument context
  - Inlet_height: height at which NH3 concentration is measured (m) with instrument context
- Metadata fields captured for each parameter include instrument, manufacturer, and description to enable cross-dataset compatibility.

## Quality control and data quality considerations
- Visual checks performed; obvious instrument/logger/power issues removed.
- Gaps from valve switching filled by linear interpolation.
- Acknowledges potential lag between height switching and downwind concentration changes due to system and adsorption/desorption dynamics.
- Background NH3 volatilisation considered; overall expected to yield a smooth NH3 field with a relatively constant background.

## Data availability and usage notes
- Data collected from 24 March 2022 to 3 April 2022 in Sri Lanka Standard Time (SLST).
- Intended to support analyses of NH3 plume behavior, vertical/horizontal dispersion, and the effectiveness of the release control strategy.
- Dataset includes comprehensive instrument and measurement metadata to aid reuse and integration with broader data systems.

## Funding
- Funding provided by the UKRI GCRF South Asian Nitrogen Hub.