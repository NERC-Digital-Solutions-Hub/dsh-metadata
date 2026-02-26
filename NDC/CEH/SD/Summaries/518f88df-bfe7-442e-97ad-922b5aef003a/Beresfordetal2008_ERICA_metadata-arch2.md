# Radionuclide data for vertebrates in the Chernobyl Exclusion Zone, 2018

- ## Overview
  - Metadata describing column headings and units for radionuclide data collected in vertebrates within the Chernobyl Exclusion Zone in 2018.
  - Data contributed by Gaschak, Beresford, Barnett, Wells, Maksimenko, and Chaplow; stored at the NERC Environmental Information Data Centre.
  - Includes three CSV data files and a Materials_and_method_ERICA.rtf document for methods.
  - n/a indicates not available; some animals had TLD collar changes upon recapture, leading to repeated Biota_sample_number entries for the same individual.
  - The dataset supports standardized environmental monitoring and assessment of radiological exposure in vertebrates, with references to ERICA methodology and prior studies.

- ## Data files included
  - ERICA_TLD_animal_results.csv
  - ERICA_soil_results.csv
  - ERICA_Non-animal_results.csv
  - Materials_and_method_ERICA.rtf (Methods)

- ## Key variables by file

  - ERICA_TLD_animal_results.csv
    - Biota_latin_name (Latin name of species)
    - Biota_sample_number (sample identifier; same animal may appear more than once due to TLD changes)
    - Sex
    - Site_Location (Low, Medium, High)
    - TLD_ID (thermoluminescent dosimeter code)
    - Sampling_Date_TLD_attached_to_biota (dd/mm/yyyy)
    - Sampling_Date_TLD_Removed_from_biota (dd/mm/yyyy)
    - Exposure_days (days TLD remained on biota)
    - Initial_capture_Cs_Bq, Initial_capture_Sr_Bq (Bq)
    - Initial_capture_fresh_mass_of_biota_mass_in_grams (g)
    - TLD_removal_capture_Cs_Bq, TLD_removal_capture_Sr_Bq (Bq) and TLD_removal_capture_fresh_mass_of_biota_grams (g)
    - Additional_1_Cs_Bq / Additional_1_Sr_Bq (Bq) and Additional_1_sampling_date_TLD_added_to_biota (dd/mm/yyyy) and Additional_1_fresh_mass_of_biota_grams (g)
    - Additional_2_Cs_Bq / Additional_2_Sr_Bq, Additional_2_sampling_date_TLD_added_to_biota, Additional_2_fresh_mass_of_biota_grams (and analogous descriptions)
    - Additional_3_Cs_Bq / Additional_3_Sr_Bq, Additional_3_sampling_date_TLD_added_to_biota, Additional_3_fresh_mass_of_biota_grams
    - Additional_4_Cs_Bq / Additional_4_Sr_Bq, Additional_4_sampling_date_TLD_added_to_biota, Additional_4_fresh_mass_of_biota_grams
    - TLD_dose_rate_microGy_per_hour (two entries in the file)
    - Notes: repeated entries reflect recapture events and multiple measurements per animal

  - ERICA_soil_results.csv
    - Latitude, Longitude (WGS84)
    - Sample_code (Chornobyl Center unique identifier)
    - Date_soil_sampled (dd/mm/yyyy)
    - Site_Location (Low, Medium, High)
    - Sampling_point (identifier)
    - Soil_sample_fresh_mass_g, Soil_sample_dry_mass_g (g)
    - %_soil_moisture_content (%)
    - Cs-137_Soil_Bq_kg_DM, Cs-134_Soil_Bq_kg_DM (Bq/kg dry mass; < indicates below LOD)
    - Sr-90_Soil_Bq_kg_DM, K-40_Soil_Bq_kg_DM (Bq/kg)
    - Co-60_<, Co-60_Soil_Bq_kg_DM (LOD indicator and measurement)
    - Am-241_Soil_Bq_kg_DM, Eu-154_< / Eu-154_Soil_Bq_kg_DM, Eu-155_< / Eu-155_Soil_Bq_kg_DM
    - Pu-238,239,240_< / Pu-238,239,240_Soil_Bq_kg_DM
    - Mean_Gamma_mean_mSv/hr (gamma dose rate at 5 cm above ground; with SE_Gamma_mSv/hr)
    - Mean_Beta_count_cm-2min-1 (beta flux; with SE_Beta_count_cm-2min-1)
    - Conversion note: method to convert beta flux to dose rate described (Gaschak et al., 2011)

  - ERICA_Non-animal_results.csv
    - TLD_ID (dosimeter ID)
    - Total_dose_milliSv (dose recorded by TLD)
    - Description (e.g., whether TLD was uncovered or in a Perspex cube)
    - Site_Location (Low, Medium, High)
    - Site_locator (location code within site)
    - Date_placed_at_site (dd/mm/yyyy)
    - Date_removed_from_site (dd/mm/yyyy)
    - Position (above/below ground; cm)
    - Exposure_days (days)

- ## Data provenance and interpretation

  - Methods reference: Estimating exposure of small mammals at three sites within the Chernobyl Exclusion Zone using the ERICA Tool; Beresford et al. 2008; Gaschak et al. 2011.
  - Data describe radionuclide activity in biota and surrounding soil, plus TLD-based dosimetry for collared animals.
  - Detection limits indicated by “<” in several soil contaminant columns; multiple measurements may exist for the same animal due to recapture events.
  - The dataset is designed for cross-site comparisons (Low/Medium/High site locations) and temporal monitoring through TLD-based exposure records and soil activity.

- ## Data quality, usage and access notes

  - n/a denotes not available for a given field.
  - Additional measurements exist for recaptured animals (Additional_N fields) to capture changes over time.
  - Data are stored at the NERC Environmental Information Data Centre; consult Materials_and_method_ERICA.rtf for detailed methodologies and measurement protocols.
  - Intended for analysis of environmental radiological exposure in vertebrates and for validation/benchmarking of models like the ERICA tool.
  - The dataset supports combining vertebrate exposure data with soil radionuclide measurements to assess environmental radiological health and policy-relevant performance over time.