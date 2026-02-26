# 1 Overview of data

- Purpose and scope
  - High-frequency water quality dataset for River Frome catchment, Dorset, UK (12 Aug 2022 – 14 Sep 2022)
  - 24 monitoring sites from upstream to downstream reach (includes river channels, major tributaries, boreholes, and STW effluents)
  - NGR coordinates provided for each site; data includes both continuous sensor readings and grab samples
  - Case study linked to river water quality management research; data contributed by Wessex Water Services Ltd. and Environment Agency; Open Government Licence for EA data

- Data structure and file
  - Single CSV file: riverfrome_waterquality_highres_2022
  - 13 columns: Date, Time_GMT, Date_time, Site_name, Site_NGR, Site_type, Source, Freq, Determinand, Result, Sign, Censored, Unit
  - Documentation references sections 3.1–3.2 for units, uncertainty, reporting limits, and methods

- Experimental design and sampling regime
  - Instruments: four EXO2 and two EXO3 multi-parameter sondes; in-situ measurements at 30-minute resolution
  - Measured parameters: conductivity, dissolved oxygen (DO), DO%, pH, temperature, turbidity; NO3-N via NitraLED (30-minute with EXO2), additional NO3-N data from Wessex Water sensors
  - Additional measurements: 15-minute discharge at STW effluents and EA gauging stations; grab samples ~3 times weekly
  - Study split: upstream period (12/08/22–30/08/22) and downstream period (30/08/22–14/09/22); Pallington sampled in both periods
  - Grab samples analyzed by Wessex Water Services Ltd.; in-situ DO and temperature measured with YSI ProSolo probe

- Data sources and determinands
  - Sensor data and discharges
    - EXO2: conductivity, DO, DO%, pH, temperature, turbidity; nitrate via NitraLED
    - EXO3: conductivity, DO, DO%, pH, temperature, turbidity
    - Nitratax sensors: NO3-N (Louds Mill, East Stoke)
    - STW and river discharge data: 15-minute intervals (STW and EA sources)
  - Grab samples (by authors and WW): alkalinity, ammonium, BOD, chloride, conductivity, DO, NO3-N, nitrite, orthophosphate, SRP, pH, total phosphorus, turbidity, temperature, total suspended solids
  - Borehole samples: ammonium, nitrate, nitrite, orthophosphate
  - Site types included: river, STW effluent, borehole

- Analysis methods and reporting limits
  - Grab samples analyzed at Wessex Water Scientific Centre following methods summarized in Kasprzyk-Hordern et al. (2022) with detailed reporting limits and uncertainties
  - Specific analytical techniques and wavelengths listed for ammonia, TON, nitrite, nitrate, orthophosphate, SRP, chloride, alkalinity, BOD, SS, pH, conductivity, turbidity, and total phosphorus
  - Uncertainty of measurement (UoM) values provided; reporting limits vary by freshwater (FW) vs final effluent (FE)

- Quality control and data quality assessment
  - Grab samples compared with continuous data using visual plots and target diagrams (bias, RMSD, correlation)
  - General good agreement between continuous and grab data; pH showed notable normalised bias due to measurement scale and calibration artefacts
  - DO agreement sometimes poorer at specific sites due to local gradients and sampling distance
  - Conclusion: confidence in high-frequency continuous measurements; some site-specific artefacts acknowledged

- Data completeness and cleaning
  - Data wrangled in R; outliers replaced with N/A when explainable
  - Filters applied: remove negative concentrations; exclude data when STW flow too low to wets sensors; remove large turbidity spikes (> 6000 NTU) due to fouling or bubbles
  - Documented criteria and rationale for data exclusion

- Contextual notes
  - Campaign occurred during an unusually dry summer; River Frome discharge was exceptionally low (e.g., East Stoke minimum 1.92 m3/s on 31 Aug)
  - Groundwater levels and discharge correspond to rare conditions (high percentile for the period)

- Licensing and access
  - Data governed by Open Government Licence (EA data); other sources (Wessex Water) contributed under their arrangements
  - Clear provenance of measurements and sources to support reuse and integration into broader data systems

- Miscellaneous metadata and references
  - 24 sites with NGRs; measurement resolution and cadence summarized; split sampling regime clarified
  - References to methodological literature on high-frequency water quality monitoring and analysis techniques provided for context

- Implications for data leaders
  - Demonstrates end-to-end data pipeline: sensor data, grab samples, borehole data, STW/EA discharges, and metadata
  - Emphasizes data governance elements: source provenance, licensing, unit consistency, metadata richness, and data quality validation
  - Highlights practical data challenges (scattered data sources, site-specific biases, drought-driven variability) and approaches to ensure data quality and usefulness
  - Provides a replicable data model for high-frequency water quality monitoring in other catchments, including data structure, QC workflows, and documentation practices