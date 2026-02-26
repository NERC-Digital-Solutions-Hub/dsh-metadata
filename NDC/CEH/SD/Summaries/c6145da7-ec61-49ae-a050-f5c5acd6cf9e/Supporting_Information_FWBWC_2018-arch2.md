# Supporting information for Ammonia measurements from passive samplers at Fenn ' s, Whixall, Bettisfield, Wem & Cadney (2018)

- Context and purpose
  - Monitoring atmospheric ammonia concentrations at multiple moss sites (Fenn’s, Whixall, Bettisfield, Wem & Cadney Mosses SAC, SSSI) as part of the LIFE project under the Site Nitrogen Action Plan (SNAP).
  - Local site operator duties performed by Natural England; analysis by CEH Lancaster; data processing by CEH Edinburgh.
  - CEH ALPHA samplers deployed in monthly cycles to produce standardized ammonia measurements for environmental health assessment and policy monitoring.

- Sampling method (CEH ALPHA sampler)
  - Passive samplers use a citric acid coated filter to capture NH3; protected by a white PTFE membrane positioned face-down during exposure.
  - Replicate samplers deployed on shelter poles at approximately 1.5 m above ground; protected in plastic containers.
  - Exposure occurs monthly; samplers remain at the site for the designated exposure period.

- Analysis and data conversion
  - Samplers are extracted into deionised water and analyzed with SEAL AA3 to quantify ammonium concentration.
  - Ammonia concentration in air is derived from sampler results using a known uptake rate (0.0028986 m3 h-1, UK uptake rate) and the exposure duration.
  - Final reported value is the average ammonia concentration over the exposure period (units: µg NH3 m-3).

- Quality assurance and validation
  - Data quality rules applied to determine validity:
    - Coefficient of variation (CV) of replicates must be < 15%; otherwise, evaluation for possible discard or retention with a 103 data flag.
    - Missing samplers flagged as invalid (-1) and set to -9999.00.
    - Sampler duration deviations (long/short) flagged when applicable.
    - Local contamination or unusual influences noted and potentially excluded; final site data may be the average of valid replicates.
  - Final dataset: FWBWC_ammonia_measurements_2018.csv, containing monthly data per site with associated flags and metadata.

- Dataset structure and fields (highlights)
  - Core columns include: site name, start date, end date, exposure start/end times, ammonia concentration (µg NH3 m-3), less-than flag (detection limit), verification id, unit id (24 = µg NH3 m-3), data capture percentage, validity id, EMEP data status code, and Month-Year (mmm-yy).
  - EMEP flags provide detailed data quality context (e.g., missing measurements, below detection limit, contamination indicators, and sampling duration considerations).
  - The dataset is organized with one row per site per month, containing the site identifier, spatial/temporal metadata, concentration, and quality flags.

- Site information and deployment
  - Example sites (MM01, MM02, MM03) with start date 01/07/2018 and ongoing end date.
  - Geographic coordinates and sensor height: latitude, longitude, and 1.5 m air inlet height above ground.
  - Each site has its own record of start/end dates, enabling temporal analysis and comparison across sites.

- Data management and accessibility
  - Data are stored and processed within CEH and uploaded to appropriate portals as part of standard monitoring workflows.
  - Outputs are designed to be usable for environmental health assessments, policy performance reviews, and cross-site data integration, aligning with the aim of monitoring environmental health over time and facilitating data reuse.