# Supporting document for diurnal soil nitrous oxide emission datasets

- Overview
  - Purpose: Support a study on diurnal variability of soil nitrous oxide (N2O) emissions, published in Global Change Biology.
  - Scope: Four data types extracted from 46 published articles (1983–2019) containing diurnal N2O flux measurements.
  - Output: 286 diurnal N2O flux datasets, with associated soil temperature and other non-diurnal parameters; datasets organized for cross-study analysis and self-service use.

- Data content and structure
  - N2O_xxx.csv files
    - Contents: time (hour, decimal), N2O_flux (μg N2O-N m-2 h-1), normalised flux (norm_flux; unitless) within a 24-hour cycle.
  - soil_temp_xxx.csv files
    - Contents: time (hour, decimal) and soil temperature at 5–10 cm depth (°C) within a 24-hour cycle.
  - dataset_info.csv
    - Contents: data code, literature title, and non-diurnal parameters (e.g., pH, bulk density, soil texture, season, soil water-filled pore space, irrigation, grazing) for each dataset.
  - diurnal_pattern_categorisation_data.csv
    - Contents: processed data including max and second-max hours (max_hour, sec_max_hour), min and second-min hours (min_hour, sec_min_hour), cumulative flux metrics (cum_all, cum_early, cum_late, cum_mid) and their percentages, adjusted threshold, and indicators for daytime and nighttime pattern conditions (first/second/third conditions; daytime_peaking, nighttime_peaking).

- Data collection and processing
  - Literature search
    - Databases: Web of Science Core Collection and ScienceDirect.
    - Cut-off date: 28 August 2019.
    - Search terms focused on greenhouse gases, N2O, fluxes, diurnal/high-temporal measurements, and soils.
    - Initial yield: 314 articles; after deduplication and screening, 46 eligible for data extraction (286 diurnal N2O datasets).
  - Inclusion criteria
    - N2O flux measurements on cropland, grassland, or forest soils.
    - Five or more N2O flux measurements per 24-hour cycle.
    - First and last measurements within 00:00–03:59 and 20:00–23:59, respectively.
  - Data extraction and harmonisation
    - N2O flux and soil temperature (if available) extracted from figures using Engauge Digitizer.
    - Data from each publication saved as separate N2O_xxx.csv and, if present, soil_temp_xxx.csv files.
    - Pairing: N2O_xxx.csv and soil_temp_xxx.csv datasets correspond to the same day/study via the numeric suffix (e.g., N2O_001.csv with soil_temp_001.csv).
  - Normalisation and time handling
    - N2O flux values standardised to 24-hour cycles and decimal hours (0.00–23.99).
    - Normalised N2O flux (N2Onorm) scaled to 0–1:
      N2Onorm,t = (N2Ot − N2Omin) / (N2Omax − N2Omin).
  - Diurnal categorisation
    - Computation of 12-hour period emissions (04:00–16:00, 06:00–18:00, 08:00–20:00) via trapezoidal integration; used to determine daytime vs. nighttime dominance.
    - Datasets classified into:
      - Daytime peaking (with morning vs. afternoon subcategories)
      - Night-time peaking
      - Non-diurnal
    - Adjusted threshold for categorisation:
      Adjusted threshold = (24 / hours between first and last measurement) × 50%

- Details of data fields and units
  - N2O flux: μg N2O-N m-2 h-1
  - Normalised flux: 0.0–1.0
  - Time: decimal hours (0.00–23.99)
  - Soil temperature: °C (5–10 cm depth)
  - Dataset linkage: N2O_xxx and soil_temp_xxx share the same dataset index; dataset_info.csv provides metadata and non-diurnal parameters; diurnal_pattern_categorisation_data.csv provides processed pattern metrics.

- Provenance and scope
  - Table 1 (in the document) lists 46 referenced articles used to compile the 286 diurnal N2O datasets.
  - Data span literature from 1983 to 2019 (cut-off 2019); fertilizer use, land use, and other non-diurnal factors are captured in dataset_info.csv.

- Practical notes for use
  - Linkage: Use the dataset suffix (xxx) to join N2O_xxx.csv with soil_temp_xxx.csv for the same day-study pair.
  - Metadata: Refer to dataset_info.csv for study context and non-diurnal variables; use diurnal_pattern_categorisation_data.csv for pre-processed diurnal pattern classifications and cumulative flux metrics.
  - Caution: Data are digitised from published figures, so consider potential digitisation error; dataset heterogeneity across studies is inherent.

- References
  - The document includes an extensive reference list (Table 1) of the 46 studies used to assemble the datasets. Full bibliographic details are provided in the Reference section of the document.