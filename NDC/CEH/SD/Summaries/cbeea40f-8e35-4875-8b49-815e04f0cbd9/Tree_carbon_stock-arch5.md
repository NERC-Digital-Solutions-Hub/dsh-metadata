# DATA HEADER information for Tree_carbon_stock.csv

## Overview
- Dataset records the carbon stock of a big tree cluster.
- DOI: https://doi.org/10.5285/cbeea40f-8e35-4875-8b49-815e04f0cbd9
- Programme: ESPA; Project: P4GES
- Acknowledgement required for products derived from these data: Laboratoire des Radio Isotopes, Université d’Antananarivo
- Related materials: Manual 1_Classical_Survey
- Notes indicate blank cells mean no data available

## Data structure and key fields
- Site_ID
  - Information: site code where the inventory was conducted
  - Type: Text String
  - Unit: not specified
- Subplot
  - Information: relative size of the inventory circle inside which sampling occurred
  - Type: Categorical
  - Unit: Large / Medium / Small
- Area
  - Information: area of the inventory circle
  - Type: Numeric
  - Unit: m²
- Trees-local_name
  - Information: vernacular name of the tree
  - Type: Text String
  - Unit: not specified
- Trees_Scientific_name
  - Information: scientific name of the tree (if available)
  - Type: Text String
  - Unit: not specified
- Trees_Genera
  - Information: genus of the tree
  - Type: Text String
  - Unit: not specified
- Trees_Family
  - Information: family of the tree
  - Type: Text String
  - Unit: not specified
- Trees_DBH
  - Information: Diameter at Breast Height (1.3 m)
  - Type: Numeric
  - Unit: Centimeter
- Trees_height
  - Information: height of the tree
  - Type: Numeric
  - Unit: meter
- WSG
  - Information: Wood Specific Gravity of the wood species
  - Type: Numeric
  - Unit: Unitless
- CHAVE 2005
  - Information: carbon stock of the tree according to the CHAVE 2005 allometric equation
  - Type: Numeric
  - Unit: Kg per tree
- MADA I.1
  - Information: carbon stock of the tree according to the MADA I.1 allometric equation
  - Type: Numeric
  - Unit: Kg per tree
- MADA II.1 V
  - Information: carbon stock of the tree according to the MADA II.1 V allometric equation
  - Type: Numeric
  - Unit: Kg per tree
- Chave_2014
  - Information: carbon stock of the tree according to the CHAVE 2014 allometric equation
  - Type: Numeric
  - Unit: Kg per tree
- Field and materials ressources
  - Indicates data collection support (e.g., botanist)

## Provenance, context, and usage notes
- The dataset pertains to inventory data used to estimate tree carbon stocks, with multiple allometric models provided to compute carbon per tree.
- References and model basis:
  - CHAVE 2005: Tree allometry and improved estimation of carbon stocks and balance in tropical forests
  - CHAVE 2014: Improved allometric models to estimate aboveground biomass of tropical trees
- Data collection is linked to fieldwork practices described in the referenced manuals.
- Acknowledgement requirement implies attribution is necessary for downstream use.

## Data quality and governance considerations
- Metadata quality: The header provides variable types, units, and descriptive information for each field, aiding standardization.
- Completeness: Blank cells indicate missing data; users should account for incomplete records when analyzing carbon stock.
- Consistency: Several allometric equations are included, allowing cross-checks and model comparisons, but require clear documentation of which model was applied per record.
- Standards and interoperability: Variables include standard fields (site, subplot, area, tree metrics, wood density, and carbon stock estimates) to facilitate integration with other datasets.
- Update and maintenance: The dataset description notes the potential for updates and the importance of syncing with portals/catalogs; ongoing governance should ensure versions are tracked and changes documented.
- Data sharing constraints: Product-derived outputs require acknowledgment of the Laboratoire des Radio Isotopes, Université d’Antananarivo.

## Implications for data stewards and users
- Ensure all data creators provide complete metadata (especially for missing values) and consistent units across records.
- Document which allometric model was used for each tree’s carbon stock to enable reproducibility and model comparison.
- Facilitate data publication in appropriate portals and catalogues, including clear provenance and acknowledgments.
- Maintain linkage to original sources (CHAVE 2005, CHAVE 2014) for methodological transparency.
- Provide guidance on interpreting subplots and area measurements, given the categorical subplot sizes and numeric area values.