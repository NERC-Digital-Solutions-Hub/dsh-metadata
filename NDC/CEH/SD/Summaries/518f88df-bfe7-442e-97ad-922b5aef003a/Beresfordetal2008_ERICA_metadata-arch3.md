# Metadata (an explanation of column headings and units) for : Radionuclide data for vertebrates in the Chernobyl Exclusion Zone, 2018

## Overview
- Provides metadata and column explanations for a dataset on radionuclide data collected from vertebrates and soils in the Chernobyl Exclusion Zone in 2018.
- Data files referenced: ERICA_Non-animal_results.csv, ERICA_soil_results.csv, ERICA_TLD_animal_results.csv.
- Accompanied by Materials_and_method_ERICA.rtf.
- Dataset hosted by NERC Environmental Information Data Centre (with a DOI provided).
- “n/a” used to denote not available in the data.

## Data Files and Key Contents

- ERICA_TLD_animal_results.csv
  - Contains biota data linked to thermoluminescent dosimeters (TLDs) attached to animals.
  - Key columns and concepts:
    - Biota_latin_name: Latin species name.
    - Site_Location: sampling location category (Low, Medium, High).
    - TLD_ID: TLD identifier code.
    - Sampling_Date_TLD_attached_to_biota and Sampling_Date_TLD_Removed_from_biota: dates (dd/mm/yyyy).
    - Exposure_days: duration the TLD remained on the animal.
    - Initial_capture Cs Sr Bq and Fresh_mass_g: initial activity measurements and fresh mass.
    - TLD_removal_capture Cs Sr Bq and Fresh_mass_g: measurements at TLD removal.
    - Additional_1…Additional_4_* fields: up to four recapture-related measurement events (dates, Cs/Sr activity, fresh mass).
    - TLD_dose_rate_microGy_per_hour: dose rate recorded by the attached TLD (two entries present in the data structure).
  - Notes: some animals may appear with the same Biota_sample_number due to re-capture; multiple measurements may exist.

- ERICA_soil_results.csv
  - Contains soil radiological measurements at sampling points.
  - Key columns and concepts:
    - Latitude/Longitude: site coordinates (WGS84).
    - Sample_code: unique sample identifier.
    - Date_soil_sampled: date of soil sampling.
    - Site_Location: Low/Medium/High site classification.
    - Soil_sample_fresh_mass_g and Soil_sample_dry_mass_g: mass measurements.
    - %_soil_moisture_content: soil moisture percentage.
    - Activity concentrations (Bq/kg DM) for Cs-137, Cs-134, Sr-90, K-40, Am-241, Eu-154/Eu-155, Pu-238/239/240, and others (with some <LOD flags).
    - Gamma and Beta measurements: Mean_Gamma_mSv/hr, SE_Gamma_mSv/hr, Mean_Beta_count_cm-2min-1, SE_Beta_count_cm-2min-1; notes on conversion from beta flux to dose rate.
  - LoD indicators: some columns show “<” to denote below detection limits.

- ERICA_Non-animal_results.csv
  - Contains non-animal TLD-related results and site placement details.
  - Key columns and concepts:
    - TLD_ID: linked to non-animal measurements.
    - Total_dose_milliSv: TLD-recorded dose.
    - Description: context (e.g., whether TLD was uncovered or in a perspex cube).
    - Site_Location and Site_locator: site classification and location code within site.
    - Date_placed_at_site and Date_removed_from_site: dates for TLD placement/removal.
    - Position: where the TLD was placed relative to the ground (in cm).

- Materials and method reference: ERICA methodology and calibration context referenced; primary bibliographic sources provided.

## Metadata, Data Quality and Interpretation

- Metadata structure provides explicit explanations and units for most columns, enabling clear interpretation and reuse.
- “n/a” denotes unavailable data within fields.
- Some fields require interpretation due to data collection design (e.g., Biota_sample_number can repeat for recaptured animals; additional_1…additional_4 fields capture follow-up measurements).
- Detection limits are indicated for certain soil measurements (<LOD flags) and should be considered when aggregating or comparing data.
- Units are specified per column (Bq, grams, dd/mm/yyyy, msv/hr, etc.), supporting cross-file integration.

## Data Governance, Access and Use

- Data is organized for reuse in monitoring and policy evaluation contexts, aligning with environmental health monitoring aims.
- Data and metadata are prepared to support transparency, data sharing, and potential public access through the data centre.
- The accompanying materials (methodology file and references) provide methodological transparency for quality assessment and replication.

## Relevance for Monitoring and Policy

- Enables assessment of radiological exposure in wildlife (via TLD-based dose rates and tissue/activity measurements) and of environmental radiation in soils.
- Supports spatial analysis by linking measurements to site locations (Low/Medium/High) and precise coordinates.
- Facilitates trend analysis across recapture events and temporal sampling, informing risk assessments and policy decisions on environmental health monitoring, remediation, and wildlife protection.

## References

- Beresford, Gaschak, Barnett et al. (2008). Estimating the exposure of small mammals at three sites within the Chernobyl exclusion zone — a test application of the ERICA Tool. Journal of Environmental Radioactivity.
- Gaschak, Maksimenko, Maklyuk, Bondarkov, Jannik, Farfan et al. (2011). Radiation ecology issues associated with murine rodents and shrews in the Chernobyl Exclusion Zone. Health Physics.