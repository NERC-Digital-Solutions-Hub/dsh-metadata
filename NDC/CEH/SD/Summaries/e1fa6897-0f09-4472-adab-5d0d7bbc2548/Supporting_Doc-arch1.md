# Snow water equivalent estimates using cosmic-ray neutron sensors in the United Kingdom (2014-2019)

## Overview
- Provides daily Snow Water Equivalent (SWE) estimates using COSMOS-UK cosmic-ray neutron sensors (CRNS) across the United Kingdom.
- Large CRNS footprint (>100 m) enables SWE estimates for heterogeneous snowpacks.
- Includes multiple SWE estimation methods: CRNS-based, SnowFox sensor-based, a snowmelt model, and depth-based estimates.
- Data span: installation of sites through 2019-08-22; 44 sites used for SWE estimates (50 initial sites with 4 exclusions due to canopy, and two sites with no detected snow). Totals 263 snow events documented.
- Outputs include daily SWE estimates, uncertainties, albedo, and supporting inputs, plus figures for each snow event.

## Data sources and site details
- COSMOS-UK network sites: initial 50 sites; exclusions due to forest canopy (Alice Holt, Gisburn Forest, Harwood Forest, Wytham Woods) and lack of snow at Holme Lacy and Moreton Morrell, leaving 44 sites.
- Site metadata includes coordinates, installation/decommission dates, and SnowFox/SNOW_SITE indicators.
- Data are provided with accompanying figures per snow event and a general guidance figure.

## SWE estimation methods

### 1) CRNS SWE (SWE_CRNS_1,2,3)
- Inputs: daily average corrected CRNS count rate (CTS_CRNS), snow-free count rate (CTS_SNOWFREE_1,2,3), and an estimate of CRNS count rate for infinite depth of water (N_WAT).
- Methods for snow-free rate (three variants):
  - Method 1: adjust if snow-free rate would imply negative SWE.
  - Method 2: includes soil moisture changes using two local soil moisture probes.
  - Method 3: conservative soil moisture correction using the minimum change from probes.
- Recommendation: Method 3 may be marginally most accurate; differences among methods are typically small.
- Uncertainty: typical one-standard-deviation uncertainty ~4 mm; depends strongly on soil water content.

### 2) SnowFox SWE (SWE_SNOWFOX_1,2,3)
- SnowFox sensors provide a smaller footprint; SWE estimates derived by normalising SnowFox counts by snow-free rate and applying Howat et al. (2018) attenuation.
- Three snow-free rate methods analogous to CRNS.
- Bias: SnowFox SWE estimates are typically ~1.7 times larger than other SWE estimates (unadjusted in dataset).
- Uncertainty: similar scale to CRNS, with weaker soil-moisture dependence than CRNS.

### 3) Snowmelt model SWE (SWE_MODEL)
- Based on the PACK snowmelt model (Moore et al., 1999); inputs are local air temperature and precipitation, with precipitation categorized as snow or rain via a temperature threshold.
- Data filtering: exclude days with suspiciously low precipitation (<2 mm) for snow events.
- Data quality control: removal of 29 snow events due to questionable input precipitation; additional removals for anomalously large modeled SWE values.
- Use: model comparisons with other SWE estimates.

### 4) Depth-based SWE (SWE_DEPTH)
- Uses daily median snow depth from sonic ranging sensors (when available); background height subtracted using a robust approach.
- Convert depth to SWE with an assumed fresh-snow density of 0.1 g cm^-3; not applied when depth decreased by more than 20% from its maximum within the event.
- Quality control: removal of problematic depths for 5 snow events; depth-derived SWE has higher sensitivity to snow aging and density assumptions.

### 5) Albedo (ALBEDO)
- Albedo measured at 10:00–14:00 GMT; mean value used to help identify snow events.
- Snow begin: mean albedo > 0.5; snow end: albedo < 0.35.
- To prevent premature termination of events, two snow-free days are required to end an event (accounting for days without albedo change).
- Noted site-specific issues (e.g., Hollin Hill slope) were cross-checked with phenocam images.

## Uncertainty and interpretation
- CRNS and SnowFox SWE uncertainties: typically < 4 mm (one standard deviation); depth-based ~4 mm; snowmelt model ~5 mm.
- Uncertainty depends on soil moisture and measurement method; CRNS uncertainties are more sensitive to soil water content.
- Uncertainty estimates are method-specific (UNCERT_CRNS_1,2,3; UNCERT_SNOWFOX_1,2,3) and should be used to gauge reliability rather than to select a single method.

## Data access, licensing, and reuse
- Datasets are available under the Open Government Licence.
- Access and citation: Wallbank et al. (2020) Snow water equivalent estimates using cosmic-ray neutron sensors from the COSMOS-UK network; DOI provided in the dataset entry.
- Data products include daily SWE estimates, uncertainties, ancillary inputs, and event-specific figures; figures show SWE, precipitation, temperature, count rates, and albedo for each snow event.

## Data products and outputs
- SWE estimates provided as:
  - SWE_CRNS_1,2,3 (CRNS-based)
  - SWE_SNOWFOX_1,2,3 (SnowFox-based)
  - SWE_MODEL (snowmelt model)
  - SWE_DEPTH (depth-based)
  - UNCERT_CRNS_1,2,3; UNCERT_SNOWFOX_1,2,3 (uncertainties)
  - CTS_CRNS, CTS_SNOWFREE_1,2,3, N_WAT, DEPTH, ALBEDO, and other supporting inputs
- Each snow event has a corresponding figure (PNG) summarizing 24-hour SWE estimates plus inputs; naming convention includes SITE_ID, EVENT_NUMBER, and event start date.

## Acknowledgments and context
- COSMOS-UK team support and discussions with D. Desilets; funded by NERC Hydro-JULES and ENTRAIN programs; SCENARIO placement supported one author.
- Related foundational work cited includes Desilets (2017), Howat et al. (2018), Moore et al. (1999), and Wallbank et al. (2020, in preparation).