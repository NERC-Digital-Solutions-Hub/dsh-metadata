# Snow water equivalent estimates using cosmic-ray neutron sensors in the United Kingdom (2014-2019)

- Purpose and scope
  - Provides daily Snow Water Equivalent (SWE) estimates using cosmic-ray neutron sensors (CRNS) across the COSMOS-UK network to support environmental monitoring and policy scrutiny.
  - Footprint of CRNS is large (typically >100 m), enabling representative SWE for heterogeneous snowpacks.
  - Data span: up to 2018/19 winter; includes additional SWE estimates from SnowFox sensors, a snowmelt model, and depth-based methods where available.
  - For quality assessment, accompanying figures summarize inputs and outputs for each snow event; uncertainty estimates accompany SWE values.

- Data coverage and site details
  - 44 COSMOS-UK sites used (initially 50; four excluded due to forest cover or lack of snow, and two with no snow detected), across the UK.
  - Total: 263 snow events documented.
  - Data fields include site metadata (SITE_ID, SITE_NAME, EASTING, NORTHING, SNOW_SITE, DATE_INSTALLED, DATE_DECOMMISSIONED) and daily event data (DATE, EVENT_NUMBER).

- SWE estimation methods
  - CRNS SWE (SWE_CRNS_1, SWE_CRNS_2, SWE_CRNS_3)
    - Based on daily corrected CRNS count rate (CTS_CRNS), snow-free count rate (CTS_SNOWFREE_1/2/3), and an estimate of CRNS count rate over infinite depth of water (N_WAT).
    - Three methods to estimate snow-free count rate; Method 3 is the most conservative and may offer slight accuracy gains.
  - SnowFox SWE (SWE_SNOWFOX_1, SWE_SNOWFOX_2, SWE_SNOWFOX_3)
    - SnowFox sensors provide a smaller footprint; SWE estimates are scaled from normalized SnowFox counts using a snow-free reference and Howat et al. attenuation.
    - Typically ~1.7x larger than CRNS/SWE_MODEL estimates; method choice affects uncertainty modestly.
  - Snowmelt model SWE (SWE_MODEL)
    - PACK snowmelt model uses local air temperature and precipitation (snow vs. rain determined by temperature threshold).
    - Data filtered to remove suspicious precipitation (e.g., <2 mm) and outliers (>50 mm) to ensure reliability.
  - Depth-based SWE (SWE_DEPTH)
    - Uses daily median snow-depth from sonic sensors; converts to SWE with assumed fresh-snow density (0.1 g/cm3).
    - Applies quality controls and excludes days with significant depth decrease (>20% from the daily maximum).
  - Albedo (ALBEDO)
    - Mean albedo 10:00–14:00 GMT used to detect snow events; snow begins when albedo > 0.5 and ends when < 0.35.
    - Two snow-free days required to close an event; some site-specific considerations (e.g., Hollin Hill slope).

- Uncertainty and data quality
  - Reported uncertainties (one standard deviation) typical of:
    - CRNS and SnowFox SWE: ≤ ~4 mm
    - Depth-based SWE: ~4 mm
    - Snowmelt model: ~5 mm
  - Uncertainties for CRNS depend on soil moisture and the method used to estimate snow-free count rate; SnowFox uncertainties show weaker soil-moisture dependence.
  - Uncertainty values should be interpreted cautiously; they inform reliability but do not dictate method choice.

- Outputs and data products
  - For each snow event at each site, a figure (png) summarizes 24-hour mean SWE estimates, precipitation, air temperature, count rates, and albedo.
  - Figures labeled by SITE_ID, EVENT_NUMBER, and first snow date; a guide figure is provided.
  - Shading around the albedo-detected period indicates days before/after the event; discontinuities may indicate unreliable estimates.

- Data access, licensing, and reuse
  - Open Government Licence; dataset available at the provided DOI.
  - Users must cite Wallbank et al. (2020) when using the dataset:
    Snow water equivalent estimates using cosmic-ray neutron sensors in the United Kingdom (2014-2019). NERC Environmental Information Data Centre. https://doi.org/10.5285/e1fa6897-0f09-4472-adab-5d0d7bbc2548

- Acknowledgments and references
  - COSMOS-UK team contributions; funding from NERC Hydro-JULES and ENTRAIN programs; related methodological references include Desilets (2017), Howat et al. (2018), and Moore et al. (1999).