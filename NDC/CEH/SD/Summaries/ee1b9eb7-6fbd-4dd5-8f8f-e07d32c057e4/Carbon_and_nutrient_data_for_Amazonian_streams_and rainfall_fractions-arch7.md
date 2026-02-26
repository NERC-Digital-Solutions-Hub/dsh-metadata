# Sampling Regime

- Geographic and temporal scope
  - Western Amazonian basin, Tambopata National Reserve, Madre de Dios region, Peru (approx. 12°49'54.30"S, 69°16'52.37"W)
  - Data collected Feb 2011–May 2012
  - Targeted hydrological seasons (wet and dry) across two small streams (NC, MT) and two rivers (LT, TP)

- Sites and catchments
  - Streams: NC (New Colpita) and MT (Main Trail)
  - Rivers: LT (La Torre) and TP (Tambopata)
  - NC stream: 4.5–7.5 m wide; upstream catchment ~7.2 km2
  - MT stream: 3.5–5 m wide; upstream catchment ~4.9 km2
  - LT catchment upstream ~2000 km2; TP upstream ~14000 km2
  - MT often dries in dry season; NC maintains flow

- Datasets included
  - Streams and rivers data
    - Analytes: DIC (mg/L) with δ13C-DIC, DOC (mg/L), POC (mg/L), Ca, Mg, K, Na (mg/L), P (μg/L), Si (mg/L)
    - Site coverage: NC, MT, LT, TP
    - Data counts: NC DIC 172 points; MT DIC 104; LT DIC 126; TP DIC 77 (similarly for δ13C-DIC, DOC, POC, etc.)
  - Rainfall fractions data
    - Analytes: DIC, δ13C-DIC, DOC, POC, Ca, Mg, K, Na, P, Si
    - Fractions: Rain water, Throughfall, Stemflow, Overland flow
    - Data counts: Rain water DIC 5 points; Throughfall 8; Stemflow 10; Overland flow 8 (and similarly for other analytes)

- Sampling campaigns and collection methods
  - Field campaigns: Feb–Apr 2011; Sept–Dec 2011; Mar–May 2012
  - Targeted different flow conditions to understand hydrological controls on carbon and nutrients
  - Description of sampling protocols for DIC, DOC, POC, nutrients, and isotopic measurements
  - MT dries up during dry season; NC used for year-round sampling

- Analytical methods and quality control
  - DIC: headspace method on Gas Bench/Delta V Plus; δ13C-DIC
  - DOC: filtration, acidification to pH 3.9, degassing, combustion TOC
  - POC: loss on ignition from filtered filter papers
  - Ca, Mg: Atomic Absorption Spectrometry (AAS)
  - K, Na: Flame photometry
  - TotP: Colorimetric phosphomolybdate-ascorbic acid method
  - Si: Colorimetric heteropoly blue method
  - Quality control:
    - Drift-correcting standards every ~10 samples
    - Replicates and randomised order
    - Calibration checks and drift standards for DOC, cations, and Si/totP
    - Subset calibration checks for consistency

- Data structure and formats
  - Files: "Amazon streams C and nutrients" and "Amazon rainfall fractions C and nutrients"
  - Streams and rivers dataset: 14 columns
  - Rainfall fractions dataset: 12 columns
  - Common fields (Streams and Rivers)
    - Time (hh:mm:ss), Date (dd/mm/yyyy), Type (stream or river), Site (MT, NC, LT, TP), CollectorID (TF=throughfall, SF=stemflow, OF=overland flow, RW=rain water)
    - Measurements: DOC, POC, DIC, δ13C-DIC, Ca, Mg, K, Na, TotP, Si
  - Common fields (Rainfall fractions)
    - Time, Date, Type (TF, SF, OF, RW), CollectorID (TF numerical; SF tree name; OF stream; RW EI)
    - Measurements: DOC, POC, DIC, δ13C-DIC, Ca, Mg, K, Na, TotP, Si
  - Data notes
    - NA indicates data not analysed
    - Units follow standard methods in the documentation

- Notes on data interpretation for GIS
  - Spatial context available via site locations and catchment extents
  - Temporal coverage across multiple campaigns enables time-series mapping
  - Data readiness for GIS: ready-to-map variables include DIC, δ13C-DIC, DOC, POC, major ions, TotP, Si, and rainfall-flow fractions
  - Some data gaps exist (NA entries) and MT’s dry-season gaps due to seasonality

- References and data provenance
  - Prior data submissions referenced with DOIs:
    - DIC and other carbon data: DOI 10.5285/507a5e1f-e056-454c-8ff6-d185f3da8556
    - Rivers DIC data (with flux chamber and velocity measurements): DOI 10.5285/02d5cea7-10aa-4591-938a-a41e1c5bc207
  - Analytical method references:
    - American Public Health Association (1999) Standard Methods
    - Waldron et al. (2014) on DIC isotopic composition measurements