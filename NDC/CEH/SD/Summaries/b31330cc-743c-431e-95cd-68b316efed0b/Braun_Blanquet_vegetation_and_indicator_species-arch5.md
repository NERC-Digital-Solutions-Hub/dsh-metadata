# DATA HEADER INFORMATION for Braun_Blanquet_vegetation_and_indicator species.csv

## Overview
- Documents the header information and data dictionary for a dataset that records percent cover of indicator species using the Braun-Blanquet scale.
- References Manual 1_Classical_Survey (for methodological context).
- DOI provided: https://doi.org/10.5285/b31330cc-743c-431e-95cd-68b316efed0b
- Programme: ESPA; Project: P4GES
- Acknowledgement requirement: Products derived from these data require acknowledgment of Laboratoire des Radio Isotopes, Université d'Antananarivo.

## Provenance and Attribution
- site_id represents the P4GES WP4 site code.
- Data fields include: site_id, Scientific_name, Local_name, Family, Life_form, Percent_cover, Indicator_species, B_B_scale.
- Life_form is a categorical variable with values indicating growth form (Fern/Shrub/Herb/Grass/Vine/Tree).
- B_B_scale is a categorical variable that encodes the Braun-Blanquet scale values.
- Additional context and field sourcing notes indicate information provenance and typical field roles (e.g., botanist).

## Data content and structure
- The dataset records percent cover of inventoried species using the Braun-Blanquet scale.
- Core fields and their roles:
  - site_id: P4GES WP4 site code; text string.
  - Scientific_name: Scientific name of the inventoried species; text string.
  - Local_name: Vernacular/local name; text string.
  - Family: Scientific family; text string.
  - Life_form: Life form category; text string via categorical variable (Fern/Shrub/Herb/Grass/Vine/Tree).
  - Percent_cover: Degree of dominance of the inventoried species; numeric; percentage (%).
  - Indicator_species: Yes/No indicating whether the species is a specific land-use indicator; binary.
  - B_B_scale: Braun-Blanquet scale value; categorical with coded levels.
- Units are specified per field (e.g., Percent_cover in %, Life_form as categorical labels).

## Metadata and standards
- Metadata aligns with a structured data dictionary defining field meaning, data types, units, and field materials/resource persons (e.g., botanist).
- Uses standardized Braun-Blanquet scale coding to support interoperability and comparable analyses.
- Cross-referenced with project/program context and data provenance to aid discovery and reuse.

## Data quality and governance considerations for Data Stewards
- Ensure metadata completeness and consistency with the data dictionary (field names, types, units, and descriptions).
- Verify adherence to the Braun-Blanquet coding scheme (B_B_scale) and maintain the mapping in documentation.
- Validate that life_form categories conform to the defined set (Fern/Shrub/Herb/Grass/Vine/Tree).
- Maintain clear provenance: retain DOI, programme, and project identifiers; enforce Acknowledgement requirements for derived products.
- Ensure proper storage, versioning, and updates to reflect any new or revised site data (site_id consistency).
- Plan for sharing through relevant data portals and cataloging holdings, with appropriate metadata tagging for discoverability.
- Be aware of potential data creators’ and users’ needs when adapting or integrating this dataset with other vegetation surveys or land-use indicators.

## Relevance to discovery and reuse
- Clear data dictionary and explicit field definitions enable researchers to understand variable meanings and constraints.
- Standardized fields and units (e.g., Percent_cover, Life_form categories, B_B_scale coding) support interoperability across datasets and studies.
- DOI and project context facilitate citation, traceability, and appropriate attribution.

## Practical implications and next steps for Data Stewards
- Confirm and/or update any missing metadata values (e.g., field materials/resource s for B_B_scale) to ensure full metadata completeness.
- Ensure dataset is prepared for upload to relevant data portals with proper metadata records and access permissions.
- Maintain the acknowledgment clause in any derived products and track provenance for data-use compliance.
- Coordinate with data creators to resolve any ambiguities in field definitions or coding schemes before sharing.