# The data in this folder is data downloaded from the Delta-t logger in the bowl study area.

## Overview
- Long-running data collection from Delta-t loggers in the bowl study area, covering multiple tensiometers at various depths and transect points.
- Data span from 2004 through 2009, with ongoing maintenance, calibration, and data quality issues addressed across years.

## Data and Equipment
- Instruments:
  - Delta-t loggers and DL6 loggers.
  - Tensiometers at 10 cm, 30 cm, and 50 cm depths across multiple cages/transects.
  - Vents and tubes (degassed vs. vent-exposed), bleed tubes, and protective housings.
- Locations/IDs:
  - Multiple transect points and cages (e.g., T1.x, T2.x; bowl and transect designations).
- Data handling:
  - Data downloads from Delta-t loggers; occasional software calibration and wiring changes to ensure readable outputs (e.g., wiring reversal to interpret negative readings correctly).
- Installation and physical integrity:
  - Periodic issues with cables, tubing, and vent exposure.
  - Animal interference: sheep damage, chewed tubes, mole activity, earthworm burrowing affecting vent burial.
  - Reinstallations and replacements when components failed or were damaged.
- Calibration/offsets:
  - 15-degree installation angle introduced depth/pressure measurement offsets.
  - Offsets applied and later adjusted (e.g., initial -4.8 cm offset; offset adjustments and eventual removal back to 0 cm in late 2008).

## Data Collection and Maintenance Activities
- Regular degassing of tensiometers; checks of vents; grass cutting and cage maintenance.
- Frequent reinstallation and re-securing of tensiometers after damage (sheep, chewing, or movement).
- DL6 logger-related adjustments and synchronization with laptop clocks; occasional logger reset and program tweaks (warm-up times, offset application).
- Recalibration and relocation:
  - August–October 2008: recalibration and relocation of tensiometers; installation angle adjustments and angle-offset consideration.
  - 16/06/08–02/09/08: changes to DL6 setup and offset calculations announced; subsequent data corrections planned.
- Data management steps:
  - Noted data missing at start due to missed downloads and logger auto-wrap issues.
  - 03/11/08: data download problem causing data corruption for the top cage.
  - 25/11/08: offset correction changes (offset back to 0) across loggers.
  - 24/07/08–01/07/09: ongoing grass management and sensor maintenance to maintain data continuity.
- End-of-period issue:
  - 30/07/09: bottom tensiometers could not respond to the logger despite battery changes.

## Data Quality and Issues
- Data gaps and irregularities:
  - Early data loss from logger wrap during the start of the sampling period.
  - Occasional data “funny” behavior and offset needs due to installation geometry and updated offsets.
  - 03/11/08: corrupted data download from the top cage; some data unavailable.
- Physical and environmental challenges:
  - Vent burial by earthworms; tubing and vent exposure issues.
  - Sheep and mole activity causing tubes/tubes removal and cage damage.
  - Logging timing discrepancies (loggers running ~3 minutes ahead of laptop clock; later corrections).
- Instrument wear and failure:
  - Snapped or chewed tubes/tubing, chewed wires, and loose tensiometers requiring replacement or reinstallation.
  - Some tensiometers eventually ceased responding (bottom set in July 2009).

## Data Transformations and Metadata
- Installation and measurement offsets:
  - Initial offset introduced to account for angled installation (-4.8 cm, later adjusted back to 0 cm in late 2008).
  - 16/10/08: -4.8 cm offset documented and applied to each tensio in the spreadsheet; 24/10/08 update events noted.
  - 25/11/08: offset reset to 0 cm on both loggers.
- Calibration/logging adjustments:
  - Rewired Delta-T box in May 2007 to ensure negative pore water pressure readings align correctly with signal polarity.
  - 06/03/08: program changes for DL6 warm-up times (1 sec to 10 sec) and data structure alignment.
- Data alignment:
  - Adjustments to account for installation angle and porous cup depth (offsets embedded in logger program for future downloads).
  - Periodic notes to reflect differences in measured depth and orientation for subsequent data processing.

## Data Access, Storage, and Governance
- Data is organized by folder with detailed event logs of maintenance, repairs, and sensor changes.
- Documentation includes serial numbers, depths, transect points, and events affecting data integrity.
- Regular data downloads and metadata updates are essential to maintain traceability and reproducibility.

## Implications for Data Leaders
- This dataset demonstrates the importance of robust metadata and governance to manage long-term environmental data with frequent field interventions.
- Key governance needs:
  - Comprehensive event logging for maintenance, animal interference, and equipment changes.
  - Clear documentation of offsets, calibration steps, and installation geometry to support reproducible analyses.
  - Consistent data quality checks and transparent handling of missing or corrupted data.
  - Strategies to reduce data loss and physical vulnerabilities (e.g., improved protective measures, more durable connections).

## Recommendations / Next Steps
- Consolidate metadata:
  - Preserve all offsets, installation angles, depths, serial numbers, and dates in a centralized metadata schema.
  - Embed offsets and calibration changes into a versioned data processing workflow to ensure traceability.
- Data quality improvements:
  - Develop a data quality report highlighting gaps, corruptions, and anomalies with root-cause analyses.
  - Implement automated alerts for sensor failures, unusual drift, or missing periods.
- Field operations enhancements:
  - Reinforce protection for tensiometers (tubes, vents) to reduce animal interference.
  - Standardize installation geometry to minimize needing large offset corrections.
- Data processing:
  - Reconcile top vs. bottom cage data with updated offsets; propagate corrections into final datasets.
  - Ensure consistency between logger outputs and spreadsheet representations; verify time synchronization across devices.
- Planning for future data collection:
  - Establish maintenance schedules, risk mitigation plans for weather/animals, and fallback procedures for data logger failures.
  - Consider additional redundancy or remote diagnostics to minimize data loss during field disturbances.