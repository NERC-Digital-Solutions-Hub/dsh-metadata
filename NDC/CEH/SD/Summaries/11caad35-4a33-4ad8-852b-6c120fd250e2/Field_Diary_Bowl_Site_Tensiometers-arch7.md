# The data in this folder is data downloaded from the Delta-t logger in the bowl study area.

## Overview
- Field log of tensiometer data collected via Delta-t loggers in the bowl study area, covering multiple years (2004–2009).
- Includes sensor readings at multiple depths (e.g., 10 cm, 30 cm, 50 cm) across several transects and cages.
- Records ongoing maintenance, calibration, data quality checks, and environmental disturbances affecting measurements.

## Data Content
- Tensiometer identifiers (e.g., T1.2.30, T2.1.10, T2.4.50) with associated depths (10 cm, 30 cm, 50 cm).
- Locations referenced by transect and cage (e.g., transect points 1.2, 2.3; cages in Bowl 1.1, Bowl 2.2, etc.).
- References to Delta-t DL6 loggers and program adjustments (e.g., warm-up times, offsets).
- Frequent notes on degassing status, vent exposure, and recalibration events.
- Observations of external disturbances (sheep, moles, grass cutting) and resulting sensor issues.
- Reinstallations, replacements, and wiring/tube integrity checks documented over time.

## Sensor and Location Details
- Sensor depths and positions vary by transect and cage (e.g., 10 cm, 30 cm, 50 cm in multiple cages).
- Spatial arrangement includes bowl-based transects and cages, with notes on relocation or removal of tensiometers.
- Wiring and data logger configurations adjusted (e.g., changes to polarity, offset calculations, installation angles).

## Data Quality, Issues, and Corrections
- Data gaps and missings:
  - Missing data due to logger auto-wrap and missed downloads (e.g., 11–15 April 2006).
  - Data download corruption (03/11/08) leading to unavailable data for that period.
- Instrument/installation issues:
  - Vents exposed, buried vents, and degassing requirements.
  - Tensiometer damage from sheep, chewing of tubing, and gear displacements.
  - Cages and tubing integrity problems requiring reinstallation or replacement.
- Calibration and offset adjustments:
  - Initial offset handling for vertically installed vs. angled installations (-4.8 cm adjustment applied per notes on 02/09/08 and related entries).
  - Offsets changed to 0 cm on 25/11/2008.
  - Programmatic adjustments to loggers to account for installation angle and measurement reference differences.
  - Wiring polarity changes to ensure negative readings correspond to negative pore-water pressure values.
- General data quality notes:
  - Temperature/pressure readings intermittently affected by equipment changes and environmental disturbance.
  - Some periods later harmonized with offset updates embedded in the logger program to minimize post-download corrections.

## Temporal and Sampling Details
- Time span: at least 2004–2009, with frequent checkpoint events (degassing, vent checks, sensor maintenance, and data downloads).
- Sampling complexity:
  - Multiple depths per sensor, across several transects and cages.
  - Recurrent data logging maintenance (degassing, recalibration, battery checks, and logger resets).

## Implications for GIS
- The dataset provides spatially referenced sensor data (locations, depths, transects) suitable for GIS-based time-series visualization and analysis.
- Data quality flags and correction metadata are essential for accurate spatial-temporal analyses (e.g., handling offsets, sensor repositioning, and data gaps).
- Requires integration of:
  - Sensor metadata (IDs, depths, transect/cage locations).
  - Time-series data with consistent time stamps and applied corrections.
  - Data quality notes (degassing status, vent exposure, disturbances) as attribute fields or separate QA/QC layers.

## Recommendations for GIS Integration
- Create a sensor supersite layer with: sensor ID, depth, transect, cage, location coordinates (derived from transect/cage design), and installation date.
- Attach time-series data and data quality flags to each sensor feature; include metadata on offsets applied (-4.8 cm, later 0 cm) and polarity adjustments.
- Build QA/QC fields capturing data gaps, corruption events, and disturbances (e.g., damage, chewed tubing, grass cutting).
- Develop a workflow to standardize timestamps, apply documented offsets, and flag periods with known data issues before visualization.
- Consider separate layers for events and maintenance (e.g., degassed, vents adjusted, reinstalled) to support historical analytics and reproducibility.