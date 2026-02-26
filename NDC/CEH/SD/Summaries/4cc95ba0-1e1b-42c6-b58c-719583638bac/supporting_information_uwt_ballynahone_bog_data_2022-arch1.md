# Ammonia measurements from passive samplers at Ballynahone Bog field site, Northern Ireland, 2022

- Context and purpose
  - Set of sites forming a transect through Ballynahone National Park (ASSI/SAC and Ramsar site) in Northern Ireland.
  - Monitoring NH3 to assess potential adverse effects from local poultry livestock installations on the ammonia-sensitive Ballynahone Bog peatland.
  - Local site operator: Ulster Wildlife Trust (UWT); analysis: UK Centre for Ecology and Hydrology (UKCEH) Edinburgh.

- Methodology (UKCEH ALPHA samplers)
  - Passive samplers deployed along a transect at about 1.5 m above ground.
  - Replicates used per site to improve reliability.
  - Exposed monthly; covered by a citric acid–coated filter to capture NH3; diffusion through a PTFE membrane.
  - Analysis: samplers extracted into deionised water and analyzed with SEAL AA3 colorimetric method.
  - Concentrations converted to average air concentration using the sampler uptake rate of 0.0038422 m3 h-1 and exposure duration.

- Data quality and validation
  - Data quality checks applied to raw data; some samples were unsuitable due to exposure errors or weather-related losses.
  - Key quality rules:
    - Coefficient of variation (CV) of replicates < 15% considered valid; otherwise replicates reviewed; valid results flagged as 103 if averages are representative.
    - Missing samplers assigned -9999.00 and marked invalid (-1).
    - Sampler duration anomalies (too long/short) flagged.
    - Local contamination or deviations noted by site operators; questionable samplers discarded.
  - Final dataset: UWT_Ballynahone_Bog_Data_2022.csv containing accepted values with appropriate flags.
  - Data status and flags follow EMEP conventions, including data capture, validity, and contamination indicators.

- Dataset structure and content
  - Each row: one month of data for a single site, with site name and a range of metadata.
  - Key columns (summarized):
    - Station name (site identifier) and network_id (BE)
    - Parameter_id (alpha_NH3_g)
    - Measurement start date/time and measurement end date/time (exposure period)
    - Ammonia concentration (units: µg NH3 m-3)
    - Less than detection limit indicator (0.03 µg/m3) and validation flags
    - Verification id (1: Verified, 2: Preliminary verified, 3: Not verified)
    - Unit id (24 = µg NH3 m-3)
    - Data capture percentage
    - Validity_id (1 = valid, -1 = not valid)
    - EMEP data status/flags
    - Month of measurement
  - Data are expressed as average concentration for the specified exposure period.

- Site information and geography
  - Ballynahone bog_1 through Ballynahone bog_8:
    - Start date: 01/09/2014; End date: Ongoing
    - Latitude/Longitude coordinates provided for each site
    - Height of air inlet above ground: 1.5 m
  - Data are intended to support spatial and temporal analyses of ambient NH3 concentrations across the transect.

- Important notes and limitations
  - Some samples were contaminated or otherwise non-representative; only the accepted data are used for analysis.
  - Data reflect monthly exposure periods and may be affected by local factors and environmental conditions.
  - The dataset is designed to enable correlation analyses with emissions sources and deposition potential, as well as trend assessment over time, while accounting for QC flags and data quality indicators.