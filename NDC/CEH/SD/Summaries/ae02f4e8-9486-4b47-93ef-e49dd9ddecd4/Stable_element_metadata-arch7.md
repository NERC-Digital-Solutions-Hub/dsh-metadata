# A 'Reference Site' in the Chernobyl Exclusion Zone: radionuclide and stable element data, and estimated dose rates

- Purpose and scope
  - Metadata for a dataset describing a reference site in the Chernobyl Exclusion Zone, focusing on radionuclide and stable element concentrations and estimated dose rates.
  - Data hosted by the NERC Environmental Information Data Centre; DOI provided for the dataset.

- Datasets included
  - Concentration_ratios.csv
    - Describes sampling metadata and per-element concentration ratios.
    - Key identifying fields: Sampling_date (dd/mm/yyyy), ICRP_RAP (ICRP Reference Animals and Plants), Latin_Name, Common_Name, Code (Chornobyl Center sample ID), GP_Point (sampling site), Sex, Fresh_sample_mass_kg, Tissue, sample (number of individuals).
    - Element-specific content (two-part per element):
      - Example elements represented: Li, Be, Na, Mg, Al, P, K, Ca, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Cd, Cs, Ba, Tl, Pb, U.
      - Each element has at least one concentration-ratio field (e.g., Li_CR) and a second field (e.g., Li_CR, 2) for additional context or unit specification.
      - Concentration ratio (CR) definition: fresh mass activity concentration in biota divided by the dry mass activity concentration in soil.
    - Data handling notes (embedded in field descriptions):
      - When an element is not detectable in all tissues, the limit of detection (LOD) is used to estimate tissue content.
      - If a tissue’s estimated contribution to total body content is >10% from below-LOD tissues, the whole-body concentration is reported as a “less than” value.
      - If the below-LOD tissues contribute <10% of body burden, the estimated whole-body concentration is treated as a reasonable approximation.
  - Stable_element_concentrations.csv
    - Describes sampling metadata and stable element concentrations.
    - Key identifying fields mirror Concentration_ratios.csv: Sampling_date, ICRP_RAP, Latin_Name, Common_Name, Code, Latitude, Longitude, GP_point, Sex, Sample_or_tissue_type, wholebody_mass_kg, sample.
    - Spatial fields: Latitude and Longitude (WGS84), enabling GIS georeferencing.
    - Per-element measurements (for each stable element present in the dataset):
      - Element_mg_kg_FM: concentration in biota per mg fresh mass.
      - Element_mg_kg_DM: concentration in soil per mg dry mass.
    - Notes indicate the same LOD-based handling as in Concentration_ratios.csv for undetectable elements; applicable elements are repeated for all stable elements.

- Data structure and units
  - Spatial context is provided via GP_Point and, for stable elements, explicit latitude/longitude (WGS84).
  - Temporal context via Sampling_date (dd/mm/yyyy) allows mapping changes over time.
  - Units:
    - Fresh mass concentrations and dose-related measurements use clear mass-based units (e.g., kg for fresh mass; mg_kg for concentrations).
    - CR fields are unitless (concentration ratios).
  - Documentation style:
    - Field explanations are embedded in the CSV metadata, including how to interpret <LOD values and how whole-body estimates are reported.

- Spatial and data integration considerations for GIS
  - Join strategies:
    - Link Concentration_ratios.csv and Stable_element_concentrations.csv to GIS layers via Code (sample ID) or GP_Point (sampling site).
  - Expected outputs:
    - Spatial distribution maps of radionuclide and stable-element concentrations across sampling sites within the Chernobyl Exclusion Zone.
    - Dose-rate estimation surfaces by site, leveraging ICRP_RAP context and concentration data.
  - Data quality and preprocessing needs:
    - Handle undetects and LOD-derived values consistently across elements.
    - Manage missing data, especially for large panels of elements per site.
    - Ensure coordinate reference system consistency (WGS84) when integrating stable-element data with other GIS layers.
  - Resolution and data management:
    - Data may be sparse or multi-resolution due to tissues and sampling efforts; consider aggregating by GP_Point or sampling date for certain analyses.

- Practical guidance for GIS specialists
  - Understand the two primary data tables and their linking keys (Code/GP_Point) to build cohesive maps.
  - Use sampling date to create time-enabled GIS visualizations of radionuclide and stable-element distributions.
  - Respect the LOD treatment rules when representing concentrations, particularly for percentage contributions to whole-body content.
  - Validate element-wise CR fields (two-part notation) to ensure correct interpretation of unitless ratios.

- Reference and access
  - Title: A 'Reference Site' in the Chernobyl Exclusion Zone: radionuclide and stable element data, and estimated dose rates
  - Source: NERC-Environmental Information Data Centre
  - DOI: https://doi.org/10.5285/ae02f4e89486-4b47-93ef-e49dd9ddecd4