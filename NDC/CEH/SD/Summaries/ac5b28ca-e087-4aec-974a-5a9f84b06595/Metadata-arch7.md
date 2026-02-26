# Sediment fluxes, discharge and acoustic Doppler current profiler (aDcp) calibrations for the Mekong Delta, Vietnam between 2005 and 2015

## Overview
- Routine flood and water level monitoring on the Mekong Delta in Vietnam using Acoustic Doppler Current Profiler (ADCP) data at four sites.
- Data span 2005–2015; aim is to back out sediment fluxes by calibrating acoustic backscatter to suspended sediment concentrations (SSCs).
- Four measurement sites with precise geographic coordinates provided.

## Sites and equipment
- Tan Chau, Chau Doc, Can Tho, and My Thaun ADCP measurement sites.
- ADCP units: Teledyne RDI Workhorse 600 kHz and one RiverRay unit.
- Site coordinates:
  - Tan Chau (10.822642, 105.227879)
  - Chau Doc (10.708268, 105.134606)
  - Can Tho (10.088109, 105.736458)
  - My Thaun (10.272038, 105.900920)

## Analytical methods
- Calibrate acoustic backscatter (dB) to observed SSCs using field SSC measurements.
- SSC samples collected with a 3 L Van Dorn sampler across depths, filtered, dried, and used to derive concentrations.
- Develop instrument-specific power-law calibration curves relating backscatter to SSC.
- Process raw ADCP data in WinRiver II, export ASCII, then use Velocity Mapping Toolbox (Matlab) to produce flux estimates.
- Convert ADCP-derived fluxes to suspended sediment fluxes via calibration curves.
- Generate daily sediment fluxes by applying site-specific flux-discharge relationships (ratings curves) to daily discharge data from the Vietnamese hydrological agency.

## Data processing workflow
- Move from raw ADCP files to ASCII, then to calibrated flux estimates with Matlab/VMT.
- Daily fluxes produced by extrapolating point fluxes using discharge records.

## Quality Assurance
- Uses established acoustic inversion techniques with robust published support.
- Industry-standard software (WinRiver II, VMT) and consistent data collection protocols.
- Flux estimates checked against upstream estimates for consistency (Darby et al., 2016).

## Data structure and files
- Data delivered as CSV files, one per site:
  - Flux files (per site): daily sediment fluxes (kg/s) over years 2005–2012 (as columns) with Date column.
  - Ratings files: discharge (m3/s), section-averaged SSC (mg/L), sediment flux (kg/s) per sample.
  - ADCPcalibrations.csv: instrument-specific calibration data linking ABS (dB) to SSC (mg/L).
- Column details:
  - ADCPcalibration file:
    - ABS (dB): Acoustic backscatter values
    - SSC (mg/L): Observed SSC corresponding to ABS
    - Instrument identified by serial numbers (e.g., INST1258); some units owned by different institutions.
  - Flux files:
    - Date: calendar day/month (year ignored)
    - Years 2005–2012: sediment fluxes (kg/s) for each year; NaN used for missing data (e.g., non-leap-year Feb 29).
  - Ratings files:
    - Month, Day, Year: sample date
    - Discharge (m3/s): derived from ADCP transects
    - Section Averaged SSC (mg/L): cross-section average SSC
    - Sediment Flux (kg/s): cross-section sediment flux
- Instrument basis and data provenance
  - Instrument ownership and identifiers, e.g., INST1258; some units owned by the Vietnamese hydrological agency.

## Data provenance and references
- References supporting methods and calibration approach:
  - Darby et al. (2016) Nature: Fluvial sediment supply to a mega-delta reduced by shifting tropical-cyclone activity.
  - Hackney et al. (2018) Earth Surface Processes and Landforms: Influence of flow variations on morphodynamics of deltaic units.
- Data collection and processing align with established hydrological and acoustic-data practices.

## How this supports GIS use
- Provides four spatially referenced measurement sites with calibrated sediment flux data across a multi-year period.
- Data can be mapped to visualize spatial patterns of sediment transport across the Mekong Delta.
- Daily flux time series linked to discharge enable temporal analyses and integration with other hydrological/geospatial layers for policy, planning, or public-facing visualization.