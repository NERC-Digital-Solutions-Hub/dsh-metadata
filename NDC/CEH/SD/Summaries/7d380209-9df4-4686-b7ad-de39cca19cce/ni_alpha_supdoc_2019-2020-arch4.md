# Monthly atmospheric ammonia concentration data from Northern Ireland ALPHA® Ammonia Monitoring Network, 2019-2020

- The document describes two data files:
  - NI_ALPHA_NH3_2019.csv (monthly NH3 concentrations from 25 NI ALPHA sites, 2019)
  - NI_ALPHA_NH3_2020.csv (monthly NH3 concentrations from 25 NI ALPHA sites, 2020)
- Data originate from the Northern Ireland ALPHA® Ammonia Monitoring Network, measuring monthly atmospheric NH3 at 25 sites across Northern Ireland for 2019–2020.
- Additional NH3 data for 2019–2020 were collected via the UKCEH DELTA® method at 4 additional sites (NI DELTA Gas and Aerosol Monitoring Network), with one site co-located for method inter-comparison between ALPHA® and DELTA®.

- Organization and purpose
  - Network operated jointly by the Agri-Food and Biosciences Institute (AFBI) and the UK Centre for Ecology & Hydrology (UKCEH).
  - Funded by the Department of Agriculture, Environment and Rural Affairs (DAERA).
  - Data used for model validation and calibration of modelled atmospheric NH3 concentrations (e.g., FRAME) and for estimating nitrogen deposition via CBED.
  - Aims to increase confidence and reduce uncertainty in NH3 modelling to evaluate policy scenarios and emissions inventories in NI.

- Experimental design and monitoring strategy
  - NAMN framework: 25 ALPHA® sites across NI (30? no; 25 total), designed to improve spatial coverage and spatio-temporal NH3 data.
  - Hillsborough site provides onsite NH3 data for local farm emission evaluation; other sites provide spatial representativeness for transport model validation and model improvement.
  - Monitoring by UKCEH ALPHA® passive samplers mounted ~1.5 m above ground; monthly, time-integrated sampling.
  - 24 rural sites and 1 urban site (AFBI14) included; 25th site Hillsborough noted for ALPHA+DELTA integration.

- Monitoring method and data parameters
  - Method: UKCEH high-sensitivity ALPHA® passive sampler; citric acid-coated filter papers capture NH3, analyzed as NH4+ and converted to NH3 concentration.
  - Reference uptake rates (air volume sampled):
    - 2019: 0.0031665 m3 h-1
    - 2020: 0.0031277 m3 h-1
  - Units: NH3 concentration in µg m-3; concentrations are time-integrated over exposure periods.
  - Limit of detection: 0.03 µg NH3 m-3 (monthly exposures).
  - Data are complemented by DELTA® measurements at co-located sites for cross-method comparisons.

- Data quality control and processing
  - Data captured and processed in an Oracle-based AAGA database with a ShinyApp for calculation of NH3 concentrations.
  - Multi-stage QC workflow:
    - Stage 1: Automatic QC with EBAS/EMEP-like data flags; auto-flagging for date overlaps, sampling duration deviations (including COVID-related extended sampling in Apr–Jun 2020), replicate precision (CV > 15% flagged), outliers, and missing samples.
    - Stage 2: Manual data review and flagging for lab/field issues (damaged samples, water ingress, instrument issues), low/high outliers, and contamination concerns.
    - Stage 3: Expert/project manager review considering site context, modelling expectations, temporal/spatial patterns, and co-located DELTA data.
  - Final output is a time-stamped, version-controlled, ratified dataset with data flags and a clear status.
  - Data flags follow EBAS/EMEP conventions; final ratified data carry a "Ratified" status.
  - Handling of missing or invalid data includes placeholder values (-9999) and data capture codes.

- Data structure and contents
  - Each row represents one month of data for a single site.
  - Key fields include:
    - site_id, site_name, network_id (AFBI)
    - parameter_id (alpha_NH3_g)
    - measurement_start_date/time and measurement_end_date/time
    - measurement (NH3 concentration in µg m-3)
    - Less_than flag (LOD indication)
    - verification_id (verification status)
    - Unit_id (µg m-3)
    - Data_capture (0 = missing/rejected, 100 = accepted)
    - Validity_id (1 = valid, -1 = invalid)
    - EMEP_code (data status/flag codes)
    - MONTH, YEAR
    - Comments (manual flags)
  - The dataset includes coordination with DELTA sites where applicable and notes confidentiality about precise coordinates (2 decimal places).

- Data management and interoperability
  - Data conform to EN 17346 (2020) for diffusive samplers.
  - Data flags align with EBAS/EMEP standards to enable cross-network harmonization.
  - References and supporting information provided for NAMN, FRAME, CBED, and EBAS flag dictionaries.

- Access and supporting resources
  - NAMN information and NH3 modelling references:
    - NAMN network information page
    - FRAME modelling framework
    - CBED deposition model
  - EBAS flag index for data flag standardization
- Notable contextual details
  - 2019–2020 data include monitoring across a spatially representative NI network and a co-located comparison with DELTA to ensure inter-method reliability.
  - COVID-19 related disruptions affected sampling duration at times (Apr–Jun 2020), with corresponding data flags to indicate representativeness or extended sampling periods.