# Metadata (an explanation of column headings and units) for: Beresford, N.A., Gaschak, S., Barnett, C.L., Maksimenko, A., Guliaichenko, E., Wells C., Chaplow J.S. A 'Reference Site' in the Chernobyl Exclusion Zone: radionuclide and stable element data, and estimated dose rates. NERC-Environmental Information Data Centre. doi: https://doi.org/10.5285/ae02f4e89486-4b47-93ef-e49dd9ddecd4

## Purpose and scope
- Provides metadata and column-level explanations for two CSV data files associated with a reference site in the Chernobyl Exclusion Zone.
- Datasets cover radionuclide and stable element concentrations and estimated dose rates.
- Data are prepared and hosted by the NERC Environmental Information Data Centre.
- Aligns with International Commission on Radiological Protection (ICRP) Reference Animals and Plants (RAP) framework.

## Datasets described
- Concentration_ratios.csv
  - Contains sampling metadata and concentration ratio (CR) fields for multiple elements.
  - Key fields include Sampling_date, ICRP_RAP, Latin_Name, Common_Name, Code, GP_Point, Sex, Fresh_sample_mass_kg, Tissue, sample.
  - For each element (e.g., Li, Be, Na, Mg, Al, P, K, Ca, and many others), there are CR-related columns:
    - Element_CR: concentration ratio where CR = fresh mass activity concentration in biota divided by dry mass activity concentration in soil.
    - Element_CR, 2: secondary descriptor for the same element.
  - Includes explicit handling of non-detects and data qualifiers (see below).

- Stable_element_concentrations.csv
  - Contains sampling metadata, location (Latitude, Longitude), and tissue/body mass information.
  - Key fields include Sampling_date, ICRP_RAP, Latin_Name, Common_Name, Code, Latitude, Longitude, GP_point, Sex, Sample_or_tissue_type, wholebody_mass_kg, sample.
  - For each stable element, reporting includes:
    - <Element: non-detect handling indicator for total body content.
    - Element_mg_kg_FM: concentration in biota (fresh mass).
    - Element_mg_kg_DM: concentration in soil (dry mass).
  - Repeats this structure across all listed stable elements.

## Key field definitions and conventions
- Sampling_date: date formatted as dd/mm/yyyy.
- ICRP_RAP: reference animals and plants per ICRP (RAP) framework.
- Latin_Name / Common_Name: taxonomy identifiers for the biota.
- Code / GP_Point / GP_point: dataset identifiers for samples and sampling sites.
- Latitude / Longitude: geographic coordinates in decimal degrees (WGS84).
- Sex: biological sex where applicable.
- Tissue / Sample_or_tissue_type: tissue type analyzed or sampling category.
- Fresh_sample_mass_kg / wholebody_mass_kg: mass measurements in kilograms.
- CR-based fields (CR): concentration ratio, defined as fresh mass activity concentration in biota divided by dry mass activity concentration in soil; unitless.
- <Element: non-detect handling:
  - If an element is not detectable in all tissues for an animal, the LOD is used to estimate total tissue content.
  - If the contribution to total body content from tissues below LOD is >10%, the whole-body concentration is reported as a ‘less than’ value.
  - If the contribution is <10%, the value is treated as a reasonable approximation; flagged as <10.. .
- Element_CR, Element_CR, 2 (and similar for other elements): two variants or descriptors of concentration ratio for each element.
- <Element (in stable elements file): non-detect handling indicator for the total body content of that element.
- Element_mg_kg_FM / Element_mg_kg_DM: measured concentration in biota (fresh mass) and soil (dry mass), respectively.
- Units: CR fields are unitless; concentration fields use mg/kg (FM or DM) as specified.

## Data quality, interpretation, and data management notes
- Metadata explicitly documents how non-detects are treated (LOD-based substitutions and reporting rules).
- The dataset uses ICRP RAP as a reference framework to support comparability across studies.
- Clear distinction between fresh mass biota concentrations and dry mass soil concentrations in stable elements.
- Emphasis on explicit data qualifiers and consistent units to facilitate integration into monitoring frameworks.
- Data sharing considerations are acknowledged via metadata transparency about LOD handling and the need for clear documentation to verify data suitability.

## Relevance for monitoring frameworks
- Provides a structured blueprint for reporting radionuclide and stable element data, including:
  - Standardized sampling and biota/soil concentration metrics.
  - Transparent treatment of nondetects and limits.
  - Clear definitions of concentration ratios to evaluate bioaccumulation.
  - Geospatial and taxonomic context to support site-specific monitoring and trend analysis.
- Facilitates cross-study comparability through RAP alignment and explicit unit conventions.
- Supports generation of dose-rate estimates by integrating radionuclide and stable element data with site-specific metadata.

## Practical implications for authors of monitoring frameworks
- Adopt similar metadata conventions to ensure data usability, reproducibility, and transparency.
- Implement clear non-detect handling rules and document them in metadata.
- Use standardized reference frameworks (e.g., ICRP RAP) for comparability across sites.
- Ensure precise unit definitions and site identifiers to enable data integration and dashboard-ready reporting.
- Plan for open data sharing while maintaining appropriate data governance and provenance documentation.