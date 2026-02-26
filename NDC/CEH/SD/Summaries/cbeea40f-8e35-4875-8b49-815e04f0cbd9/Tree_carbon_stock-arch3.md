# DATA HEADER information for Tree_carbon_stock.csv

## Overview
- Dataset records the carbon stock of a big tree cluster.
- Associated with ESPA Programme and P4GES Project.
- Requires acknowledgement of Laboratoire des Radio Isotopes, Université d'Antananarivo for products derived from data.
- Data notes indicate blank cells mean no data available.

## Dataset contents and purpose
- Captures tree-level and plot-level information to support environmental health monitoring and policy evaluation.
- Key aim: provide carbon stock estimates for informed decision-making and future monitoring.
- Includes both field inventory data and modeled carbon stock estimates.

## Data fields, units, and structure
- Site_ID: code of the inventory site.
- Subplot: information about the circular inventory subplot (size categories: Small, Medium, Large); unit: categorical; variable type: text.
- Area: area of the inventory circle; unit: m²; variable type: Numeric.
- Trees_local_name: vernacular tree name; variable type: Text.
- Trees_Scientific_name: scientific name; variable type: Text.
- Trees_Genera and Trees_Family: taxonomic classification; variable types: Text.
- Trees_DBH: Diameter at Breast Height; unit: cm; variable type: Numeric.
- Trees_height: tree height; unit: meter; variable type: Numeric.
- WSG: Wood Specific Gravity; unit: unitless; variable type: Numeric.
- CHAVE 2005: carbon stock per tree using CHAVE 2005 allometric equation; unit: Kg per tree; variable type: Numeric.
- MADA I.1: carbon stock per tree using MADA I.1 allometric equation; unit: Kg per tree; variable type: Numeric.
- MADA II.1 V: carbon stock per tree using MADA II.1 V allometric equation; unit: Kg per tree; variable type: Numeric.
- Chave_2014: carbon stock per tree using CHAVE 2014 allometric equation; unit: Kg per tree; variable type: Numeric.
- Field and materials resources: various contributors (e.g., botanist, forester compass); metadata notes accompany each field.

## Allometric models and carbon stock estimates
- Carbon stock per tree calculated using multiple allometric models:
  - CHAVE 2005
  - CHAVE 2014
  - MADA I.1
  - MADA II.1 V
- Enables cross-model comparison and robustness checks of carbon stock estimates.

## Data provenance and references
- References for models:
  - CHAVE 2005: Tree allometry and improved estimation of carbon stocks and balance in tropical forests. Oecologia, 145:87-99. DOI: 10.1007/s00442-005-0100-x
  - Chave 2014: Improved allometric models to estimate aboveground biomass of tropical trees. Global Change Biology, 20(10):3177-3190. DOI: 10.1111/gcb.12629
- Data linked to DOIs and project pages (ESPA and P4GES).
- Information fields and units are documented to facilitate data reuse and comparability.

## Data governance, sharing, and metadata considerations
- Emphasizes need for good metadata quality; some metadata gaps may require contacting data originators.
- Public sharing of underlying data is a consideration and can be a barrier depending on governance.
- Data provenance, quality assurance, and documentation are essential for verifying suitability for monitoring purposes.
- Acknowledgement and data-use requirements must be observed.

## Practical implications for monitoring frameworks
- Provides standardized, model-based carbon stock estimates at the tree and plot levels, useful for policy evaluation and trend analysis.
- Facilitates data integration with other environmental indicators through consistent units and allometric models.
- Highlights importance of metadata completeness, data access, and governance to enable timely and transparent decision-making.

## Notes
- Blank cells indicate no data available.