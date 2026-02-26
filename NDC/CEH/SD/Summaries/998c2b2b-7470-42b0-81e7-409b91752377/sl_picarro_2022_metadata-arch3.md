# High-resolution ammonia concentration data from Queensberry experimental site in Sri Lanka (2022)

## Overview
- Purpose: to study the effects of high atmospheric ammonia (NH3) on forest vegetation, bryophytes, lichens, and soil.
- Location: Queensberry Estate, central Sri Lanka (6.9693°, 80.5911°, altitude 1645 m), tropical sub-montane forest.
- Timeframe: data collected from 24 March 2022 to 3 April 2022.
- Experimental aim: optimize NH3 release rates to achieve target enhancement concentrations and understand lateral and vertical NH3 plume movement within the canopy.

## Experimental Setup and Release System
- NH3 enhancement system is activated only under specific wind conditions so that release aligns with monitoring quadrats (wind direction thresholds 5–75° and 185–255° at certain speeds 0.3–10 m/s).
- Release hardware: three parallel 20 m long tubes (110 mm OD) at ground-normal heights 0.5, 1.35, and 2.2 m.
- NH3 delivery: 6.35 mm diameter stainless steel pipe feeds NH3 from a cylinder through a mass flow controller (MFC) and solenoid valve into a central fan manifold, enabling controlled dilution and release via holes along the tubes.
- Control: solenoid valve opens only when wind conditions meet targets.

## Sampling, Measurement and Analyzers
- Measurement downwind: Picarro G2123 NH3/H2O analyser located ~10 m downwind of the release system, inside a climate-controlled enclosure.
- Sampling heights: four levels—0.5, 1, 1.5, and 2.5 m above ground.
- Sampling protocol: 2-minute sampling at each height via a valve manifold controlled by LabVIEW; four 5.5 m PTFE inlet lines used.
- System conditioning: inlet lines heated to ~40°C (±3°C) to minimize adsorption/desorption delays; continuous purge between sampling phases (7 to 12 standard L/min).
- Data frequency: NH3 concentrations recorded at 10 Hz and averaged to 0.016 Hz; data timestamped in Sri Lanka Standard Time (SLST).
- Additional considerations: some lag expected due to NH3 adsorption/desorption on inlet surfaces; heating may volatilize ammonium nitrate (NH4NO3) aerosols, but background levels expected to be smooth.

## Data Quality Control and Processing
- QC approach: visual inspection to remove obvious instrument Malfunction, datalogger issues, and power-cut artefacts.
- Gaps due to valve switching interpolated linearly.

## Data Structure and Accessibility
- Dataset size: 14,094 measurements across 6 parameters.
- File format: CSV with columns including:
  - Timestamp (date/time)
  - NH3_status (release status)
  - NH3_flow (source flow rate)
  - Wind_speed (downwind wind speed)
  - Wind_direction (downwind wind direction)
  - NH3_conc (NH3 concentration downwind)
  - Inlet_height (sampling height)
- Instrument/source metadata linked to each parameter (e.g., NH3_status, NH3_flow, NH3_conc, Wind_speed, Wind_direction, Inlet_height).

## Limitations and Uncertainties
- Potential lag in concentration measurements due to NH3 adsorption/desorption in inlet plumbing.
- Possible volatilisation of NH4NO3 aerosols from heating, though the background is expected to remain relatively constant.
- Some data gaps remain despite interpolation, and precise cross-instrument timing may introduce minor alignment issues.

## Funding
- Funded by the UKRI GCRF South Asian Nitrogen Hub.