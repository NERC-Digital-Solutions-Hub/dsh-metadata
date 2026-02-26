# Ebullition dataset (5 files), details as follows:

- Overview
  - 5 files documenting methane fluxes from two lowland floodplain fens in 2013 (Sutton and Strumpshaw).
  - Data types include ebullition fluxes, chamber methane fluxes, controlling factors, and environmental variables.
  - Site coordinates: Strumpshaw and Sutton Fens.

- Data content
  - Ebullition flux: methane fluxes (mg CH4 m-2 h-1), methane concentration in bubbles (ppmv), and bubble volume flux (ml m-2 h-1) via ebullition funnels.
  - Chamber flux: methane fluxes (mg CH4 m-2 h-1) measured with static chambers.
  - Controlling factors: mean, SD, and slope of water level; mean/SD of net radiation; mean/SD of soil temperature; mean/SD/slope of air pressure; Vascular Green Area.
  - Environmental variables: hourly soil temperature, air pressure, and water table depth relative to ground.
  - Timeframe: 2013 with Julian Day ranges specified for each data type.
  - NA indicates missing measurements.

- Field methods and QA
  - Protocols based on Defra SP1210 for Lowland Peatland Systems.
  - Ebullition measured with 12 inverted glass funnels per site; chamber flux with 6 tall static chambers per site.
  - Study area: 0.04 km2 at each site, vegetation dominated by Phragmites australis.
  - Instrumentation: automatic weather station; six dipwells with pressure transducers; monthly manual calibration.
  - Vascular Green Area monitored non-destructively (Wilson et al., 2007).
  - Field instrumentation QA details available; full instrumentation details in Stanley (2015) PhD thesis.
  - Gas measurements by gas chromatography with FID; instrument calibration with certified gases; typical precision: CO2 ~6%, CH4 ~7%.

- Data structure (formats and organization)
  - Four Excel spreadsheets containing data (plus accompanying documentation on instrumentation/QA):
    - Ebullition flux: includes flux measurements and components needed to calculate ebullition flux.
    - Chamber flux: methane fluxes from static chambers; NA indicates not taken.
    - Controlling factors: summary metrics for water level, net radiation, soil temperature, air pressure, and vascular green area.
    - Environmental variables: hourly soil temperature, air pressure, and water level.
  - Additional notes: field instrumentation and QA documentation referenced; contact for questions provided below.

- Data usage and benefits
  - Enables self-service exploration and creation of data products (e.g., dashboards, time-series analyses) to link methane fluxes with environmental drivers.
  - Facilitates comparison between ebullition and chamber fluxes and assessment of factors governing methane emissions.
  - Supports temporal analysis (Julian Day ranges) and cross-dataset analyses using the controlling factors and hourly environmental variables.

- Access and contact
  - For queries about the dataset, contact Kate Heppell: c.m.heppell@qmul.ac.uk