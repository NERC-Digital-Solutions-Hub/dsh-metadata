# Bowl tipping bucket rain gauge

## Overview
- Tipping bucket rain gauge (0.2 mm resolution) located in the bowl study area at Tyn-ybryn, originally RG3.
- Installed 6 April 2005; gauge is above ground level.
- Location and purpose: bowl study site with ongoing rain measurements.

## Data quality notes and issues
- 02/06/05: Data suspected because sheep could access gauge; small tag bitten; protective trench installed.
- 06/12/05: Gauge was blocked and subsequently unblocked; readings may be affected.
- 25/01/06: Gauge rebalanced using spirit level on base plate.
- 29/06/06: Gauge required a new cable.
- 04/07/06: 0925–0950 GMT tips ignored; wiring in tiny tag noted.
- 05/07/06: Tipping buckets calibrated; ignore tips between 13:30–14:30.
- 14/07/06: Rain gauge download checked; functioning after re-installation.
- 03/10/06: Gauge had come off securing bolt and became unbalanced; minor time discrepancy corrected.
- Feb 2007: February 07 data deemed dodgy due to snow and wind affecting readings.
- 30/04/07: Battery, seal, and desiccant replaced on Tinytag data logger.
- 19/02/08: Base pedestal collapsed; wooden stand installed; potential frozen readings mid-February.
- 08/05/08: Base erosion worsened; wooden stand in place; ignore tips temporarily.
- 12/06/08: Tips around 1200 GMT ignored during rebalancing.
- 21/08/08: Calibration check prompted ignoring tips ~1503–1518 GMT (about 292 tips).
- 31/10/08: Time stamp issue; adjusted to follow on after previous download.
- 07/01/09: Download from bowl RG; tipping bucket data found frozen.
- 02/04/09: Time stamp issues likely due to GMT/BST changes; resolved in analysed dataset.

## Maintenance, calibration, and instrumentation
- Physical protections and adjustments: trenching to protect from sheep; wooden stand installed to replace eroding pedestal.
- Electrical and sensor upkeep: new cable installation; battery, seal, and desiccant changes; rebalancing and calibration.
- Timekeeping and data integrity: multiple time stamp corrections; notes on GMT/BST transitions; calibration periods where tips are ignored to preserve data quality.
- Data logger notes: Tinytag battery/seal/desiccant maintenance; occasional freezing of data at extreme conditions.

## Timestamp, time zone, and data integrity considerations
- Recurrent time stamp issues and DST transitions (GMT/BST) affecting record times.
- Instances of data being ignored or treated differently during calibration or maintenance windows.
- Some periods flagged as unreliable (e.g., heavy snow, calibration intervals) and require careful treatment in analyses.

## Data availability and sharing considerations
- The log provides essential provenance for the dataset, including maintenance events, data quality flags, and timestamps.
- Users should rely on explicit notes about when data were ignored or treated as unreliable and when calibrations occurred.
- Metadata should include instrument health events, calibration timestamps, and any time zone adjustments to ensure reproducibility.

## Recommendations for data governance and stewardship
- Formalize metadata to capture instrument ID, location, installation date, and any physical protections.
- Attach data quality flags to periods affected by maintenance, calibration, or environmental interference (e.g., calibration windows, blocked measurements, DST changes).
- Maintain a clear audit trail of all maintenance actions, replacements, and rebalancing events with timestamps.
- Implement standardized handling of time stamps across DST transitions and ensure datasets align with a single, well-documented time reference.
- Document known issues and their impact on data (e.g., sheep interference, erosion, freezing, cal/ignore periods) to inform users and prevent misinterpretation.
- Consider storing this as structured metadata (instrument metadata, event log, quality control log) alongside the primary rainfall measurements to support discoverability and usability.