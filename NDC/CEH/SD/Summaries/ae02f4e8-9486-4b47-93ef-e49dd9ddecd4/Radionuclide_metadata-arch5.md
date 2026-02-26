# A 'Reference Site' in the Chernobyl Exclusion Zone: radionuclide and stable element data, and estimated dose rates

## Overview
- Metadata description for two CSV data files accompanying the publication: Biota_radionuclide_data.csv and Soil_radionuclide_data.csv.
- Study focus: radionuclide and stable element data, and estimated dose rates within the Chernobyl Exclusion Zone.
- Source: Beresford, N.A. et al.; NERC-Environmental Information Data Centre. DOI provided.

## Datasets and Schema

### Biota_radionuclide_data.csv
- Chornobyl_Center_ID: unique sample identifier (no unit).
- Biota_latin_name / Biota_Common_name: taxonomic identification (no units).
- Date_biota_sampled: sampling date (dd/mm/yyyy).
- Latitude / Longitude: decimal coordinates in WGS84.
- Trap: site trapping line for biota (where applicable).
- Age_of_biota: sub-adult (SAD), juvenile (Juv), or adult.
- Sex_of_biota: recorded sex where available.
- Fresh_mass_of_biota_in_grams: mass of biota sample (grams, fresh mass).
- Individuals_in_sample: number of individuals in the sample when >1.
- Cs-137_Bq_per_kg_FM, Sr-90_Bq_per_kg_FM, Am-241_Bq_per_kg_FM, Pu239_240_Bq_per_kg_FM, Pu-238_Bq_per_kg_FM: radionuclide activity concentrations in biota (Bq per kg fresh mass).
- Cs-137_CR, Sr-90_CR, Am-241_CR, Pu_CR: concentration ratios (biota fresh mass activity / soil dry mass activity); unitless.
- Notes indicate occasional data quality or availability remarks; some fields show non-critical typos or formatting inconsistencies.

### Soil_radionuclide_data.csv
- N: laboratory unique sample identifier (no unit).
- GP_Point: sampling site indicator or bulking note.
- Latitude_WGS84 / Longitude_WGS84: decimal coordinates (WGS84).
- Date_Soil_sampled: date soil was sampled (dd/mm/yyyy).
- Dose_rate_microSv_per_hour_measurement_1–10: ambient dose rate measurements at the site (µSv/h); up to 10 separate measurements.
- Dry_mass_of_soil_in_grams: dry mass of soil analysed (grams).
- Cs-137_Soil_Bq_per_sample_DM, Am-241_Soil_Bq_per_sample_DM, Sr-90_Soil_Bq_per_sample_DM, Pu-239_240_Soil_Bq_per_sample_DM, Pu-238_Soil_Bq_per_sample_DM: radionuclide activity concentrations per soil sample dry mass (Bq per sample dry mass).
- error_Cs-137_Bq_per_Sample_DM_P, error_Am-241_Bq_per_Sample_DM_P, error_Sr-90_Bq_per_Sample_DM_P, error_Pu-239_240_Bq_per_Sample_DM_P, error_Pu-238_Bq_per_Sample_DM_P: measurement errors with 95% confidence (P=0.95).
- Cs-137_Soil_Bq_kg_DM, Sr-90_Soil_Bq_kg_DM, Am-241_Soil_Bq_kg_DM, Pu-239_240_Soil_Bq_kg_DM, Pu-238_Soil_Bq_kg_DM: radionuclide activity concentrations per kilogram of dry soil (Bq/kg DM).
- The dataset includes both per-sample and per-kg dry-mass concentration values for soil.

## Geospatial and Temporal Coverage
- Coordinates provided for sample locations (latitude and longitude in WGS84).
- Sampling dates for both biota and soil datasets are recorded (dd/mm/yyyy format).
- Dose-rate measurements are organized as a series of up to 10 ambient dose-rate readings per soil sample site.

## Measurement Details and Uncertainty
- Radionuclide measurements include Cs-137, Sr-90, Am-241, Pu-239/240, and Pu-238 across both biota (per kg fresh mass) and soil (per sample dry mass and per kg dry mass).
- Derived metric: concentration ratios (CR) for biota-to-soil comparisons.
- Uncertainty reported for soil measurements via explicit 95% confidence error fields (e.g., error_*_P=0.95), aiding propagation of uncertainty in analyses.

## Provenance, Documentation, and Access
- Publication authors: Beresford, N.A.; Gaschak, S.; Barnett, C.L.; Maksimenko, A.; Guliaichenko, E.; Wells C.; Chaplow J.S.
- Data Centre: NERC Environmental Information Data Centre (EIDC).
- DOI link provided for the dataset: https://doi.org/10.5285/ae02f4e89486-4b47-93ef-e49dd9ddecd4.
- Data are structured for cataloguing and reuse, with clear sample identifiers and coordinate-based location data.

## Data Governance and Stewardship Considerations
- Metadata completeness: key fields are present (sample IDs, taxonomic names, dates, coordinates, measurement values, units, and uncertainty fields); ensure consistency in field naming and unit usage across datasets.
- Standardization: units are specified (Bq per kg, Bq per sample, µSv/h, grams, etc.) and coordinates follow WGS84; maintain consistency to facilitate interoperability.
- Data quality and completeness: some fields note ‘not applicable’ or not available (n/a); plan for handling missing data in analyses and cataloging.
- Updates and revisions: multiple measurements per site (dose rates) and multiple radionuclides per sample imply potential updates or additions; maintain versioning and clear provenance for updates.
- Access and sharing: data are stored in a recognized data centre with a DOI, enabling discoverability and reuse by data users and other stakeholders.

## Practical Takeaways for Data Stewards
- Ensure metadata completeness and consistency when ingesting these datasets into data portals or governance systems.
- Maintain clear links between biota and soil datasets via sample identifiers (Chornobyl_Center_ID / N) to support cross-dataset analyses (e.g., CR calculations).
- Preserve unit conventions (Bq/kg FM for biota; Bq/sample DM and Bq/kg DM for soil; dose rates in µSv/h) and capture uncertainty (95% confidence) for robust downstream analyses.
- Confirm geospatial coordinates accuracy and align with WGS84 across records for reliable mapping and spatial analyses.
- Document data provenance (authors, publication, DOI) and ensure access instructions are retained for future discovery and citation.