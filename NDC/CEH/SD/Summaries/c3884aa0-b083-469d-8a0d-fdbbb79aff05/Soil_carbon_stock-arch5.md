# DATA HEADER INFORMATION for Soil_carbon_stock.csv

## Dataset scope and purpose
- Presents soil carbon stock at two depths: 0-30 cm and 0-100 cm.
- Stocks are provided as both equivalent mass (SOC_Me_30, SOC_Me_100) and equivalent volume (SOC_Ve_30, SOC_Ve_100).
- Derived from carbon content predicted by a Mössbauer/Infrared (MIRS) prediction model.
- Associated with ESPA Programme and P4GES project; includes a DOI for citation.
- Site identifiers use P4GES site codes; subplot identifiers indicate sampling location within sites (S1/S2/S3/S4).

## Data provenance and generation
- Carbon content used to compute stocks via the MIRS model.
- Detailed calculations documented in Manual_1_Classical_Survey.rtf (page 17, section 4.4).
- DOI provided for dataset provenance and citation.
- Acknowledgement required for the Laboratoire des Radio Isotopes, Université d'Antananarivo for products derived from these data.

## Metadata and data model
- Site_id: P4GES site code; Type: Text String; Unit: not specified.
- SOC_subplot: Subplot where the sample was collected; Type: Categorical; Values: S1, S2, S3, S4.
- SOC_Me_30: Soil carbon stock (mass equivalent) at 30 cm; Type: Numeric; Unit: Mg ha^-1.
- SOC_Me_100: Soil carbon stock (mass equivalent) at 100 cm; Type: Numeric; Unit: Mg ha^-1.
- SOC_Ve_30: Soil carbon stock (volume equivalent) at 30 cm; Type: Numeric; Unit: Mg ha^-1.
- SOC_Ve_100: Soil carbon stock (volume equivalent) at 100 cm; Type: Numeric; Unit: Mg ha^-1.
- Note: Some header fields (e.g., field_materials_resources) are empty; data is linked to the P4GES site codes and subplots.

## Data governance and sharing considerations
- Requires proper acknowledgement of the Laboratoire des Radio Isotopes, Université d'Antananarivo for derived products.
- Use and citation guided by the DOI and ESPA/P4GES project context.
- Sharing limitations and update mechanisms should be in place; dataset should be uploaded to relevant portals with complete metadata.

## Data quality, maintenance, and versioning
- Documentation exists for calculations and model method; ensures traceability to the MIRS-based approach.
- Updates should follow established processes to maintain consistency across site IDs, subplots, and depth layers.

## Practical guidance for data stewards
- Ensure metadata completeness and alignment with data user needs (e.g., researchers focusing on depth-specific carbon stock).
- Maintain linkages between Site_id, SOC_subplot, and stock measurements; preserve units and data types.
- Plan for timely data updates and clear communication of any embargoes or restrictions.