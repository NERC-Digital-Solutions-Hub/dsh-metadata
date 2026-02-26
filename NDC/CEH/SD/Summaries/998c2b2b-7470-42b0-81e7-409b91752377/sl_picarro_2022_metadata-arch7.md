# High-resolution ammonia concentration data from Queensberry experimental site in Sri Lanka (2022)

- Purpose and scope
  - Data from an ammonia (NH3) enhancement experiment conducted in a tropical sub-montane forest at Queensberry Estate, central Sri Lanka (coordinates: 6.9693°, 80.5911°, altitude 1645 m).
  - Aimed to study how high NH3 levels affect forest vegetation, bryophytes, lichens, and soil, including plume movement within the canopy.

- Experimental setup and data collection
  - NH3 release system
    - Controlled by wind conditions; NH3 released only when wind direction falls within 5–75° and 185–255° at threshold speeds (0.3–10 m/s).
    - Release from three parallel PVC tubes (20 m long, 110 mm OD) at ground-to-0.5/1.35/2.2 m heights.
    - NH3 delivered via a stainless steel manifold and a mass flow controller with a solenoid valve to regulate flow.
  - Monitoring and sampling
    - Picarro NH3/H2O analyser located 10 m downwind of the release system.
    - Sampling at four heights (0.5, 1.0, 1.5, 2.5 m) using a multi-channel, temperature-controlled PTFE tubing system (~40°C) to minimize adsorption/desorption delays.
    - Air sampled at 10 Hz and averaged to approximately 0.016 Hz intervals; a custom LabVIEW program automates sampling.
    - Data collected March 24, 2022 to April 3, 2022.
  - Lag and background considerations
    - Some lag due to switching of heights and NH3 adsorption/desorption on inlet surfaces.
    - Volatilisation from NH4NO3 aerosols expected to generate a relatively constant background.

- Data quality control
  - Visual QC to remove instrument malfunctions, datalogger issues, and power-cuts.
  - Gaps from valve switching filled by linear interpolation.
  - Data described as 14,094 measurements across 6 parameters.

- Data structure and metadata
  - Format: CSV with 14,094 rows and 6 key parameters.
  - Columns (with examples of metadata available for each):
    - Timestamp: 1-minute timestamps (format dd/mm/yyyy hh:mm).
    - NH3_status: status of NH3 release (codes indicating OFF/ON and related states).
    - NH3_flow: NH3 flow through the system (units vary by instrument; e.g., slpm, etc.).
    - Wind_speed: wind speed (m/s) measured by a specified instrument.
    - Wind_direction: wind direction (degrees) from a specified instrument.
    - NH3_conc: NH3 concentration in air at 10 m downwind (ppb), measured by a specified instrument.
    - Inlet_height: height above ground at which NH3 concentration is measured (m).
  - Instrument and data-source context
    - NH3_status: instrument Type 6027, Manufacturer Bürkert.
    - NH3_flow: instrument from MFC families (e.g., MKS Instruments).
    - Wind_speed: instrument WXT536 or equivalent.
    - Wind_direction: instrument Vaisala or equivalent.
    - NH3_conc: instrument G2123 or Picarro.
    - Inlet_height: height reference related to sampling height (context linked to the measurement system).

- Spatial and temporal context for GIS use
  - Site-level coordinates and altitude provide geographic grounding for GIS analyses.
  - Downwind NH3 concentrations measured at a fixed location relative to the release system, across multiple vertical heights, enabling plume and vertical profiling analyses.
  - Temporal coverage spans late March to early April 2022 with per-minute timestamp resolution, suitable for linking NH3 concentrations to wind fields and staging events.

- Funding
  - Funded by UKRI GCRF South Asian Nitrogen Hub.