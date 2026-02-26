# Data Overview

- A two-year study (January 2020 – December 2021) measuring greenhouse gas concentrations (CO2, CH4, N2O) and physico-chemical water properties across 26 locations in the River Clyde and its tributaries plus 2 estuary sites to understand GHG sources, sinks, and controlling mechanisms.
- Primary objectives:
  - Quantify sources, concentrations, fluxes, and sinks of GHGs entering the Clyde from source to sea, comparing anthropogenic and non-anthropogenic inputs (semi-natural, agricultural, urban).
  - Develop a model of controls and mechanisms for GHG production, transport, consumption, and release to the atmosphere.
  - Identify conditions under which different sources and sinks are active within the catchment, river, and estuary, and their mechanisms.

- Site description and sampling scope:
  - 26 measurement locations along the River Clyde and major tributaries, plus 2 Clyde estuary locations.
  - Locations distributed from near-source to Glasgow Green, with sampling aligned where possible to SEPA gauging stations.
  - Location codes indicate Clyde main stem (C), tributaries (T), loch inflows (L), and estuary (E); detailed site information provided in Table 1 and Appendix 1.
  - Sampling occurred monthly across 2020–2021, with 21 campaigns due to Covid-19 related access restrictions (April–June 2020 not permitted).

- Sampling regime and field procedures:
  - Water samples collected in 10 L plastic buckets from river banks or bridges (not directly in-water measurements).
  - In-field measurements: conductivity, temperature, dissolved oxygen (DO), DO%, and pH at ~10 cm depth.
  - Headspace gas sampling in triplicate at each location using a standard equilibration method to determine dissolved gas concentrations; ambient air samples collected as part of the headspace analysis.
  - Sub-samples transported to the lab in cool conditions for subsequent analyses.
  - Sampling campaigns conducted over two consecutive days (upper catchment first, then lower catchment).

- Analytical methods and measured parameters:
  - Gas analysis: headspace samples analyzed with a GC (CO2, CH4, N2O) and calibration against mixed gas standards.
  - Water chemistry (on filtered samples): total dissolved nitrogen (TDN), total dissolved carbon (TDC), dissolved organic carbon (DOC), dissolved inorganic carbon (DIC) derived from TDC–DOC, total phosphorus (TP), SUVA254 (aromaticity proxy).
  - Ion chromatography for major ions: chloride, nitrate, sulfate, sodium, ammonium, potassium, calcium, magnesium.
  - Unfiltered samples for TP using acid digestion and colorimetric detection.
  - Data management notes: some samples were frozen or refrigerated for processing; DO measurements began in December 2021.

- Gas calculations and data interpretation:
  - Dissolved gas concentrations and partial pressures derived from a mass-balance approach using equilibration between liquid and gas phases; results converted to units of μmol/L and then to ppmv via the ideal gas law.
  - Partial pressures and saturations for CH4, CO2, and N2O computed, with saturation values reported for context.

- Data structure, units, and metadata:
  - Data organized in CSV format with standardized columns (Survey_Name, Location_Code, Sample_Code, Latitude, Longitude, Date, Time, Elevation, Water depth, Conductivity, Temperature, pH, DO, DO%, DOC, TDC, DIC, TDN, TP, SUVA254, major ions, NH4+, CH4, CO2, N2O, saturation values, etc.).
  - Detailed unit mapping provided (e.g., Cond: µS/cm; Temp: °C; pH: unitless; DOC, TDC, DIC, TDN, TP in mg/L; ions in µmol/L; gas partial pressures in µatm; CH4/CO2/N2O in µmol/L or µatm as appropriate).
  - Missing data are marked with an asterisk (*) in the CSV.
  - Notable data gaps and caveats:
    - Data not collected at Mouse Water (T13) before August 2020.
    - Access constraints due to heavy snowfall prevented sampling at Roger Clench (T1) and Daer Water reservoir inflow (C2) in Jan–Feb 2021.
    - Some sites (C16 Garrion Bridge, E27 Govern Pontoon, E28 Braehead Pontoon) missed in January 2020.
    - DO measurements were only available from December 2021.
    - NH4+ data may be unreliable where high Na+ concentrations dominate peaks, leading to asterisks in the dataset.

- Quality control and data integrity:
  - Field and lab instruments calibrated and standards included in runs.
  - Data quality controlled via time series and spatial checks, outlier/rate-of-change/spike/stationarity analyses, and cross-checks with river flow data.
  - Suspect data flagged and replaced with asterisk markers to indicate missing data.

- Data governance and stewardship considerations:
  - Comprehensive documentation of methods, locations, and units supports reproducibility and reuse.
  - Appendix 1 provides site-specific details and photographic context to aid data interpretation and metadata richness.
  - Data are suitable for contributing to open data portals or institutional repositories with proper metadata, enabling discovery, reuse, and integration into GHG source–sink models for river catchments.
  - Acknowledgement of data provenance (primary data collected by a named researcher with DTP/NERC support) supports traceability.

- Practical implications for data stewardship:
  - Maintain the full data lineage, including field conditions, access limitations, and any deviations from standard sampling (e.g., delays, freezing/refrigeration).
  - Preserve both raw headspace gas data and processed gas concentrations, along with all supporting chemical analyses (DOC, TDN, TDC, DIC, TP, SUVA254, major ions).
  - Ensure clear documentation of data gaps and limitations to guide users in applying the dataset to models of GHG sources/sinks and catchment-scale processes.
  - Consider publishing the dataset with accompanying metadata and a data dictionary, and provide updates or versioning as future campaigns or reprocessing occur.