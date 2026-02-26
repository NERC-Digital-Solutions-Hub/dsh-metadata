# Supporting_Information_UWT_Ballynahone_Bog_Data_2020

- Context: Data from Ballynahone National Park in Northern Ireland (Area of Special Scientific Interest, SAC; Ramsar site) collected to assess potential NH3 impacts from local poultry installations. Local site operator duties by Ulster Wildlife Trust (UWT); analysis by UK Centre for Ecology and Hydrology Edinburgh (UKCEH).
- Objective: Measure ammonia concentrations along a transect through Ballynahone Bog using passive UKCEH ALPHA samplers to monitor ammonia air levels in a peatland ecosystem.

## Sampling and Analysis Method
- Samplers: UKCEH ALPHA passive samplers with citric acid coated filters; diffusion through a PTFE membrane; mounted on shelters at ~1.5 m above ground; replicates used for reliability.
- Exposure: Monthly cycles, exposed at the beginning of each month.
- Analysis: Exposed samplers extracted into deionised water; analysed with SEAL AA3 colorimetry to determine ammonium concentration.
- Calculation: Convert ammonium concentration to average NH3 in air using uptake rate of 0.003241315 m3 hr-1 (2020 calibration) and exposure duration.
- Data flags: Data flagged to indicate concerns (see details on page 4 in the original document).

## Data Quality and Validation
- Quality rules:
  - Coefficient of variation (CV) of replicates < 15% expected for valid data; if >15%, replicates may be discarded or noted; dataset may still be considered valid (flag 103).
  - Values > calibration range may be reported if dilution is not possible due to instrument issues; still considered valid.
  - Missing data or metadata are marked with -9999, or lack of date/time metadata prevents calculation.
- Final dataset: UWT_Ballynahone_Bog_Data_2020.csv containing accepted values with appropriate flags; includes site identifiers and data status.

## Dataset Structure and Contents
- Each row: one month of data for a single site.
- Key columns:
  - Site name, unique site identifier, network_id (RSW)
  - Parameter_id (type of measurement: alpha_NH3_g)
  - Measurement start date/time and measurement end date/time (exposure period)
  - Ammonia concentration (µg NH3 m-3)
  - Less than flag (whether value is below detection limit 0.03)
  - Verification id (Not verified, Preliminary verified, Verified)
  - Unit id (24 = µg NH3 m-3)
  - Data capture percentage
  - Validity_id (valid or not valid)
  - EMEP code and related flags (data status, contamination indicators, etc.)
  - Month-Year (mm-yy)
- Data status codes (EMEP flags) describe capture quality, validity, and reasons (e.g., contamination, detection limits, sampling duration, nearby activities).

## Site Information
- Ballynahone bog_1 to Ballynahone bog_8:
  - Start date: 01/09/2014; End date: Ongoing
  - Latitude/Longitude: ranges provided for each site
  - Height of air inlet above ground: 1.5 m
- Site identifiers and coordinates allow spatial alignment of monthly NH3 concentrations across the transect.

## Using the Data
- Units: NH3 concentrations expressed as micrograms per cubic meter (µg NH3 m-3) for each exposure period.
- Outputs usable for:
  - Trend and spatial analyses of ammonia exposure along the transect
  - Quality-assured dashboards or self-serve data products with data flags
  - Assessing potential impacts of NH3 emissions on Ballynahone Bog and surrounding ecosystems
- Important considerations:
  - Review data flags and CV-based validity notes before interpretation
  - Be aware of missing data indicated by -9999 and any metadata gaps that prevented calculation

## Access and Metadata References
- Primary data file: UWT_Ballynahone_Bog_Data_2020.csv
- Site and metadata details are described in the accompanying sections of the Supporting Information (site names, spatial identifiers, and data status codes) and page references within the original document.