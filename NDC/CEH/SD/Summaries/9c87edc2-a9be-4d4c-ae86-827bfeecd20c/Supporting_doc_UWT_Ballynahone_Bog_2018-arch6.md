# Supporting information for Ammonia measurements from passive samplers at Ballynahone Bog field site (2018)

- Context and purpose
  - Data from a transect through Ballynahone National Park (ASSI/SAC) and Ramsar site in Northern Ireland.
  - Managed by Ulster Wildlife Trust (UWT); analysis performed by the Centre for Ecology and Hydrology Edinburgh (CEH).
  - Samplers used to assess potential NH3 deposition from local poultry livestock installations.

- Sampling and analysis methods
  - CEH ALPHA® passive samplers with citric acid coated filters and PTFE membranes; exposed with membrane end facing downward.
  - Replicate samplers mounted on shelters at about 1.5 m height above ground; monthly exposure cycles.
  - Analysis: exposed samplers extracted into deionised water and measured by SEAL AA3 colorimetry.
  - NH3 concentration in air calculated using sampler uptake rate of 0.003241315 m3 h-1 and exposure duration.

- Data quality, cleaning and flags
  - Raw data flagged for quality concerns (e.g., samples exposed incorrectly, weather-related losses).
  - Quality rules applied:
    - CV < 15% across replicates → data considered valid (flag 103); otherwise evaluation/discard as needed.
    - Missing samplers → value set to -9999.00 and marked invalid (-1).
    - Sampler duration longer/shorter than normal → flagged accordingly.
    - Local contamination or influences → affected samples evaluated and possibly discarded; reported as averages of valid results.
  - Final dataset: UWT_Ballynahone_Bog_Data_2018.csv containing accepted data values with appropriate flags.
  - Data columns include: site name, start/end dates, ammonia concentration (µg NH3 m-3), and a data flag.
  - Data quality and traceability details are documented (e.g., page 4 notes for exclusions; page 5 for site information).

- Data product and structure
  - Each row represents one month of data for a single site.
  - Key fields in the data structure:
    - Station name, unique site identifier, network_id (UWT), parameter_id (alpha_NH3_g)
    - Measurement start/end dates and times (exposure period)
    - Ammonia concentration (µg NH3 m-3)
    - Less than detection indicator (0/1)
    - Verification id, unit id (24 = µg NH3 m-3)
    - Data capture percentage, validity_id (1 = valid, -1 = not valid)
    - EMEP status code and related flags
    - Month-Year of measurement (mmm-yy)
  - EMEP flags provide context for data status, detection limits, period representativeness, and potential contamination.

- Site information
  - Ballynahone bog_1 to Ballynahone bog_8: eight sampling sites forming the transect.
  - Start_date for all sites: 01/09/2014; End date: ongoing.
  - Coordinates and sampling setup:
    - Latitude/Longitude provided for each site
    - Height of air inlet above ground: 1.5 m

- Format, units, and intended use
  - Concentrations reported as micrograms NH3 per cubic meter of air (µg NH3 m-3).
  - Data intended for assessing spatial-temporal ammonia levels and supporting interpretation of potential deposition impacts within Ballynahone Bog ecosystem.

- Practical notes for users
  - Refer to the final dataset for valid measurements and associated flags.
  - Pay attention to data capture percentages, detection limits, and any site-specific exclusions noted in the accompanying documentation.