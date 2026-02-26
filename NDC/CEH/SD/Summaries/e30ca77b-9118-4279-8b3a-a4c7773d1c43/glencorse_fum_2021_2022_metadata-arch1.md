# Ammonia enhancement data from Glencorse experimental site near UKCEH, Edinburgh (2021-2022)

- Purpose and scope
  - Study the effects of elevated atmospheric NH3 on forest vegetation, bryophytes, lichens, and soil.
  - Conducted as a wind-controlled NH3 enhancement experiment at the Glencorse woodland, near Edinburgh (latitude 55.8539, longitude -3.2151; altitude 200 m).
  - Data collected from 16 September 2021 to 5 January 2023; all times in GMT.
  - Funding: UKRI GCRF South Asian Nitrogen Hub.

- Experimental design and NH3 release control
  - NH3 released through three horizontal PVC tubes (each 20 m long, 110 mm OD) at heights 0.5, 1.35, and 2.2 m, with six 4 mm holes per tube (every 20 cm along length).
  - Ammonia delivered from a cylinder via a manifold with a mass flow controller (MFC) and solenoid valve; controlled by a central fan to dilute NH3 into the airflow.
  - Release is triggered only when wind conditions are favorable: wind direction within 275–345 degrees and wind speed within 0.3–10 m/s, measured below the forest canopy.
  - Gas is released into the under-canopy airflow; a WXT536 weather station provides wind data; MFC records NH3 flow setpoints and actual flow.

- Data collection and structure
  - Data captured at 20-second intervals; 15-minute averages reported.
  - Dataset includes 45,538 measurements across 5 parameters (plus time-related fields) in a CSV format.
  - Key fields (per row): Timestamp (15-minute interval), NH3_status (0 = OFF, >0 = ON), NH3_flow_set (slpm; NH3 flow setpoint), NH3_flow (slpm; actual NH3 flow into release manifold), Wind_speed (ms^-1; below-canopy), Wind_direction (degrees).
  - Instrumentation:
    - NH3 release monitoring and control: mass flow controller (G series MFC; MKS Instruments), solenoid valve (Type 6027; Bürkert).
    - Wind monitoring: WXT536 weather station (Vaisala).
  - Location details: Glencorse woodland (55.8539°, -3.2151°), altitude 200 m.

- Data quality and limitations
  - Quality control performed visually to remove obvious instrument errors, power outages, and logger issues.
  - Some gaps present due to time required to replace faulty gas-control components.
  - Data reflect designed exposure windows rather than continuous ambient NH3 levels; exposure depends on wind direction and speed thresholds.

- Metadata and accessibility
  - Complete experimental design, methodology, analysis, and findings described in Deshpande et al. (2024).
  - Data intended to support analyses of NH3 deposition and environmental responses; linked to the study: Estimation of ammonia deposition to forest ecosystems in Scotland and Sri Lanka using wind-controlled NH3 enhancement experiments.

- Related findings and usage
  - The dataset underpins analyses of correlations between controlled NH3 exposure and forest ecosystem responses.
  - Used in the cited Atmosphere Environment study (Deshpande et al., 2024) to estimate ammonia deposition to forest ecosystems.