# Suspended organic matter stocks of Welsh upland rivers in response to organic matter addition

## Overview
- A BACI (before-after-control-impact) study across multiple streams to quantify suspended organic matter (SOM) stocks in response to added leaf litter.
- Each stream has an upstream reference zone and a downstream experimental zone, with a short separation to ensure independent treatment.
- Temporal design: before period (T1) ~61–65 days with no manipulation; after period (T2) ~57–62 days with leaf litter addition in the experimental zone.
- Leaf litter (oak, birch, alder) added at the start of T2; additional leaf litter added after storm events in Feb–Mar 2013.
- Aims to support GIS-enabled understanding of spatial patterns in SOM response across Welsh upland rivers.

## Experimental Design & Sampling Regime
- Two zones per stream: upstream reference and downstream experimental, similar in length and habitat; 20–50 m separation between zones.
- Treatments applied only in the experimental zone during T2; reference zones remained untreated.
- Leaf litter distributed proportionally to experimental zone area; leaf packs maintained with leaf litter through the period.
- Additional litter additions occurred on 12 February 2013 and 5 March 2013 after storm events.

## Data Collection & Analytical Methods
- Sampling of Suspended Organic Matter (SOM): collected at the downstream end of each reach by filtering 100 L of stream water through 10 µm and 1 mm filters (n = 3).
- Sample handling: refrigerated at ~4°C, frozen within 24 h, freeze-dried, weighed to 0.0001 g, ground and subsampled for analysis.
- Analyses: elemental composition (C, N) and stable isotopes (δ13C, δ15N) via mass spectrometry; inorganic content corrected by ash-free conversion.
- Reporting units: coarse and fine particulate organic matter reported as grams; additional measurements in mg/L and related subsample metrics.

## Data Structure & Variables
- Data format: flatbed CSV files.
- 33 columns describing suspended organic matter data, including:
  - site_code, landuse, region, time (Before/After), date, sampling month, discharge (L/s), reach (Experimental/Control), replicate (A–F), CPOM and FPOM metrics (g per sample, g per AFDM, mg/L, etc.), subsample weights, carbon and nitrogen contents, δ13C, δ15N, and related comments.
- Key measurements include:
  - CPOM.g.per.sample, CPOM.afdm.mg.l, cpom.d13C, cpom.d15N
  - FPOM.g.per.sample, fpom.afdm.mg.l, fpom.d13C, fpom.d15N
  - Subsample weights and associated isotope/elemental data

## Supporting Materials & GIS-Ready Site Information
- Site Description (site_description.csv) providing geo-referenced context:
  - site_code, Name, Eastings, Northings, Grid, Latitude, Longitude, Elevation
  - Survey campaign and Catchment information
- These data enable GIS mapping and spatial joins with the SOM measurements for spatial analysis and visualization.

## Quality Control & Data Reliability
- Replicate coding (A–F) supports assessment of measurement precision across streams and time.
- Rigorous sample handling and processing (refrigeration, freeze-drying, ash-free conversion) to ensure data quality.
- Standardized analytical workflow for elemental and isotopic composition.

## GIS Applications & How to Use
- Spatial visualization of SOM stocks across Welsh upland streams by reach (experimental vs control) and period (Before vs After).
- Join SOM data with Site Description to create georeferenced maps and perform spatial analyses (e.g., SOM distribution, effects of leaf litter addition, spatial correlation with land use and catchment characteristics).
- Temporal mapping: compare SOM changes between T1 and T2 across streams to identify spatial patterns of response to organic matter addition.
- Integrate with discharge and habitat data to explore relationships between hydrology, channel zone (riffle/glide/pool), and SOM dynamics.