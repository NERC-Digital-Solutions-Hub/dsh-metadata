# Data Overview

- What was measured and why
  - Greenhouse gas (GHG) concentrations (CO2, CH4, N2O) and physio-chemical water properties in the Clyde estuary, Scotland.
  - Measurements taken across the tidal cycle from the Braehead pontoon to understand sources/sinks and mechanisms of GHG production, transport, and release to the atmosphere.
  - Aimed to quantify sources (anthropogenic vs non-anthropogenic) and how conditions (tidal regime, stratification, temperature, river flow) affect active sources/sinks.

- Study scope and timeline
  - Seven survey occasions from August 2020 to May 2022.
  - Measurements at surface and near-bed (0.2 m below surface and 0.5 m above bed) to capture vertical variability.
  - Sampling designed to cover ebb and flood tides where possible; data include both surface-only and surface+bed samples.

- Site description and data collection
  - Location: Braehead pontoon, inner Clyde estuary, mid-point between fresh and saltwater zones; 7.9 km from the tidal weir.
  - Environmental context: dredging activity in the estuary; water depth typically 3–7 m (tide-dependent); estuary subject to tidal currents and river flow.
  - Data collection setup: samples collected from the outer face of the pontoon, northward-facing; coordinates recorded; river flow data linked to mid-survey timing from SEPA gauge; tidal range data from Renfrew gauge.

- Sampling regime and measurements
  - Water samples for chemical analyses collected in 2 L bottles; in-field measurements of conductivity, temperature, dissolved oxygen, DO saturation, and pH.
  - Dissolved gas samples: headspace method with triplicate samples at each location; ambient air samples collected at ~1 m above surface.
  - GHG evasion measurements: CH4 and CO2 evasion using a floating chamber and an ABB GGA, with three-minute measurement windows to minimize headspace saturation effects.
  - Wind data recorded 2 m above the pontoon to support evasion calculations.

- Analytical methods
  - Gas concentrations (CO2, CH4, N2O) determined by GC with headspace auto-sampler; standard gas mixtures used for calibration.
  - Turbidity measured; water samples filtered for sub-samples to analyze: total dissolved nitrogen (TDN), total dissolved carbon (TDC), dissolved organic carbon (DOC), nitrite, nitrate, ammonia, and total phosphorus (TP).
  - DOC vs TDC used to derive dissolved inorganic carbon (DIC); SUVA254 calculated from UV absorbance to infer aromaticity and potential anthropogenic influence.
  - Nitrate, nitrite, ammonia measured with SEAL AQ2; TP via acid digestion and colorimetric detection.
  - All analyses were conducted on samples processed shortly after collection; preservation and refrigeration details documented.

- Gas partial pressures and data calculations
  - Dissolved gas concentrations derived from headspace equilibration using a mass-balance approach; converted to gas-phase partial pressures and then to ppmv using the ideal gas law.
  - Calculations account for temperature (βT) and barometric pressure (P_BAR); references provided for equilibrium and gas exchange methods.

- Data structure, units, and quality notes
  - Data are organized with a defined set of parameters (e.g., Latitude, Longitude, Date, Time, Water_depth, Depth, Cond, Temp, pH, DO, DO%, Turbidity, DOC, TDC, DIC, TDN, TP, ABS254, SUVA254, NH4, NO2, NO3, TN, pCO2air, pN2Oair, CH4, CH4(evasion), CO2(evasion), etc.).
  - Units specified in accompanying documentation; missing values marked with an asterisk in the CSV.
  - One site-specific limitation noted: CEP1 (August 2020) lacked near-bed data; depth sampling conditions could affect representativeness.
  - Dredging and depth-sampler notes indicate potential mixing or sampling disturbances that could impact results.

- Data governance and dissemination considerations for data leaders
  - Metadata clarity: extensive method details, sampling depths, timing relative to tides, and instrument calibration are documented to support reproducibility and reuse.
  - Data quality indicators: explicit notes on sampling limitations, need for refrigeration, and standards used for calibration and QA/QC.
  - Discoverability and interoperability: a CSV dataset with defined column headings and units; alignment with related Clyde estuary transect datasets (Appendix references) enables cross-domain analyses.
  - Potential data products: time-stamped, location-based dataset of GHG concentrations and partial pressures combined with water quality parameters to support modelling of GHG sources/sinks and evasion fluxes.
  - Collaboration and reuse considerations: data linked to a broader Clyde estuary research program; acknowledges NERC support and access provisions for researchers, enabling cross-institutional use and validation.

- Acknowledgements and references (context)
  - Funded by Natural Environment Research Council (NERC) under IAPETUS Doctoral Training Partnership.
  - Data collection support and access to Braehead pontoon acknowledged.
  - Key references provided for methods and calibration standards (gas exchange theory, headspace equilibration, SUVA, and analytical techniques).