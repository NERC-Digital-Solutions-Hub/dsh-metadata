# Passive sampler ammonia measurements indoors and outdoors at a rural dwelling in South Lanarkshire, 2021

- Overview
  - Two sampling sites in a rural South Lanarkshire dwelling: indoor in the hall and outdoor in the garden.
  - Sampling managed by the dwelling owner; analysis performed by the Centre for Ecology and Hydrology (UKCEH) Edinburgh.
  - UKCEH ALPHA® passive samplers used to measure ammonia (NH3) concentrations, with monthly exposure cycles.

- Sampling Methodology
  - UKCEH ALPHA® passive samplers use a citric acid coated filter to capture NH3; a white PTFE membrane protects the filter and allows diffusion.
  - Samplers positioned about 1.5 m above ground on shelters, with replicas for each site to improve reliability.
  - Exposures conducted monthly at the start of each month; replicated samplers provide an average air concentration.

- Analysis and Calculation
  - Exposed samplers are extracted with deionised water and analyzed by SEAL AA3 using colorimetry to determine ammonium concentration.
  - Concentration of NH3 in air derived from the ammonium concentration using the sampler uptake rate: 0.003241315 m3 h-1.
  - Final reported value is the average NH3 concentration over the exposure period, in micrograms per cubic metre (µg NH3 m-3).

- Data Quality, Flags, and Validation
  - Data flagged to indicate concerns; details available in accompanying pages.
  - Quality rules:
    - Coefficient of variation (CV) of replicates < 15% considered valid; if >15%, replicates reviewed, but dataset can still be valid (flag 103).
    - Some samples exceeded calibration range but were deemed valid (instrument issues prevented reanalysis).
    - Missing data or metadata shown as -9999.
  - Final dataset: NH3_SouthLanarkshire_indoors_outdoors2019-2020.csv; contains monthly data per site with site name, exposure dates, NH3 concentration, and data flags.
  - Data status flags and codes referenced from EMEP data flags, including common cases such as data capture, validity, verification, and reasons for adjustments or concerns.

- Dataset Structure and Contents
  - Columns include:
    - Site ID, Site name, Network ID (RSW), Parameter ID (alpha_NH3_g)
    - Measurement start/end date and time (exposure period)
    - Measurement (NH3 concentration, µg NH3 m-3)
    - Less than flag (detection limit indicator)
    - Verification ID (verification status)
    - Unit ID (µg NH3 m-3)
    - Data capture percentage
    - Validity ID (valid/not valid)
    - EMEP data flag codes
    - Month-Year (mmm-yy)
    - Comments on data
  - Site information:
    - Indoor: located in hall of dwelling; coordinates 55.64072, -3.59705; indoor air inlet height 1.5 m.
    - Outdoor: located in garden; same coordinates and height.
    - Start date: 01/01/17; End date: ongoing.

- Site Details
  - Indoor and outdoor samplers share the same geographic coordinates and inlet height.
  - Continuous operation since 2017 with ongoing data collection noted for 2019–2020 in the dataset naming.

- Metadata and Access
  - Data and metadata describe measurement methods, uptake rate, calculation, quality controls, and flag meanings (including detailed EMEP flag mappings).
  - Data are organized per site and per month, with explicit start/end exposure dates and times, enabling reproducibility and trend analysis.

- Implications for Data Strategy (Data Leaders)
  - Demonstrates a standardized approach to passive air monitoring with replicated samplers to improve reliability.
  - Highlights the importance of clear data quality rules (CV thresholds, calibration range considerations, and handling of missing data) for trustworthy datasets.
  - Uses comprehensive metadata and standardized flag systems (EMEP) to communicate data quality and provenance, aiding cross-network comparability.
  - Accessible dataset structure and explicit documentation support integration into broader air-quality assessments and decision-making processes.
  - Potential gaps and considerations: ensuring gap-free coverage and continuing to monitor data capture and validation, especially where calibration or detection limits are involved; leveraging site metadata (indoor vs. outdoor contexts) for nuanced interpretation.