# Metadata (an explanation of column headings and units) for: Radionuclide data for vertebrates in the Chernobyl Exclusion Zone, 2018, Gaschak, S.P., Beresford, N.A., Barnett, C.L., Wells, C., Maksimenko, A. and Chaplow, J.S. NERC-Environmental Information Data Centre. doi: https://doi.org/10.5285/518f88df-bfe7-442e-97ad-922b5aef003a

## Overview
- Documents metadata for the Radionuclide data for vertebrates in the Chernobyl Exclusion Zone, 2018, including the CEZ_reptile_data.csv and Materials_and_methods_CEZ_reptile.rtf.
- Focus on reptile data (lizards) collected from the Red Forest (site 1 and site 2) in the CEZ; data compiled by Gaschak, Beresford, Barnett, Wells, Maksimenko, and Chaplow.
- Hosted by the NERC Environmental Information Data Centre (EIDC); DOI provided for access and citation.

## Data structure and content
- Metadata explains column headings and units for the CEZ_reptile_data.csv dataset and related materials.
- Key columns (with explanations and units):
  - Chornobyl_Center_sample_code; Sample (lizard or soil); Biota_latin_name; Depth_of_soil_layer_collected_cm (0–10 cm; cm).
  - Location (Red Forest site 1 or site 2); Date_snake_or_lizard_or_soil_sampled (dd/mm/yyyy); Sex_of_snake_or_lizard; Lizard_or_snake_total_length_mm; Lizard_tail_length_mm; Lizard_body_length_mm; Fresh_mass_of_snake_or_lizard_grams; Fresh_mass_of_snake_or_lizard_carcass_grams.
  - Notes; Cs-137_Bqkg_FM; Cs-137_error_Bqkg_FM; Sr-90_Bqkg_FM; Sr-90_error_Bqkg_FM; Pu-239,240_Bqkg; Pu-239,240_error_Bqkg_FM; Pu-238_Bqkg_FM; Pu-238_error_Bqkg_FM.
  - Soil_Cs-137_Bqkg_DM; Soil_Cs-137_error_Bqkg_DM.
- Units are specified for each field (e.g., cm, mm, g, Bq/kg, dd/mm/yyyy).

## Sampling context and provenance
- Sampling targets vertebrates (reptiles) and associated soil data from the CEZ.
- Location references to Red Forest site 1 and site 2; cross-referenced with Barnett et al., 2009 for site details.
- Guts removed prior to analysis (Notes field indicates gut removal).

## Measurements and data quality
- Radionuclide activity concentrations reported for reptiles as Bq/kg fresh mass (biota) and for soil as Bq/kg dry mass.
- Includes measurement errors for each radionuclide (e.g., Cs-137_error_Bqkg_FM, etc.).
- Metadata points to Materials_and_methods_CEZ_reptile.rtf for methodological detail and to the Barnett 2009 study for context.

## Standards, governance, and accessibility
- Metadata aimed at facilitating data discovery, interoperability, and reuse within the NERC EIDC framework.
- References to original data collection methods and previous related work ensure traceability and lineage.
- DOI provided for persistent access; dataset and methods are intended to be accessible and citable.

## Challenges for Data Stewards
- Aligning comprehensive column definitions across datasets and formats.
- Ensuring timely data provision from multiple data creators and formats.
- Achieving standardization of metadata to support interoperability (e.g., consistent units and naming).
- Handling large, multi-component datasets (biota and soil, multiple isotopes) and updating records as new analyses are completed.
- Managing updates in the context of legacy or updating databases and non-interoperable systems.

## Recommendations for stewardship and reuse
- Maintain a detailed data dictionary (as in this metadata) and ensure it stays synchronized with the primary dataset (CEZ_reptile_data.csv) and methods document.
- Enforce consistent field naming, units, and date formats; clearly document any deviations.
- Provide clear provenance, linking each data row to collection events, methods, and site details; reference Barnett 2009 for site context.
- Facilitate updates and versioning, with notes on changes and data embargoes if applicable.
- Ensure metadata and data are accessible via the NERC EIDC, with a stable DOI and clear licensing to support reuse by data stewards, researchers, and network catalogues.