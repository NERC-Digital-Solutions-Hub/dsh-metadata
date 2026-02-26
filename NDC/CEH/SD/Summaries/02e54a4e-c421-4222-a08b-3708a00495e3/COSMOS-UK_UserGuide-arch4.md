# COSMOS-UK User Guide

- COSMOS-UK delivers UK-wide near real-time soil moisture data using cosmic-ray neutron sensors that cover large footprints (tens to hundreds of hectares) and sit above ground, enabling automated remote monitoring without on-site intrusion.
- Primary goal: empower environmental research and modelling (meteorology, water resources, flood warnings, crop management, greenhouse gas flux studies) with soil moisture information and related environmental variables.

## What data COSMOS-UK provides

- Monitored data (cadence and variables)
  - Precipitation (1 min)
  - Absolute humidity (30 min)
  - Relative humidity (30 min)
  - Air temperature (30 min)
  - Atmospheric pressure (30 min)
  - Incoming/outgoing shortwave and longwave radiation (30 min)
  - Wind direction and wind speed (30 min; 3D wind components available)
  - Snow depth and Snow Water Equivalent (SWE)
  - Volumetric water content (VWC) from IMKO Profile at depths (15 cm, 40 cm, 65 cm)
  - Soil heat flux (two sensors; 30 min)
  - Soil temperature at five depths (2 cm, 5 cm, 10 cm, 20 cm, 50 cm; 30 min)
  - Profile soil moisture sensors (TDT; 10 cm and additional depths; 30 min)
- Derived data
  - Net radiation (derived from component fluxes; 30 min)
  - CRNS-derived VWC (daily/hourly; CRNS counts corrected to produce VWC)
  - Typical CRNS sensing depth (D86) and an evidence-based footprint characterization (distance-dependent)
  - Corrected neutron counts from CRNS
  - Potential evaporation (daily)
- Data status
  - Data are provisional and may be revised; licensing terms apply
  - Graphs and standard retrievals available on COSMOS-UK website; data accessible via CEH Environmental Information Data Centre (EIDC)

## How data are produced and processed

- Processing chain
  - Raw sensor data are logged and transmitted; automatically converted to usable formats
  - Level 1 data undergo automated QC tests; Level 2 data are produced after quality checks
  - Data processing converts CRNS neutron counts to soil moisture (VWC) using calibration methods and site-specific parameters
  - Averaging and aggregation (e.g., hourly to daily) to reduce noise and produce stable VWC values
- Calibration and methods
  - Site-specific N0 calibration derived from field calibration; uses a generic soil matrix for conversion from corrected counts to VWC
  - Correction factors account for atmospheric pressure, water vapor, altitude, and cosmic ray intensity
  - Methods used to derive VWC include site-specific N0, hydrogen molar fraction (hmf), and neutron transport modelling; COSMOS-UK predominantly uses site-specific N0 with calibration
- Footprint and depth
  - CRNS footprint typically extends hundreds of metres; effective depth varies with soil moisture (roughly 10–80 cm; often 15–40 cm for typical conditions)
  - D86 provides depth to which 86% of detected neutrons have interacted with soil; used to inform sampling and interpretation
- Updates and improvements
  - 2018: introduction of a site-specific gamma correction factor to remove spurious trends
  - Processing method revisions applied to all sites for consistency; legacy methods may still be in the background

## Data quality, limitations, and challenges

- Quality control
  - Two-stage QC: automatic tests (Table 6.1) and daily visual inspection of plots
  - Level 1 data are filtered; Level 2 data retain a record of flagged/removed values
  - Common QC flags include zero data where not possible, out-of-range values, sensor faults, diagnostic flags, and spike or error codes
- Gap handling
  - Currently no automatic gap filling; gaps may occur due to instrument, logging, or communication failures
- Data reliability and peat soils
  - VWC estimates can be less reliable in peat soils (very high organic matter; potential for higher VWC values and data loss)
  - Daily VWC values have improved with revised averaging methods but caution is advised for peat-derived sites
- Comparison with other sensors
  - CRNS data are noisier than point sensors (e.g., TDT); however, CRNS covers larger areas
  - TDT sensors provide less noisy local measurements; differences across sensors can reflect true spatial variability or sensor differences
- Data completeness and availability
  - Data availability can vary by site and year; some data are provided with a lag and may be revised

## Accessing and using COSMOS-UK data

- Primary access
  - CEH Environmental Information Data Centre (EIDC): http://eidc.ceh.ac.uk/
  - Data uploaded in annual tranches; typically 1–2 years behind current upload date
  - Data requests for non-EIDC items considered on a reasonable effort basis
  - Data are provisional and licensed; CEH disclaims liability for use
- Display and retrieval
  - Live data graphs available on the COSMOS-UK website (precipitation, air temperature, soil moisture from CRNS or neutron counts)
  - Standard graphical retrievals provided (see Appendix D)
  - Embedding plots in websites via a simple URL-based service (see Appendix E)
- Documentation and site metadata
  - Appendix A lists expanded site properties (location, start date, soil type, bulk density, organic matter, land cover)
  - Appendix B shows data availability by variable group and year
  - Appendix C describes phenocams (for vegetation and surface conditions)
  - Appendix D–G cover standard plots, quality control, and graphical retrievals

## Site network design and scope

- UK-wide network
  - Sites selected to sample varied climate, soil types, land cover, and geology
  - Clustering to analyze regional and national variability
- Site selection factors
  - Positive: geographic coverage, environmental diversity, high soil moisture variability, long-term permissions, access ease, mobile data connectivity
  - Negative: proximity to open water or perched groundwater, vandalism risk
- Site details
  - A substantial list of sites across the UK (e.g., Rothamsted, Rothamsted; The Lizard; Glensaugh; etc.) with calibration status, coordinates, altitude, and soil/land-cover metadata

## Practical takeaways for Data Leaders

- Governance and strategy
  - COSMOS-UK provides a scalable, non-intrusive, large-footprint soil moisture monitoring capability suitable for model validation, data assimilation, and inter-organisational collaborations
  - Data are provisional, carefully QC’d, and subject to revisions; ensure governance for using provisional data in decision-making
- Data integration and systems
  - Data available via EIDC with a latency of 1–2 years; consider integration pipelines that accommodate data liaison, licensing, and versioning
  - Derived CRNS VWC products complement point sensors (TDT) for broader spatial context; plan for cross-validation
- Data quality and risk management
  - Expect noise in CRNS-derived VWC; rely on daily means and, where peat soils are involved, apply cautious interpretation
  - Be aware of potential gaps and plan for redundancy with in situ sensors or alternative data sources
- Opportunities and collaboration
  - COSMOS-UK supports collaboration for data assimilation, model validation, drought/flood forecasting, and broader environmental science applications
  - Engagement with the COSMOS-UK project can enable access to data, methods, and potential co-authored research

## Contact and further information

- COSMOS-UK project contact: cosmosuk@ceh.ac.uk
- CEH locations and core contacts: listed in the guide (Wallingford, Edinburgh, Bangor, Lancaster, etc.)
- Additional resources: site-by-site metadata, data availability appendices, standard graphical retrievals, and embedding tools described in the appendices