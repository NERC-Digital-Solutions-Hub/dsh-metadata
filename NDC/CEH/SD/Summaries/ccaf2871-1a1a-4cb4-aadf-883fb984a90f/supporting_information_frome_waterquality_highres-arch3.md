# Overview of data

- Objective and scope
  - A high-resolution water quality dataset for the River Frome catchment, Dorset, UK, collected between 12/08/2022 and 14/09/2022.
  - Aimed at informing river water quality management, modelling, and policy scrutiny; supports monitoring framework decisions with detailed, multi-source data.

- Study area and sampling framework
  - 24 measurement sites spanning upstream to downstream reach between Dorchester and East Stoke, including river channels, major tributaries, boreholes, and STW effluents.
  - The campaign was split into two periods: upstream monitoring (12/08/22–30/08/22) and downstream monitoring (30/08/22–14/09/22), with Pallington sampled in both periods.
  - Data collected at high frequency (30-minute) from in-situ sensors, plus grab samples several times per week.

- Determinands and data types
  - High-frequency measurements (continuous/30-minute) of: conductivity, dissolved oxygen (DO), DO%, pH, temperature, turbidity, and nitrate (NO3-N) via UV sensor.
  - Additional high-frequency data: ammonium NH4-N and discharge at STW and EA sites (15-minute intervals from some sources).
  - Grab samples (approximately three times per week) for: alkalinity, ammonium, BOD, chloride, conductivity, DO, nitrate, nitrite, orthophosphate, soluble reactive phosphorus (SRP), total phosphorus, pH, turbidity, and suspended solids.
  - Borehole water quality data for NH4-N, NO3-N, nitrite, and orthophosphate.
  - Data sources include Wessex Water Services Ltd., Environment Agency, and the PhD project team (with support from Meteor Communications Ltd. and University of Bath).

- Data structure and metadata
  - Single CSV file: riverfrome_waterquality_highres_2022 with 13 columns: Date, Time_GMT, Date_time, Site_name, Site_NGR, Site_type, Source, Freq, Determinand, Result, Sign, Censored, Unit.
  - Site locations provided with British national grid references; borehole sites resolved to 1 km accuracy.
  - Determinants and units detailed; measurement uncertainty, reporting limits, and context provided in accompanying sections.

- Experimental design and measurement protocol
  - In-situ sensors: four YSI EXO2 and two EXO3 multisensor sondes measuring conductivity, DO, DO%, pH, temperature, turbidity; EXO2 sondes equipped with NitraLED for NO3-N (and 30-minute frequency).
  - Additional NO3-N data from Nitratax sensors at Louds Mill and East Stoke; NH4-N data from ProAm ammonia monitor at Dorchester STW effluent.
  - Sensors calibrated prior to deployment; automatic self-cleaning wipers; no mid-campaign maintenance due to short deployment.
  - Grab samples analyzed at Wessex Water Scientific Centre; NO3-N and NH4-N analyzed with standard methods; BT/RC/other parameters analyzed as described.
  - 15-minute discharge data from STW effluents and EA hydrology data explorer; river discharge data from Environment Agency.

- Data analysis, quality control and validation
  - Grab samples and continuous data cross-checked using visual time series and target diagram methodology to assess bias and pattern agreement (normalised bias, RMSE′, etc.).
  - Overall good agreement between continuous and grab data; pH showed greater normalised bias; DO disagreements at some sites attributed to local gradients and sampling proximity.
  - Data cleaning: outliers removed or flagged as N/A; negative concentrations eliminated; exclusion of readings when STW flow was too low to wet sensors; removal of large turbidity spikes due to fouling or bubbles.
  - Data wrangling and cleaning performed in R; quality control summarized and documented.

- Data completeness and governance
  - Documentation notes the importance of metadata completeness and data provenance for reuse in monitoring frameworks.
  - Data licensing: EA discharge data provided under Open Government Licence; other data sources’ sharing terms are described in the dataset documentation.
  - Emphasis on data openness, traceability, and reproducibility, while acknowledging practical barriers in combining multi-source datasets.

- Context and environment during collection
  - The sampling period coincided with an unusually dry and hot summer, resulting in very low river discharge (e.g., East Stoke at its lowest since 1976 drought) with groundwater levels exceeding typical conditions.

- Practical relevance for monitoring framework authors
  - Demonstrates integration of multi-source data (sensor, grab, borehole, and discharge) into a single, well-documented dataset.
  - Highlights the need for clear data structure, metadata, and provenance to support policy evaluation and future decision-making.
  - Illustrates how high-frequency data can be reconciled with traditional grab samples using quantitative quality checks.
  - Provides explicit methodologies for data analysis, quality control, and data cleaning that can inform governance and standard-setting in monitoring frameworks.

- References and methods
  - Analytical methods for grab samples follow established protocols with reporting limits and measurement uncertainties; quality control approaches reference established literature (e.g., target diagrams for data comparison).

- Potential applications for policymakers and researchers
  - Inform development and refinement of high-frequency monitoring strategies.
  - Assist in assessing data governance, transparency, and interoperability across organisations.
  - Support scenario analysis and modelling efforts within monitoring frameworks, particularly in low-flow or drought conditions.