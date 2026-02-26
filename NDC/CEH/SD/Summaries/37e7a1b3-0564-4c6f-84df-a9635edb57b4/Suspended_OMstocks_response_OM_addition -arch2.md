# Suspended organic matter stocks of Welsh upland rivers in response to organic matter addition

- Aim and context
  - Investigates how suspended organic matter (SOM) stocks in Welsh upland rivers respond to additions of leaf litter.
  - Uses a standardised monitoring-style study design to enable assessment of environmental health over time.

- Experimental design
  - Before-after-control-impact (BACI) setup.
  - Each stream divided into an upstream reference zone and a downstream experimental zone, with 20–50 m between zones to maintain independence.
  - Before period (T1): 61–65 days (early Nov 2012 to early Jan 2013) with no manipulation; both zones treated equally.
  - After period (T2): 57–62 days (early Jan 2013 to Mar 2013) with the experimental zone receiving leaf litter additions.
  - Leaf litter treatment: 1 t bags (oak, birch, alder) added above the experimental zone; vegetable nets maintained to keep minimum wet weight; additional 630 kg (wet weight) added on two storm-event dates (12 Feb and 5 Mar 2013).

- Sampling and treatments
  - SOM sampling at the downstream end of each reach on each occasion.
  - Method: filter 100 L of water through a stacked 10 µm and 1 mm mesh to collect SOM (3 replicates per site).
  - Samples refrigerated (~4°C), frozen within 24 h, freeze-dried (-20°C for 48–72 h), weighed to 0.0001 g.
  - Subsampled (3 mg ±0.3 mg) for elemental (C, N) and stable isotope (δ13C, δ15N) analyses.
  - Inorganic content corrected using an ash-free conversion factor (ash content determined by combusting a subset at 550°C for 5 h).

- Data collection and units
  - Measurements include coarse particulate organic matter (CPOM) and fine particulate organic matter (FPOM).
  - Units: grams per sample, concentrations (mg L⁻¹), and other derived metrics.
  - Time reference variables: site_code, landuse, region, time (Before/After), sampling month, date, and time.

- Analytical methods and quality control
  - Weighting of organic matter stocks to the nearest 0.01 g.
  - Subsamples analyzed for carbon and nitrogen content and δ13C/δ15N values.
  - Quality control includes inorganic content correction via ash furnace technique and clear documentation of replicate structure.

- Data structure and variables
  - Data stored as flatbed CSV files.
  - Core dataset includes 33 columns with fields such as:
    - site_code, landuse, region, time, date, time, discharge (L s⁻¹), reach (Experimental or Control), replicate (A–F), cpom.g.per.sample, cpom.afdm.mg.l, cpom.d13C, cpom.d15N, cpom.N, cpom.C, fpom.g.per.sample, fpom.afdm.mg.l, fpom.d13C, fpom.d15N, among others.
  - Detailed column descriptions cover CPOM/FPOM measurements, concentrations, subsample weights, and isotopic compositions.

- Supporting data
  - DURESS_CU_site_description.csv provides site-level metadata: Site_code, Name, coordinates (Eastings/Northings, Latitude/Longitude), Elevation, Survey, Catchment, etc.
  - Data include site-specific context for mapping and spatial analyses.

- Practical implications for monitoring and policy
  - Demonstrates a standardised monitoring approach to quantify SOM stocks and responses to organic matter input.
  - Produces rich, structured datasets suitable for reporting, mapping, and trend analysis over time.
  - Data are prepared for upload to monitoring portals, enabling broader access and reuse by researchers and policymakers.

- Relationships to the broader monitoring challenges
  - Aligns with the goal of increasing dataset value by integrating SOM data with other environmental datasets.
  - Provides a transparent, reusable data framework to facilitate broader access and secondary analyses.