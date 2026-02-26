# A 'Reference Site' in the Chernobyl Exclusion Zone: radionuclide and stable element data, and estimated dose rates

## Overview
- Dataset describing radionuclide and stable element concentrations and estimated dose rates for a reference site within the Chernobyl Exclusion Zone.
- Compiled by the NERC Environmental Information Data Centre (EIDC).
- Contains two main CSV files: Concentration_ratios.csv and Stable_element_concentrations.csv.
- Includes detailed metadata for sample identification, geographic location, sample type, tissue mass, and per-element concentration metrics.

## Data files and structure

- Concentration_ratios.csv
  - Core sample metadata: Sampling_date, Latin_Name, Common_Name, Code, GP_Point, Sex, Fresh_sample_mass_kg, Tissue, sample.
  - ICRP_RAP field describing reference animals and plants (RAP) standards.
  - For each element, concentration ratio fields (e.g., Li_CR, Be_CR, Na_CR, Mg_CR, Al_CR, P_CR, K_CR, Ca_CR, V_CR, Cr_CR, Mn_CR, Fe_CR, Co_CR, Ni_CR, Cu_CR, Zn_CR, As_CR, Se_CR, Rb_CR, Sr_CR, Mo_CR, Cd_CR, Cs_CR, Ba_CR, Tl_CR, Pb_CR, U_CR, etc.).
  - Each element has associated CR definition: fresh mass biota concentration divided by dry mass soil concentration.
  - Non-detects and censoring handled via LOD-based rules; values may be reported as "<" with guidance on interpretation (see Data handling notes).

- Stable_element_concentrations.csv
  - Core sample metadata: Sampling_date, ICRP_RAP, Latin_Name, Common_Name, Code, Latitude, Longitude, GP_point, Sex, Sample_or_tissue_type, wholebody_mass_kg, sample.
  - Per-element stable element measurements provided as:
    - Element_mg_kg_FM: concentration in biota per mg fresh mass.
    - Element_mg_kg_DM: concentration in soil per mg dry mass (units mg/kg DM).
  - Repeats for all stable elements present in the dataset; geographic coordinates use WGS84 (lat/long).

## Data handling and interpretation

- Non-detects and censoring
  - If an element is not detectable in all tissues for an animal, the LOD value is used to estimate tissue content.
  - If the estimated total body content’s >10% contribution comes from tissues below the LOD, the whole-body concentration is reported as a "<" value.
  - If the >10% contribution comes from tissues above the LOD, the reported value is a "<" with an explanatory approach noted as "<10..".
  - For contributions <10% of the body burden, the estimated whole-body concentration is considered a reasonable approximation.
- Concentration ratios (CR)
  - Defined as fresh mass activity concentration in biota divided by the dry mass activity concentration in soil.
  - Numerous element-specific CR fields are provided to support radiological and ecological interpretation.
- Units and mass bases
  - Fresh biota mass (kg) and dry soil mass are used for CR calculations.
  - Stable elements are reported as mg per kg of fresh mass (FM) and dry mass (DM) for the soil/biota context.
- Spatial/temporal scope
  - Sampling_date fields indicate date of sample collection.
  - Geographic coordinates (Latitude, Longitude, GP_point) use the WGS84 datum.

## Key considerations for data use (archetype alignment)

- Enables end users to self-serve analyses through per-element CRs and stable element concentrations.
- Supports dashboards and reports that compare radionuclide activity in biota to soil baselines and track spatial patterns.
- Facilitates dose-rate estimation by combining radionuclide data with RAP context and tissue-specific concentrations.
- Requires careful handling of censored data (LOD-based "<" values) during analysis and visualization.

## Source and accessibility

- Title: A 'Reference Site' in the Chernobyl Exclusion Zone: radionuclide and stable element data, and estimated dose rates
- Repository: NERC Environmental Information Data Centre (EIDC)
- DOI: https://doi.org/10.5285/ae02f4e89486-4b47-93ef-e49dd9ddecd4

## Summary of usefulness for data support

- Provides comprehensive, structured data to explore radionuclide and stable element distributions in biota and soil within a Chernobyl reference site.
- The two-file structure (concentration ratios and stable element concentrations) supports cross-filtering by species, location, and element.
- Metadata-rich design (tissue type, sample mass, RAP references) aids data quality checks, provenance, and reproducibility.
- Clear rules for handling non-detects and censored data help in producing robust, transparent analyses and data products.