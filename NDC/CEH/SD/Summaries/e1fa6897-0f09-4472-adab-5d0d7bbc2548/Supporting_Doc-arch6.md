# Snow water equivalent estimates using cosmic-ray neutron sensors in the United Kingdom (2014-2019) . NERC Environmental Information Data Centre. (Dataset)

## Overview
- A dataset documenting daily Snow Water Equivalent (SWE) estimates across the COSMOS-UK network using cosmic-ray neutron sensors (CRNS), with supplementary SWE estimates from SnowFox sensors, a snowmelt model, and a depth-based approach.
- Large footprint of CRNS (~>100 m) enables representative SWE estimates for heterogeneous snowpacks.
- Data support materials include figures per snow event to assess reliability and inputs.

## Datasets and SWE estimation methods
- SWE_CRNS_1, SWE_CRNS_2, SWE_CRNS_3
  - Daily mean SWE derived from CRNS neutron counts (three methods controlling for soil moisture).
  - Key inputs: daily average corrected CRNS count rate (CTS_CRNS), snow-free count rate (CTS_SNOWFREE_1/2/3), and CRNS count rate over infinite water depth (N_WAT).
  - Snow-free count rate methods:
    - Method 1: adjust if lower than current count rate to avoid negative SWE.
    - Method 2: adds soil moisture variation correction using two local soil moisture probes.
    - Method 3: conservative moisture correction using the minimum change from probes.
  - Uncertainty: daily uncertainties UNCERT_CRNS_1/2/3; depends on soil moisture and method used.
- SWE_SNOWFOX_1, SWE_SNOWFOX_2, SWE_SNOWFOX_3
  - SnowFox sensors (buried, footprint < 1 m) provide SWE estimates via normalised corrected SnowFox count rate and snow-free rate, using Howat et al. attenuation.
  - SnowFox SWE typically ~1.7x CRNS-based SWE (unadjusted for bias).
  - Uncertainty: UNCERT_SNOWFOX_1/2/3; relatively weak soil-moisture dependence.
- SWE_MODEL
  - Daily mean SWE from the PACK snowmelt model (Moore et al., 1999) using local air temperature and precipitation (snow/rain threshold).
  - Precipitation quality control: excluding days with suspiciously low input precipitation; some events removed due to questionable data (e.g., 29 events removed).
- SWE_DEPTH
  - Depth-based SWE using daily median snow depths from sonic ranging sensors (where available).
  - Robustness: daily median used; background height adjusted; 5 of 78 snow events removed after quality checks.
  - Conversion: SWE_DEPTH = depth × 0.1 g cm^-3 for fresh snow density; not reported when snow depth declined >20% from the event maximum.
- ALBEDO
  - Site albedo averaged 10:00–14:00 GMT to help detect snow onset/offset.
  - Snow events identified when mean albedo > 0.5 (start) and < 0.35 (end); two snow-free days required to end an event.
- Uncertainty context
  - Typical uncertainties: CRNS and SnowFox SWE < ~4 mm; depth-based ~4 mm; snowmelt model ~5 mm.
  - Uncertainty for CRNS depends on soil moisture; for SnowFox, soil moisture dependence weaker.

## Snow event figures
- A figure for each snow event at each site, with 24-hour average SWE, precipitation, air temperature, count rates, and albedo.
- Figures labeled by SITE_ID, EVENT_NUMBER, and first snow day date (e.g., CGARW_event_1_date_2017-12-10.png).
- Guides provided to aid interpretation; shaded days denote proximity to albedo-detected snow onset/offset.

## Sites and data coverage
- 50 COSMOS-UK sites considered; four excluded due to dense forest footprints or lack of snow detection.
- Excluded sites: Alice Holt, Gisburn Forest, Harwood Forest, Wytham Woods.
- Snow detected at none of Holme Lacy or Moreton Morrell (installed 2018); remaining usable data from 44 sites.
- Data span up to 2018/19 winter; as of installation, 263 snow events recorded in total across sites.

## Data access, licensing and reuse
- Open Government Licence.
- Access and citation: Wallbank et al. (2020) Snow water equivalent estimates using cosmic-ray neutron sensors from the COSMOS-UK dataset, NERC Environmental Information Data Centre; DOI provided in dataset.
- Usage includes reference to the dataset and publication details.

## Acknowledgments and references
- Acknowledges COSMOS-UK team and D. Desilets; funded by NERC Hydro-JULES and ENTRAIN programs.
- Key references: Desilets (2017) on calibrating CRNS; Howat et al. (2018) on SnowFox; Moore et al. (1999) on snowmelt modeling; Wallbank et al. (2020) on SWE derivation methods.