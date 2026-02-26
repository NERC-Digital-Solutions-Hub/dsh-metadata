# A 'Reference Site' in the Chernobyl Exclusion Zone: radionuclide and stable element data, and estimated dose rates.

## Overview
- Metadata describing two datasets on radionuclide activity and dose rates from a reference site in the Chernobyl Exclusion Zone.
- Datasets cover radionuclide measurements in biota and soils, plus ambient dose-rate measurements.

## Datasets included
- Biota_radionuclide_data.csv
  - Contains sample identifiers, taxonomic names, sampling details, location, biological attributes, mass, count, and radionuclide activity concentrations (Cs-137, Sr-90, Am-241, Pu-239,240, Pu-238) in fresh mass, plus concentration ratios (CRs) linking biota to soil dry-mass activity.
- Soil_radionuclide_data.csv
  - Contains soil sample identifiers and site details, ambient dose-rate measurements across up to 10 replicates, dry mass, and activity concentrations for Cs-137, Am-241, Sr-90, Pu-239,240, Pu-238 in both dry mass and per kilogram dry mass, plus associated 95% confidence interval error fields where provided.

## Key fields and units (Biota)
- Chornobyl_Center_ID: unique biota sample identifier.
- Biota_latin_name / Biota_Common_name: taxonomic details.
- Date_biota_sampled: date in dd/mm/yyyy.
- Latitude / Longitude: decimal degrees (WGS84).
- Trap: biota trapping line (where applicable).
- Age_of_biota: SAD (sub-adult), Juv (juvenile), or adult.
- Sex_of_biota: recorded sex when available.
- Fresh_mass_of_biota_in_grams: fresh mass in grams.
- Individuals_in_sample: number of individuals in the sample (if >1).
- Radionuclide activities (per kg fresh mass): Cs-137, Sr-90, Am-241, Pu-239,240, Pu-238 (Bq/kg FM).
- Cs-137_CR, Sr-90_CR, Am-241_CR, Pu_CR: concentration ratios defined as biota fresh-mass activity concentration divided by soil dry-mass activity concentration (unitless).

## Key fields and units (Soil)
- N: laboratory sample identifier.
- GP_Point: sampling site identifier (inner area or pine tree) and bulked samples noted.
- Latitude_WGS84 / Longitude_WGS84: decimal degrees (WGS84).
- Date_Soil_sampled: date of soil sampling (dd/mm/yyyy).
- Dose_rate_microSv_per_hour_measurement_1…_10: ambient dose rate measurements at the site (µSv/h).
- Dry_mass_of_soil_in_grams: dry mass analyzed (grams).
- Cs-137_Soil_Bq_per_sample_DM / Am-241_Soil_Bq_per_sample_DM / Sr-90_Soil_Bq_per_sample_DM / Pu-239_240_Soil_Bq_per_sample_DM / Pu-238_Soil_Bq_per_sample_DM: activity concentrations per sample dry mass (Bq) for each isotope.
- Cs-137_Soil_Bq_kg_DM / Sr-90_Soil_Bq_kg_DM / Am-241_Soil_Bq_kg_DM / Pu-239_240_Soil_Bq_kg_DM / Pu-238_Soil_Bq_kg_DM: activity concentrations per kilogram of dry soil (Bq/kg).
- Error fields (e.g., error_Cs-137_Bq_per_Sample_DM_P): 95% confidence interval indicators for the soil dry-mass measurements (P=0.95).
- Note on Cs-137_Soil_Bq_per_Sample_DM_P and similar fields: specify confidence level (e.g., 95%).

## Sampling and measurement details
- Biota: includes date, location, biological characteristics, and mass for radiological assessment.
- Soil: includes multiple ambient dose-rate measurements (up to 10 replicates) and detailed soil radionuclide concentrations in both dry mass and per kg dry mass.
- Units emphasize fresh mass (FM) for biota measurements and dry mass (DM) for soil measurements, with clear per-sample and per-kg expressions.

## Data quality and notes
- Many fields marked as not applicable or not available (n/a), indicating missing or inapplicable data.
- Several fields carry explicit 95% confidence interval notes for soil measurements, reflecting reported uncertainty around activity concentrations.
- Some metadata naming inconsistencies (e.g., “CR” descriptions and formatting) require careful interpretation during integration.

## How this data can be used (Data support perspective)
- Enable cross-dataset analyses by linking biota radionuclide concentrations with corresponding soil concentrations via CRs.
- Assess radiological uptake in biota by comparing Cs-137, Sr-90, Am-241, Pu-239/240, Pu-238 across species and sites.
- Integrate ambient dose-rate measurements with soil contamination to evaluate environmental exposure at the reference site.
- Build self-serve data products (dashboards, pivot tables) to compare isotopes, species, and sampling locations.
- Promote reproducibility by documenting sample identifiers, dates, coordinates, and mass units; use CRs to relate biota and soil contamination levels.
- Support data-quality improvements by accounting for missing values and the provided uncertainty indicators.

## Potential data issues and reuse considerations
- Patchy data across biota and soil datasets; incomplete sampling dates or coordinates may arise.
- Mixed units (FM for biota, DM for soil) require harmonization when aggregating across datasets.
- Many fields are marked n/a or not applicable; plan for robust handling of missing values.
- Ensure understanding of CR definitions (biota fresh-mass activity divided by soil dry-mass activity) for correct interpretation and analysis.
- When using dose-rate fields, consider multiple replicates and their temporal or spatial variability.

## Access and reference
- Data described in the data centre entry: NERC-Environmental Information Data Centre.
- DOI: https://doi.org/10.5285/ae02f4e89486-4b47-93ef-e49dd9ddecd4.