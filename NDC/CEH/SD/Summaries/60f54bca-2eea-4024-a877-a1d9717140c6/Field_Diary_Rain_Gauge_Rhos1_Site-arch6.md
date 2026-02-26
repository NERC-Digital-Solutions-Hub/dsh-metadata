# Rhos 1 Rain gauge read me document

## Overview
- Maintenance and data quality log for the Rhos1 rain gauge (2006–2008).
- Documents calibration actions, rebalancing, wiring issues, time/data integrity problems, and subsequent data adjustments.
- Notes that measurement values may be affected by hardware differences (gauge aperture) and by data corrections.

## Data collection setup
- Sensor/logging chain: Tinytag data logger connected to a reed switch and storage gauge (funnel and collection cylinder).
- Time reference: All times recorded in GMT.
- Measurement caveat: Aperture differences between gauges can make rainfall totals inconsistent across readings (e.g., 21 mm noted as not being correct due to aperture mismatch).

## Chronology of maintenance and events
- 03/10/06: Gauge blocked; 21 mm collected from the funnel. Logger behind by ~69 minutes. Reset performed; gauge removed due to unblocking issues in the field.
- 12/10/06: Gauge reinstalled ~09:20 after rebalancing with spirit level on base plate.
- Feb 2007: Rebalanced during significant snow; data considered dodgy as wind-blown snow likely not recorded properly.
- 01/05/07: Battery, seal, and desiccant replaced on Tinytag.
- 01/04/08: Rebalanced; wiring issue where wire came away from the Tinytag connector near the reed switch.
- 02/04/08: Cable between reed switch and Tinytag replaced; system reported as working again.
- 21/08/08: Rebalanced; calibration check conducted; tips between ~14:25–14:44 GMT disregarded during calibration.
- 03/11/08: Rebalanced; noted that last month’s data were deemed 5 minutes fast; adjustments made in the Excel document.

## Data quality and adjustments
- Time drift and synchronization: Initial ~69-minute lag corrected during the 03/10/06 maintenance.
- Data integrity during extreme weather: Snow events (Feb 2007) likely compromised data capture; adjustments or caveats noted.
- Calibration-related adjustments: Some calibration tips were disregarded during 21/08/08 calibration.
- Post-hoc corrections: 03/11/08 entry states that the previous month’s data were adjusted because they were considered fast by about 5 minutes; adjustments recorded in the accompanying Excel document.

## Observations and guidance for data users
- Be aware of potential under/overestimation due to gauge aperture differences when comparing with other gauges.
- Consider time drift corrections and documented adjustments when analyzing time-series rainfall data.
- Recognize data quality risk during field blocks (e.g., blocked gauges, wiring issues, heavy snow) and refer to the maintenance log for context around anomalies.
- Data adjustments are documented in the Excel sheet referenced in the log; consult it for precise corrected values.