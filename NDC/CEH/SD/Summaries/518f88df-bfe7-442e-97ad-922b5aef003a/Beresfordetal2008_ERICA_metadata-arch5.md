# Metadata (an explanation of column headings and units) for : Radionuclide data for vertebrates in the Chernobyl Exclusion Zone, 2018, Gaschak, S.P., Beresford, N.A., Barnett, C.L., Wells, C., Maksimenko, A., Chaplow, J. NERC-Environmental Information Data Centre. https://doi.org/10.5285/518f88df-bfe7-442e-97ad-922b5aef003a

## Overview
- Provides column-level metadata and units for three data files related to radionuclide data in vertebrates from the Chernobyl Exclusion Zone (2018).
- Data are archived and discoverable via the NERC Environmental Information Data Centre; includes a Materials_and_method_ERICA.rtf document for methods.
- “n/a” indicates not available; some fields use detection-limit conventions (e.g., < denotes below LOD).

## Data files and structure
- ERICA_TLD_animal_results.csv
  - Contains biota-specific TLD data and radioisotope activity measurements.
  - Key fields cover species, individual identifiers, sex, sampling site (Low/Medium/High), TLD IDs, attachment/removal dates, exposure days, and dose/activity measurements (Cs-134/137, Sr-90), biota mass, and multiple potential recapture-related measurements (Additional_1 to Additional_4 sets).
  - TLD dose rate fields and mass measurements accompany each timepoint, including post-removal measurements.
- ERICA_soil_results.csv
  - Contains soil sample coordinates (Latitude, Longitude), sampling metadata (Sample_code, Date_soil_sampled, Site_Location, Sampling_point), and physical properties (soil masses, moisture).
  - Radioisotope concentrations reported for Cs-137, Cs-134, Sr-90, K-40, Co-60, Am-241, Eu-154/ Eu-155, Pu-238/239/240, with means and standard errors for gamma and beta measurements.
- ERICA_Non-animal_results.csv
  - Records non-animal (TLD) results related to site placement/removal and total dose (Total_dose_milliSv).
  - Includes site location, position (above/below ground, etc.), exposure days, and placement/removal dates.

## Key metadata standards and field guidance
- Geographic and site metadata: Latitude/Longitude (WGS84), Site_Location (Low/Medium/High), Site_locator, Sampling_point.
- Temporal data: Date_placed_at_site, Date_removed_from_site, Date_soil_sampled, Sampling_Date_TLD_attached_to_biota, Sampling_Date_TLD_Removed_from_biota, and additional recapture dates for up to four additional measurement events.
- Measurements and units: 
  - Radioisotope activities: Bq (becquerel) for Cs-137, Cs-134, Sr-90, Pu isotopes, Am-241, Eu-154/Eu-155, etc.
  - Masses: grams for biota and soil samples.
  - Doses: milliSv or microGy/h as applicable.
  - Datasets include both raw measurements and derived/summary fields (Means, Standard Errors).
- Data quality flags: "<" indicates values below detection limit (LOD) for several isotopes; n/a used where not applicable.
- Recording conventions: Some fields allow repeated Biota_sample_number values to denote the same animal across TLD attachment/removal events; Additional_1–Additional_4 sets account for recapture-related measurements.

## Data provenance, references, and context
- Measurements tied to established references and methodologies:
  - Beresford et al. 2008 (ERICA tool application for small mammals at Chernobyl sites).
  - Gaschak et al. 2011; related radiation ecology work.
- Measurement approaches described for gamma and beta dose assessments (e.g., MKS-01R-01 meters, with standard positioning to ensure consistent height).
- Links to broader ERICA-derived methodologies and prior site characterizations (Beresford, Gaschak, Maksimenko et al.).

## Data governance and access
- Data are curated by the NERC Environmental Information Data Centre.
- DOI provided for the metadata/resource set: https://doi.org/10.5285/518f88df-bfe7-442e-97ad-922b5aef003a.
- A supplementary Materials_and_method_ERICA.rtf is available to detail methods and data handling.
- Clear field definitions and units support discoverability, interoperability, and reuse by data creators, data sharers, and data users.

## Practical considerations for Data Stewards
- Ensure consistent interpretation of detection-limit indicators (<) and n/a across all three files.
- Maintain linkage between TLD-based biota data and soil data via site location and sampling dates for integrated analyses.
- Preserve provenance by maintaining references to Beresford (2008) and Gaschak (2011) within data context.
- Manage updates and versioning, given recurring measurements (Additional_1 to Additional_4) and potential recaptures.
- Confirm data formatting standards (e.g., date formats dd/mm/yyyy, Site_Location categories) during ingestion into catalogs and portals.