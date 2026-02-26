# Ammonia enhancement data from Queensberry experimental site in Sri Lanka (20232024)

- Purpose and context
  - Study the effects of high atmospheric ammonia (NH3) on forest vegetation, bryophytes, lichens, and soil.
  - Site: tropical sub-montane forest at Queensberry Estate, central Sri Lanka (coordinates and altitude provided in original study).
  - Established in 2022; dataset is an extension of the 2022 study and covers 2023–2024.

- Experimental design and NH3 enhancement mechanism
  - NH3 release is wind-controlled: NH3 is released only when wind conditions (below canopy) come from directions (5–75°, 185–255°) at threshold speeds (0.3–10 m s⁻¹).
  - Three parallel 20 m long tubes (0.5, 1.35, 2.2 m above ground) with six 4 mm holes around each tube emit NH3.
  - A central manifold with a fan drives airflow; a stainless steel line delivers pure anhydrous NH3 from a cylinder via a mass flow controller (MFC) and a solenoid valve to the release manifold.
  - The solenoid valve opens NH3 flow only when wind conditions are appropriate.

- Data collection and instrumentation
  - Below-canopy wind data collected with a WXT536 weather station (Vaisala).
  - NH3 release rate recorded by the MFC; intervals of 20 seconds, averaged to 15-minute periods.
  - Measurements include NH3 release timing, NH3 flow, and wind conditions.

- Temporal scope and data timing
  - Monitoring period: 1 January 2023 to 31 December 2024.
  - All data timestamped in Sri Lanka Standard Time (SLST).

- Data structure and contents
  - Total observations: 61,751 measurements capturing 4 parameters.
  - Data format: CSV with the following columns:
    - Timestamp (plus metadata fields: Description, Unit, Instrument, Manufacturer)
    - NH3_status (minutes): duration NH3 is released; related to solenoid valve (Type 6027) from Bürkert.
    - NH3_flow (slpm): NH3 flow through the MFC into the release manifold (G series MFC; MKS Instruments).
    - Wind_speed (ms⁻¹): below-canopy wind speed (WXT536; Vaisala).
    - Wind_direction (degrees): below-canopy wind direction (WXT536; Vaisala).

- Data quality and caveats
  - Visual quality control performed; obvious instrument malfunctions, programming issues, and power-cut artifacts removed.
  - Some data gaps resulted from replacement of faulty gas control components.

- Data availability and provenance
  - This dataset extends the 2022 dataset from the same site.
  - Complete details on experimental design, methodology, analyses, and findings available in:
    - Deshpande et al. (2024a)
    - Deshpande et al. (2024b) for meteorological data and ammonia concentration/deposition rates
  - Funding: UKRI GCRF South Asian Nitrogen Hub (NE/S009019/1).