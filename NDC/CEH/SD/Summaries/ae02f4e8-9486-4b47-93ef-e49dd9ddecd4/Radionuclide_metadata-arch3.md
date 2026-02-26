# A 'Reference Site' in the Chernobyl Exclusion Zone: radionuclide and stable element data, and estimated dose rates

## Overview
- Describes a dataset stored at the NERC Environmental Information Data Centre (EIDC) focused on a reference site within the Chernobyl Exclusion Zone.
- Combines radionuclide and stable element measurements in biota and soil, plus estimated ambient dose rates.
- Source: Beresford et al.; includes metadata and a DOI for the dataset.
- Purpose aligned with environmental monitoring and evaluation to inform policy decisions and future monitoring.

## Data files and structure
- Biota_radionuclide_data.csv
- Soil_radionuclide_data.csv
- Each file includes a metadata block detailing the explanation, units, and notes for each column (header-level metadata).

## Key variables and units (biota dataset)
- Sample identifiers and location
  - Chornobyl_Center_ID (sample identifier)
  - Biota_latin_name, Biota_Common_name
  - Date_biota_sampled (dd/mm/yyyy)
  - Latitude, Longitude (WGS84)
  - Trap (sampling line/area, where applicable)
- Biological characteristics
  - Age_of_biota (SAD/sub-adult, Juv/juvenile, or adult)
  - Sex_of_biota
  - Fresh_mass_of_biota_in_grams
  - Individuals_in_sample
- Radionuclide concentrations (fresh mass basis, Bq/kg)
  - Cs-137_Bq_per_kg_FM
  - Sr-90_Bq_per_kg_FM
  - Am-241_Bq_per_kg_FM
  - Pu239_240_Bq_per_kg_FM
  - Pu-238_Bq_per_kg_FM
- Concentration ratios (biota dry soil basis, unitless)
  - Cs-137_CR, Sr-90_CR, Am-241_CR, Pu_CR

## Key variables and units (soil dataset)
- Sample and site identifiers
  - N (laboratory unique sample identifier)
  - GP_Point (sampling area designation)
  - Latitude_WGS84, Longitude_WGS84
  - Date_Soil_sampled
- Ambient dose rates (microSv/hour)
  - Dose_rate_microSv_per_hour_measurement_1 to _10 (site measurements 1–10)
- Soil mass and content
  - Dry_mass_of_soil_in_grams (grams dry mass)
- Radionuclide activity concentrations (soil, Bq per sample dry mass)
  - Cs-137_Soil_Bq_per_sample_DM (with 95% confidence error)
  - Am-241_Soil_Bq_per_sample_DM (with 95% confidence error)
  - Sr-90_Soil_Bq_per_sample_DM (with 95% confidence error)
  - Pu-239_240_Soil_Bq_per_sample_DM (with 95% confidence error)
  - Pu-238_Soil_Bq_per_sample_DM (with 95% confidence error)
  - Corresponding 95% error fields (e.g., error_Cs-137_Bq_per_Sample_DM_P)
- Radionuclide activity concentrations (soil, Bq per kg dry mass)
  - Cs-137_Soil_Bq_kg_DM
  - Sr-90_Soil_Bq_kg_DM
  - Am-241_Soil_Bq_kg_DM
  - Pu-239_240_Soil_Bq_kg_DM
  - Pu-238_Soil_Bq_kg_DM

## Data quality, metadata, and uncertainty
- The dataset provides explicit column-level metadata (explanation, units, notes) to aid interpretation and reuse.
- Several fields include explicit measurement units (Bq/kg FM for biota, Bq per sample DM, Bq per kg DM for soil, and microSv/hour for dose rates).
- Uncertainty information is represented via 95% confidence errors for soil concentration measurements (e.g., error_Cs-137_Bq_per_Sample_DM_P; 95% indicators present in several fields).
- Some fields are tagged as not applicable or not available, indicating incomplete data in certain cells.
- The metadata format supports transparency about measurement contexts (sampling site, date, coordinates) and data quality, which supports reproducibility and governance.

## Provenance, access, and governance
- Data are curated for public sharing and transparency via the NERC Environmental Information Data Centre.
- DOI provided for dataset access and citation.
- Column metadata explains data origins (sample identifiers, site details) and measurement methods to enable data governance, quality assurance, cleaning, and analysis.
- Facilitates dissemination of outputs (reports, charts, dashboards) and supports data governance practices for long-term use and update.

## How this supports monitoring frameworks
- Provides a structured, transparency-focused dataset for monitoring environmental radioactivity and related dose implications in a high-contamination context.
- Enables calculation of concentration ratios and biota/soil comparisons, supporting risk assessment and policy evaluation.
- The explicit metadata and standardized units facilitate data integration, cross-site comparisons, and time-series monitoring, aiding the design and evaluation of monitoring frameworks.

## Challenges and considerations for reuse
- Metadata completeness is high but some entries show not-applicable or missing values, which may require careful handling during reuse.
- Data from a sensitive site (Chernobyl Exclusion Zone) requires appropriate governance, permissions, and context to interpret results responsibly.
- Users should account for potential variability in measurement methods across years or sites and the interpretation of 95% confidence error fields.
- Consistency checks may be needed to align units (e.g., FM vs DM vs DM_P) and ensure correct aggregation or normalization for cross-dataset analyses.

## Endnotes
- Title reference: A 'Reference Site' in the Chernobyl Exclusion Zone: radionuclide and stable element data, and estimated dose rates
- Source: Beresford et al.; NERC Environmental Information Data Centre; DOI: https://doi.org/10.5285/ae02f4e89486-4b47-93ef-e49dd9ddecd4