# Suspended organic matter stocks of Welsh upland rivers in response to organic matter addition

- Experimental design
  - Before-after-control-impact (BACI) setup with each stream divided into an upstream reference zone and a downstream experimental zone, separated by 20–50 m for independence.
  - Time periods: before (T1) 61–65 days (Nov 2012–Jan 2013) with no manipulation; after (T2) 57–62 days (Jan–Mar 2013) with leaf litter addition in the experimental zone.
  - Leaf litter addition: 1 tonne bags containing oak, birch, and alder leaves added above the experimental zone proportional to zone area; bags maintained a minimum wet mass of 1.7 kg/m2; additional 630 kg (wet weight) of leaf litter added on 12 Feb and 5 Mar 2013 after storm events.
  - A short stretch between zones to maintain independence; both zones originally similar in habitat, slope, flow, substratum, and land use.

- Data collection and measurements
  - Suspended Organic Matter (SOM) sampling: 100 L of stream water per sample filtered through 10 µm and 1 mm meshes, at the lower end of each reach (n = 3 per sampling event).
  - Sample handling: filters refrigerated at ~4°C, then frozen within 24 h; freeze-dried at -20°C for 48–72 h; ground and subsampled (3 mg ± 0.3 mg) for elemental (C, N) and stable isotopes (δ13C, δ15N) analysis via mass spectrometry.
  - Inorganic content correction: subset samples combusted at 550°C for 5 h to apply ash-free conversion factors.
  - Field and lab equipment: water filtration setup; storage and lab facilities include UC Davis Stable Isotope Facility for isotope analysis.

- Data structure and variables
  - Data stored as flat CSV files with 33 columns for SOM data, including:
    - site_code, landuse, region, time (Before/After), month, date, time, discharge (L/s)
    - reach (Experimental or Control), replicate (A–F)
    - CPOM (coarse particulate organic matter) metrics: g/sample, AFDM g/sample, concentration mg/L, subsample weight µg, C and N content, δ13C, δ15N, related comments
    - FPOM (fine particulate organic matter) metrics: g/sample, AFDM g/sample, concentration mg/L, subsample weight µg, C and N content, δ13C, δ15N, related comments
  - Supporting metadata: site descriptions file with site_code, name, coordinates (Eastings/Northings, Latitude/Longitude), grid reference, elevation, survey campaign, catchment region.

- Quality control and processing
  - Inorganic content correction via ash-free conversion for SOM samples.
  - Consistent sample handling, storage, and preparation protocol to ensure comparability across sites and time periods.
  - Replication scheme (replicates A–F) to support variability assessment and statistical analysis.

- Supporting documentation and data availability
  - Supporting document: DURESS_CU_site_description.csv providing site descriptions and geospatial context (site_code, name, grid references, latitude/longitude, elevation, survey campaign, catchment).
  - Data format and unit standardization designed for data reuse and cross-study integration, with clearly defined variable names and metadata.

- Relevance for data leaders
  - Demonstrates a well-documented, controlled field experiment with a clear data lifecycle: collection, processing, storage in a consistent format (CSV), and comprehensive metadata.
  - Emphasizes data discoverability and interoperability through standardized units, column naming, and accompanying site description data.
  - Highlights potential data governance considerations: ensuring consistency across replicates, managing time-series data across before/after periods, and maintaining provenance of sample processing steps (freeze-drying, combustion, isotopic analysis).
  - Provides a model for integrating ecological measurements (SOM, CPOM, FPOM, isotopes) with robust experimental design to support meta-analyses and broader data community collaboration.