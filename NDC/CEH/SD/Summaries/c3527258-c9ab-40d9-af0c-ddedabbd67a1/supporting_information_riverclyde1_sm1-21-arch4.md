# River Clyde GHG concentrations and physio-chemical water properties study (January 2020 - December 2021)

- Purpose and objectives
  - Quantify sources, concentrations, fluxes and sinks of greenhouse gases (GHGs) entering the Clyde catchment (source-to-sea) and compare anthropogenic and non-anthropogenic sources, including semi-natural, agricultural, and urban impacts.
  - Develop a model of controls and mechanisms for GHG production, transport, consumption, and release to the atmosphere.
  - Determine the conditions under which different sources and sinks are active within the catchment, river, and estuary, and their associated mechanisms.

- Data coverage and sampling design
  - 26 measurement locations on the River Clyde and major tributaries, plus two locations within the Clyde estuary (E27, E28).
  - Sampling occurred monthly from January 2020 to December 2021; 21 sampling campaigns were conducted (April–June 2020 paused due to Covid-19).
  - Sampling regime: two-day campaigns with upper catchment sites on day 1 and lower catchment on day 2; samples collected from river banks or bridges.

- Data collected and key variables
  - In situ water quality: conductivity (Cond), temperature (Temp), dissolved oxygen (DO), DO saturation (DO%), pH.
  - Dissolved gases: headspace method to determine concentrations of CO2, CH4, and N2O; ambient air samples collected for reference; triplicate headspace samples per location.
  - Water chemistry: total dissolved nitrogen (TDN), total dissolved carbon (TDC), dissolved organic carbon (DOC), and dissolved inorganic carbon (DIC); total phosphorus (TP).
  - Organic/inorganic carbon measures: SUVA254 to indicate aromaticity of DOC.
  - Anions and cations: chloride, nitrate, sulfate, sodium, ammonium, potassium, calcium, magnesium (via ion chromatography).
  - Phosphorus: orthophosphate after digestion (colorimetric method).
  - Gas-related quantities: partial pressures of CH4, CO2, N2O in air; CH4 and CO2 saturations in water; CH4-C and CO2-C concentrations.

- Analytical methods and workflow
  - GHGs: headspace gas chromatography (Agilent 7890B GC with 7697A headspace autosampler); multiple mixed gas standards included per run.
  - Water chemistry: filtration (0.7 µm) for DOC, TDN, TDC; TOC-L analyser for TDN, TDC, DOC; SUVA via UV254 absorbance; IC for major ions; TP via acid digestion and colorimetric assay.
  - Data handling: samples processed the same day when possible; some refrigeration/re-run timing variations across days; data combined per survey run.

- Gas calculations and units
  - Dissolved gas concentrations calculated from headspace equilibration using a mass-balance approach and Henry’s law adjustments (temperature-dependent beta; barometric pressure).
  - Concentrations converted to μmol/L and then to ppmv using the Ideal Gas Law.
  - Saturation, concentration, and carbon-specific metrics (CH4, CO2, CH4-C, CO2-C) included as part of the dataset.

- Data structure, metadata, and quality control
  - Data and metadata structured with a detailed column mapping (Survey_Name, Location_Code, Sample_Code, Latitude/Longitude, Date, Time, Elevation, Water depth, Cond, Temp, pH, DO, DO%, DOC, TDC, DIC, TDN, TP, SUVA, major ions, NH4+, CH4, CO2, N2O, saturations, CH4-C, CO2-C, etc.).
  - Missing data flagged with an asterisk; several planned measurements were not collected at specific sites or times (e.g., DO not measured until December 2021; some locations inaccessible due to weather; certain estuary and urban sites intermittently limited by interferences).
  - Data quality assurance included instrument calibration, use of multiple standards, and checks for outliers, rate of change, spikes, and stationarity; hydrology used as a major context for QC; suspect data removed and marked as missing.
  - Some data limitations noted: ammonium measurements can be confounded by high sodium in estuarine/urban contexts; concentrations exceeding calibration standards were diluted and re-measured; some data gaps due to weather or operational constraints.

- Location references and data governance
  - Location codes indicate the sampling point type: C = Clyde River, T = tributary, L = inflow from loch, E = estuary.
  - Distances are measured from the most upstream sampling point toward the sea; tributary distances reflect points where they join the Clyde.
  - Appendix 1 provides detailed sample locations, coordinates, and site visuals; includes methodology and photographs for each site.

- Data products, usage, and potential impact
  - The dataset supports understanding GHG sources and sinks across the Clyde catchment, enabling:
    - Source attribution (anthropogenic vs natural; urban vs rural).
    - Evaluation of controls and mechanisms governing GHG production, transport, and atmospheric exchange.
    - Model development for catchment-scale GHG dynamics and potential policy or management implications.
  - Data can be integrated with hydrological data (river flow, gauge data) to contextualize GHG dynamics and validate system-wide models.

- Acknowledgements and references
  - Funded by Natural Environment Research Council (NERC) through the IAPETUS Doctoral Training Partnership; acknowledgments include access permissions to sampling sites.
  - References include methodological sources for gas exchange, DO, SUVA, and analytical techniques.

- Appendix and site-level details
  - Appendix 1 – Sample locations: comprehensive list of 28 sites (26 Clyde catchment locations plus estuary sites) with coordinates, sampling context, and accompanying imagery.
  - Notes emphasize the sampling logic, data gaps, and site-specific considerations (e.g., proximity to SEPA gauges, presence of weirs, urban outfalls, and land-use context).