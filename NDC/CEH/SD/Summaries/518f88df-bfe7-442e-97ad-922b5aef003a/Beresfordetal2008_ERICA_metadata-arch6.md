# Metadata (an explanation of column headings and units) for : Radionuclide data for vertebrates in the Chernobyl Exclusion Zone, 2018, Gaschak, S.P., Beresford, N.A., Barnett, C.L., Wells, C., Maksimenko, A., Chaplow, J. NERC-Environmental Information Data Centre. https://doi.org/10.5285/518f88df-bfe7-442e-97ad-922b5aef003a

## Overview
- Describes three data files and a related materials/method document that underpin radionuclide measurements for vertebrates and surrounding soil within the Chernobyl Exclusion Zone (2018).
- Provides explanations of column headings and units, with n/a indicating not available.
- Data files: ERICA_Non-animal_results.csv, ERICA_soil_results.csv, ERICA_TLD_animal_results.csv; Materials_and_method_ERICA.rtf present for methods.
- Context and methods referenced include the ERICA tool and related radiation ecology literature.

## Datasets included
- ERICA_TLD_animal_results.csv
  - Contains data for collared vertebrates with thermoluminescent dosimeter (TLD) attachments.
  - Key fields include species Latin name, biopsy/sample identifiers, sex, sampling site location (Low/Medium/High), TLD_ID, dates TLD attached/removed, exposure days, initial capture radionuclide activities (Cs-137, Sr-90), initial fresh mass, TLD removal measurements, and multiple recapture-related measurements (Additional_1 to Additional_4) with corresponding dates, masses, and Cs/Sr activities.
  - Includes dose rate at the biota (TLD_dose_rate_microGy_per_hour) with two possible entries.
  - Notes on data structure: same Biota_sample_number may appear more than once due to re-capture events; data fields are suffixed to indicate recapture event 1–4.

- ERICA_soil_results.csv
  - Contains soil monitoring data with location coordinates.
  - Key fields include Latitude, Longitude, Sample_code, Date_soil_sampled, Site_Location, Sampling_point, Soil_sample_fresh_mass_g, Soil_sample_dry_mass_g, %_soil_moisture_content.
  - Radionuclide activity concentrations (Cs-137, Cs-134, Sr-90, K-40, Co-60, Am-241, Eu-154/Eu-155, Pu-238/239/240) with some <LOD markers indicating below detection limits.
  - Dosimetry fields: Mean_Gamma_mSv/hr (gamma dose rate) with two definitions, SE_Gamma_mSv/hr; Mean_Beta_count_cm-2min-1 with SE_Beta_count_cm-2min-1, plus notes on converting beta flux to dose rate (Gaschak et al., 2011).

- ERICA_Non-animal_results.csv
  - Contains non-animal TLD records (e.g., environmental or device placements).
  - Key fields include TLD_ID, Total_dose_milliSv, Description (e.g., uncovered or in perspex cube), Site_Location, Site_locator, Date_placed_at_site, Date_removed_from_site, Position, Exposure_days.

- Materials_and_method_ERICA.rtf
  - Related methods document referenced for data collection and processing.

## Key fields and schema highlights
- TLD-based vertebrate data (ERICA_TLD_animal_results.csv)
  - Biota_latin_name, Biota_sample_number (may repeat per animal due to re-capture)
  - Sex, Site_Location (Low/Medium/High)
  - TLD_ID; Sampling_Date_TLD_attached_to_biota; Sampling_Date_TLD_Removed_from_biota
  - Exposure_days; Initial_capture_Cs_Bq; Initial_capture_Sr_Bq; Initial_capture_fresh_mass_of_biota_mass_in_grams
  - TLD_removal_capture_Cs_Bq; TLD_removal_capture_Sr_Bq; TLD_removal_capture_fresh_mass_of_biota_grams
  - Additional_1 to Additional_4 measurements: Cs_Bq, Sr_Bq, sampling dates, fresh mass (various units as described)
  - TLD_dose_rate_microGy_per_hour (two columns for potentially different measurement definitions)
- Soil data (ERICA_soil_results.csv)
  - Geographic coordinates: Latitude, Longitude
  - Sample_code, Date_soil_sampled
  - Site_Location, Sampling_point
  - Soil_sample_fresh_mass_g, Soil_sample_dry_mass_g, %_soil_moisture_content
  - Radionuclide concentrations: Cs-137_Soil_Bq_kg_DM, Cs-134_Soil_Bq_kg_DM, Sr-90_Soil_Bq_kg_DM, K-40_Soil_Bq_kg_DM, Co-60_Soil_Bq_kg_DM, Am-241_Soil_Bq_kg_DM, Eu-154_Soil_Bq_kg_DM, Eu-155_Soil_Bq_kg_DM, Pu-238,239,240_Soil_Bq_kg_DM
  - Mean_Gamma_mSv/hr and SE_Gamma_mSv/hr; Mean_Beta_count_cm-2min-1 and SE_Beta_count_cm-2min-1
- Non-animal (ERICA_Non-animal_results.csv)
  - TLD_ID; Total_dose_milliSv
  - Description; Site_Location; Site_locator
  - Date_placed_at_site; Date_removed_from_site; Position; Exposure_days

## Data quality and caveats
- n/a indicates not available for the given field.
- Some columns denote below-detection-limit values with “<” markers.
- Data includes repeated measurements due to animal recaptures (Additional_1–Additional_4), requiring careful alignment/joining by animal ID and recapture event.
- Units vary by column (Bq for activity, grams for mass, dd/mm/yyyy for dates, mSv/hr or microGy/hr for dose rates).
- Spatial data are tied to sampling sites with qualitative tiers (Low/Medium/High) and precise coordinates for soil samples.
- Interpretation of dose and exposure requires combining TLD measurements with soil activity data and assumptions from cited references (ERICA tool methods).

## Potential uses for data support
- Build self-serve dashboards to explore radionuclide exposure across species, sites, and time (via attachment/removal dates and recapture events).
- Join vertebrate TLD data with soil measurements to model biota-to-soil transfer and estimate effective dose rates (gamma and beta components).
- Map spatial patterns of contamination using latitude/longitude and Site_Location categories; compare against Beresford et al. (2008) site classifications.
- Data validation and quality checks: verify consistency of TLD_ID mappings, cross-check dates, and unit conversions; identify gaps where n/a or missing fields exist.
- Reproducible analyses of dose reconstruction for vertebrates in the Chernobyl Exclusion Zone, supported by the accompanying Materials_and_method_ERICA.rtf and cited literature (e.g., Beresford et al. 2008; Gaschak et al. 2011).

## References and context
- Estimating the exposure of small mammals at three sites within the Chernobyl exclusion zone – a test application of the ERICA Tool. Beresford et al., 2008.
- Radiation ecology issues for murine rodents and shrews in the Chernobyl Exclusion Zone. Gaschak et al., 2011.
- Methods for converting beta flux to dose rate as discussed in Gaschak et al., 2011.