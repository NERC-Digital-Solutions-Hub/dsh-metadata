# Snow water equivalent estimates using cosmic-ray neutron sensors in the United Kingdom (2014-2019)

- Purpose and scope
  - Provides daily estimates of Snow Water Equivalent (SWE) derived from Cosmic Ray Neutron Sensors (CRNS) across the COSMOS-UK network.
  - SWE estimates support representation of heterogeneous snow packs with large CRNS footprints (>100 m).
  - Includes multiple SWE estimates per site and snow event: CRNS-based SWE, SnowFox-based SWE, snowmelt model SWE, and depth-based SWE, plus albedo data and event-specific figures.
  - Data covers 2014-2019, up to 2018/19 winter, with 263 snow events and 44 active sites (initial 50 sites; four excluded due to forest cover; Holme Lacy and Moreton Morrell had no detected snow).

- Data content and structure
  - Site metadata: SITE_ID, SITE_NAME, EASTING, NORTHING, SNOW_SITE, DATE_INSTALLED, DATE_DECOMMISSIONED.
  - Event data: DATE (snow day), EVENT_NUMBER, and per-event SWE estimates and diagnostics.
  - SWE estimates:
    - SWE_CRNS_1, SWE_CRNS_2, SWE_CRNS_3 with corresponding UNCERT_CRNS_1/2/3 and CTS_CRNS, CTS_SNOWFREE_1/2/3, N_WAT.
    - SWE_SNOWFOX_1, SWE_SNOWFOX_2, SWE_SNOWFOX_3 with UNCERT_SNOWFOX_1/2/3, CTS_SNOWFOX, CTS_SNOWFOX_SNOWFREE_1/2/3.
    - SWE_MODEL (PACK snowmelt model) with inputs from local air temperature and precipitation; exclusions applied for low or anomalous precipitation data.
    - DEPTH (median daily snow depth from sonic ranger), SWE_DEPTH (derived from depth with assumed density 0.1 g cm-3; QC excludes days with large anomalies or substantial depth reductions).
    - ALBEDO (mean 10:00–14:00 GMT albedo) used to identify snow events.
  - Time frame and daily granularity: daily averages from 00:00 GMT to 00:00 GMT the following day; snow events identified by albedo thresholds and require two snow-free days to end an event.
  - Event-level outputs: a figure per snow event (PNG) plus an explanatory guide image; figures show 24-hour SWE estimates, precipitation, temperature, neutron count rates, and albedo with shading around the event onset/offset.

- Methods for SWE estimation
  - CRNS-based SWE (SWE_CRNS_1/2/3)
    - Uses daily corrected CRNS count rate (CTS_CRNS), snow-free count rate (CTS_SNOWFREE_1/2/3), and water-depth reference (N_WAT).
    - Three methods for estimating snow-free count rates, differing in soil moisture adjustment:
      - Method 1: adjust only if CTS_SNOWFREE is lower than current count rate.
      - Method 2: includes soil moisture variation using two local soil moisture probes.
      - Method 3: uses the minimum soil moisture change to reduce artefact influence.
    - Method 3 often marginally most accurate; occurrence of differences between methods is typically small.
  - SnowFox SWE (SWE_SNOWFOX_1/2/3)
    - Normalises SnowFox count rate by its snow-free rate and applies Howat et al. attenuation curve to derive SWE.
    - SnowFox footprint is small (<1 m) and SWE estimates tend to be about 1.7× higher than CRNS estimates; bias not corrected in the dataset.
    - Three snow-free rate estimation methods analogous to CRNS (1–3); method 3 may offer robustness but adds complexity.
  - Snowmelt model SWE (SWE_MODEL)
    - Based on PACK snowmelt model (Moore et al., 1999) using locally measured air temperature and precipitation.
    - Precipitation classified as snow or rain using a temperature threshold; requires reasonable input precipitation (≥2 mm for the snow event); data with suspicious precipitation removed.
    - Certain events removed or adjusted if precipitation inputs were suspect or yielded implausibly high SWE.
  - Depth-based SWE (SWE_DEPTH)
    - Derived from daily median snow depth (sonic ranging) to reduce noise; background height subtracted using a rule based on surrounding days.
    - Converts depth to SWE assuming 0.1 g cm-3 density for fresh snow; not reported on days where snow depth decreased >20% from its maximum in the event.
    - QC includes removal of noisy depths (e.g., 5 snow events).
  - Albedo-based event detection (ALBEDO)
    - Albedo means used to detect snow onset/zenith: start when mean albedo > 0.5; end when mean albedo < 0.35; use two snow-free days to finalize end due to possible short-lived snow persistence.
    - Mean albedo used as a trigger, with caveat for variations (e.g., Hollin Hill slope effects).

- Uncertainty and quality considerations
  - Typical one-sigma uncertainties:
    - CRNS-based SWE: <~4 mm; dependence on soil moisture content; uncertainties provided per method (UNCERT_CRNS_1/2/3) forewarn reliability for certain days.
    - SnowFox SWE: ~4 mm uncertainty (UNCERT_SNOWFOX_1/2/3); weaker soil moisture dependence.
    - Depth-based SWE: ~4 mm uncertainty.
    - Snowmelt model SWE: ~5 mm uncertainty; elevated in days with dubious input data.
  - Uncertainty values are method-dependent and should be used cautiously; they help identify reliable vs unreliable days but should not dictate method choice in isolation.

- Data access, licensing, and reuse
  - Open Government Licence; dataset available at the provided DOI.
  - Citation requirement: Wallbank et al. 2020, Snow water equivalent estimates using cosmic-ray neutron sensors from COSMOS-UK (dataset).

- Acknowledgments and references
  - COSMOS-UK team contributions; funding from NERC Hydro-JULES and ENTRAIN programs; thanks to individuals for data support and discussions.
  - Key references include Desilets (2017), Howat et al. (2018), Moore et al. (1999), and Wallbank et al. (2020, in preparation).