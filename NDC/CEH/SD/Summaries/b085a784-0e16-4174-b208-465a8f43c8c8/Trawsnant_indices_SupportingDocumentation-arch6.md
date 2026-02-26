# Experimental Design/Sampling Regime/Collection Methods

- Context and purpose
  - Data from the Nant Trawsnant experimental catchment (LI8) near Llyn Brianne, Powys, Wales, UK.
  - Focus on streamflow and pH, with accompanying rainfall, temperature, and NAO index data to enable hydrological and water-quality analysis.
  - All data released via the Environmental Information Data Centre (EIDC) and vetted for IP rights (IPR) by NERC EIDC.

- Catchment and hydro-climate context
  - Contributory areas: streamflow gauging 1.23 km2; upstream pH monitoring 1.21 km2.
  - Geological and soils: Lower Paleozoic shales, mudstones, greywackes, grits; Podzols and Histosols.
  - Land cover: ~88% conifer forest during the data period.
  - Related publications: Jones & Chappell (2014); Jones, Chappell & Tych (2014).

- Data collection and temporality
  - Streamflow and pH: Lancaster University observations at regular 15-minute intervals in 2013; data logged on a Campbell Scientific CR1000.
  - Rainfall: monthly measurements aggregated from multiple Welsh water authorities (1982–2013); gaps filled via correlations with nearby raingauges.
  - Temperature: monthly values from Felindre weather station (near Talgarth); data from Met Office MIDAS (1853–current).
  - NAO index: monthly values from a public source.
  - Calibration and instrumentation: field measurements taken with a pressure transducer for flow and a digital pH sensor; data logged by CR1000.

- Analytical approach and modelling
  - Daily modelling to derive monthly streamflow and pH statistics from observed daily rainfall, using the RIVC algorithm (CAPTAIN Toolbox for Matlab) for model identification.
  - Model validation: 1 January – 31 March 2013 used for identification; 1 April – 31 December 2013 used for validation.
  - Daily models extended back in time (1 April 1982 – 1 April 2013) via the LSIM (Linear Simulation) routine in Matlab to produce daily streamflow and pH data, from which monthly statistics were derived.

- Data processing and quality control
  - Data quality: QA procedures to identify and replace erroneous CR1000 data (e.g., power-related spikes) with NaN.
  - Software and code: Matlab-based implementations for statistical metrics (mean, percentiles, moving min/max, CV, exceedence, pulse metrics, rates of rise/fall, etc.).
  - Availability of code: Examples of functions and methodology are provided (Mean, Median/percentiles, Moving-window calculations, Peak/Range/CoV, growing season, pulse metrics, rate calculations).

- Data structure and contents
  - Data format: a single .csv file with 159 columns of statistical variables (columns 2–5 intentionally blank) and 32 rows.
  - Coverage: statistics for the first day of each month from 1 April 1982 to 1 April 2013.
  - Columns and units: extensive metadata detailing variables such as rainfall and flow statistics (means, percentiles, moving statistics), flow pulse counts and durations, pH statistics, temperature metrics, and growth-season indicators; estimation periods vary (mostly 365 days prior to sampling; some metrics use shorter windows like 30 days or 120 days).
  - Key example variables: Mean Rainfall, Total Rainfall, Mean Flow, Flow percentiles, moving-average minima/maxima of flow, number/duration of high/low flow pulses, average rise/fall rates in flow, Mean pH, pH percentiles, temperature statistics, and growth-season indicators.
  - Documentation: Detailed description of each statistic and its estimation period is provided within the dataset documentation.

- Data provenance and reuse
  - Primary data sources: on-site streamflow (flow), pH sensors, rainfall records from multiple authorities, Felindre temperature data, and NAO index.
  - Metadata and reproducibility: documented modelling workflow (RIVC CAPTAIN toolbox in Matlab) and validation approach; monthly statistics derived from daily simulations; dataset validated and curated with explicit QA steps.
  - Licensing and access: IP rights vetted by NERC EIDC; data intended for broad use and re-use within environmental and hydrological research.