# Metadata (an explanation of column headings and units) for: Radionuclide data for vertebrates in the Chernobyl Exclusion Zone, 2018, Gaschak, S.P., Beresford, N.A., Barnett, C.L., Wells, C., Maksimenko, A. and Chaplow, J.S. NERC-Environmental Information Data Centre. doi: https://doi.org/10.5285/518f88df-bfe7-442e-97ad-922b5aef003a

## Overview
- Provides column definitions and units for the CEZ_reptile_data.csv dataset (reptile and soil radionuclide data from the Chernobyl Exclusion Zone, 2018).
- Dataset accompanying Materials_and_methods_CEZ_reptile.rtf; references Barnett et al. 2009 for context.
- Captures sample metadata, biological measurements, and radionuclide activity concentrations (Cs-137, Sr-90, Pu isotopes) with associated uncertainties.

## Data structure and key fields
- Sample identifiers andContext
  - Chornobyl_Center_sample_code: internal sample code; not applicable units.
  - Sample: sample type (lizard or soil).
  - Biota_latin_name: Latin name of the biota; not applicable units.
  - Location: Red Forest site 1 or site 2; supports site-level analyses.
  - Date_snake_or_lizard_or_soil_sampled: sampling date (dd/mm/yyyy).
  - Notes: e.g., guts removed before analysis.
- Biological measurements (reptiles)
  - Sex_of_snake_or_lizard: biological sex; not applicable units.
  - Lizard_or_snake_total_length_mm: total length (mm).
  - Lizard_tail_length_mm: tail length (mm).
  - Lizard_body_length_mm: body length (mm).
  - Fresh_mass_of_snake_or_lizard_grams: fresh mass (g).
  - Fresh_mass_of_snake_or_lizard_carcass_grams: carcass mass with gut removal (g).
- Sampling and depth
  - Depth_of_soil_layer_collected_cm: soil depth for 0–10 cm layer (cm).
- Radionuclide activity concentrations (biota and soil)
  - Biota (fresh mass basis)
    - Cs-137_Bqkg_FM; Cs-137_error_Bqkg_FM
    - Sr-90_Bqkg_FM; Sr-90_error_Bqkg_FM
    - Pu-239,240_Bqkg; Pu-239,240_error_Bqkg_FM
    - Pu-238_Bqkg_FM; Pu-238_error_Bqkg_FM
  - Soil (dry mass basis)
    - Soil_Cs-137_Bqkg_DM; Soil_Cs-137_error_Bqkg_DM
- Data quality indicators
  - Error terms: uncertainties reported for radionuclide concentrations (where provided).
  - Notes: interpretative or methodological details (e.g., gut removal).

## Measurement details and units
- Units used
  - Lengths: millimeters (mm)
  - Mass: grams (g) for fresh mass and carcass mass
  - Depths: centimeters (cm)
  - Radionuclide activity: becquerels per kilogram (Bq/kg)
    - Fresh mass basis for biota (FM)
    - Dry mass basis for soil (DM)
- Date format: day/month/year (dd/mm/yyyy)
- For certain fields, units are not applicable (e.g., sample type, biota Latin name)

## Sampling scope and context
- Species/biota: reptiles (lizards and snakes) sampled at two Red Forest sites.
- Matrixes: biota (reptiles) and soil (0–10 cm layer) analyzed for radionuclide activity.
- Temporal scope: data from 2018; metadata documents collection protocols in Materials_and_methods_CEZ_reptile.rtf.
- Reference context: Barnett, Gaschak, Beresford, Howard, Maksimenko (2009) for related radionuclide activity data in Chernobyl reptiles.

## Data provenance and access
- Source dataset: CEZ_reptile_data.csv; metadata file provides definitions and units.
- Repository: NERC Environmental Information Data Centre (EIDC).
- DOI: to access dataset and accompanying documentation.

## Data quality considerations and caveats
- Data presented with explicit measurement uncertainties for radionuclide concentrations.
- Metadata supports reuse by clarifying column meanings, units, and sampling context.
- Potential data alignment considerations when merging with other datasets (e.g., Barnett 2009) due to differing formats or scopes.

## Data products and reuse opportunities (Data Support perspective)
- End-user capabilities
  - Build self-service analyses by linking biota data with radionuclide concentrations (per species, site, and date).
  - Create dashboards or pivot tables to compare Cs-137, Sr-90, and Pu isotopes across reptiles and soils.
  - Explore correlations between morphometrics (length, mass) and radionuclide burdens, if relevant.
  - Compare activity concentrations between Red Forest site 1 and site 2; assess temporal or methodological trends against 2009 datasets.
- Potential data products
  - Species- and site-specific radionuclide concentration tables (FM for biota; DM for soil).
  - Visualizations of radionuclide burden distributions with associated uncertainties.
  - Documentation-linked data products enhanced by the Materials_and_methods_CEZ_reptile.rtf content for reproducibility.
- Reuse considerations
  - Ensure correct interpretation of units (FM vs DM) and sample type distinctions.
  - Reference original dataset and Barnett 2009 context when comparing across studies.

## Citations and references
- Barnett, C.L., Gaschak, S., Beresford, N.A., Howard, B.J., Maksimenko, A. 2009. Radionuclide activity concentrations in two species of reptiles from the Chernobyl exclusion zone. Radioprotection, 44, 537-542. http://dx.doi.org/10.1051/radiopro/20095099