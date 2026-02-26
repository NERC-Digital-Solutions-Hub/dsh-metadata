# High-resolution ammonia concentration data from Queensberry experimental site in Sri Lanka (2022)

- Purpose and scope
  - Studied effects of high ambient ammonia (NH3) on forest vegetation, bryophytes, lichens, and soil.
  - Conducted at Queensberry Estate, central Sri Lanka, 2022.
  - Data collected to understand NH3 release dynamics, plume movement, and canopy interactions under controlled wind conditions.

- Experimental setup
  - Ammonia enhancement system activated only under specific wind directions (5-75° and 185-255°) and threshold speeds (0.3–10 m/s).
  - Release hardware: three 20 m long PVC tubes arranged horizontally; NH3 injected via a stainless steel manifold and mass flow controller into a fan-generated airflow.
  - Campaign study to optimize release rates to achieve target concentrations and to assess lateral/vertical plume movement within the canopy.

- Measurement system and sampling
  - Analyser: Picarro G2123 NH3/H2O, positioned 10 m downwind of the release system.
  - Sampling: four heights (0.5, 1.0, 1.5, 2.5 m) along a downwind sector; automated LabVIEW-controlled valve manifold sampled in 2-minute intervals per height.
  - Inlets and lines: 5.5 m PTFE sampling lines per height; system temperature maintained at ~40°C; purge/scan flow rates varied during sampling to minimize response delays.
  - Data cadence: NH3 concentrations recorded at 10 Hz and averaged to 0.016 Hz.

- Data quality control and processing
  - Visual QC; removal of obvious instrument or datalogger issues and power-cut artifacts.
  - Gaps from valve switching filled by linear interpolation.
  - Acknowledged potential lag due to NH3 adsorption/desorption on inlet surfaces; background NH3/nitrate volatilisation considered.

- Data structure and contents
  - Dataset size: 14,094 measurements across 6 parameters.
  - Format: CSV with detailed metadata fields, including:
    - Timestamp (date/time with time zone)
    - NH3_status (status of NH3 release; multiple coded states)
    - NH3_flow (flow rate through MFC; multiple unit references)
    - Wind_speed (m/s; sensor/instrument source specified)
    - Wind_direction (degrees; sensor/instrument source specified)
    - NH3_conc (NH3 concentration downwind; ppb; sensor specified)
    - Inlet_height (m; height of sampling inlet; sensor specified)
  - Each parameter includes instrument/manufacturer/descriptions to aid reproducibility.

- Temporal and geographic scope
  - Timeframe: 24 March 2022 to 3 April 2022 (Sri Lanka Standard Time).
  - Location: Queensberry experimental site, tropical sub-montane forest, altitude ~1645 m (coordinates provided).

- Funding and provenance
  - Funded by UKRI GCRF South Asian Nitrogen Hub.

- Relevance for environmental monitoring analysts
  - Provides high-resolution, standardized NH3 concentration data linked to controlled release experiments.
  - Facilitates analysis of plume dynamics, canopy NH3 interactions, and validation of atmospheric dispersion models.
  - Designed for integration with other datasets and portals; emphasizes data quality assurance, traceability, and accessibility of underlying data.