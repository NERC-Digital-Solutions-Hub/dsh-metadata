# Supporting document for diurnal soil nitrous oxide emission datasets

- Purpose and scope
  - Supports a study on diurnal variability in soil nitrous oxide (N2O) emissions, to be published in Global Change Biology.
  - Contains four data types extracted from 46 published articles, totaling 286 diurnal N2O flux datasets.

- Data types and relationships
  - N2O_flux datasets (N2O_xxx.csv): time (hour), N2O flux (μg N2O-N m-2 h-1), and normalised flux (norm_flux) within each 24-hour cycle.
  - Soil temperature datasets (soil_temp_xxx.csv): time and soil temperature at 5–10 cm depth (°C) within each 24-hour cycle.
  - dataset_info.csv: bibliographic data (data code, literature title) plus non-diurnal parameters (e.g., pH, bulk density, soil texture, season, soil water-filled pore space, irrigation, grazing) for each dataset.
  - diurnal_pattern_categorisation_data.csv: processed data including time of maximum/minimum N2O flux (max_hour, sec_max_hour, min_hour, sec_min_hour), cumulated flux metrics (cum_all, cum_early, cum_mid, cum_late) and percentages for 04:00–16:00, 06:00–18:00, 08:00–20:00, plus adjusted thresholds and condition flags for daytime and nighttime patterns.

- Data collection and processing methodology
  - Literature search: Web of Science Core Collection and ScienceDirect up to 28 August 2019.
  - Search terms focused on N2O diurnal/high-temporal flux measurements in soils.
  - Initial yield: 314 articles; after de-duplication and screening, 46 publications included, yielding 286 diurnal N2O flux datasets.
  - Data extraction: N2O flux and soil temperature values extracted from figures using Engauge Digitizer and converted to numerical format.
  - Data organization: Each publication’s data aligned so that N2O_flux and corresponding soil_temp (if available) share the same dataset index (e.g., N2O_001.csv with soil_temp_001.csv).

- Diurnal categorization and thresholds
  - Datasets categorized into three diurnal patterns: daytime peaking, night-time peaking, non-diurnal.
  - Emission percentiles calculated for three 12-hour windows (04:00–16:00, 06:00–18:00, 08:00–20:00) using trapezoidal integration; thresholds adjusted per dataset due to varying measurement durations.
  - Daytime peaking subcategories: morning peaking (04:00–16:00 window) or afternoon peaking (08:00–20:00 window) based on which window exceeds the adjusted threshold and the distribution of daytime vs. afternoon emissions.
  - Night-time peaking criteria: primary night-time dominance with a reduced daytime emission threshold.
  - Non-diurnal: does not meet daytime or night-time criteria.
  - Adjusted threshold formula:
    - Adjusted threshold = (24 / Hours between first and last measurement) × 50%
  - Key outputs in diurnal_pattern_categorisation_data.csv include condition flags (first_condition_D, second_condition_D, third_condition_D; similarly for N for night), daytime_peaking, and nighttime_peaking indicators.

- Data structure and field details
  - N2O_xxx.csv: fields include time (hour), N2O_flux (μg N2O-N m-2 h-1), norm_flux (0–1).
  - soil_temp_xxx.csv: fields include time (hour/minute in decimal form) and Curve1 (°C).
  - dataset_info.csv: fields include literature title and non-diurnal parameters (pH, bulk density, soil texture, season, SWP, irrigation, grazing).
  - diurnal_pattern_categorisation_data.csv: fields include max_hour, sec_max_hour, min_hour, sec_min_hour, cum_all, cum_early, cum_early_percent, cum_late, cum_late_percent, cum_mid, cum_mid_percent, adjusted_threshold, first_condition_D/N, second_condition_D/N, third_condition_D/N, daytime_peaking, nighttime_peaking, and related categorical indicators.

- Data coverage and sources
  - 46 journal articles (1983–2019) represented in Table 1 (references listed in the document).
  - 286 diurnal N2O flux datasets; of these, 160 include soil temperature data, 157 include soil pH, 115 include bulk density, 175 include soil texture, 135 include soil moisture, and 261 include data on the season of flux measurements.
  - All articles provided information on N fertilisation and land use; non-diurnal parameters are captured in dataset_info.csv.

- Data quality, limitations, and governance considerations
  - Data extraction relied on digitizing figures, which may introduce digitization errors.
  - Metadata completeness varies across source articles; the dataset collects non-diurnal parameters where available, but gaps may remain.
  - Data normalization (N2Onorm) standardizes magnitudes across studies but may obscure absolute flux differences.
  - The approach provides a harmonised diurnal categorization framework suitable for monitoring and comparative analyses, but users should consider potential biases due to uneven sampling durations and measurement methods across studies.
  - The documentation implies sharing underlying data and processing methods (e.g., data codes, processed categorization data), aligning with open data practices, albeit actual data access would depend on dissemination policies of the study.

- Reference context
  - The dataset compiles and references 46 published articles, covering a broad range of soils, land uses, and measurement methodologies relevant to diurnal N2O dynamics.