# Drain flow data log

- A historical log of drain flow measurement using a tipping bucket (TB) system, weir box, and transducer, including interval settings, calibrations, maintenance, data issues, and calibration-driven adjustments from 2005 to 2009.

## Overview
- The recording interval was adjusted from 10 minutes to 5 minutes to align with the overland flow trap.
- Drain flow is monitored via a tipping bucket system connected to a weir box; multiple maintenance and calibration steps were performed to improve or verify measurements.
- Data quality frequently affected by hardware issues, calibration events, timing (GMT/BST) shifts, and environmental factors (e.g., algae/gunk in the TB).

## Key events by date (timeline highlights)
- 22/02/05: Interval reset to 5 minutes.
- 09/11/05 – 01/02/06: Indications that drain water may not fully flow through TB; issues with ice/forming obstructions.
- 17/02/06 – 23/02/06: TB mechanical issues (bolt dislodged) and TB removal for testing.
- 11/04/06 – 21/04/06: Weir box installed; transducer setup adjustments; data readings affected by transducer handling.
- 29/06/06 – 05/07/06: Data uploads; some readings incorrect; tipping buckets calibrated; ignore specific periods.
- 21/08/06 – 03/10/06: Battery failures; weir box maintenance; interval remains at 5 minutes.
- 25/10/06 – 08/11/06: Draining too fast for TB system; TB removal due to leaks; reinstallation mid-11/2006.
- 14/11/06 – 06/12/06: TB reinstalled; later notice to ignore prior data after leak.
- 01/03/07 – 30/04/07: Leaks sealed; TB reinstalled; calibration checks performed; battery/kit maintenance.
- 07/06/07: Calibration: 30 L through TB yielded 10 tips + 0.9 L remainder; tip volume determined as 2.91 L; magnet issues noted and corrected.
- 15/08/07: Magnet reattached; tips registered; ignore tips around 2:30–3:30 BST.
- 30/08/07 – 19/02/08: Periods of no-flow or TB freezing; data flagged for quality concerns.
- 12/06/08 – 31/10/08: Data flagged due to PT checks and calibration activities; time stamps adjusted or ignored during calibration.
- 14/11/08 – 17/11/08: Calibration re-evaluated; new calibration: 30.04 L = 11 tips; 2.79 L per tip; approach to adjust for drift since initial calibration.
- 07/01/09 – 30/07/09: System briefly frozen or issues with TB; zero-flow checks; data periods marked as not suitable; bucket dislodgement and reattachment noted.
- 04/06/09 – 15/07/09: Drain inflow pipe reinstallation issues; data periods deemed usable or not based on reliability.

## Data quality, calibration, and measurement notes
- TB calibration changes over time:
  - 07/06/07: 30 L through TB -> 10 tips; each tip ~2.91 L.
  - 14/11/08: 30.04–30.66 L for 11 tips; each tip ~2.79 L; later adjustments to account for drift.
  - 6 months after initial calibration: applied a linear incremental change to tip volume to reflect observed drift.
- Periods of data exclusion:
  - Explicit calibrations, hardware adjustments, or anomalies led to exclusion of data (e.g., 13:30–14:30 BST on 07/06/07; 08:54–12:00 GMT on 24/10/08–31/10/08; various “ignore data” notes during calibration events).
  - Data during ranges of sensor maintenance (weir box calibration, PT checks) were disregarded to avoid bias.
- Timing and timestamp issues:
  - GMT to BST transitions introduced timing inconsistencies; adjustments documented in the data file.
  - Some time stamps noted as anomalous during calibration (e.g., 102:4 GMT).
- Hardware and reliability challenges:
  - Tipping bucket mechanical issues: bolts, magnets, reed switches, and axles.
  - Weir box and PT checks: require access; data flagged during emptying or diversion operations.
  - Battery failures, transducer mounting, and water ingress in sensor housings affected data integrity.
  - Algae/gunk in TB observed and removed; turbidity or debris impacted tipping behavior.
- Data processing and provenance:
  - Regular downloads of drain flow and auxiliary data (OLF) for verification.
  - Calibration references and reprocessing notes indicate efforts to harmonize historical data with updated calibration constants.
  - Some datasets marked as “not suitable for use” due to installation or calibration artefacts.

## System components and calibration values
- Tipping bucket (TB) system: primary measurement device; connected to drain flow via a weir box; magnet and reed switch-based tipping mechanism.
- Weir box: secondary flow measurement component; periodically serviced or calibrated.
- Transducer/logger: records TB tips and flow; occasionally misregistered data or misalignment corrected on-site.
- Calibration values:
  - 07/06/07: Tip volume = 2.91 L (30 L giving 10 tips + 0.9 L remainder).
  - 14/11/08: Tip volume = 2.79 L (30.04–30.66 L for 11 tips); later alignment indicates drift correction.
- Maintenance actions affecting measurements:
  - Magnet reattachment (07/06/07; 15/08/07) to restore proper tipping.
  - Weir box cleaning and PT checks (late 2008) with data exclusion during those periods.
  - TB removal/reinstallation due to leakage or mechanical faults (various dates).
  - Recalibration after cleaning/gunk removal and calibration diversions.

## Implications for analysis and data use
- Expect non-stationarity in tip volume over time; apply calibration-adjusted tip volumes, especially when integrating data across 2007–2009.
- Treat calibration events and maintenance periods as separate regimes; exclude or flag data during calibrations and maintenance to avoid bias.
- Correct for time-stamp shifts between GMT and BST; synchronize all data to a consistent time reference.
- Be aware of periods with missing or corrupted data (e.g., data flagged as “ignore,” TB/magnet issues, or pipe reinstallation) and document any imputation or exclusion.
- Maintain metadata with each dataset copy, noting calibration dates, maintenance actions, and data-quality flags to enable reproducible analyses.