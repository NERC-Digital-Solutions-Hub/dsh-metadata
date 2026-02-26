# Metadata (an explanation of column headings and units) for: Radionuclide data for vertebrates in the Chernobyl Exclusion Zone, 2018, Gaschak, S.P., Beresford, N.A., Barnett, C.L., Wells, C., Maksimenko, A. and Chaplow, J.S. NERC-Environmental Information Data Centre. doi: https://doi.org/10.5285/518f88df-bfe7-442e-97ad-922b5aef003a CEZ_reptile_data.csv; please also see Materials_and_methods_CEZ_reptile.rtf

## What the dataset contains
- Radionuclide data for vertebrates in the Chernobyl Exclusion Zone during 2018.
- Includes reptile samples (lizards and snakes) and soil samples.
- Sampling locations: Red Forest site 1 and Red Forest site 2.
- Depth of soil sampled: 0–10 cm.
- Data organized in CEZ_reptile_data.csv with accompanying Materials_and_methods_CEZ_reptile.rtf.

## Key columns and what they mean
- Chornobyl_Center_sample_code: internal sample identifier.
- Sample: sample type (lizard or soil).
- Biota_latin_name: Latin name of the biota (for reptiles).
- Depth_of_soil_layer_collected_cm: depth of soil layer collected (cm).
- Location: site designation (Red Forest site 1 or site 2).
- Date_snake_or_lizard_or_soil_sampled: sampling date (dd/mm/yyyy).
- Sex_of_snake_or_lizard: sex of the biota (where recorded).
- Lizard_or_snake_total_length_mm: total length (mm) of the snake or lizard.
- Lizard_tail_length_mm: tail length (mm) of the lizard.
- Lizard_body_length_mm: body length (mm) of the lizard.
- Fresh_mass_of_snake_or_lizard_grams: fresh mass (g) of the biota sample.
- Fresh_mass_of_snake_or_lizard_carcass_grams: fresh mass of the carcass with gut removal (g).
- Notes: notes (e.g., guts removed before analysis).
- Cs-137_Bqkg_FM: Cs-137 activity concentration in biota (fresh mass, Bq/kg).
- Cs-137_error_Bqkg_FM: error on Cs-137 concentration (Bq/kg, FM).
- Sr-90_Bqkg_FM: Sr-90 activity concentration in biota (fresh mass, Bq/kg).
- Sr-90_error_Bqkg_FM: error on Sr-90 concentration (Bq/kg, FM).
- Pu-239,240_Bqkg: Pu-239,240 activity concentration in biota (fresh mass, Bq/kg).
- Pu-239,240_error_Bqkg_FM: error on Pu-239,240 concentration (Bq/kg, FM).
- Pu-238_Bqkg_FM: Pu-238 activity concentration in biota (fresh mass, Bq/kg).
- Pu-238_error_Bqkg_FM: error on Pu-238 concentration (Bq/kg, FM).
- Soil_Cs-137_Bqkg_DM: Cs-137 activity concentration in soil (dry mass, Bq/kg).
- Soil_Cs-137_error_Bqkg_DM: error on soil Cs-137 concentration (Bq/kg, DM).

## Units and measurement context
- Fresh mass (FM): grams for biota; used for biota radionuclide concentrations.
- Dry mass (DM): kilograms for soil Cs-137; used for soil radionuclide concentrations.
- Activity concentrations: becquerels per kilogram (Bq/kg) for both biota (FM) and soil (DM).
- Lengths: millimeters (mm); depths: centimeters (cm).
- Dates: day/month/year format (dd/mm/yyyy).

## Sampling and study design notes
- Two Red Forest sites referenced for location context.
- Guts removed from lizard and snake samples before analysis (affects mass-based measurements).
- Focused on vertebrates (reptiles) and associated soil samples to examine radionuclide transfer in a Chernobyl context.
- Biota measurements include morphological data (lengths and masses) to enable linking physical traits with radionuclide levels.

## Data provenance and accessibility
- Primary dataset: CEZ_reptile_data.csv.
- Methods and protocols: Materials_and_methods_CEZ_reptile.rtf.
- Data Centre: NERC Environmental Information Data Centre.
- Reference for broader context: Barnett, C.L., et al. 2009. Radionuclide activity concentrations in two species of reptiles from the Chernobyl exclusion zone. Radioprotection, 44, 537–542. DOI: 10.1051/radiopro/20095099.

## How analysts can use this data
- Correlate radionuclide concentrations (Cs-137, Sr-90, Pu-239,240, Pu-238) with biota size metrics (lengths, masses) and sex where available.
- Compare radionuclide levels between Red Forest site 1 and site 2.
- Assess transfer of radionuclides from soil (Cs-137 DM) to reptiles and examine relationships with soil contamination.
- Use date information to explore temporal patterns or sampling season effects.
- Integrate with other datasets (e.g., 2009 study) to examine consistency or changes over time.

## Considerations and limitations
- Guts removal before analysis influences interpretation of fresh-mass-based concentrations.
- Local-scale sampling (two sites) may limit broader generalizations.
- Data may require harmonization with other datasets (unit consistency, boundary definitions) for cross-study comparisons.
- Some fields are species- and site-specific; ensure proper handling of missing or non-recorded values.