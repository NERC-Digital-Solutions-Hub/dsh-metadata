# High-resolution ammonia concentration data from Queensberry experimental site in Sri Lanka (2022)

- Purpose and context
  - Ammonia (NH3) enhancement experiment to study effects on forest vegetation, bryophytes, lichens, and soil.
  - Campaign aimed to optimize NH3 release rates and understand lateral and vertical plume movement within the canopy post-release.

- Location and site details
  - Queensberry Estate, central Sri Lanka (6.9693°N, 80.5911°E), altitude 1645 m.

- NH3 release system
  - Three 20 m long tubes (110 mm OD) placed horizontally at ground proximity levels 0.5, 1.35, and 2.2 m.
  - NH3 injected from a cylinder via a 6.35 mm stainless steel pipe, through a mass flow controller (MFC) and solenoid valve into a central fan-driven airflow.
  - Release occurs through six 4 mm holes along each tube, spaced 20 cm apart.
  - Wind-condition control: release activated only when wind direction falls in 5–75° or 185–255° relative to the monitoring quadrats and wind speeds are 0.3–10 m s^-1.

- Downwind measurement setup
  - Picarro NH3/H2O analyser located 10 m downwind in the northeastern sector.
  - Sampling at four heights: 0.5, 1, 1.5, and 2.5 m from ground.
  - Sampling duration: 2 minutes per height; four sampling inlets connected via a 5.5 m PTFE tubing network.
  - Inlet system temperature maintained at ~40°C (±3°C) with heating tape and insulation.
  - Automated control via LabVIEW; valve manifold enables sequential sampling.
  - Inlet lines purged at 7 standard L/min between samples; 12 standard L/min during sampling.

- Data characteristics and timing
  - NH3 concentrations recorded at 10 Hz and averaged to 0.016 Hz intervals.
  - Data collection period: 24 March 2022 to 3 April 2022.
  - Data quality notes: some lag expected due to NH3 adsorption/desorption on inlet surfaces; potential residual volatilisation of NH4NO3 may produce a smooth background.

- Quality control and handling
  - Visual checks performed; obviously erroneous data due to instrument issues, datalogger problems, or power cuts removed.
  - Gaps created during valve switching filled by linear interpolation.

- Data structure and fields
  - Total measurements: 14,094
  - Stored as CSV with the following columns (each with unit, instrument, and description):
    - Timestamp: date and time (dd/mm/yyyy hh:mm)
    - NH3_status: release status (values indicate ON/OFF/valve states)
    - NH3_flow: NH3 flow rate through the system (units and source vary by instrument)
    - Wind_speed: wind speed (m s^-1), source varies by instrument
    - Wind_direction: wind direction (degrees), source varies by instrument
    - NH3_conc: NH3 concentration in air at 10 m downwind (ppb)
    - Inlet_height: measurement height above ground (m)
  - Each field includes the instrumental source, manufacturer, and descriptive notes.

- Data provenance and funding
  - Data collection funded by the UKRI GCRF South Asian Nitrogen Hub.