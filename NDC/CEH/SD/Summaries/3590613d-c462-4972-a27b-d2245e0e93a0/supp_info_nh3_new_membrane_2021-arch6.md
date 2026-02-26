# Monthly ammonia measurements from passive samplers at four UK Eutrophying and Acidifying Pollutants (UKEAP) network sites, new membrane validation, 2021

- Overview
  - Initial results from validating a new PTFE membrane for ALPHA® samplers prepared and analysed at UKCEH Edinburgh.
  - Local site operator duties performed by UKCEH, AFBI, and Ricardo AEA; analysis by CEH Edinburgh.
  - Samplers deployed in monthly cycles at the start of each month to measure NH3 in air.

- UKCEH ALPHA® Sampler Method
  - Passive sampler uses a citric acid coated filter to capture ammonia.
  - PTFE membrane protects the filter; membrane faces downward during exposure.
  - Samplers mounted ~1.5 m above ground on shelters; replicated samplers used for reliability.
  - Exposed to air, then analysed by SEAL AA3 after extraction in deionised water using colourimetry to determine ammonium concentration.
  - Ammonia air concentration calculated from the sampler ammonium concentration using a uptake rate for the new membrane (0.0039701 m3 hr-1). The uptake rate was derived from data at three sites; Hillsborough was excluded due to unreliable exposure times.

- Uptake Rate and Site Details
  - Uptake rate for new membrane ALPHA® samples: 0.0039701 m3 hr-1.
  - Uptake rate calculation based on three sites; Hillsborough excluded.
  - Site information includes Edinburgh uptake rate details (OTC and Auch) and their coordinates, with 1.5 m air inlet height and collocation identifiers.

- Data Quality Assurance and Processing
  - Data are flagged to indicate concerns (see dataset documentation, page 4 for details).
  - Quality checks:
    - Coefficient of variation (CV) of replicates: CV < 15% required for valid representative results; if >15%, replicates may be discarded; otherwise data considered valid (flag 103).
    - Values above calibration range but still valid if rerun/dilution not possible due to instrument issues.
    - Missing data indicated by -9999 in measurement or meta data (prevents calculation of concentration).
  - Final dataset NH3_New_Membrane_2021.csv contains accepted data with appropriate flags; site names listed on page 5; dataset contents summarized on page 3; each row corresponds to one month of data for a single site with columns for site, exposure period, ammonia concentration (µg NH3 m^-3), and a data flag.

- Data Products and Dataset Schema
  - Final dataset: NH3_New_Membrane_2021.csv
  - Key columns (examples):
    - Site id, Site name, network_id (RSW), parameter_id (alpha_NH3_g)
    - Measurement start date/time, measurement end date/time (exposure period)
    - Measurement (ammonia concentration, units: µg NH3 m^-3)
    - Less than detection flag (1 if below detection limit 0.03)
    - Verification id (Not Verified, Preliminary Verified, Verified)
    - Unit id (24 = µg NH3 m-3)
    - Data capture percentage
    - Validity_id (1 = valid, -1 = not valid)
    - EMEP code (data status and flags)
    - Month-Year and Comments
  - EMEP flags provide detailed reasons for data status (e.g., below detection, contaminated samples, sampling period adjustments, nearby activity, etc.) with codes like 999, 781, 780, 654, 653, 652, 651, 647, 646, 645, 599, 593, 591, 559, 558, 557, 556, 555, 553, 532, 103.

- Data Flags and EMEP Flags
  - Data capture and validity indicators accompany each measurement, including:
    - 999: Data capture = 0; Valid/Invalid = -1; Reasoning = Missing measurement
    - 781, 780, 654, 653, 652, etc.: Various meanings related to detection limits, sampling periods, contamination sources, and validity
    - 103: CV of replicate ALPHA samplers > 15%; still considered valid measurement
  - EMEP flag details (as examples): indicates verification status, data issue number, and specific EMEP flag reasoning (e.g., contamination, nearby activity, or measurement limitations).

- Site Information
  - Site-specific uptake rate details and metadata:
    - Edinburgh uptake rate – OTC, Auch, Hills, Chilbolton
    - Each site includes start date (e.g., 01/03/2020 for OTC and Auch; 01/01/2021 for Chilbolton), ongoing end date, latitude, longitude, height of air inlet (1.5 m), and collocation identifiers (e.g., UKA00128, UKA00451, UKA00293, UKA00614).

- Notes and Context
  - Aimed at providing a validated data product for ammonia air concentrations using the new PTFE membrane, enabling cross-site comparability and long-term monitoring.
  - Emphasizes the importance of data quality, replication, and clear flagging for data usability and re-use.
  - Data are intended for broader use in policy and environmental monitoring contexts, consistent with the role of data support in enabling self-serve data products and clear documentation of data quality and provenance.