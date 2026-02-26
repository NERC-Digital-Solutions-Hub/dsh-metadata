# Suspended organic matter stocks of Welsh upland rivers in response to organic matter addition

- Aim and context
  - Investigates how suspended organic matter (SOM) stocks in Welsh upland rivers respond to added organic matter (leaf litter) using a controlled BACI design.
  - Seeks to quantify environmental health indicators related to organic matter dynamics and inform monitoring decisions.

- Experimental design
  - Before-after-control-impact (BACI) setup: each stream divided into an upstream reference zone and a downstream experimental zone.
  - Zones similar in length, habitat structure, slope, flow, substratum, and land use; minimum 20–50 m between zones to ensure independence.
  - Time periods: before period (T1) lasting 61–65 days (early Nov 2012 to early Jan 2013) with no manipulation; after period (T2) lasting 57–62 days (early Jan to Mar 2013) with leaf litter addition in the experimental zone.
  - Leaf litter manipulation: ~1 tonne bags of oak, birch, and alder leaves placed above the experimental zone to simulate natural senescence; additional 630 kg (wet weight) of leaf litter added after two storm events (12 Feb and 5 Mar 2013).

- Sampling regime
  - Sampling locations: lower end of each reach; samples collected on each occasion.
  - Reference vs experimental: labels used to distinguish upstream reference zone and downstream experimental zone throughout data collection.
  - Replication: multiple replicates per site (replicate codes A–F).

- Collection and processing of suspended organic matter
  - SOM defined as particles >10 µm and <1 mm.
  - Sampling method: filter 100 L water through stacked 10 µm and 1 mm meshes; samples refrigerated (~4°C), then frozen and later freeze-dried for analysis.
  - Processing: freeze-dried SOM ground and subsampled for elemental and stable isotope analysis (C, N, δ13C, δ15N) via mass spectrometry; inorganic content corrected by ash-free conversion using combustion at 550°C for 5 h on a subset of samples.

- Analytical methods and quality control
  - Measurements include coarse (CPOM) and fine (FPOM) particulate organic matter, reported as grams per sample and ash-free dry matter (AFDM) equivalents.
  - Concentrations reported as mg/L; subsample weights and derived isotopic and elemental contents (C, N) included for each subsample.
  - Isotopic corrections and calibration performed via standard lab procedures (mass spectrometry).
  - Quality controls include correction for inorganic content and standardized sample processing to ensure comparability across sites and times.

- Data structure and content
  - Data format: flatbed CSV files; structured with 33 columns for SOM data.
  - Key columns include:
    - site_code, landuse, region, time (Before/After), date, time, discharge (L/s)
    - reach (Experimental or Control), replicate (A–F)
    - CPOM and FPOM metrics: g per sample, AFDM per sample, concentration (mg/L), subsample weight (µg), carbon and nitrogen contents (µg), and δ13C/δ15N values, plus any comments
  - Separate, supporting metadata: DURESS_CU_site_description.csv containing site-level metadata (Site_code, Name, coordinates, grid references, latitude/longitude, elevation, survey campaign, catchment)

- Supporting data and governance
  - Supporting site description file provides essential metadata for data provenance and geographic context.
  - Dataset design emphasizes traceability from field collection through laboratory analysis to final variables, aiding reproducibility and monitoring utility.
  - Metadata availability and detailed data structure facilitate integration into monitoring frameworks and open data sharing, addressing common barriers such as incomplete metadata and data standardization.

- Relevance for monitoring frameworks (archetype perspective)
  - Demonstrates a robust monitoring design (BACI) to attribute ecological responses to a controlled environmental input.
  - Highlights the importance of clear definitions of zones, temporal sequencing, and standardized sampling protocols.
  - Shows comprehensive data management, including detailed variable definitions, unit clarity, isotopic and elemental analyses, and accompanying site metadata—critical for evaluating environmental health measures and informing policy decisions.