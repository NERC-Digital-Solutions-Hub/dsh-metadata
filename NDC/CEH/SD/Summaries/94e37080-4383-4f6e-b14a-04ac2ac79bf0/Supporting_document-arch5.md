# Supporting document for diurnal soil nitrous oxide emission datasets

- Purpose: Document the diurnal N2O emission datasets used in the study "Diurnal variability in soil nitrous oxide emissions is a widespread phenomenon" (to be published in Global Change Biology). The data enable analysis of diurnal patterns in soil N2O flux across multiple studies.

## Data scope and content

- Data origins: Extracted from 46 published journal articles (1983–2019) that performed diurnal N2O flux measurements.
- Dataset types:
  - N2O_flux datasets: csv files named N2O_xxx.csv containing time (hour), N2O_flux (μg N2O-N m-2 h-1), and norm_flux (0–1) per 24-hour cycle.
  - Soil temperature datasets: csv files named soil_temp_xxx.csv containing time (hour) and soil temperature at 5–10 cm depth (°C).
  - Non-diurnal parameters: dataset_info.csv with data code, literature title, and additional parameters (pH, bulk density, soil texture, season, soil water-filled pore space, irrigation, grazing, etc.).
  - Diurnal categorisation data: diurnal_pattern_categorisation_data.csv with processed fields describing diurnal pattern classification and related metrics.
- Coverage:
  - 286 diurnal N2O datasets extracted from the 46 publications.
  - 160 datasets include soil temperature data; 157 include soil pH data; 115 include bulk density; 175 include soil texture; 135 include soil moisture; 261 include season of flux measurements. All articles report N fertilisation and land use.

## Data collection and processing

- Literature search and selection:
  - Databases: Web of Science Core Collection and ScienceDirect.
  - Cut-off: 28 August 2019.
  - Initial results: 314 articles identified; 83 duplicates removed.
  - Inclusion criteria: N2O flux measurements on cropland/grassland/forests; five or more measurements per 24-hour cycle; first and last measurements within 00:00–03:59 and 20:00–23:59 respectively.
  - Final dataset: 46 articles eligible; 286 diurnal N2O flux datasets.
- Data extraction:
  - N2O flux and soil temperature data extracted from figures using Engauge Digitizer (Mitchell et al., 2020) and saved as csv per publication per day.
  - N2O flux values standardized to μg N2O-N m-2 h-1.
  - Time data converted to decimal hours (0.00–23.99 h).
- Normalization:
  - N2Onorm = (N2O_t − N2O_min) / (N2O_max − N2O_min); bound 0–1.
- Diurnal pattern categorisation:
  - Datasets categorized into three patterns: daytime peaking, night-time peaking, non-diurnal.
  - Threshold for pattern classification adjusted for datasets with measurement windows shorter than 24 hours:
    Adjusted threshold = (24 / hours between first and last measurement) × 50%.
  - Emission percentage calculations for 12-hour windows:
    04:00–16:00 h, 06:00–18:00 h, 08:00–20:00 h (via trapezoidal integration).
  - Daytime peaking subcategories:
    - Morning peaking vs afternoon peaking based on which 12-hour window surpasses the threshold and pattern of max/min times.
  - Night-time peaking:
    - Based on positions of max/min within 04:30–19:30 h and the 06:00–18:00 h emission share being below the threshold.
  - Non-diurnal:
    - Datasets not meeting daytime or night-time conditions.
- Processed data outputs:
  - diurnal_pattern_categorisation_data.csv contains for each dataset: max_hour, sec_max_hour, min_hour, sec_min_hour, cum_all, cum_early, cum_early_percent, cum_late, cum_late_percent, cum_mid, cum_mid_percent, adjusted_threshold, first_condition_D, second_condition_D, third_condition_D, first_condition_N, second_condition_N, third_condition_N, daytime_peaking, nighttime_peaking.

## Data structure and fields

- N2O_xxx.csv:
  - Fields: time (hour, decimal), N2O_flux (μg N2O-N m-2 h-1), norm_flux (0–1).
- soil_temp_xxx.csv:
  - Fields: time (hour, decimal), Curve1 (soil temperature at 5–10 cm depth, °C).
- dataset_info.csv:
  - Fields: dataset code, literature title, and non-diurnal parameters (pH, bulk density, soil texture, season, soil water-filled pore space, irrigation, grazing).
- diurnal_pattern_categorisation_data.csv:
  - Fields: max_hour, sec_max_hour, min_hour, sec_min_hour, cum_all, cum_early, cum_early_percent, cum_late, cum_late_percent, cum_mid, cum_mid_percent, adjusted_threshold, first_condition_D, second_condition_D, third_condition_D, daytime_peaking, nighttime_peaking, and related flags (N-conditions for night-time categorisation).

## References and provenance

- 46 primary publications form the data backbone (full references listed in the document), covering diverse soils, management practices, and geographic regions.
- Data recovery and transformation steps (e.g., Engauge Digitizer) are documented to support reproducibility and provenance.

## Governance and data stewardship considerations

- Provenance and reproducibility:
  - Clear linkage between N2O_xxx.csv and soil_temp_xxx.csv via the dataset number; traceable back to 46 source publications.
  - Original data were digitized from figures, introducing potential digitization error; normalization and diurnal categorisation steps are documented to enable auditability.
- Metadata and interoperability:
  - Comprehensive metadata included (study literature, non-diurnal context, measurement times, and environmental variables where available).
  - Data are standardized to common units and time representation, but rely on cross-study harmonization (e.g., 5–10 cm soil temperature depth, μg N2O-N m-2 h-1).
- Quality and completeness:
  - Large, multi-study compilation with varying data availability (some datasets missing soil temperature, pH, moisture, etc.).
  - Diurnal pattern categorisation is rule-based with an adjustable threshold to accommodate heterogeneous measurement windows.
- Access, reuse, and licensing:
  - Data derive from published articles; assess licensing and reuse terms for each source when external use or redistribution is planned.
- Data governance recommendations for stewardship:
  - Maintain and periodically refresh metadata to reflect any updates or new studies.
  - Provide a data dictionary and method notes for the normalization, time conversion, and diurnal categorisation processes.
  - Consider implementing data quality flags to indicate digitization-derived uncertainties and any missing auxiliary parameters.
  - Ensure robust linkage between day-level N2O flux data and auxiliary parameters (e.g., soil properties, management) to support discoverability and reuse.
  - Document versioning and changes to categorisation rules or thresholds to preserve traceability of results over time.