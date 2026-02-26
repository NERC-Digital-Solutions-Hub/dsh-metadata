# This file is for the weir boxes that are measuring drain and overland flow in the bowl. They were installed on 01/11/06.

## Overview
- Documents installation and ongoing monitoring of two weir boxes: DRAIN (drain flow) and OLF (overland flow).
- Monitoring period spans 2006–2008 with numerous maintenance, calibration, and data-logging events.
- Data points include weir geometry, water depth, and logger readings, used to assess flow and identify data issues.

## Setup and Measurements
- DRAIN weir box positioned ~23.33 mm above the v-notch; OLF weir box ~106 mm below the v-notch.
- Average internal area (from 07/06/07 measurements): ~0.520 m^2 for DRAIN (75.2 cm x 69.2 cm) and ~0.517 m^2 for OLF (74.5 cm x 69.1 cm; values averaged).
- V-notch geometry: note of non-verticality in DRAIN (9 mm difference in V-lengths, average ~212.5 mm; CV ~3%); OLF V-length average ~211 mm (CV ~1.3%).
- Water depth measurements taken at the edge away from the V-notch to minimize drawdown effects; average water depth around 112 mm; depth above V-notch calculated as ~37.3 mm for DRAIN.
- Data downloads and visual checks performed to relate observed hand-measured conditions to logger data.

## Data Collection & Logging Events
- 08/11/06: Download; observed OLF weir box leaking.
- 14/11/06–22/11/06: Weir box removed, dried, and reinstalled; issues with OLF weir box suspected to be the leak source.
- 23/11/06: OLF weir box leak confirmed near stilling-well attachment; box removed to dry and repair.
- 27/11/06: Last download indicated a problem with DRAIN flow due to a loose wire; repaired.
- 29/11/06: OLF re-installed; water level zeroed relative to V-notch.
- 06/12/06, 03/01/07, 08/03/07: Logging interruptions due to wiring/sensor issues; attempts to resume.
- 18/04/07–30/04/07: Evaporation affecting OLF/ditch levels; hillslope OLF trap disturbance from mole/vole activity leading to repairs.
- 02/05/07–07/06/07: OLF/trap repairs; materials pegged to stabilize setup; geometry measurements completed to refine area calculations.
- 30/08/07: Drains not flowing; investigation likely needed.
- 17/09/07: OLF blockages noted; minor clearance performed.
- 12/12/07–23/01/08: Data review suggests OLF observations may be lower than expected compared with on-site observations; possible blockage; mop-up of puddle in logger cabinet; downpipe block cleared 30/01/08.
- 13/03/08: Noted a gap in data (03/03/08–13/03/08); 13/03/08 file appeared to duplicate data from 30/07/08 download.
- 15/08/08: Data jump observed after last download on 30/07/08.

## Data Quality Issues & Anomalies
- Leaks and blockages intermittently affecting data integrity (OLF leaks, downpipe/blocked gutter).
- Evaporation impacting water depth measurements on the overland flow path.
- Blockages suspected in data periods where observed field conditions did not match logged data (notably early 2008).
- Gaps in data caused by logger handling issues (battery changes, improper logger handling) and periodic data duplication concerns.
- V-notch geometry not perfectly vertical in DRAIN, potentially affecting depth-to-flow conversions.

## Maintenance, Repairs, and Adjustments
- Leaks addressed: OLF weir box leak repaired; stilling-well attachment checked; box dried and repaired as needed.
- Sensor/wiring issues resolved (s'belt weir box wiring; loose wire in DRAIN detected and fixed).
- Structural/physical adjustments: extended plastic guiding materials toward the end of trenches; stabilization of OLF trench with pegged roofing material where soil was crumbly.
- Calibration steps: measured weir box internal areas to refine flow calculations; reinstalled and zeroed water levels relative to V-notch after maintenance.

## Data Products & Potential Uses
- Flow estimation using V-notch geometry and measured water depths (DRAIN and OLF).
- Derived metrics: water depth above V-notch, head over weir, and estimated discharge using box areas.
- Longitudinal data quality checks: identify periods of potential blockage, leakage, or evaporation effects to flag for cleaning or recalibration.
- Outputs suitable for dashboards or self-service data analysis (e.g., time series of depth, inferred flow, and data quality flags).

## Recommendations for Data Support
- Maintain detailed maintenance and incident logs to accompany data: leaks, blockages, repairs, and calibration events.
- Implement data quality flags for each download interval indicating issues (leak, blockage, evaporation impact, wiring problems, data gap).
- Regularly verify geometry assumptions (V-notch verticality) and update flow-conversion parameters accordingly.
- Proactively monitor for data gaps and duplication, with protocols to re-download and validate data after maintenance.
- Capture and metadata-annotate field observations (evaporation effects, soil conditions, mole/vole disturbance) to contextualize anomalies.
- Consider automated checks linking field notes (evaporation, blockages, and maintenance) to corresponding data windows to facilitate quick QA and reprocessing.