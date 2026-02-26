Metadata (an explanation of column headings and units) for: Radionuclide data for vertebrates in the Chernobyl Exclusion Zone, 2018, Gaschak, S.P., Beresford, N.A., Barnett, C.L., Wells, C., Maksimenko, A. and Chaplow, J.S. NERC-Environmental Information Data Centre. doi: https://doi.org/10.5285/518f88df-bfe7-442e-97ad-922b5aef003a CEZ_reptile_data.csv; please also see Materials_and_methods_CEZ_reptile.rtf

## Overview
- Provides explanations of column headings and units for the CEZ reptile radionuclide dataset published in 2018.
- Dataset cover: Radionuclide activity concentrations measured in vertebrates (lizards/snakes) and related sample data from the Chernobyl Exclusion Zone; stored under NERC-Environmental Information Data Centre.
- Includes metadata for a CSV file (CEZ_reptile_data.csv) and an accompanying methods document.

## Dataset structure and key fields
- Identifiers and sample characteristics
  - Chornobyl_Center_sample_code: sample identifier.
  - Sample: sample type (lizard or soil).
  - Biota_latin_name: Latin name of the biota.
  - Chornobyl_Center_sample_code and Sample explanations are provided, with units noted as not applicable where appropriate.
- Spatial context
  - Location: Red Forest site 1 or Red Forest site 2.
  - Depth_of_soil_layer_collected_cm: depth of soil sampling for the 0–10 cm layer (cm).
- Temporal context
  - Date_snake_or_lizard_or_soil_sampled: date of sampling (dd/mm/yyyy).
- Biological measurements
  - Sex_of_snake_or_lizard: sex of the biota.
  - Lizard_or_snake_total_length_mm: total length (mm).
  - Lizard_tail_length_mm: tail length (mm).
  - Lizard_body_length_mm: body length (mm).
  - Fresh_mass_of_snake_or_lizard_grams: fresh mass (g).
  - Fresh_mass_of_snake_or_lizard_carcass_grams: carcass mass with gut removal (g).
  - Notes: gut removal prior to analysis (if applicable).
- Radionuclide measurements (mass basis details)
  - Cs-137_Bqkg_FM, Cs-137_error_Bqkg_FM: Cs-137 activity concentration and associated error (Bq/kg, fresh mass).
  - Sr-90_Bqkg_FM, Sr-90_error_Bqkg_FM: Sr-90 activity concentration and error (Bq/kg, fresh mass).
  - Pu-239,240_Bqkg_FM, Pu-239,240_error_Bqkg_FM: Pu-239,240 activity concentration and error (Bq/kg, fresh mass).
  - Pu-238_Bqkg_FM, Pu-238_error_Bqkg_FM: Pu-238 activity concentration and error (Bq/kg, fresh mass).
  - Soil_Cs-137_Bqkg_DM, Soil_Cs-137_error_Bqkg_DM: Cs-137 in soil (dry mass), concentration and error (Bq/kg).
  - Soil_Cs-137_error_Bqkg_DM: associated error for soil Cs-137 (dry mass).
- Units
  - Depth: cm; lengths: mm; masses: g; concentrations: Bq/kg; mass basis notes differentiate fresh mass (FM) and dry mass (DM).

## Spatial and temporal details
- Location-based scope: Red Forest site 1 and Red Forest site 2 (reference to Barnett et al., 2009 for further site details).
- Temporal scope: sampling date recorded; dataset pertains to 2018 radionuclide data.

## Data quality, standards and considerations for GIS
- Data are richly described with explicit column explanations and units, aiding consistent attribute interpretation.
- Potential GIS-relevant considerations
  - Location granularity: site-level location (Red Forest sites) rather than precise coordinates in this metadata; georeferencing may require supplementary spatial annotations.
  - Mass basis consistency: some measurements are fresh mass (FM) while soil measurements use dry mass (DM); harmonisation may be needed for cross-field comparisons.
  - Data integration: multiple data types (biota vs soil, various radionuclides, biology measurements) may come from different sources or methods; ensure consistent standards when joining with other GIS layers.
  - Data completeness: date, location, and measurement fields may have gaps; plan for missing-value handling.
- Broader challenges (aligned with GIS specialist perspective)
  - Data distributed across multiple sources; ensure provenance and versioning.
  - Need for consistent data standards when combining with other CEZ datasets.
  - Handling large/complex datasets by structuring and chunking data where necessary.
  - Skill development within teams to manage GIS-derived data products effectively.

## How to use in GIS workflows
- Potential GIS products
  - Spatial layers showing radionuclide activity concentrations by species and site.
  - Choropleth or point maps by individual reptiles or by soil samples, colored by Cs-137, Sr-90, Pu isotopes, etc.
  - Time-enabled analyses if multiple years or sampling dates are incorporated.
- Suggested workflow steps
  - Ingest CEZ_reptile_data.csv and, if available, link to precise spatial coordinates for Red Forest sites.
  - Normalize mass basis where needed (FM vs DM) to enable valid comparisons.
  - Join biometric data (species, length, mass) with radionuclide measurements by sample.
  - Validate units and handle any metadata inconsistencies (e.g., potential typographical notes in some fields).
  - Create QA checks for missing values, outliers, and measurement uncertainties (using Cs-137_error_Bqkg_FM, etc.).
  - Produce maps and dashboards supporting policy, client, or public audiences with clear legend and uncertainty notes.

## References
- Barnett, C.L., Gaschak, S., Beresford, N.A., Howard, B.J., Maksimenko, A. 2009. Radionuclide activity concentrations in two species of reptiles from the Chernobyl exclusion zone. Radioprotection, 44, 537-542. http://dx.doi.org/10.1051/radiopro/20095099
- Materials_and_methods_CEZ_reptile.rtf (associated methods document)