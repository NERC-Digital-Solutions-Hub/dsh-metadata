# Bore Hole monitoring

- A multi-borehole groundwater monitoring effort at Tyn y Bryn farm, with divers and barodivers installed and readings taken from 2005 through 2008.
- Key setup changes: barodiver initially in Bowl borehole, then moved to borehole above the shelterbelt on 09/08/05 to achieve more stable temperature.
- Boreholes monitored: 1 (Above ground measuring)... 2, 3 (Bowl), 4 (Above shelterbelt), 5 (Below shelterbelt); each with detailed depth information and frequent water level readings.

## Data Architecture and Collection

- Data sources and equipment
  - Divers and barodiver devices installed in various boreholes; diver status (in/out) and deployment locations documented.
  - Borehole depths: 1 (11.6 m), 2 (5.5 m), 3 (5.89 m, Bowl), 4 (1208.5 cm), 5 (below shelterbelt, ~775 cm).
- Measurements and metadata
  - Water levels recorded with timestamps (GMT/UTC) and numerous notes on measurement context.
  - Measurements often include adjustments:
    - Reading point is typically above ground level (e.g., 15 or 31 cm); actual water level calculated accordingly.
    - Distinctions between water level with diver in vs diver out (for accuracy and calibration).
    - Some entries include w/o diver (without diver) corrections.
  - Additional data fields implied: diver depth, manual readings, and occasional 30-minute sampling intervals.
- Data collection workflow
  - Divers downloaded and reinstalled at various times; some sessions involved manual dips to verify readings.
  - Occasional recordings of divergent data (e.g., “diver dirty,” “jump of almost 10 cm”) indicate calibration/reading challenges.
  - 2007–2008 entries show ongoing maintenance: diver reliability checks, reinstallation, and eventual removal with wire left in hole on several occasions.
  - Operational guidance appears: “Remind everyone to delete files from diver after download.”

## Data Quality, Metadata and Provenance

- Data quality issues and reliability concerns
  - Several notes on diver reliability problems and data integrity (e.g., “diver quite dirty,” “suspicions on reliability of diver,” jumps in readings).
  - Situations where readings could not be obtained when diver was inside borehole.
  - Data anomalies documented (e.g., jumps in diver readings, muddy measurements, diver/dipper calibration issues).
- Metadata complexity
  - Frequent corrections to convert raw measurements to actual water levels (accounting for ground offset and diver in/out).
  - Ground reference offsets explicitly specified in multiple entries (e.g., measuring point above ground level of 15 cm, 31 cm, etc.).
  - Frequent notes about diver installation/removal, and occasional notes about “manual reading” or “downloaded diver.”
- Provenance and governance
  - Logs indicate careful tracking of diver deployments, recalibrations, and data handling steps.
  - Occasional operational reminders about data hygiene (delete diver files after download).

## Data Gaps and Reliability Challenges

- Inconsistent data capture across boreholes due to equipment and diver issues.
- Missing or unreliable readings when divers were in boreholes or when devices were altered.
- Data continuity impacted by:
  - Diver replacements, re-deployments, and temporary removals.
  - Environmental factors (muddy divers, debris) and mechanical issues (screw difficulties, wire handling).
- Some entries reflect manual dips and cross-checks to validate or adjust logged data.

## Data Management and Governance Recommendations

- Standardize data schema
  - Borehole ID, total_depth_m, measuring_point_above_ground_cm, timestamp_UTC, water_level_cm, diver_status_in_out, w/o_diver_cm, actual_water_level_cm, data_quality_flag, notes.
- Improve metadata quality
  - Capture device type (diver/barodiver), calibration events, diver depth, and whether reading is corrected to w/o diver.
- Implement QA rules and flags
  - Flag readings with diver in, readings with large jumps, and muddy/dirty sensor events.
  - Require cross-checks with manual dips for problematic sessions.
- Centralize data storage and provenance
  - Use a centralized repository with versioning and clear data provenance, including deployment/removal dates and device reconfiguration.
- Data hygiene and operations
  - Enforce post-download data handling policies (e.g., delete diver data files) and document any deviations.
- Data sharing and interoperability
  - Adopt consistent units and reporting formats to enable inter-borehole comparisons and potential integration with wider groundwater data networks.
- Documentation and training
  - Provide a data dictionary and standard operating procedures for borehole monitoring, including handling of anomalies and maintenance logs.

## Key Takeaways for Data Leaders

- The Bore Hole monitoring project collects time-stamped, device-contextualized water level data across five boreholes, with frequent equipment changes and necessary corrections for measurement context.
- Data quality is challenged by diver reliability, measurement conditions, and occasional data anomalies; robust QA and metadata are essential.
- Effective data governance should standardize schema, improve metadata richness, implement quality flags, centralize storage, and enforce data hygiene practices to enable reliable trend analysis and cross-borehole comparisons.