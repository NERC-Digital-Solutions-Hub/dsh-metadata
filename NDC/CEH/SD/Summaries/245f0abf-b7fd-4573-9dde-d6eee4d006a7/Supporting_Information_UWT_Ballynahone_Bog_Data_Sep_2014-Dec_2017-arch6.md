# Supporting information for Ammonia measurements from passive samplers at Ballynahone Bog field site (2014 - 2017)

## Purpose and context
- Study of ammonia (NH3) concentrations along a transect through Ballynahone Bog, Northern Ireland, a protected peatland within ASSI/SAC and Ramsar sites.
- Initiated due to concerns about NH3 emissions from local poultry livestock installations.
- Local site operator: Ulster Wildlife Trust (UWT); analysis: Centre for Ecology and Hydrology Edinburgh (CEH).

## Sampling methodology
- Instrument: CEH ALPHA® passive samplers using a citric acid coated filter to capture NH3.
- Deployment: replicates mounted on shelters at about 1.5 m above ground on poles or posts.
- Sampling cycle: monthly exposure aligned with each month; samplers exposed at the beginning of each month.
- Sample replication: multiple samplers per site to improve reliability.
- Analysis: exposed samplers extracted into deionised water, analyzed by AMFIA (Ammonia Flow Injection Analysis) to determine NH3 concentration via conductivity response.
- Conversion: sampler concentration converted to average ambient air concentration using the known uptake rate of ALPHA samplers (0.003241315 m3/hr) and exposure duration.

## Data processing and quality control
- Some raw samples were excluded due to incorrect exposure or weather-related losses; flagged data noted on page 4 of the accompanying document.
- Quality criteria:
  - Coefficient of variation (CV) of replicates < 15% used to determine validity; if CV > 15%, replicates reviewed for potential discards; valid results may be flagged (103).
  - Missing samplers assigned -9999.00 and marked invalid (-1).
  - Sampler duration longer or shorter than normal (due to weather/staffing) flagged.
  - Local contamination or other deviations recorded; results from affected samplers discarded if not representative; final site data is the average of remaining results.
- Final dataset consolidation:
  - Dataset: UWT_Ballynahone_Bog_Data_Sep_2014-Dec_2017.csv containing accepted data with appropriate flags.
  - Data fields per row: site name, exposure start/end dates, NH3 concentration (µg NH3 m-3), and a data flag.
  - All NH3 concentrations are monthly averages for the specified exposure period (units: µg NH3 m-3).

## Data structure and dataset contents
- Dataset contents:
  - Rows: one month of data per site.
  - Columns include: site name, unique site identifier, network_id (UWT), parameter_id, exposure start/end dates and times, NH3 concentration, detection/qualification flags (e.g., less than detection limit), verification status, data capture percentage, validity status, EMEP data status code, and Month-Year (mmm-yy).
- Site information included:
  - Ballynahone bog_1 through Ballynahone bog_8.
  - For each site: start date (01/09/2014), end date (ongoing at the time of dataset), latitude, longitude, and height of air inlet above ground (1.5 m).

## Data quality flags and status
- Data quality and provenance are captured via EMEP and internal UK-AIR flags:
  - Data capture, validity, and reason codes (e.g., detection limits, CV issues, sampling period deviations, contamination, local influences, and other data issues) accompany each record.
  - Flags indicate whether a value is valid, whether a measurement is below detection/quantification limits, and whether any remediation or exclusion applied.
- Typical outcomes:
  - Valid measurements (with or without minor caveats).
  - Measurements flagged as not valid or with specific reasons (e.g., contamination, sampling period anomalies, nearby activity).

## How to use the data
- Use for assessing spatial and temporal patterns of NH3 along the Ballynahone Bog transect from 2014 to 2017.
- Consider data flags and quality notes to determine inclusion in analyses and whether certain months/sites should be excluded or treated as uncertain.
- Concentrations represent monthly average ambient NH3 during the exposure period, enabling trend analyses and impact assessments for peatland NH3 exposure.

## Limitations, caveats, and recommendations
- Raw data contained issues: some samples exposed incorrectly or lost due to adverse weather; such data are not used for deposition estimates.
- Data completeness can be impacted by weather and animal interference leading to missing samplers.
- Some months/sites have longer/shorter sampling durations; these are flagged and should be treated accordingly in analyses.
- Users should consult the accompanying dataset documentation for detailed definitions of flags and field codes before analysis.

## Data provenance and access
- Origin: field measurements conducted by Ulster Wildlife Trust and analyzed by CEH Edinburgh.
- Final data are compiled into the CSV: UWT_Ballynahone_Bog_Data_Sep_2014-Dec_2017.csv, with accompanying site information for mapping and context.
- Site coordinates and metadata provided to enable geospatial analyses and reproducibility.