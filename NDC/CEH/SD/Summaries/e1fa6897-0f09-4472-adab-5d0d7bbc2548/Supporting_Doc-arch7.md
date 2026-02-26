# Snow water equivalent estimates using cosmic-ray neutron sensors in the United Kingdom (2014-2019)

## Overview
- A dataset of daily Snow Water Equivalent (SWE) estimates using cosmic-ray neutron sensors (CRNS) across the COSMOS-UK network.
- SWE estimates derived from multiple methods: CRNS, SnowFox (buried neutron sensors), a snowmelt model, and depth-based measurements.
- Data cover 2014–2019 with 263 snow events across 44 site installations (out of an initial 50 sites; four forested sites and two non-snow sites excluded).

## Site coverage and data structure
- 44 sites used for SWE estimates (site metadata includes SITE_ID, SITE_NAME, EASTING, NORTHING, installation/decommission dates, and snow-day dates).
- Variables include: SWE_CRNS_1/2/3, UNCERT_CRNS_1/2/3, CTS_CRNS, CTS_SNOWFREE_1/2/3, N_WAT; SWE_SNOWFOX_1/2/3 and UNCERT_SNOWFOX_1/2/3; CTS_SNOWFOX, CTS_SNOWFOX_SNOWFREE_1/2/3; SWE_MODEL; DEPTH; SWE_DEPTH; ALBEDO.
- Units are specified per variable (e.g., SWE in mm, EASTING/NORTHING in m, DATE related fields).

## SWE estimation methods
- CRNS SWE (SWE_CRNS_1/2/3)
  - Based on the CRNS footprint (>100 m) using daily corrected CRNS count rate (CTS_CRNS), snow-free rate (CTS_SNOWFREE_1/2/3), and water-depth reference (N_WAT).
  - Three methods for estimating snow-free count rate; Method 3 often preferred for accuracy.
- SnowFox SWE (SWE_SNOWFOX_1/2/3)
  - SnowFox (smaller footprint) SWE estimates normalized by snow-free rate (CTS_SNOWFOX_SNOWFREE_1/2/3) and converted via Howat et al. attenuation curve.
  - Typically yields SWE ~1.7x CRNS estimates; Method 3 may be marginally most accurate.
- Snowmelt model SWE (SWE_MODEL)
  - Daily mean SWE from the PACK snowmelt model using local air temperature and precipitation (snow/rain classified by temperature threshold).
  - Precipitation input quality controls; data with low precipitation or anomalous values excluded (29 of 256 events removed; additional removals for large precipitation values).
- Depth-based SWE (SWE_DEPTH)
  - Daily median snow depth from sonic sensors; background height estimated from surrounding days.
  - Converted to SWE using assumed fresh-snow density (0.1 g/cm^3); not reported when snow aged beyond 20% depth change from the maximum.

## Snow detection and inputs
- Albedo used to identify snow onset/offset: mean albedo (10:00–14:00 GMT) > 0.5 signals start; < 0.35 signals end.
- Two snow-free days required to end a snow event to avoid misclassification due to short gaps.
- Hollin Hill site noted for slope-related albedo detection challenges; cross-checked with phenocam data.

## Uncertainty and data quality
- Typical uncertainties (one standard deviation): ~4 mm for CRNS and SnowFox; ~4 mm for depth-based; ~5 mm for snowmelt model.
- Uncertainty depends on soil moisture and the method used to estimate snow-free count rate (particularly for CRNS); weaker soil-moisture dependence for SnowFox.
- Uncertainty estimates provided per method (UNCERT_CRNS_1/2/3 and UNCERT_SNOWFOX_1/2/3).

## Data products and visualization
- Daily SWE estimates and uncertainties, plus supporting inputs (CTS, N_WAT, albedo, counts).
- Snow-event figures produced for every snow event at each site (PNG files named by SITE_ID, EVENT_NUMBER, and date). Each figure displays 24-hour SWE estimates, precipitation, air temperature, count rates, and albedo; shaded days indicate before/after detection; discontinuities may indicate unreliable estimates.

## Data access, licensing, and reuse
- Open Government Licence; data accessible via DOI: 10.5285/e1fa6897-0f09-4472-adab-5d0d7bbc2548
- Citation required: Wallbank et al. (2020) Snow water equivalent estimates using cosmic-ray neutron sensors from COSMOS-UK (2014-2019).

## Processing notes and references
- Site selection: initial 50 COSMOS-UK sites; four forested sites excluded due to footprint complications; Holme Lacy and Moreton Morrell excluded due to lack of snow during study; 44 sites remain.
- Snow depth data undergo quality control and background noise handling; 5 events removed from SWE_DEPTH due to data quality.
- Key references: Desilets (2017) on CRNS calibration; Howat et al. (2018) for SnowFox; Moore et al. (1999) PACK snowmelt model; Wallbank et al. (2020) methodology for SWE estimation and uncertainty.