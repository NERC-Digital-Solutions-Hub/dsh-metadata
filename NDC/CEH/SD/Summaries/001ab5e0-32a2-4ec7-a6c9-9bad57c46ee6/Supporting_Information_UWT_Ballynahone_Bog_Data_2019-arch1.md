# Ammonia measurements from passive samplers at Ballynahone Bog field site, Northern Ireland, 2019

## Overview
- A transect of sampling sites through Ballynahone National Park (an ASSI/SAC and Ramsar site) in Northern Ireland.
- Monitoring ammonia (NH3) concentrations due to potential emissions from local poultry installations.
- Local site operator: Ulster Wildlife Trust (UWT); analysis performed by UK Centre for Ecology and Hydrology Edinburgh (CEH).
- Measurement method: CEH ALPHA passive samplers deployed monthly along the transect to estimate ambient NH3 concentrations.

## Measurement method and protocol
- Samplers: CEH ALPHA ® passive samplers with citric acid coated filter; diffusion through a PTFE membrane; orientation with membrane end facing downward.
- Deployment: Replicate samplers attached to a shelter on a pole at ~1.5 m above ground; exposed in monthly cycles.
- Analysis: Exposed samplers extracted into deionised water and analyzed by SEAL AA3 using a colorimetric method.
- Concentration calculation: Convert sampler concentration to average ambient NH3 concentration using a known uptake rate (0.003241315 m3 h-1) and exposure duration.
- Data units: Micrograms of NH3 per cubic metre of air (µg NH3 m-3).
- Data issues: Some samples were exposed incorrectly or lost due to weather; flagged in the dataset.

## Data processing and quality control
- Final dataset: UWT_Ballynahone_Bog_Data_2019.csv containing accepted data values with flags.
- Quality rules:
  - CV check: Coefficient of variation across replicates < 15%; if >15%, replicates reviewed; data flagged as valid (103) if considered representative.
  - Missing samplers: Replaced by -9999.00 and marked invalid (-1).
  - Sampler duration: Deviations from the usual monthly cycle flagged.
  - Local contamination/influences: Site operator notes used to discard non-representative samplers; reported site data reflect the average of remaining results.
- Data structure: Each row represents one month’s data for a single site with:
  - Site name, start and end dates, ammonia concentration for the exposure period, and a data flag.
  - Concentrations are the monthly average for the exposure period.
- Dataset metadata: Includes site identifiers, network_id, parameter_id, measurement start/end dates and times, detection information, verification status, unit, data capture percentage, validity, EMEP status codes, and month-year.

## Data content and metadata
- Content format: Rows correspond to month-by-site measurements; columns include site name, unique identifiers, exposure period, ammonia concentration, and a series of flags and metadata.
- Measurement details:
  - Ammonia concentration in µg NH3 m-3 for the specified exposure period.
  - Detection-related flags: values below detection limit (0.03 µg NH3 m-3) noted.
  - Verification status: codes indicating verification level (Not verified, Preliminary verified, Verified).
  - Data capture: percentage of data captured for the period.
  - Validity flag: indicates whether the data point is considered valid.
  - EMEP data status and related flags (including data capture and validity interpretations).
- Data status examples: Flags describe issues such as sampling period length, contamination, nearby activities, or other quality concerns; some flags denote valid measurements despite potential minor concerns.

## Site information
- Ballynahone bog_1 to Ballynahone bog_8:
  - Start date: 01/09/2014 for all sites.
  - End date: Ongoing.
  - Coordinates:
    - bog_1: 54.82223827, -6.67860685
    - bog_2: 54.82303694, -6.67686906
    - bog_3: 54.82331637, -6.67530382
    - bog_4: 54.82396942, -6.67339952
    - bog_5: 54.82446239, -6.67000651
    - bog_6: 54.82514962, -6.67946104
    - bog_7: 54.82165647, -6.67468906
    - bog_8: 54.81616100, -6.65596700
  - Inlet height above ground: 1.5 m
- Site information provides the spatial context necessary for analyzing spatial gradients along the transect.

## Data flags, interpretation, and usage for analysis
- Data quality flags indicate:
  - Valid measurements vs. not valid
  - Reasons for data flagging (e.g., detection limits, contamination, sampling period deviations, or local influences)
  - Verification status and data status codes (EMEP codes) accompanying each record
- For analysts:
  - Use replicates to assess precision (CV < 15% as a quality criterion).
  - Exclude or carefully treat records with missing samplers, abnormal sampling durations, or documented local contamination.
  - Consider applying data capture percentages and verification status to filter datasets for specific analyses.
  - Combine spatial (site coordinates) and temporal (month-year) data to examine temporal trends, transect spatial gradients, and potential correlations with local sources.
  - Use EMEP and validity codes to align with reporting standards and to document data quality in analyses and visualizations.

## Purpose and potential analyses
- Objective: Support assessment of NH3 exposure across Ballynahone Bog and evaluation of potential impacts from local poultry installations.
- Analytic opportunities for an analyst:
  - Temporal trends of NH3 concentrations at each site and along the transect.
  - Spatial gradients across the eight sites to detect local source influence or deposition patterns.
  - Correlation of NH3 concentrations with potential local activity indicators (from site notes and metadata).
  - Integration with broader environmental data (e.g., meteorology, vegetation) to explore deposition and ecological effects.
  - Data quality screening to produce a robust subset for modelling NH3 dispersion and deposition.

## Availability and file naming
- Final dataset name: UWT_Ballynahone_Bog_Data_2019.csv
- Content: Contains the accepted, quality-flagged monthly NH3 concentration data for each site along the Ballynahone Bog transect, with detailed metadata and quality flags per record.
- Site metadata and coordinates are provided to enable reproducible spatial analyses.