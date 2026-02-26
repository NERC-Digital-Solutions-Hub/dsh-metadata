# Supporting document for diurnal soil nitrous oxide emission datasets

- Purpose and scope
  - Supporting datasets were created for the study “Diurnal variability in soil nitrous oxide emissions is a widespread phenomenon” to be published in Global Change Biology.
  - Datasets compile diurnal N2O flux measurements from 46 published articles, enabling analysis of diurnal patterns across cropland, grassland, and forest soils.

- Data types and structure
  - N2O_flux datasets (csv files named N2O_xxx.csv)
    - Contain time of flux measurement (hour), measured N2O flux in μg N2O-N m-2 h-1, and normalised flux (norm_flux) within each 24-hour cycle.
  - Soil temperature datasets (csv files named soil_temp_xxx.csv)
    - Contain time of measurement and soil temperature at 5–10 cm depth (°C) within each 24-hour cycle.
  - Pairing
    - The digits after N2O_ and soil_temp_ indicate the same day and study; N2O_001.csv pairs with soil_temp_001.csv for joint analysis.
  - Metadata and processing files
    - dataset_info.csv: literature title, data code, and other non-diurnal parameters (e.g., pH, bulk density, soil texture, season, soil moisture, irrigation, grazing) linked to each dataset.
    - diurnal_pattern_categorisation_data.csv: processed outputs describing diurnal pattern classification and derived metrics (see below).

- Data collection and generation process
  - Literature search
    - Databases: Web of Science Core Collection and ScienceDirect.
    - Cut-off: August 28, 2019.
    - Search terms focused on N2O flux/emissions, diurnal/high-temporal data, soils.
  - Study selection
    - Initial set: 314 articles; after de-duplication and inclusion criteria, 46 articles were retained.
    - Datasets: 286 diurnal N2O flux datasets extracted from these articles; of these, 160 included soil temperature data, 157 included soil pH, 115 bulk density, 175 soil texture, 135 soil moisture, and 261 seasonal data; fertilisation and land use data were available in all articles.
  - Data extraction and digitisation
    - N2O flux and soil temperature values were extracted from figures using Engauge Digitizer and converted to numerical form.
    - Each 24-hour cycle’s flux was extracted and saved as a separate CSV file.
  - Normalisation
    - N2O flux within each dataset was normalised to a 0–1 scale:
      - norm_flux,t = (N2O_t − N2O_min) / (N2O_max − N2O_min)
    - This eliminates magnitude differences across datasets to focus on diurnal patterns.

- Diurnal pattern categorisation
  - Data categorisation into three patterns (based on diurnal timing) using a dataset-specific, adjusted threshold approach:
    - Daytime peaking
      - Subcategories: morning peaking and afternoon peaking.
      - Criteria include timing of peak values (highest/second highest between 04:30–19:30 h), a trough timing criterion, and a percentage-emission threshold.
    - Night-time peaking
      - Criteria include trough timing (lowest/second lowest between 04:30–19:30 h), a peak timing criterion (highest between 00:00–09:00 h or 18:00–00:00 h), and a percentage-emission threshold.
    - Non-diurnal
      - Datasets not meeting daytime or night-time criteria.
  - Threshold adjustment
    - The emission percentage threshold is dataset-specific:
      - Adjusted threshold = (24 / hours_between_first_and_last_measurement_in_dataset) × 50%
      - This accounts for datasets shorter than a full 24-hour period.
  - Derived metrics in diurnal_pattern_categorisation_data.csv
    - max_hour, sec_max_hour: times of maximum and second maximum N2O flux.
    - min_hour, sec_min_hour: times of minimum and second minimum N2O flux.
    - cum_early, cum_early_percent: cumulative N2O flux and its percentage for 04:00–16:00 h.
    - cum_late, cum_late_percent: cumulative N2O flux and its percentage for 08:00–20:00 h.
    - cum_mid, cum_mid_percent: cumulative N2O flux and its percentage for 06:00–18:00 h.
    - cum_all: cumulative N2O flux across the first to last measurement in a dataset.
    - first_condition_D, second_condition_D, third_condition_D: indicators for daytime peaking criteria (Y/N/E; with morning/evening nuance).
    - first_condition_N, second_condition_N, third_condition_N: indicators for night-time peaking criteria.
    - daytime_peaking, nighttime_peaking: final classification flags (Y/N) for daytime/night-time peaking; non-diurnal indicated when both are N.

- Data quality, standards, and limitations
  - Data provenance
    - All N2O flux and temperature values were digitised from published figures, which may introduce digitisation uncertainty.
  - Standardisation and comparability
    - Normalisation to 0–1 enables comparison of diurnal shapes but removes absolute magnitude, which may be important for some analyses.
  - Metadata and discoverability
    - dataset_info.csv provides literature context and additional soil/management variables, supporting richer interpretation and cross-dataset analyses.
  - Temporal scope and coverage
    - Coverage spans studies from 1983–2019; 46 articles form the basis of 286 diurnal datasets.
  - Potential gaps
    - Some datasets lack temperature or other non-diurnal parameters; not all datasets have full metadata across all variables.

- References and scope
  - Table 1 and the References section enumerate 46 cited articles used to build the diurnal N2O emission datasets (spanning soils, management practices, and diurnal patterns).

- Notes for data leaders and reuse
  - Emphasises the importance of diurnal variability in N2O emissions and the value of high-temporal-resolution data for accurate emission estimates.
  - Demonstrates a workflow for assembling, digitising, normalising, and categorising diurnal soil gas flux data from diverse studies.
  - Provides a framework (with datasetInfo and diurnalPatternCategorisation data) to support data governance, interoperability, and potential community of practice around diurnal GHG flux datasets.