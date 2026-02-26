# Suspended organic matter stocks of Welsh upland rivers in response to organic matter addition

## Aim and study design
- Investigates how suspended organic matter (SOM) stocks respond to added leaf litter in Welsh upland rivers.
- Experimental design: before-after-control-impact (BACI) with each stream split into:
  - Upstream reference (control)
  - Downstream experimental (receives leaf litter)
- Time periods:
  - Before period (T1): 61–65 days, Nov 2012–Jan 2013; no manipulation
  - After period (T2): 57–62 days, Jan–Mar 2013; experimental zone receives leaf litter
- Independent treatment details:
  - Leaf litter bags (one tonne) containing oak, birch, alder leaf litter added proportionally to experimental zone
  - Vegetable net bags maintained to ensure minimum wet weight; leaf packs reflect naturally occurring litter
  - Additional 630 kg (wet weight) of leaf litter added on two storm-flow events (12 Feb and 5 Mar 2013)
- Experimental independence: 20–50 m between reference and experimental zones; similar habitat and land use within each stream

## Data collected and collection methods
- Primary metric: Suspended Organic Matter (SOM) sampled from the lower end of each reach
- Sampling method:
  - Filter 100 L of water through 10 µm and 1 mm mesh filters (n = 3 per sampling occasion)
  - Samples refrigerated (~4°C), frozen within 24 h, then freeze-dried (-20°C, 48–72 h)
  - Ground, homogenised, subsampled (3 mg ±0.3 mg) for analysis
  - Analyses: elemental (C, N) and stable isotopes (δ13C, δ15N) via mass spectrometry
  - Inorganic content correction: ash-free conversion factor derived from combusting a subset of samples at 550°C for 5 h
- Scheduling: samples collected during T1 (before manipulation) and T2 (after manipulation) for each reach

## Data structure and content
- Data format: flatbed comma-separated value (CSV) files
- Core SOM data columns (33 total) include:
  - site_code: site identifier; landuse; region (basin, catchment)
  - time indicators: time (Before/After), sampling month, date, and time of measurement
  - discharge: water discharge in L s⁻¹
  - reach: Experimental or Control
  - replicate: replicate code (A–F)
  - cpom.g.per.sample: coarse particulate organic matter per grab sample (g)
  - cpom.afdm.mg.l: CPOM concentration in water (mg/L)
  - cpom.d13C, cpom.d15N: stable isotope values; cpom.ug.C.per.subsample, cpom.ug.N.per.subsample: elemental content per CPOM subsample
  - cpom.subsample.wt.ug: CPOM subsample weight (µg)
  - cpom.d15N/comment: comments on d15N
  - fpom.g.per.sample, fpom.afdm.mg.l, fpom.d13C, fpom.d15N, and related subsample and elemental columns analogous to CPOM for fine particulate organic matter
  - Additional fields cover volumes filtered, ash-free dry mass (AFDM) context, and related metadata
- Additional supporting data: site description file (Site_code, Name, Eastings/Northings, Grid, Latitude/Longitude, Elevation, Survey, Catchment)

## Units and quality control
- Recorded units include:
  - CPOM/FPOM per sample (grams); AFDM mass (grams)
  - Concentrations (mg/L)
  - Subsample weights (µg)
  - Carbon/Nitrogen content (µg per subsample)
  - Isotopic ratios (δ13C, δ15N in per mil)
  - Discharge (L s⁻¹)
- Quality control measures:
  - Inorganic correction of SOM via ash-free conversion factor
  - Documentation of sample handling (refrigeration, freeze-drying, grinding, homogenisation)
  - Metadata capturing sampling times, locations, and replication to enable reproducibility

## Data accessibility and potential use
- Data are organized for self-serve analysis and cross-site comparisons:
  - Time-series capture of SOM components before and after organic matter addition
  - Spatially distributed data across paired reference and experimental reaches
- Potential data products for users:
  - BACI-style analyses of SOM responses to leaf litter addition
  - Time-resolved trends of CPOM and FPOM stocks and concentrations
  - Isotopic and elemental signatures to trace organic matter sources and processing
  - Geospatial mapping of site characteristics (land use, catchment) with SOM metrics
- Related materials:
  - Site descriptions provide contextual location data for mapping and aggregation across catchments