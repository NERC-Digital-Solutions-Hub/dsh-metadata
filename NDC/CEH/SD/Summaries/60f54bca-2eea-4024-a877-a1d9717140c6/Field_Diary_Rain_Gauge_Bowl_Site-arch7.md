# Bowl tipping bucket rain gauge

- 0.2 mm tipping bucket rain gauge RG3 located in the bowl study site at Tyn-ybryn; installed 6 April 2005; gauge is above ground level. 

## Overview and purpose
- Provides time-stamped rainfall measurements for the bowl study area.
- Data are used for spatial and temporal rainfall analyses within GIS contexts and are linked to calibration and maintenance events.

## Data provenance and time context
- Records span from 2005 to 2009, with various maintenance notes and data quality remarks.
- Time stamps were recorded in GMT; several notes indicate adjustments when BST/GMT changes occurred and potential time stamp issues.
- Some readings are flagged as suspect or require ignoring during specific intervals due to calibration or technical issues.

## Data quality, issues, and caveats
- Data quality concerns include:
  - Suspect readings when sheep could access the gauge (sheep attacked the device; protective trench dug).
  - Gauge blocks or becomes unblocked; wiring and tiny tag issues.
  - Periods where tips should be ignored (e.g., 04/07/06 between 13:30–14:30).
  - Time stamp issues and overlaps between downloads; occasional adjustments to align with actual time.
  - Snow events potentially causing inaccurate readings (e.g., Feb 2007 snow not recorded properly due to wind).
  - Sensor misalignment or physical instability (e.g., base erosion, squint positioning, rebalancing required).
- Data readers should treat certain intervals as unreliable or require correction flags, and consider calibrations or maintenance events when interpreting rainfall totals.

## Maintenance, calibration, and hardware changes
- 02/06/2005: Sheep protection measures implemented due to sheep damage.
- 06/12/2005: Gauge blocked and later unblocked; mitigation steps noted.
- 25/01/2006: Bowl rain gauge rebalanced using a spirit level.
- 29/06/2006: Rain gauge wiring issues with a new cable noted.
- 04/07/2006: Ignore tips between 13:30 and 14:30 during calibration; tiny tag wiring adjustments.
- 14/07/2006: Download checked; gauge functioning after re-installation.
- 03/10/2006: Gauge had become unbalanced due to a securing bolt issue; time correction needed.
- 07/01/2009: Data download indicated gauge frozen.
- 02/04/2009: Time stamp issues accounted for due to GMT to BST transition.
- 08/05/2008: Base erosion addressed; wooden stand installed to stabilize and level the gauge.
- 12/06/2008 and following: Calibration checks and rebalancing activities noted.
- 19/02/2008: Pedestal collapse previously noted; wooden supports or stands implemented to prevent recurrence.

## GIS-related considerations and recommendations
- Include a data quality flag field to identify periods with suspect data, ignored tips, or timestamp corrections.
- Link rainfall readings to maintenance/calibration events to aid interpretation of anomalies.
- Document time zone handling (GMT/BST) and any post-download time adjustments to ensure correct temporal alignment.
- Capture spatial metadata of the above-ground gauge location for accurate mapping and integration with other spatial datasets.
- When visualising time-series in maps or dashboards, provide filters to exclude or annotate periods affected by maintenance, environmental interference (e.g., sheep access, weather), or noted data quality issues.

## Summary for use in GIS products
- The Bowl tipping bucket rain gauge provides valuable long-term rainfall data for the bowl study site but contains multiple documented quality issues and calibrations.
- For robust GIS analyses, treat several intervals as unreliable or flagged, incorporate maintenance events as metadata, and ensure time stamps are normalized across GMT/BST transitions.
- With proper quality controls and annotations, the dataset supports spatial-temporal rainfall visualization and analysis in map-based formats.