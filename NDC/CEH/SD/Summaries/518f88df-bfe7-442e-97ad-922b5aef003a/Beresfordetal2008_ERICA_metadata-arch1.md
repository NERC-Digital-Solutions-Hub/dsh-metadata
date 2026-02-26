Metadata (an explanation of column headings and units) for : Radionuclide data for vertebrates in the Chernobyl Exclusion Zone, 2018, Gaschak, S.P., Beresford, N.A., Barnett, C.L., Wells, C., Maksimenko, A., Chaplow, J. NERC-Environmental Information Data Centre. https://doi.org/10.5285/518f88df-bfe7-442e-97ad-922b5aef003a

- Scope and contents
  - Metadata describing column headings and units for three data files and related materials from the Chernobyl Exclusion Zone study (2018).
  - Data files included:
    - ERICA_TLD_animal_results.csv
    - ERICA_soil_results.csv
    - ERICA_Non-animal_results.csv
  - Additional documentation: Materials_and_method_ERICA.rtf
  - n/a in the data means not available.
  - References to ERICA tool applications and related radiation ecology studies.

- Data structure and files
  - ERICA_TLD_animal_results.csv
    - Key fields include: Biota_latin_name, Biota_sample_number, Sex, Site_Location (Low/Medium/High), TLD_ID, Sampling_Date_TLD_attached_to_biota, Sampling_Date_TLD_Removed_from_biota, Exposure_days
    - Measurements around initial and removal Cs-137 (Cs_Bq) and Sr-90 (Sr_Bq) activities, fresh biota mass (g), and TLD removal masses
    - Additional measurement blocks: Additional_1 to Additional_4 (Cs_Bq, Sr_Bq, sampling dates, fresh mass) representing recapture events
    - TLD dose rate (microGy per hour); assay data may include multiple readings per animal due to recapture
  - ERICA_soil_results.csv
    - Spatial and sampling metadata: Latitude, Longitude, Sample_code, Date_soil_sampled, Site_Location, Sampling_point
    - Masses: Soil_sample_fresh_mass_g, Soil_sample_dry_mass_g, %_soil_moisture_content
    - Radioactivity concentrations (Bq per kg dry mass) for multiple nuclides: Cs-137, Cs-134, Sr-90, K-40, Co-60, Am-241, Eu-154, Eu-155, Pu-238/239/240
    - Gamma and beta dose metrics: Mean_Gamma_mSv/hr, SE_Gamma_mSv/hr, Mean_Beta_count_cm-2min-1, SE_Beta_count_cm-2min-1
  - ERICA_Non-animal_results.csv
    - Non-animal TLD data: TLD_ID, Total_dose_milliSv
    - Site context: Description (e.g., whether TLD was uncovered or in a Perspex cube), Site_Location, Site_locator
    - Placement/removal dates: Date_placed_at_site, Date_removed_from_site
    - Position and exposure duration: Position, Exposure_days
  - Notes: Column names come with explanations and units in the table headers; some columns indicate detection limits (e.g., <LOD) or vary by measurement type

- Key variables and units
  - Biota measurements: Biota_sample_number, Biota_latin_name, Sex, Site_Location; Mass in grams
  - TLD measurements: TLD_ID; Exposure_days; Sampling_Date_*; Sampling_Date_TLD_removed_from_biota; TLD_dose_rate_microGy_per_hour
  - Radioactivity (biota): Initial_capture_Cs_Bq, Initial_capture_Sr_Bq, TLD_removal_capture_Cs_Bq, TLD_removal_capture_Sr_Bq, Additional_1-4_Cs_Bq and Sr_Bq; Additional_1-4_sampling_Date_TLD_added_to_biota; Additional_1-4_fresh_mass_of_biota_grams
  - Soil measurements: Latitude, Longitude; Cs-137_Soil_Bq_kg_DM, Cs-134_Soil_Bq_kg_DM, Sr-90_Soil_Bq_kg_DM, K-40_Soil_Bq_kg_DM, Co-60_Soil_Bq_kg_DM, Am-241_Soil_Bq_kg_DM, Eu-154_Soil_Bq_kg_DM, Eu-155_Soil_Bq_kg_DM, Pu-238,239,240_Soil_Bq_kg_DM; Mean_Gamma_mSv/hr, SE_Gamma_mSv/hr; Mean_Beta_count_cm-2min-1, SE_Beta_count_cm-2min-1
  - Non-animal (TLD) measurements: Total_dose_milliSv
  - Data quality cues: Some columns use “<” to indicate below detection limits; n/a indicates not available

- Data quality, limitations, and access
  - The dataset provides detailed metadata for harmonizing analyses across three data types (biota, soil, non-animal TLDs).
  - Some measurements are only available for subsets (e.g., recapture events yield Additional_1..4 blocks).
  - Detection-limit indicators (e.g., <LOD) and missing values require careful handling in analyses.
  - Data are designed to support correlational and predictive analyses relating soil radioactivity to biota contamination, exposure doses, and dose-rate assessments.
  - The materials are hosted by NERC Environmental Information Data Centre; data provenance and metadata support reproducibility.

- Analytical opportunities for data scientists
  - Explore correlations between soil radioisotope concentrations and biota tissue activities (Cs-137, Cs-134, Sr-90) across sites with Low/Medium/High exposure.
  - Model dose-rate exposure for vertebrates using TLD-based microGy/hr and total dose (mSv) outcomes.
  - Assess time-at-risk through Exposure_days and Sampling_Date_TLD_* variables; evaluate recapture effects via Additional_1..4 measurements.
  - Compare gamma versus beta dose-rate metrics and relate to soil gamma/beta measurements.
  - Map and summarize site-level differences (latitude/longitude and Site_Location) to understand spatial patterns.
  - Integrate soil and biota data to parametrize ecological radiation-exposure models (as per ERICA framework).

- Documentation and references
  - ERICA methodology and prior studies cited:
    - Estimating the exposure of small mammals at three sites within the Chernobyl exclusion zone – a test application of the ERICA Tool (Beresford et al., 2008)
    - Radiation ecology issues for murine rodents and shrews in the Chernobyl Exclusion Zone (Gaschak et al., 2011)
  - Data housed with the NERC Environmental Information Data Centre; links and DOIs provided in the metadata.