# Metadata (an explanation of column headings and units) for: Radionuclide data for vertebrates in the Chernobyl Exclusion Zone, 2018, Gaschak, S.P., Beresford, N.A., Barnett, C.L., Wells, C., Maksimenko, A. and Chaplow, J.S. NERC-Environmental Information Data Centre. doi: https://doi.org/10.5285/518f88df-bfe7-442e-97ad-922b5aef003a

## Purpose and scope
- Provides explanations of column headings and units for the radionuclide data collected on vertebrates in the Chernobyl Exclusion Zone (CZ) in 2018.
- Data are stored in Biota_radionuclide_data.csv; an accompanying Materials_and_methods_biota.rtf document is available for methodology context.
- Notes that n/a indicates not available.

## Data file and access
- Primary data file: Biota_radionuclide_data.csv.
- Related methodological document: Materials_and_methods_biota.rtf.
- DOI reference included for data citation and traceability.

## Key columns and data types (highlights relevant for GIS use)
- Identifiers and species
  - Chornobyl_Center_ID: Laboratory sample identifier (string).
  - Biota_latin_name: Latin name of species (string).
  - Biota_common_name: Common name of species (string).
- Sampling and location
  - Date_sampled: Date biota was sampled (dd/mm/yyyy).
  - Site_Location_within_Chernobyl_exclusion_zone: Sampling site location categorized as Low, Medium, or High, based on Beresford et al. 2008.
  - Sex: Sex of biota (female/male) or n/a when not recorded.
- Biological measurements
  - Fresh_mass_of_biota_grams: Mass of fresh biota sample (grams).
  - Mass_of_biota_carcass_grams: Mass of carcass after preparation (grams).
  - Notes: Notes on preparation and handling (text, may be n/a).
- Radionuclide activity measurements (per sample and per kg fresh weight)
  - Sr-90_< and Cs-137_< and Pu-238_<: Indicators for measurements below detection limit (< in column) where applicable.
  - Sr-90_Bq_per_sample, Cs-137_Bq_per_sample, Pu-239_240_Bq_per_sample, Pu-238_Bq_per_sample: Activity per sample (units: Bq per sample).
  - error_Sr-90_Bq_per_Sample, error_Cs-137_Bq_per_Sample, error_Pu-239_240_Bq_per_Sample, error_Pu-238_Bq_per_Sample: Measurement error per sample (Bq per sample); n/a if not reported.
  - Sr-90_Bq_per_kg_FW, Cs-137_Bq_per_kg_FW, Pu-239_240_Bq_per_kg_FW, Pu-238_Bq_per_kg_FW: Activity concentration in fresh weight (units: Bq per kg FW); n/a if not reported; < indicates below detection for Pu-238 and Sr-90/Cs-137 when applicable.
  - Pu-238_<, Pu-238_Bq_per_kg_FW, etc.: Conditions and values for Pu-238 concentration (same notation as above).
- Concentration ratios (biota vs. soil)
  - Sr-90_Concentration_ratio, Cs-137_Concentration_ratio, Pu-239_240_Concentration_ratio, Pu-238_Concentration_ratio: Ratios of biota activity concentration (per kg FW) to soil activity concentration (per kg soil dry weight); where not reported, n/a.
  - Formats vary by nuclide, with explicit notes about whether the ratio is reported in weight or per sample terms (e.g., Biota Bq kg-1 FW / soil Bq kg-1 dry).

## Units and data quality indicators
- Units used include:
  - Bq per sample (for per-sample activity)
  - Bq per kg fresh weight (FW) (for tissue-concentration measurements)
  - Bq per kg soil dry weight (for soil comparisons in concentration ratios)
- Detection limits and data availability
  - "<" preceding a value indicates the measurement is below the limit of detection (LOD) for that nuclide/measurement.
  - n/a indicates not available for a given field or measurement.
- Data preparation notes
  - The Notes field contains information on how biota were prepared for analysis (where applicable).

## GIS applicability and integration considerations
- Spatial context
  - Site_Location_within_Chernobyl_exclusion_zone provides a straightforward spatial classification (Low/Medium/High) that can be linked to CZ site polygons or sampling location attributes for thematic mapping.
- Temporal context
  - Date_sampled enables time-series or seasonal analyses when combined with other datasets.
- Multivariate analysis potential
  - Allows mapping of species-specific radionuclide burdens (by species, date, site category) and visualization of biota-to-soil transfer via concentration ratios.
- Data integration
  - Columns for species, mass, and preparation notes aid data cleaning and standardization when joining with other GIS layers (e.g., soil contamination maps, land-use layers, or Beresford 2008 CZ site categorizations).
- Data quality considerations
  - Presence of n/a and < markers requires careful handling during GIS analyses (e.g., masking, imputation, or exclusion depending on the analysis).

## Summary for GIS work
- This metadata defines a structured, column-level schema for radionuclide data in vertebrates from the CZ (2018), enabling map-based visualization of species-specific contamination, site-level exposure categories, and biota-to-soil transfer analyses.
- Key mapping-ready fields include:
  - Site_Location_within_Chernobyl_exclusion_zone (Low/Medium/High)
  - Date_sampled and Biota_latin_name/Biota_common_name (taxonomy and temporal context)
  - Fresh weight and carcass mass measurements for normalization
  - Sr-90, Cs-137, Pu-238/239/240 activity per sample and per kg FW
  - Concentration ratios (biota/soil) for cross-site and cross-species comparisons
- Ensure treatment of < (LOD) values and n/a indicators during GIS processing, and reference the accompanying notes and methodology for data preparation steps.