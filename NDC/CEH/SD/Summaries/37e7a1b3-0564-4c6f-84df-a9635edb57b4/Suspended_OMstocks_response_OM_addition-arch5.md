# Suspended organic matter stocks of Welsh upland rivers in response to organic matter addition

## Overview
- A BACI (before-after-control-impact) study with upstream reference zones and downstream experimental zones in multiple streams.
- Objective: quantify how suspended organic matter stocks respond to the addition of leaf litter (oak, birch, alder).
- Experimental timeline: before period (T1; 61–65 days) with no manipulation; after period (T2; 57–62 days) with leaf litter additions. Leaf litter added initially in January 2013 and supplemented with two additional large additions after storm events in February and March 2013.
- Data collected include measurements of suspended organic matter (SOM), coarse and fine particulate organic matter (CPOM/FPOM), and their carbon and nitrogen content, including stable isotope ratios (delta-13C, delta-15N).

## Experimental design
- Each stream contains:
  - An upstream reference (control) zone
  - A downstream experimental (manipulated) zone
- Zones of similar length and habitat structure (riffle, glide, pool) with 20–50 m separation to ensure independence.
- Leaf litter deployment: one tonne bags placed above the experimental zone and below the reference zone; additional wet weight maintenance to ensure minimum litter levels; two extra 630 kg additions during the study.

## Data collected and methods
- Suspended Organic Matter (SOM): collected by filtering 100 L of water through 10 µm and 1 mm mesh filters; samples refrigerated at ~4°C, then frozen and freeze-dried for analysis.
- Analytical workflow:
  - Dry weight measurement to the nearest 0.01 g.
  - Subsampling (≈3 mg ±0.3 mg) for elemental composition (carbon, nitrogen) and stable isotopes (delta-13C, delta-15N) via mass spectrometry.
  - Inorganic content correction by ash-free conversion: combusting a subset at 550°C for 5 h.
- Units and components recorded:
  - CPOM and FPOM concentrations and masses (g per sample, mg/L, etc.).
  - Subsample weights, elemental contents (C, N), isotopic values (d13C, d15N), and related comments.
- Field and lab setup: use of a water filter system; standard handling and preservation prior to analysis.

## Data structure and variables
- Data format: flat CSV files.
- Key data file: Suspended organic matter data with 33 columns, including:
  - site_code, landuse, region, time (Before/After manipulation), date, time, discharge (L/s), reach (Experimental or Control), replicate (A–F), and multiple CPOM/FPOM metrics.
  - CPOM.g.per.sample, cpom.afdm.mg.l, cpom.d13C, cpom.d15N, cpom.ug.C.per.subsample, cpom.ug.N.per.subsample, cpom.subsample.wt.ug, cpom.d15N comments, and corresponding FPOM fields.
  - Additional metadata fields for each measurement (e.g., subsample weights, volumes filtered, etc.).
- Supporting documentation:
  - Site description file (DURESS_CU_site_description.csv) with site_code, full name, coordinates (Eastings/Northings, latitude/longitude), grid reference, elevation, survey campaign, and catchment.

## Quality control and data processing
- QA measures include:
  - Correction for inorganic content using ash-free conversion factors.
  - Precise gravimetric measurement (to 0.01 g) and standardized preservation (refrigeration at ~4°C; freeze-drying).
  - Controlled subsampling for isotopic and elemental analyses.
  - Clear replication scheme (Replicate codes A–F) to assess variability.
- Documentation of measurement protocols and unit definitions to support reproducibility and cross-study comparability.

## Data availability and sharing
- Data are organized for interoperability and reuse, with explicit field names and units.
- Metadata-rich data structure (sampling times, treatment status, site attributes, and replicate information) to support discoverability and context for reuse.
- Supporting site metadata enhances spatial context and enables integration with other datasets (e.g., land use, catchment characteristics).

## Documentation and provenance
- Experimental protocol described (BAC I design, timing of before/after periods, litter addition strategy, and storm-event-driven additions).
- Sample handling and analytical methods documented to ensure traceability from field collection to final measurements.
- Site-level documentation exists to provide geographic and catchment context.

## Potential data governance considerations for reuse
- Ensure consistent interpretation of the time indicator (Before/After manipulation) across sites.
- Maintain the integrity of the replicate coding (A–F) when aggregating data.
- Preserve the linkage between SOM measurements and CPOM/FPOM components, along with isotopic data, to support multi-metric analyses.
- Consider updating or enriching metadata with any future data additions (e.g., additional leaf litter events or extended time series).
- Recognize measurement specifics (e.g., units, ash-free corrections, sample volumes) to maintain comparability with other datasets.