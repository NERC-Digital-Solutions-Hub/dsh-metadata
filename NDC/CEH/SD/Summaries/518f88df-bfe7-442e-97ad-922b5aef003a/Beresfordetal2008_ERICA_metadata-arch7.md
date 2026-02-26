# Metadata (an explanation of column headings and units) for : Radionuclide data for vertebrates in the Chernobyl Exclusion Zone, 2018, Gaschak, S.P., Beresford, N.A., Barnett, C.L., Wells, C., Maksimenko, A., Chaplow, J. NERC-Environmental Information Data Centre. https://doi.org/10.5285/518f88df-bfe7-442e-97ad-922b5aef003a

## Overview
- Describes column headings and units for three data files: ERICA_TLD_animal_results.csv, ERICA_soil_results.csv, and ERICA_Non-animal_results.csv (with accompanying materials referenced).
- Focus is on radionuclide measurements in vertebrates, soil samples, and non-animal TLD data from the Chernobyl Exclusion Zone (2018).
- Data are structured for GIS-style reuse and cross-dataset linking (e.g., by TLD_ID, Sample_code, and site/location fields).

## Datasets and key fields (GIS-relevant highlights)

- ERICA_TLD_animal_results.csv (TLD-backed vertebrate data)
  - Biota_latin_name: Latin species name.
  - Sex: Biological sex of the individual.
  - Site_Location: Sampling site category (Low, Medium, High).
  - TLD_ID: Thermoluminescent dosimeter ID code.
  - Sampling_Date_TLD_attached_to_biota and Sampling_Date_TLD_Removed_from_biota: TLD attachment/removal dates (dd/mm/yyyy).
  - Exposure_days: Duration the TLD remained on the animal.
  - Initial_capture_Cs_Bq, Initial_capture_Sr_Bq: Initial radionuclide activity (Cs and Sr) in Bq.
  - Initial_capture_fresh_mass_of_biota_mass_in_grams: Fresh biota mass at initial capture.
  - TLD_removal_capture_Cs_Bq, TLD_removal_capture_Sr_Bq, TLD_removal_capture_fresh_mass_of_biota_grams: Measurements at TLD removal.
  - Additional_1…Additional_4_*: Recapture-based additional measurements (Cs/Sr, date, fresh mass, etc.).
  - TLD_dose_rate_microGy_per_hour_1 and _2: Dose rate readings from the TLDs.
  - This dataset supports spatial-temporal analysis of radionuclide uptake in vertebrates and links to site-level geometry via location fields.

- ERICA_soil_results.csv (soil radionuclide data)
  - Latitude, Longitude: Geospatial coordinates (WGS84).
  - Sample_code: Unique sample identifier.
  - Date_soil_sampled: Sampling date (dd/mm/yyyy).
  - Site_Location: Site category (Low, Medium, High).
  - Sampling_point: Site-specific point code.
  - Soil_sample_fresh_mass_g, Soil_sample_dry_mass_g: Fresh and dry soil masses.
  - %_soil_moisture_content: Soil moisture percentage.
  - Cs-137_Soil_Bq_kg_DM, Cs-134_Soil_Bq_kg_DM, Sr-90_Soil_Bq_kg_DM, K-40_Soil_Bq_kg_DM, Co-60_Soil_Bq_kg_DM, Am-241_Soil_Bq_kg_DM, Eu-154_Soil_Bq_kg_DM, Eu-155_Soil_Bq_kg_DM, Pu-238,239,240_Soil_Bq_kg_DM: Activity concentrations (Bq/kg dry mass). "<" entries indicate below detection limit (LOD) for certain isotopes.
  - Pu-238,239,240_<: Below LOD indicator for these isotopes.
  - Mean_Gamma_mSv/hr, SE_Gamma_mSv/hr: Gamma dose-rate metrics (in mSv/hr) with standard error.
  - Mean_Beta_count_cm-2min-1, SE_Beta_count_cm-2min-1: Beta flux measurements and uncertainties; includes note on conversion to dose rate per Gaschak et al. 2011.
  - This dataset enables mapping of soil contamination patterns and linkage to vertebrate data via shared site/location fields.

- ERICA_Non-animal_results.csv (non-animal TLD data)
  - TLD_ID: Thermoluminescent dosimeter ID code.
  - Total_dose_milliSv: Dose recorded by TLD (milliSievert).
  - Description: Context (e.g., whether the TLD was uncovered or in a Perspex cube).
  - Site_Location: Site category (Low, Medium, High).
  - Site_locator: Code for location within site.
  - Date_placed_at_site, Date_removed_from_site: Placement/removal dates (dd/mm/yyyy).
  - Position: TLD position relative to ground (cm).
  - Exposure_days: Number of exposure days.
  - This file supports panoramic or site-scale radiation exposure visualization independent from biota.

## Spatial, temporal, and data-quality considerations

- Spatial coverage: Point coordinates for soils (Latitude, Longitude) and site-level categorizations (Low/Medium/High) enabling GIS layering by site zone.
- Temporal aspects: Multiple dates per animal (attachment/removal, recapture events) and soil sampling dates; TLD exposure intervals can be used to compute durations.
- Data integration: Cross-dataset linking via TLD_ID, Sample_code, Site_Location, and Site_locator; however, recapture events introduce multiple records per animal.
- Data quality cues:
  - n/a denotes not available in fields.
  - Some isotope concentrations use "<" to denote below detection limits.
  - Units are explicitly listed per column, aiding consistent mapping and calculations.
- Reference methodology:
  - Gamma and beta dose computations follow methods described (Gaschak et al., 2011) and ERICA-related exposure estimation approaches (Beresford et al., 2008).
  - Primary references provided for context and methodological basis.

## Practical GIS usage hints

- Join strategy: Link vertebrate and soil data via site_locators, site_location, or Sample_code/TLD_ID where applicable to create integrated maps of exposure.
- Visualization ideas:
  - Map TLD locations and associated dose rates for biota (TLD_dose_rate_microGy_per_hour) over time.
  - Display soil contamination hotspots using Cs-137, Cs-134, Sr-90, and other radionuclide concentrations.
  - Create choropleth or symbol-based layers by Site_Location (Low/Medium/High) for both soils and biota exposure.
- Data preparation notes:
  - Handle missing values (n/a) and below-LOD entries appropriately (e.g., as gaps or censored data).
  - Temporal alignment may require aggregating multiple recapture records per individual.
  - Ensure coordinate reference system consistency (WGS84 for latitude/longitude in soil data).

## References
- Beresford, Gaschak, Barnett, et al. Estimating the exposure of small mammals at three sites within the Chernobyl exclusion zone - a test application of the ERICA Tool. Journal of Environmental Radioactivity, 2008.
- Gaschak et al. Radiation ecology issues associated with murine rodents and shrews in the Chernobyl Exclusion Zone. Health Physics, 2011.