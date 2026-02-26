# Dataset Summary and contextual information

- Aims and scope
  - Provides Above Ground Carbon Density (ACD) estimates from forest census surveys (1992–2016) in mixed logged and unlogged tropical lowland dipterocarp forests in Ulu Segama Forest Reserve (USFR) and Danum Valley Conservation Area (DVCA), Sabah, Malaysia.
  - Supports monitoring environmental health and policy performance over time using standardized outputs.

- Study area and history
  - USFR: 1268 km2, divided into coupes logged once (1972–1993) using tractor or high-lead methods; restoration treatments (climber cutting, tree planting) 1993–2004.
  - Data compiled from 257 plots (51,803 trees; 45.56 ha) across three independent plot networks.

- Plot networks and sampling
  - INDFORSUS (Network A): 53 plots of 0.1 ha; logged 1981–1993 and unlogged primary forest; relocations and recensus in 2016 (funded by STEED and INFAPRO projects).
  - Pinard & Putz (Network B): 32 plots of 0.08 ha; nested plots for different DBH classes; recensus in 1996 and 2005.
  - INFAPRO (Network C; INFRAPRO): 205 plots of 0.2 ha across logged areas; recensus in 2010 and 2015.
  - Data contributed by Yayasan Sabah’s Conservation and Management Division; three plot networks developed independently with slightly different field protocols.

- Measurements and protocols
  - Field measurements vary by network but share core approach: measure free-standing woody plants above 20 cm DBH; multi-circle sampling in nested plots; in some networks measure down to smaller DBH classes.
  - DBH measurement adjustments when buttress roots require; in some cases DBH at POM is converted to DBH at 1.3 m (DBH_1.3m) using a taper model.
  - Tree height recorded directly for many trees or estimated via a three-parameter function calibrated to nearby datasets.
  - Wood density drawn from global database; species-identified stems use species average; missing botanical info assigned plot averages.

- Units and carbon modelling
  - ACD reported as Mg ha^-1.
  - Carbon content assumed to be 47% of aboveground biomass (AGB).
  - AGB estimated with allometric equation: AGB_est = 0.0673 * (ρ * DBH^2 * H)^0.976, with ρ as wood density.
  - POM adjustments used to estimate DBH at 1.3 m when measurements were taken higher.
  - Height estimation equation: H = 89.53 * (1 − exp(−0.0225 * DBH^0.7383)).
  - For missing species data, plot-average wood density applied.

- Data structure and metadata
  - Fields recorded per plot: Plot Identifier, Coupe Name, Plot identifier (network-specific), LoggingMethod (High lead, Tractor, UnLogged), Year logged, Forest (Logged/UnLogged), YearsSinceLogging, MeasureTime (year of census), Dataset (INDFORSUS, FACE, or RIL_PinardLincoln).
  - Restoration scenario indicator: FACE field distinguishes Project Scenario, Baseline, or N/A for unlogged forest.

- Quality control and analysis
  - Data quality steps include numeric range checks, formatting conformity, and logical integrity checks.
  - Data analyses and modelling described by Philipson et al. (in press); associated code available at Zenodo (doi provided).

- Access, code and references
  - Code and modelling framework accessible via the referenced Zenodo repository.
  - Key references include Foody et al. (2001, 2003), Tangki & Chappell (2008), Pinard & Putz (1996), Lincoln (2008), Face the Future (2011), and the ongoing work by Philipson et al. (in press).

- Particular challenges for analysts monitoring the environment
  - Increasing the value of datasets by integrating with other relevant data sources to avoid single-use outputs.
  - Ensuring accessible, underlying data for reuse and scrutiny, enabling broader data interoperability and policy monitoring.