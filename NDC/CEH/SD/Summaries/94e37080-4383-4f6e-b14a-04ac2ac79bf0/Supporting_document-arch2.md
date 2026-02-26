# Supporting document for diurnal soil nitrous oxide emission datasets

## Overview
- Provides diurnal N2O emission datasets used in the study “Diurnal variability in soil nitrous oxide emissions is a widespread phenomenon” (Global Change Biology).
- Compiles data from 46 published journal articles (1983–2019) that reported diurnal N2O flux measurements in cropland, grassland, or forest soils.
- Aims to support standardized environmental monitoring by delivering harmonised data and processing methods.

## Data types and contents
- Four data types extracted from source articles:
  - N2O_*.csv: time of flux measurement, diurnal N2O flux (μg N2O-N m^-2 h^-1), and normalised N2O flux data (N2Onorm) within every 24-hour cycle.
  - soil_temp_*.csv: time of soil temperature measurement and soil temperature at 5–10 cm depth within every 24-hour cycle.
  - dataset_info.csv: bibliographic data, article titles, and additional non-diurnal parameters (e.g., pH, bulk density, soil texture, season, soil moisture, irrigation, grazing) for each dataset.
  - diurnal_pattern_categorisation_data.csv: processed data including maximum/minimum hours, cumulative flux, percentage of flux in 04:00–16:00, 08:00–20:00, and 06:00–18:00 periods, and the criteria flags for daytime and nighttime peaking.
- Diurnal categorisation data include fields describing whether a dataset meets conditions for daytime peaking, morning vs. afternoon peaks, night-time peaking, or non-diurnal patterns.

## Data collection and processing
- Literature search sources:
  - Web of Science Core Collection and ScienceDirect.
  - Cut-off date: 28 August 2019.
  - Search terms focused on N2O/diurnal/soil fluxes.
- Initial set and filtering:
  - Identified 314 articles; 83 duplicates removed.
  - Inclusion criteria: N2O flux measured on cropland/grassland/forest soils; five or more flux measurements per 24-hour cycle; first/last measurement within 00:00–03:59 and 20:00–23:59 respectively.
  - Result: 46 articles eligible, yielding 286 diurnal N2O flux datasets.
- Additional variables:
  - Of the 286 datasets: 160 had soil temperature data (5–10 cm), 157 had soil pH, 115 bulk density, 175 soil texture, 135 soil moisture, 261 season data.
  - Fertilisation and land-use information reported across articles; recorded in dataset_info.csv.
- Data extraction:
  - N2O flux and soil temperature data were digitised from figures using Engauge Digitizer.
  - Each 24-hour cycle data saved as a separate CSV file.
- Normalisation and units:
  - N2O flux standardised to μg N2O-N m^-2 h^-1.
  - Normalised flux (N2Onorm) bound to 0–1 via N2Onorm,t = (Nt - N2Omin) / (N2Omax - N2Omin).
- Pattern categorisation (diurnal patterns):
  - Datasets categorized into daytime peaking, night-time peaking, or non-diurnal based on three conditions and a dataset-length-adjusted threshold.
  - Threshold adjustment accounts for datasets shorter than 24 h:
    - Adjusted threshold = (24 / hours between first and last measurement) × 50%.
  - Emission shares calculated for three 12-hour windows: 04:00–16:00, 06:00–18:00, 08:00–20:00 using trapezoidal integration (R package pracma).
  - Daytime peaking subcategories: morning peaking (04:00–16:00 > threshold and afternoon share appropriate) or afternoon peaking (08:00–20:00 > threshold with morning share).
  - Night-time peaking criteria focus on minimum/maximum timing and 06:00–18:00 share relative to threshold.
  - Non-diurnal if neither daytime nor night-time criteria are met.

## Diurnal pattern categorisation data
- diurnal_pattern_categorisation_data.csv includes:
  - max_hour, sec_max_hour, min_hour, sec_min_hour.
  - cum_all (cumulative N2O flux across first to last measurement) and cumulative shares for early, mid, and late day windows with their percentages.
  - first_condition_D, second_condition_D, third_condition_D (daytime peaking criteria) and first_condition_N, second_condition_N, third_condition_N (night-time peaking criteria).
  - daytime_peaking and nighttime_peaking flags indicating pattern classification (Y/N) and sub-classifications (morning/afternoon for daytime).

## Data structure and accessibility
- N2O_xxx.csv: per-dataset time, N2O_flux, and N2Onorm (within a 24-hour cycle).
- soil_temp_xxx.csv: per-dataset time and soil temperature at 5–10 cm (Curve1).
- dataset_info.csv: literature titles and additional non-diurnal parameters (pH, bulk density, soil texture, season, SWP, irrigation, grazing).
- diurnal_pattern_categorisation_data.csv: processed diurnal pattern metrics and categorisation flags.

## Coverage and references
- Table 1 lists 46 referenced articles providing the diurnal N2O data (examples include Akiyama & Tsuruta; Laville et al.; Reeves & Wang; Scheer et al.; Williams et al.; Yang et al.; Yao et al.; Zona et al. and others).
- The compiled body supports cross-study analyses of diurnal N2O behavior and informs methodologies for monitoring and policy evaluation related to soil N2O emissions.

## Implications for monitoring and policy analysis
- Delivers a harmonised, multi-study dataset suitable for:
  - Comparing diurnal N2O emission patterns across land uses and management practices.
  - Assessing the diurnal timing of emissions to improve sampling strategies and flux estimates.
  - Integrating diurnal N2O data with other environmental datasets (e.g., soil physics, climate, land use) to enhance monitoring programs.
- Emphasises the importance of data accessibility and reusability by providing raw diurnal data, processed pattern classifications, and non-diurnal parameters.