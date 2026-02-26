# Tyn y Fron: Notes from field visits for tensiometers and OLF

## Overview
- Longitudinal field log (2005–2009) detailing field instrumentation and activities for tensiometers and overland flow (OLF) traps.
- Documents sensor deployments, maintenance, data collection, and data issues that impact GIS-ready spatial and temporal data products.

## Sensor network and data streams
- Plots and subplots:
  - Plot 1, Plot 2, Plot 3 (with subplots 3.1, 3.2, 3.3; control vs treatment context).
- Sensor types and depths:
  - Tensiometers at 10 cm, 30 cm, and 50 cm depths.
  - OLF (overland flow) traps with tipping buckets.
  - Delta-T loggers and Tinytags for tipping buckets.
  - Pumps, reed switches, and associated cabling.
- Data streams and logging:
  - Regular data downloads andDegassed/tensio maintenance.
  - Frequent recalibration, battery changes, and occasional downtimes.
  - Data quality notes include “ignore tips” during certain periods (e.g., sampling, maintenance, or sensor checks).

## Data collection, formats, and time coverage
- Field notes span 2005–2009, with detailed daily/periodic entries.
- Data integrity is variably affected by field events (storms, heavy rainfall, floods), equipment malfunctions, and maintenance activities.
- Occasional data gaps due to battery failures, pump issues, or logger software resets.

## Data quality issues and field events
- Weather and hydrological events:
  - Storms and heavy rain causing electrical surges, floods, and overland flow impacts on traps.
- Equipment and sensor reliability problems:
  - Batteries die or fail, logs stop, and loggers reset.
  - Cables and tensiometers damaged by animals (sheep, voles, fox/badger interactions) and physical disturbance.
  - Reed switches misbehaving; tinytags failing or needing replacement/calibration.
  - Pits/trenches can flood or overflow; pumps may fail or require recalibration.
- Data corrections and notes:
  - Frequent mentions of “ignore tips” during maintenance or known issues.
  - Reinstallations, recalibrations, and sensor replacements to restore functionality.

## Data management implications for GIS
- Fragmented data custody:
  - Data and logs appear to be stored in multiple formats/systems over time.
- Metadata needs:
  - Consistent naming for plots and depths (e.g., 3.1, 3.2, 3.3; 10 cm, 30 cm, 50 cm).
  - Sensor status flags (degassed, recalibrated, battery status, faults).
  - Event annotations (storm days, maintenance, calibration events, pump failures).
  - Time zone context (BST/GMT) and exact timestamps for synchronization.
- Quality control:
  - Flag data with known issues and gaps.
  - Capture maintenance actions and their timestamps to aid data interpretation.
- GIS-ready outputs:
  - Spatial layer of sensor locations with depth and sensor type attributes.
  - Time-series data linked to sensor IDs, with quality flags and event overlays (storms, maintenance).

## Maintenance, troubleshooting, and field operations
- Regular field activities:
  - Degassing tensiometers, reinstallation after disturbances, and battery changes.
  - Cleaning gutters, repairing lawn edging, trench adjustments, and sump maintenance.
  - Calibration and recalibration of tipping buckets and Delta-T loggers.
- Troubleshooting patterns:
  - Replacing faulty tensiometers, reed switches, Tinytags, and loggers.
  - Addressing data gaps caused by battery failures or clogged gutters.
  - Responding to animal interference and weather-induced data anomalies.

## Notable observations and implications
- Storms and heavy rainfall significantly affect data quality and trap performance.
- Animal activity frequently disrupts hardware, necessitating repeated field interventions.
- Data continuity relies on timely maintenance, calibration, and cross-checks between multiple logging systems (Delta-T, Tinytag, Tinytag, tipping buckets).

## Recommendations for GIS-focused data products
- Build a robust metadata schema:
  - Sensor IDs, depth, plot, location, type, status, calibration dates, battery status, and fault notes.
- Create data quality tiers:
  - OK, suspect, missing, and corrected, with logs of corrective actions.
- Develop spatial layers:
  - Sensor locations with depth-coded symbols; status-colored by sensor health.
  - Overlays for events (storm days, pump failures) and maintenance activities.
- Link time-series to events:
  - Attach event annotations to corresponding time windows to aid interpretation of spikes, gaps, or anomalies.
- Establish data governance:
  - Centralized storage with versioning, backups, and consistent naming conventions across plots and sensors.
- Plan for data standardization:
  - Uniform units, timestamp formats, and time-zone handling to ensure GIS temporal analyses are reliable.