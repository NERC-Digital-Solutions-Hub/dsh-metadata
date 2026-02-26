# Suspended organic matter stocks of Welsh upland rivers in response to organic matter addition

## Overview
- Investigates suspended organic matter (SOM) stocks in Welsh upland rivers and how they respond to added leaf litter.
- SOM is partitioned into coarse (CPOM) and fine (FPOM) organic matter, with elemental (C, N) and stable isotope (δ13C, δ15N) analyses.
- Data are collected to enable spatial-temporal analysis of SOM dynamics in relation to experimental manipulation and river reach characteristics.

## Experimental design
- BACI (before-after-control-impact) design across multiple streams.
- Each stream has:
  - Upstream reference zone (control) and downstream experimental zone, with 20–50 m separation to ensure independence.
- Time periods:
  - Before period (T1): ~61–65 days, Nov 2012 to Jan 2013; January samples included.
  - After period (T2): ~57–62 days, Jan 2013 to Apr 2013; February–April samples included.
- Manipulation during T2:
  - Addition of leaf litter to the experimental zone using one-tonne bags (oak, birch, alder) proportioned by zone area; minimum wet weight target ~1.7 kg/m2.
  - Additional leaf litter (630 kg wet weight) added on 12 Feb and 5 Mar 2013 after two storm events.
- Structure ensures comparability between zones and periods.

## Data collection and laboratory procedures
- SOM collection:
  - Sampling at the lower end of each reach; 100 L of stream water filtered through 10 µm and 1 mm meshes.
  - Samples refrigerated (~4°C), frozen within 24 h, freeze-dried, and weighed (to 0.0001 g).
- Analytical methods:
  - Ground, homogenised, and subsampled (3 mg ±0.3 mg) for elemental (C, N) and stable isotope (δ13C, δ15N) analysis using mass spectrometry.
  - Inorganic content correction via ash-free conversion (subset combusted at 550°C for 5 h).
- Units and measures:
  - CPOM and FPOM quantified per sample (grams) and as concentrations (mg/L); additional subsample data for isotopes and elements.

## Data structure and content
- Data stored as flat CSV files; SOM dataset comprises 33 columns.
- Key fields include:
  - site_code, landuse, region, time (Before/After), date, discharge (L/s), reach (Experimental/Control), replicate (A–F).
  - CPOM metrics: cpom.g.per.sample, cpom.afdm.mg.l, cpom.d13C, cpom.d15N, cpom.ug.C.per.subsample, cpom.ug.N.per.subsample, cpom.subsample.wt.ug, etc.
  - FPOM metrics: fpom.g.per.sample, fpom.afdm.mg.l, fpom.d13C, fpom.d15N, fpom.ug.C.per.subsample, etc.
- Purpose: enables detailed spatial-temporal analyses and cross-site comparisons, with linking to discharge and sampling context.

## Site information and geographic context
- Supporting site description file (DURESS_CU_site_description.csv) with:
  - site_code, Name, Eastings, Northings, Grid, Latitude, Longitude, Elevation, Survey, Catchment.
- Provides precise geospatial coordinates (British National Grid and WGS84) for GIS mapping and integration with other spatial datasets.

## Quality control and provenance
- Ash-free correction for inorganic content to improve organic matter estimates.
- Replicate coding (A–F) allows assessment of within-reach variability.
- Clear separation of Before/After periods and Reach type (Experimental vs Control) supports robust interpretation.

## GIS-relevance and practical applications
- Rich, georeferenced time-series data suitable for map-based visualization of SOM dynamics across streams and seasons.
- Can be integrated with land-use, catchment, and hydrography data to explore spatial drivers of SOM stocks.
- Highlights typical GIS challenges for ecogeochemical datasets: multi-source data, varying formats, and the need for standardized, linked spatial-temporal data products.