# Suspended organic matter stocks of Welsh upland rivers in response to organic matter addition

- Aim
  - Examine how adding leaf litter affects suspended organic matter stocks (SOM) in Welsh upland rivers.
  - quantify components (CPOM and FPOM) and their carbon and nitrogen content, plus stable isotopes (delta-13C, delta-15N) to identify sources and processing.
  - use a BACI framework to detect downstream responses relative to upstream references and to inform predictive understanding of organic matter dynamics.

- Experimental design
  - Before-after-control-impact (BACI) setup with each stream divided into upstream reference and downstream experimental zones.
  - Zones chosen to be similar in length, habitat structure, slope, flow, substratum, and land use; ~20–50 m separation to ensure independence.
  - Time periods:
    - Before period (T1): ~61–65 days from early November 2012 to early January 2013; both zones untreated.
    - After period (T2): ~57–62 days from early January 2013 to March 2013; experimental zone receives leaf litter manipulation.
  - Leaf litter addition:
    - 1 tonne bags of deciduous leaves (oak, birch, alder) added to experimental zone at start of T2, with proportions by zone area to maintain natural distribution.
    - Vegetable nets used to maintain minimum wet weight (~1.7 kg m-2) of leaf litter; bags fixed in the experimental reach.
    - Leaf packs reflectively simulate senescence/abscission in wooded catchments; two large storm events prompted additional litter additions (12 Feb 2013 and 5 Mar 2013), totaling ~630 kg (wet weight) per stream after storms.

- Sampling and collection methods
  - Suspended Organic Matter (SOM) defined as particles >10 µm and <1 mm.
  - Sampling points at the lower end of each reach; 100 L of stream water filtered through 10 µm and 1 mm filters (n = 3 per sample).
  - Samples refrigerated at ~4°C, frozen within 24 h, then freeze-dried (-20°C, 48–72 h) and weighed to 0.0001 g.
  - Subsamples ground and analyzed for elemental C and N and stable isotopes (d13C, d15N) by mass spectrometry.
  - Inorganic content corrected by combusting a subset at 550°C for 5 h and applying an ash-free correction factor.

- Analytical methods and data scope
  - Weightings of organic matter reported to 0.01 g.
  - NOM/organic matter split into:
    - CPOM (coarse particulate organic matter) measurements:
      - cpom.g.per.sample, cpom.afdm.mg.l, cpom.ug.C.per.subsample, cpom.ug.N.per.subsample, cpom.d13C, cpom.d15N, etc.
    - FPOM (fine particulate organic matter) measurements:
      - fpom.g.per.sample, fpom.afdm.mg.l, fpom.ug.C.per.subsample, fpom.ug.N.per.subsample, fpom.d13C, fpom.d15N, etc.
  - Additional fields per sample include discharge (L/s), time, date, month, replicate code, site code, land use, region, reach (Experimental or Control).
  - Data structure comprises flat CSV files with 33 columns for SOM and related metrics; a separate site description file provides coordinates and catchment context.

- Sites, replication, and metadata
  - Multiple streams with replicated measurements (replicates A–F).
  - Site metadata include land use, region, and precise geolocation (site_code, Eastings, Northings, Latitude, Longitude, Elevation, etc.).
  - Supporting site description data available separately to contextualize sampling locations.

- Quality control and data notes
  - Described quality control is limited; inorganic correction via ash-based method applied to subset samples.
  - Data captured as a time-series across before/after periods and across upstream/downstream reaches, enabling BACI-style analyses while accounting for discharge and replicate variation.

- Potential analyses and applications
  - Compare upstream reference vs downstream experimental zones to quantify the effect of added leaf litter on SOM stocks.
  - Assess differences in CPOM vs FPOM response and associated carbon and nitrogen content and isotopic signatures.
  - Explore temporal dynamics across T1 and T2, including responses to storm-driven litter additions.
  - Use discharge and site metadata to model drivers of OM stocks and to infer changes in organic matter sources and processing within upland river systems.
  - Data suitable for cross-stream synthesis and integration with broader environmental datasets, given detailed site and sampling metadata.