# Metadata (an explanation of column headings and units) for : Radionuclide data for vertebrates in the Chernobyl Exclusion Zone, 2018, Gaschak, S.P., Beresford, N.A., Barnett, C.L., Wells, C., Maksimenko, A., Chaplow, J. NERC-Environmental Information Data Centre. https://doi.org/10.5285/518f88df-bfe7-442e-97ad-922b5aef003a

## Overview
- Provides metadata (column headings and units) for the Radionuclide data for vertebrates in the Chernobyl Exclusion Zone, 2018.
- Data are organized into three CSV data files and a materials/methods document:
  - ERICA_TLD_animal_results.csv
  - ERICA_soil_results.csv
  - ERICA_Non-animal_results.csv
  - Materials_and_method_ERICA.rtf

## Data files and key fields

- ERICA_TLD_animal_results.csv
  - Biota_latin_name: Latin name of species
  - Biota_sample_number: sample number for the biota (same animal may appear more than once if recaptured; denotes the same animal)
  - Sex: sex of the animal
  - Site_Location: sampling site location (Low, Medium, High)
  - TLD_ID: thermoluminescent dosimeter ID
  - Sampling_Date_TLD_attached_to_biota: date TLD collar attached (dd/mm/yyyy)
  - Sampling_Date_TLD_Removed_from_biota: date TLD collar removed (dd/mm/yyyy)
  - Exposure_days: number of days the TLD remained on the biota
  - Initial_capture_Cs_Bq: initial Cs activity (Bq) at capture
  - Initial_capture_Sr_Bq: initial Sr activity (Bq) at capture
  - Initial_capture_fresh_mass_of_biota_mass_in_grams: initial fresh mass of biota (grams)
  - TLD_removal_capture_Cs_Bq: Cs activity at collar removal (Bq)
  - TLD_removal_capture_Sr_Bq: Sr activity at collar removal (Bq)
  - TLD_removal_capture_fresh_mass_of_biota_grams: mass at collar removal (grams)
  - Additional_1_Cs_Bq … Additional_4_Cs_Bq: additional Cs measurements if recaptured (up to four additions)
  - Additional_x_Sr_Bq: corresponding Sr measurements for each additional reading
  - Additional_x_sampling_Date_TLD_added_to_biota: date TLD was re-attached for the addition
  - Additional_x_fresh_mass_of_biota_grams: fresh mass at each additional sampling
  - TLD_dose_rate_microGy_per_hour: dose rate recorded by the TLD (microGy/hour) (two fields for each measurement set)
  - Additional_4_sampling_D ate_TLD_ added_to_biota, 1/2: date for the fourth addition (two parts)
  - Additional_4_fresh_mass_of_biota_grams, 1/2: mass for the fourth addition
  - Note: column names indicate measurement type and sequencing of recapture events

- ERICA_soil_results.csv
  - Latitude: decimal latitude (WGS84)
  - Longitude: decimal longitude (WGS84)
  - Sample_code: unique sample identifier
  - Date_soil_sampled: date soil was sampled (dd/mm/yyyy)
  - Site_Location: site location (Low, Medium, High)
  - Sampling_point: point identifier within site
  - Soil_sample_fresh_mass_g: soil mass at sampling (grams)
  - Soil_sample_dry_mass_g: soil dry mass (grams)
  - %_soil_moisture_content: soil moisture percentage
  - Cs-137_Soil_Bq_kg_DM: Cs-137 activity concentration (Bq per kg dry mass)
  - Cs-134_Soil_Bq_kg_DM: Cs-134 activity concentration (Bq per kg dry mass)
  - Sr-90_Soil_Bq_kg_DM: Sr-90 activity concentration (Bq per kg dry mass)
  - K-40_Soil_Bq_kg_DM: K-40 activity concentration (Bq per kg dry mass)
  - Pu-238,239,240_Soil_Bq_kg_DM: Pu isotopes activity concentration (Bq per kg dry mass)
  - Am-241_Soil_Bq_kg_DM: Am-241 activity concentration (Bq per kg dry mass)
  - Eu-154_Soil_Bq_kg_DM and Eu-155_Soil_Bq_kg_DM: Eu isotopes activity concentrations (Bq per kg dry mass)
  - Co-60_Soil_Bq_kg_DM: Co-60 activity concentration (Bq per kg dry mass)
  - Mean_Gamma_mSv/hr: mean gamma dose rate (mSv/hr) at 5 cm above ground; derived from gamma measurements
  - SE_Gamma_mSv/hr: standard error of the mean gamma dose rate
  - Mean_Beta_count_cm-2min-1: mean beta flux (counts per cm^2 per min) at 5 cm above ground
  - SE_Beta_count_cm-2min-1: standard error of beta flux
  - Notes: some columns may include "<" indicating readings below the limit of detection (LOD)

- ERICA_Non-animal_results.csv
  - TLD_ID: thermoluminescent dosimeter ID
  - Total_dose_milliSv: dose recorded by TLD in milliSieverts
  - Description: notes whether the TLD was uncovered or in a Perspex cube
  - Site_Location: site location (Low, Medium, High)
  - Site_locator: code for location within site
  - Date_placed_at_site: date TLD placed at the site (dd/mm/yyyy)
  - Date_removed_from_site: date TLD removed from the site (dd/mm/yyyy)
  - Position: positioning of the TLD (above ground, below ground, ground level in cm)
  - Exposure_days: number of exposure days

- n/a and LOD notes
  - In the data, n/a indicates not available
  - Some fields indicate below detection limits using the “<” symbol

## Data conventions and notes
- Dates are in dd/mm/yyyy format where specified
- Site_Location categories follow Beresford et al. 2008 (Low/Medium/High) for site comparisons
- "<" denotes measurements below the limit of detection (LOD) in relevant soil and isotopic concentration columns
- Measurements include Cs-137, Cs-134, Sr-90, K-40, Pu isotopes, Am-241, Eu-154/155, and Co-60 among others, plus dosimetry and beta/gamma dose indicators
- Units are specified per field (e.g., Bq, grams, mSv/hr, etc.)

## References and methodology
- Estimates of exposure and data context drawn from:
  - Beresford et al. (2008) on estimating exposure of small mammals at three sites within the Chernobyl exclusion zone (J Environ Radioactivity)
  - Gaschak et al. (2011) on radiation ecology issues related to rodents and shrews in the Chernobyl Exclusion Zone
- Materials_and_method_ERICA.rtf provides methodological details for the ERICA-based data collection and interpretation

## Access and provenance
- Data originate from the NERC Environmental Information Data Centre
- DOI for the metadata collection: https://doi.org/10.5285/518f88df-bfe7-442e-97ad-922b5aef003a
- Includes separate Materials_and_method_ERICA.rtf document for detailed methodologies