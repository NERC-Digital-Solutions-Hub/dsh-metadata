# DATA HEADER INFORMATION for Soil_carbon_content.csv

## Quick snapshot
- Dataset: Soil organic carbon content inferred using the MIRS prediction model.
- Related documentation: Manual_1_Classical_Survey.rtf, page 17, section 4.4.
- Project context: ESPA Programme; Project P4GES.
- DOI: https://doi.org/10.5285/c3884aa0-b083-469d-8a0d-fdbbb79aff05
- Acknowledgement: Required for products derived from these data to Laboratoire des Radio Isotopes, Université d'Antananarivo.

## Data model and content
- File: Soil_carbon_content.csv
- Key fields and definitions:
  - Site_id
    - Information: P4GES site code
    - Variable Type: Text String
  - Site_id, Variable Type
    - Value: Text String (same as Site_id)
  - Site_id, Unit
    - Value: .
  - SOC_subplot
    - Information: Subplot where sampling was conducted
    - Variable Type: Categorical
    - Unit: S1 / S2 / S3 / S4
  - SOC_sampling_depth
    - Information: Depth of the sampled soil layer
    - Variable Type: Numeric
    - Unit: centimeter
  - SOC_content
    - Information: Carbon content of the sample (g/kg of soil) generated using the MIRS prediction model
    - Variable Type: Numeric
    - Unit: grammes per kilo (g.kg-1)

## Metadata, provenance, and standards
- Prediction method: Derived via MIRS model; SOC_content is model-generated rather than direct measurement.
- Related materials: Manual_1_Classical_Survey.rtf (section 4.4) provides context for the data generation.
- Project and program metadata: ESPA Programme; Project P4GES; links provided for both organisations.

## Data governance, access, and reuse
- Attribution: Acknowledgement of Laboratoire des Radio Isotopes, Université d'Antananarivo required for products derived from these data.
- Identifiers and discoverability: Data described with explicit field definitions, types, and units; DOI provided to support citation and access.
- Collaboration context: Part of a larger data ecosystem (ESPA/P4GES) with emphasis on data sharing and cross-project usability.

## Implications for data leadership
- Data assets are clearly structured with defined fields, types, and units to support discoverability and reuse.
- Metadata includes model-based derivation information, aiding assessment of data quality and suitability for analysis.
- Clear attribution requirements and referenced manuals help ensure consistent governance and responsible use across partners.
- Emphasizes the need to maintain provenance, document data lineage, and align with project-level data management practices.