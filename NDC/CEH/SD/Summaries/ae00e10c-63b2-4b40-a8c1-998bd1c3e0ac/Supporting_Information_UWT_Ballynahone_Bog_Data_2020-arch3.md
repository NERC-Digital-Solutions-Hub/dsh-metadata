# Supporting_Information_UWT_Ballynahone_Bog_Data_2020

## Objective and context
- Data collection to assess potential NH3 emissions impacts on Ballynahone Bog, an ammonia-sensitive peatland within Ballynahone National Park, Northern Ireland.
- Area managed locally by Ulster Wildlife Trust (UWT); analysis performed by UK Centre for Ecology and Hydrology (UKCEH) Edinburgh.
- Monitoring conducted along a transect through the bog using UKCEH ALPHA® passive samplers to measure ammonia concentrations in air on a monthly cycle.

## Sampling and analysis methods
- Passive sampling with UKCEH ALPHA® samplers: citric acid coated filters capture ammonia; PTFE membrane protects the filter; membrane orientation and protective caps described.
- Deployment: replicates mounted on shelters at about 1.5 m above ground; samplers exposed in monthly cycles at the beginning of each month.
- Analysis workflow: exposed samplers extracted into deionised water and analyzed with SEAL AA3 colorimetry to determine ammonium concentration; ammonia concentration in air calculated using the known uptake rate of the samplers (0.003241315 m3 hr-1) and exposure duration.
- Data are expressed as average NH3 concentration in air (µg NH3 m-3) for each month and site.

## Data management, QA and metadata
- Raw data are reviewed and quality-checked against predefined rules; data points may be flagged for concerns.
- QA criteria:
  - Coefficient of variation (CV) of replicates must be <15% to be considered representative; if CV >15%, replicates may be discarded; otherwise the averaged result is treated as valid (flag 103).
  - Values above calibration range may be reported due to instrument issues; such results can remain valid.
  - Missing data or missing metadata are indicated with -9999 (inability to calculate concentrations).
- Final dataset: UWT_Ballynahone_Bog_Data_2020.csv, containing accepted data with appropriate flags. Site identifiers and spatial details are provided in accompanying material.

## Data structure and fields
- Each row corresponds to one month of data for a single site.
- Core fields include:
  - Site name and unique site identifier
  - Network ID (RSW)
  - Parameter ID (type of measurement: alpha_NH3_g)
  - Measurement start/end dates and times (exposure period)
  - Measurement value: ammonia concentration (µg NH3 m-3)
  - Less than detection flag
  - Verification ID and unit ID
  - Data capture percentage
  - Validity ID (1 = valid, -1 = not valid)
  - EMEP data status code (flags related to QA/EMEP reporting)
  - Month-Year of measurement (MMM-YY)

## EMEP and data quality flags
- EMEP flags provide context for data validity and issues, including:
  - 999: Data capture 0; missing measurement
  - 781/780/654/653/652/651 etc.: various reasons (e.g., below detection limit, sampling period issues, nearby contamination sources)
  - 103: CV of replicate ALPHA samplers >15%; still considered valid
  - 460/553/559/555/557/556/ etc.: contamination or local influences; may be valid or invalid depending on context
- Flags distinguish issues such as contamination, instrument limitations, and representative sampling, helping enforce data governance and transparency.

## Site information and layout
- Ballynahone bog_1 through Ballynahone bog_8:
  - Start date: 01/09/2014
  - End date: Ongoing
  - Coordinates (latitude and longitude) and 1.5 m inlet height above ground provided for each site
  - Sites form a transect within Ballynahone Bog, enabling spatial assessment of NH3 along the bog

## Data accessibility and governance
- Data are prepared to be shared publicly, with clear documentation of QA decisions and flag meanings.
- The final dataset contains validated values with flags indicating any issues or caveats; detailed site metadata and flag definitions accompany the dataset for proper interpretation.