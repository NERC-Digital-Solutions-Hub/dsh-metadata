# Supporting document for diurnal soil nitrous oxide emission datasets

- Overview
  - A compilation and processing of diurnal N2O emission datasets used in the study “Diurnal variability in soil nitrous oxide emissions is a widespread phenomenon” (Global Change Biology).
  - Based on 46 published journal articles (1983–2019) and yields 286 diurnal N2O flux datasets.
  - Datasets integrate N2O flux measurements, soil temperature, and ancillary soil parameters across multiple studies.

- Data types and structure
  - Four data types/files:
    - N2O_xxx.csv: time of flux measurement, diurnal N2O flux (μg N2O-N m^-2 h^-1), and normalised N2O flux (norm_flux) for each 24-hour cycle.
    - soil_temp_xxx.csv: time of soil temperature measurement and soil temperature at 5–10 cm depth (°C) for each 24-hour cycle.
    - dataset_info.csv: literature title, data code, and non-diurnal parameters (e.g., pH, bulk density, soil texture, season, soil water-filled pore space, irrigation, grazing) for each dataset.
    - diurnal_pattern_categorisation_data.csv: processed data including max/second max/min/second min times, cumulative N2O flux for various periods, percentages for 04:00–16:00, 06:00–18:00, and 08:00–20:00, and adjusted thresholds per dataset; flags for daytime and night-time pattern criteria.
  - Dataset alignment: N2O_001.csv pairs with soil_temp_001.csv (same day/study) and should be analyzed together.

- Data collection and generation methods
  - Literature search conducted in Web of Science Core Collection and ScienceDirect, with cut-off date 28 August 2019.
  - Search terms focused on diurnal/high-temporal N2O fluxes in soils.
  - From 314 initial articles (215 Web of Science, 99 ScienceDirect), 83 duplicates removed, yielding 46 eligible publications.
  - Data extraction:
    - N2O flux and soil temperature data were digitised from figures using Engauge Digitizer (Mitchell et al., 2020) and saved as 24-hour cycle datasets.
  - Data scope:
    - 286 diurnal N2O flux datasets extracted; subset with temperature data: 160 datasets; with pH: 157; with bulk density: 115; with soil texture: 175; with soil moisture: 135; with season data: 261.
  - Additional factors: fertilisation and land-use information provided in dataset_info.csv.

- Processing and diurnal pattern categorisation
  - Normalisation:
    - N2O flux per dataset standardised to μg N2O-N m^-2 h^-1 and normalised to a 0–1 scale using (N2O_t − N2O_min) / (N2O_max − N2O_min).
  - Time handling:
    - Time-of-day converted to decimal hours (0.00–23.99 h).
  - Diurnal categorisation:
    - Datasets classified into three diurnal patterns using three objective conditions and an adjusted threshold.
    - Adjusted threshold calculation:
      - Adjusted threshold = (24 / Hours between first and last measurement) × 50%.
    - Emission window analysis (12-hour periods):
      - 04:00–16:00 h, 06:00–18:00 h, 08:00–20:00 h; cumulative emissions computed via trapezoidal integration (R package pracma).
  - Pattern definitions:
    - Daytime peaking (with subcategories):
      - Condition 1: Highest and second highest N2Onorm occur between 04:30–19:30 h.
      - Condition 2: Lowest N2Onorm occurs outside 00:00–09:00 h or 18:00–00:00 h.
      - Condition 3: Emission percentage in daytime windows exceeds adjusted threshold.
      - If daytime percentage in 04:00–16:00 h exceeds threshold and is higher than afternoon percentage → morning peaking; if 08:00–20:00 h exceeds threshold and higher than morning → afternoon peaking.
    - Night-time peaking:
      - Condition 1: Lowest and second lowest N2Onorm occur between 04:30–19:30 h.
      - Condition 2: Highest N2Onorm is between 00:00–09:00 h or 18:00–00:00 h.
      - Condition 3: Emission percentage in 06:00–18:00 h is smaller than the threshold.
    - Non-diurnal:
      - Dataset that does not meet daytime peaking or night-time peaking conditions.
  - Outputs:
    - diurnal_pattern_categorisation_data.csv includes max_hour, sec_max_hour, min_hour, sec_min_hour, cum_all, cum_early, cum_early_percent, cum_mid, cum_mid_percent, cum_late, cum_late_percent, first/second condition flags, and daytime/night-time pattern labels.

- Nature, units, and data structure details
  - N2O flux units: μg N2O-N m^-2 h^-1.
  - Time units: decimal hours (0.00–23.99 h).
  - Normalised flux: unitless, 0–1 range.
  - Data structure:
    - N2O_xxx.csv: time, N2O_flux, norm_flux.
    - soil_temp_xxx.csv: time, Curve1 (soil temperature at 5–10 cm).
    - dataset_info.csv: literature title, data code, and non-diurnal parameters.
    - diurnal_pattern_categorisation_data.csv: pattern metrics and categorisation results.

- Dataset coverage and documentation
  - 46 published articles contributing to 286 diurnal N2O datasets.
  - Temperature data present in 160 datasets; soil pH in 157; bulk density in 115; soil texture in 175; soil moisture in 135; seasonal data in 261.
  - All articles provided information on N fertilisation and land use (recorded in dataset_info.csv).
  - Table 1 in the document lists the 46 references with study titles.

- References and sources
  - Consolidated references from the 46 articles (e.g., Akiyama & Tsuruta; Laville; Reeves & Wang; Scheer; Shurpali; and others) used to compile and contextualise the diurnal N2O datasets.
  - Engauge Digitizer tool used for data recovery from figures (Mitchell et al., 2020).