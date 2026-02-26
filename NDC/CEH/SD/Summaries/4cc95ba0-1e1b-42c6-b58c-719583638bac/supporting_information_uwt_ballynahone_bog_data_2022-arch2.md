# Ammonia measurements from passive samplers at Ballynahone Bog field site, Northern Ireland, 2022

## Purpose and context
- Passive sampler campaign to monitor NH3 air concentrations along a transect through Ballynahone Bog, an ammonia-sensitive peatland within Ballynahone National Park (ASSI/SAC and Ramsar site) in Northern Ireland.
- Initiated due to concerns that NH3 emissions from nearby poultry livestock installations could affect the bog.
- Site operator: Ulster Wildlife Trust (UWT); analysis: UK Centre for Ecology and Hydrology Edinburgh (UKCEH).

## Sampling design and measurement method
- UKCEH ALPHA® passive samplers deployed along a transect through the bog, attached to shelters at ~1.5 m above ground.
- Replicate samplers used per site to improve reliability.
- Exposure: monthly cycles at the start of each month.
- Analysis workflow:
  - Exposed samplers extracted into deionised water.
  - Water analysed by SEAL AA3 colorimetric method to determine ammonia concentration.
  - Concentrations converted to average ambient air concentration using a known sampler uptake rate (0.0038422 m3 hr-1) and exposure duration.

## Data quality assurance and flags
- Raw data quality checks and exclusion:
  - Samples exposed incorrectly or lost due to weather/animal interference are excluded from deposition estimates; flagged accordingly.
- Quality rules applied:
  - Coefficient of variation (CV) of replicates: CV < 15% required; otherwise replicates may be discarded; valid data flagged.
  - Missing samplers: flagged and recorded as -9999.00 and invalid (-1).
  - Sampling duration anomalies: longer/shorter than normal cycles flagged.
  - Local contamination or other deviations: notes reviewed; non-representative results discarded if necessary; final data represent averages of remaining valid results.
- Data status and flags align with EMEP conventions (data quality, capture, and validity flags).

## Data product and structure
- Final dataset: UWT_Ballynahone_Bog_Data_2022.csv
- Key contents:
  - Each row: one month of data for a single site; includes site name, start and end dates, ammonia concentration for exposure period, and a data flag.
  - Concentrations reported as micrograms per cubic meter (µg NH3 m-3) of air for the exposure period.
- Dataset metadata and coding:
  - Columns include: site name, unique site identifier, network_id, parameter_id (ALPHA_NH3_g), measurement start/end dates and times, concentration value, detection flag, verification status, data capture percentage, data validity, EMEP status codes, and month.
  - EMEP flags provided to indicate data capture, validity, and reasoning (e.g., contamination, detection limits, sampling period length, etc.).

## Site information and transect
- Ballynahone bog_1 to bog_8: eight sampling sites along the transect.
- Start date for all sites: 01/09/2014; End date: ongoing.
- Geographic coordinates (latitude/longitude) and 1.5 m air inlet height above ground for each site are provided.

## Environment and policy monitoring relevance
- Demonstrates consistent, auditable data collection and processing workflows for environmental monitoring.
- Outputs are designed for standardized presentation (reports, maps, charts) and are suitable for temporal trend analysis and policy performance scrutiny.
- Emphasizes data stewardship: data are stored, quality-assured, and prepared for upload to appropriate portals; transparency around data limitations and flagging to enable secondary analyses.

## Challenges and opportunities for analysts
- Challenge: increasing the value of the ammonia dataset by integrating with other relevant data sources to avoid “single-use” datasets.
- Challenge: enabling broader access to the underlying data used to produce final outputs, supporting transparency and secondary analyses.