# Rhos1: Notes from field visits for tensiometers and OLF

## Overview
- Field notes from 2005–2009 documenting operation, maintenance, and data-related decisions for tensiometers and Overland Flow (OLF) traps at the Rhos1 site.
- Covers equipment status, calibration, data downloads, quality control actions, and end-user data considerations.
- Focuses on enabling reliable data collection across plots with multiple measurement devices (tensiometers, tipping buckets, tinytags, loggers).

## Data Collection & Instrumentation
- Instruments and systems
  - Tensiometers at multiple depths (e.g., plots 1.1, 1.2, 1.3; 10 cm, 30 cm, 50 cm references).
  - Overland Flow (OLF) traps with tipping buckets and associated tubes.
  - Data logging hardware: Delta-T loggers, tinytags, and Delta-T boxes; external power considerations.
  - Supporting components: batteries, desiccants, reed switches, jumpers, gutters, covers, and WD-40-treated components.
- Data types recorded
  - Sensor readings from tensiometers, tipping bucket tips (including recalibration data), and pump status.
  - Event logs noting data download times, degassing, and system adjustments.
  - Observational notes on weather, storm events, and potential data anomalies.
- Data collection practices
  - Regular field visits, on-site maintenance, and subsequent data downloads.
  - Documentation of calibration activities and any anomalies observed during logging.

## Data Quality, Cleaning & Anomalies
- Common data integrity challenges
  - Storms or electrical disturbances causing non-sensible sensor readings; readings later re-evaluated after logger interventions.
  - Patchy or variable data due to weather, moisture ingress, or desiccant depletion.
  - Hardware failures: pump jams, reed switch faults, float switch stickage, miscalibrations, and battery or power issues.
  - Physical blockages and environmental factors: clogged gutters, worms, leaves, vole damage, and water-filled pits affecting data collection.
- Data cleaning and validity decisions
  - Data flagged as invalid or to be ignored during specific time windows (e.g., certain tips to disregard; times with calibration or maintenance ongoing).
  - Recalibration and recalibration sheets referenced to ensure tip counts reflect actual events.
  - Notes indicating when data should be treated as unreliable or excluded from analysis (e.g., data from a storm event or during maintenance).
- Data signals and calibration patterns
  - Tipping bucket calibration sessions recorded with explicit tip counts and sequences (e.g., 20 (5,5,5,5)).
  - Recurrent checks that calibration and sensor alignment were correct, sometimes requiring multiple adjustments across plots.

## Data Management & Maintenance Activities
- Maintenance actions aimed at data reliability
  - Regular degassing, cleaning, and reinstallation of tensiometers.
  - Replacement of batteries, desiccants, and worn components; repairs to pumps and wiring.
  - Recalibration of tipping buckets and sensors; replacement of reed switches and float switches when necessary.
  - Physical site work: trench widening, sealing, gutter maintenance, and protective box/cover adjustments to prevent damage.
- Data governance practices observed
  - Frequent data downloads and contemporaneous note-keeping to document data quality and equipment status.
  - Use of calibration sheets and explicit logs to track data integrity and calibration states.
  - Clear annotations about when to ignore or treat data with caution, enabling downstream users to filter data accordingly.
- End-user readiness and outputs
  - Documentation supports data users by signaling when data are trustworthy, when calibrations occurred, and when data should be excluded.
  - Mention of calibration sheets and detailed equipment logs as ancillary data products to accompany raw measurements.

## Data Structure & Outputs
- Data elements captured in the notes
  - Tensiometer readings and degassing actions; depths and plot locations (e.g., M1.1, M1.2, M1.3).
  - OLF trap status, pump conditions, and tip counts from tipping buckets.
  - Tinytag logging events and battery/desiccant changes.
  - Calibration events with numerical tip sequences for each bucket.
- Spatial and device metadata
  - Locations and identifiers for tensiometers (e.g., M1.1, M1.2, M1.3) and depths (10 cm, 30 cm, 50 cm).
  - End-of-file notes listing sensor IDs and their corresponding depths, indicating where data originate.

## Notable Observations / Patterns
- Data quality is tightly coupled to hardware reliability and environmental conditions.
  - Storms and electrical disturbances frequently trigger unreliable readings, necessitating data cleaning or exclusion.
  - Recurrent hardware issues (reed switches, float switches, pumps, batteries) require iterative maintenance and recalibration.
- Data usability improves after systematic maintenance
  - Degassing, recalibration, battery changes, and proper wiring alignment consistently followed by improved data integrity.
  - Regular documentation of issues (with timestamps) supports transparent data curation and traceability.
- Data management practices are explicit
  - Explicit notes about when to ignore data, plus calibration sheets and tip sequence records, demonstrate a structured approach to data cleaning and provenance.

## End Matter (Metadata)
- Final notes include a mapping of tensiometer identifiers to depths and locations:
  - Example: M1.1 at 10 cm (235), 30 cm (243), 50 cm (254)
- This metadata supports locating and aligning data streams from multiple sensors across plots.