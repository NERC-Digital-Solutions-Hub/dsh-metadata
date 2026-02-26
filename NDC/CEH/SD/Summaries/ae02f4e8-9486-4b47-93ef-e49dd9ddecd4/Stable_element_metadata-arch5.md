# A 'Reference Site' in the Chernobyl Exclusion Zone: radionuclide and stable element data, and estimated dose rates

## Overview
- Metadata and data files from the NERC Environmental Information Data Centre for a reference site in the Chernobyl Exclusion Zone.
- Contains radionuclide and stable element data and estimated dose rates.
- Data published as two CSV files: Concentration_ratios.csv and Stable_element_concentrations.csv.
- DOI: https://doi.org/10.5285/ae02f4e89486-4b47-93ef-e49dd9ddecd4.

## Data files and schema (high-level)
- Concentration_ratios.csv
  - Core sample and organism metadata:
    - Sampling_date (dd/mm/yyyy)
    - ICRP_RAP (ICRP Reference Animals and Plants)
    - Latin_Name, Common_Name
    - Code (Chornobyl Centre unique sample identifier)
    - GP_Point (sampling site identifier)
    - Sex (where applicable)
    - Fresh_sample_mass_kg
    - Tissue
    - sample (number of individuals)
  - Element-related fields:
    - For each target element, a concentration ratio (CR) field is provided (e.g., Li_CR, Be_CR, Na_CR, Mg_CR, Al_CR, P_CR, K_CR, Ca_CR, V_CR, Cr_CR, Mn_CR, Fe_CR, Co_CR, Ni_CR, Cu_CR, Zn_CR, As_CR, Se_CR, Rb_CR, Sr_CR, Mo_CR, Cd_CR, Cs_CR, Ba_CR, Tl_CR, Pb_CR, U_CR, etc.)
    - All CR fields are unitless.
  - Non-detect handling and data quality notes:
    - Where an element was not detectable in all tissues, LOD-based estimation is used to approximate tissue content.
    - If the estimated total body content from below-LOD tissues is >10%, the whole-body concentration is reported as a “less than” value; if <10%, the estimate is treated as a reasonable approximation.
    - These values are identified by indicators like <10.. (per element) and documented rules.

- Stable_element_concentrations.csv
  - Core sample and location metadata (similar to above, with spatial context):
    - Sampling_date
    - ICRP_RAP
    - Latin_Name, Common_Name
    - Code
    - Latitude, Longitude (WGS84)
    - GP_point
    - Sex
    - Sample_or_tissue_type
    - wholebody_mass_kg (fresh mass-based)
    - sample
  - Stable element measurements:
    - For each stable element, two columns:
      - <Element>_mg_kg_FM (mg per kg fresh mass)
      - <Element>_mg_kg_DM (mg per kg dry mass)
  - Non-detect handling:
    - Similar LOD-based approach as in Concentration_ratios.csv; non-detects may be reported as less-than values or approximated, with notes indicating contribution to body burden.
  - Spatial and taxonomic context:
    - Uses latitude/longitude in WGS84; sample identifiers align with the Code field.

## Key data governance and stewardship considerations
- Data provenance and discoverability:
  - Study site, sampling dates, organism identifiers, and sampling locations are captured to enable traceability and reuse.
  - Code field provides a unique sample identifier linking metadata to measurements.
- Standardization and interoperability:
  - Consistent use of ICRP_RAP alignment, Latin/Common names, and uniform date/units (dd/mm/yyyy, kg, mg/kg).
  - Spatial coordinates in WGS84 for mapping and integration with other geospatial datasets.
- Metadata completeness and usage:
  - Detailed documentation of measurement units and the meaning of each CR and elemental field.
  - Explicit handling rules for non-detects to support transparent data interpretation and downstream dose assessment.
- Constraints and governance:
  - Title indicates inclusion of dose-rate estimates; ensure full documentation of methods used to derive dose rates is linked or embedded in data discovery records.
  - Embargo or access controls are not specified here; ensure appropriate licensing and data-use terms accompany the dataset.

## Practical guidance for reuse
- When integrating into catalogs, index by:
  - Project/site (Chernobyl Exclusion Zone reference site), Code, Sampling_date, ICRP_RAP, Latin_Name/Common_Name.
- Use CR fields (e.g., Li_CR, Na_CR, etc.) for cross-element comparison of biota-to-soil transfer, ensuring unitless interpretation.
- For stable elements, utilize both FM and DM concentrations to support dose and mass-balance calculations.
- Pay attention to LOD-induced flags (<10.. or similar) to understand potential underestimation in tissues with non-detects.
- Cross-link radionuclide and stable-element data via the Code field to enable comprehensive dose-rate assessment per sample.

## End