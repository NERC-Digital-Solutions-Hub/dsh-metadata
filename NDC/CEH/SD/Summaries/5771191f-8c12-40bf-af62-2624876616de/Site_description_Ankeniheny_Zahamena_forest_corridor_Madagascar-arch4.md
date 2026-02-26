# DATA HEADER INFORMATION for Site_description_Ankeniheny_Zahamena_forest_corridor_Madagascar.csv

## Overview
- Documents the topographical characteristics of sampling sites in the Ankeniheny-Zahamena forest corridor, Madagascar.
- Part of the ESPA program and the P4GES project; includes DOIs and project pages.
- Requires acknowledgement of Laboratoire des Radio Isotopes, Université d'Antananarivo for products derived from these data.
- Provides a metadata-rich header describing each field, its type, unit, and collection resources.

## Key fields and data structure
- site_ID: P4GES site code; text string; no unit (identifier)
- ZOI (Zone of Interest): categorical; values Lakato, Andasibe, Anjahamana, Didy
- Location: sampling point location; text string
- LU (Land use): categorical; examples include Closed Canopy, Tree Savoka, Shrub Savoka, Degraded Land
- Type: categorical; values Plot or Transect
- X (Longitude): numeric; decimal degrees (WGS84); GPS device noted
- Y (Latitude): numeric; decimal degrees (WGS84); GPS device noted
- Altitude: numeric; meters; GPS device noted
- Precision: numeric; meters; GPS accuracy
- slope_up: numeric; degrees; upward slope measurement
- slope_down: numeric; degrees; downward slope measurement
- topographic_position: text; positions on slope (e.g., Mid side, High side, Low side)
- age_of_deforest: numeric; years; estimated age since deforestation (from field interviews)
- age_of_fallow: numeric; years; estimated age of fallows (from field interviews)
- Historic: text string; site history based on local interviews
- For each field, the header also records the field and materials resources used (e.g., botanist, local guides, GPS device)

## Provenance, access, and governance
- Source/program references: ESPA and P4GES, with associated URLs
- Data identifiers and discoverability: includes a DOI link for the dataset
- Data usage and attribution: explicit requirement to acknowledge the Laboratoire des Radio Isotopes in outputs derived from these data
- Data collection context: topographical site descriptions collected via field surveys with specified resources

## Data quality, standards, and gaps
- Clear data types and units are specified for each field, aiding consistency and interoperability
- Some fields may be incomplete in the header (e.g., Historic may be partially filled); variability in age estimates derived from interviews noted
- Emphasizes the need for standardized metadata, traceability to field resources, and consistent coordinate reference (WGS84)

## Implications for data strategy and actions (Data Leaders)
- Use this header as a template for documenting site-level environmental data, ensuring metadata completeness and consistency across projects
- Maintain clear provenance: cite ESPA/P4GES and acknowledge contributing laboratories and field teams
- Ensure data discoverability and reusability by preserving units, data types, and collection methods; track updates and revisions
- Facilitate cross-network collaboration by aligning field categories (e.g., LU, ZOI) and sharing with partner datasets
- Plan for data quality improvements: fill gaps in Historic narrative, verify coordinates and land-use classifications, and harmonize deforestation/fallow age estimates across datasets