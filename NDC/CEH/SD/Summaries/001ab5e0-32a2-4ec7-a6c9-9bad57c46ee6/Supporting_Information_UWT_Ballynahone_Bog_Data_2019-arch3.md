# Ammonia measurements from passive samplers at Ballynahone Bog field site, Northern Ireland, 2019

## Aim and scope
- Document reporting ammonia concentrations using passive samplers along a transect through Ballynahone Bog (ASSI/SAC and Ramsar site) in Northern Ireland.
- Managed locally by Ulster Wildlife Trust (UWT); analysis by UK Centre for Ecology and Hydrology (CEH) Edinburgh.
- Data collected to assess potential NH3 impacts from local poultry livestock installations; samplers exposed monthly.

## Methodology

- Sampling device: CEH ALPHA® passive samplers with citric acid coated filter; diffusion through a PTFE membrane; mounted at ~1.5 m height on shelters.
- Deployment: replicate samplers at each site to improve reliability; exposure cycles monthly.
- Analysis workflow:
  - Extract samplers into deionised water.
  - Analyze with SEAL AA3 colorimetric method to determine ammonia concentration on the sampler.
  - Convert to average air concentration using the known uptake rate (0.003241315 m3 h-1) and exposure duration.
- Data quality and flags:
  - Some samples excluded due to incorrect exposure or weather-related loss.
  - Data flagged for issues; final dataset includes only accepted values.

## Data structure and contents

- Final dataset: UWT_Ballynahone_Bog_Data_2019.csv.
- Row-level structure: one row per month per site; fields include site name, exposure start/end dates, ammonia concentration (µg NH3 m-3), and a data flag.
- Key fields and codes:
  - Site identifiers, network_id, parameter_id, exposure start/end dates and times.
  - Measured concentration in micrograms per cubic metre.
  - Masks for below detection limit, verification status, data capture percentage, and validity.
  - EMEP data status codes and corresponding flags (e.g., data capture quality, contamination indicators, sampling period adjustments).
- Data content notes:
  - Concentrations are average values for the specified exposure period.
  - Some data are flagged as non-ideal (e.g., below detection limit, validation status, or contamination concerns).

## Data quality assurance and flags

- Quality rules applied to raw data:
  - Coefficient of variation (CV) of replicates: CV < 15% required for reliability; otherwise replicates may be discarded or results re-evaluated (flag 103).
  - Missing samplers: denoted -9999.00 and marked invalid (-1).
  - Abnormal sampler duration: longer/shorter exposure than monthly cycle flagged.
  - Local contamination or influence: site operator notes used to discard non-representative samples; reported data averaged over remaining valid results.
- Data status codes (EMEP flags) provide:
  - Verification status (e.g., verified, preliminary verified).
  - Data capture completeness and reasonings for any exclusions.
  - Contextual reasons such as contamination, nearby activities, or detection-limit considerations.

## Site information and metadata

- Ballynahone bog_1 to Ballynahone bog_8:
  - Start date: 01/09/2014; End date: ongoing.
  - Precise latitude and longitude for each site.
  - Height of air inlet above ground: 1.5 m.
- Purposeful coverage along transect within Ballynahone National Park to represent ammonia exposure gradient.

## Practical notes and limitations

- Some data were lost or deemed invalid due to weather conditions or misexposure; such data are flagged and excluded from deposition estimates.
- Data processing relies on a fixed uptake rate and consistent exposure protocols; weather and operational constraints can affect data representativeness.
- Public sharing of underlying datasets and metadata is a consideration; data governance practices are stated to ensure transparency and quality.

## Relevance for monitoring and decision-making

- Demonstrates end-to-end monitoring workflow: site selection, passive sampling, laboratory analysis, data processing, quality assurance, and data dissemination.
- Illustrates how to handle data gaps, replicates, and contamination concerns in a monitoring framework.
- Provides a publicly shareable dataset structure and metadata to support policy scrutiny, trend analysis, and planning for future environmental health monitoring.