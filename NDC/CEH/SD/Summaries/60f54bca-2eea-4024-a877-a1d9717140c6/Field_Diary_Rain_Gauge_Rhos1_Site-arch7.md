# Rhos 1 Rain gauge read me document

## Overview
- A maintenance and data-quality log for the Rhos1 rain gauge spanning 2006–2008.
- Documents repeated actions to unblock and realign the gauge, timing discrepancies with the logger, and subsequent data adjustments.
- Notes the practical challenges of field instrumentation, including calibration checks, wiring issues, and environmental impacts (e.g., snow).

## Key Events and Maintenance Timeline
- 03/10/06: Rain gauge blocked; 21mm collected from funnel. Aperture differences mean readings may be incorrect. Last sample time (laptop) 17:19 GMT vs recorded 16:10 GMT; logger was ~69 minutes behind. Gauge removed to Bangor because unblocking in the field wasn’t possible; logger reset.
- 12/10/06: Gauge rebalanced using spirit level; reinstalled around ~09:20.
- Feb 07: Significant snowfall; data deemed dodgy due to wind-blown snow not being captured properly.
- 01/05/07: Battery, seal, and desiccant changed on Tinytag (data logger).
- 01/04/08: Tinytag disconnected from reed switch during reinstallation; wire came away from connector.
- 02/04/08: Cable connecting reed switch to Tinytag replaced; system reported as working again.
- 21/08/08: Calibration tip window (~14:25–14:44 GMT) disregarded due to calibration check being performed at that time.
- 03/11/08: The previous month’s data deemed 5 minutes fast; adjustments made in Excel.

## Data Quality, Provenance, and Timestamp Issues
- Sensor blockage and aperture differences affect calibration and comparability of readings.
- Time synchronization issues: logger lagged behind laptop time by ~69 minutes on one occasion, necessitating a reset.
- Environmental factors (snow, wind) can cause data gaps or inaccuracies.
- Calibration events and checks sometimes conflict with logged data (e.g., calibration window ignored).
- Data adjustments performed post-collection (e.g., 5-minute offset corrections) and recorded in an Excel document.

## Data Processing and Adjustments
- Data corrections were applied to align timestamps with actual events, and some months’ data were adjusted based on calibration checks and quality assessments.
- Repeated rebalancing and component replacements (Tinytag, battery, seals, desiccant, wiring) indicate periods of sensor maintenance that may affect data continuity and comparability.

## Impact on GIS Data Products
- Metadata needs: detailed sensor/device IDs, location, data logger type (Tinytag), calibration history, and time-offset records.
- Data integrity flags: indicate periods of blockage, calibration events, and known time lags (e.g., the 69-minute delay).
- Provenance trail: maintenance actions, dates, and rationale to support traceability and reproducibility of map-based analyses.
- Temporal alignment: ensure time series are aligned across datasets when integrating with other spatial datasets (e.g., rainfall maps, hydrological models).
- Data cleaning requirements: document corrections (e.g., 5-minute fast adjustment) and maintain an auditable Excel/metadata record.

## Recommendations for GIS Metadata and QA (Implications for Data Products)
- Capture sensor metadata: device ID (Rhos1), placement, aperture details, and mounting configuration.
- Record calibration history: last calibration times, checks performed, and any flagged anomalies.
- Log timing information: baseline time, observed lag, and any offsets applied to align with reference time.
- Maintain data quality flags: indicate gaps due to blockage, snow, or wiring issues; note data points adjusted post-hoc.
- Provide a maintained data provenance document or metadata file linking maintenance events to data quality changes.
- Establish standard procedures for handling environmental disruptions and for documenting when data should be flagged or excluded from analyses.