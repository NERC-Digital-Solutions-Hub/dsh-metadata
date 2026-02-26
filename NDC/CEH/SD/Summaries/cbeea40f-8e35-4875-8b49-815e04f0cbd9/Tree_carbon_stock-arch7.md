# DATA HEADER information for Tree_carbon_stock.csv

- Purpose and scope
  - Records the carbon stock of big tree clusters.
  - Associated with the ESPA programme and P4GES project.
  - Aims to support map-based data products and GIS analyses of tree carbon stocks.
  - See also Manual 1_Classical_Survey for additional guidance.

- Provenance, access, and acknowledgments
  - DOI: https://doi.org/10.5285/cbeea40f-8e35-4875-8b49-815e04f0cbd9
  - Programme: ESPA; Project: P4GES
  - Acknowledgement required for products derived from these data: Labouratoire des Radio Isotopes, Université d'Antananarivo

- GIS-relevant dataset structure
  - Site_ID: inventory site code; Type: Text String
  - Subplot: relative circle size used for inventory (Small/Medium/Large); Type: Categorical; Unit: L: Large / M: Medium / S: Small
  - Area: area of the inventory circle; Type: Numeric; Unit: m²
  - Trees-local_name: vernacular tree name; Type: Text String
  - Trees_Scientific_name: scientific name; Type: Text String
  - Trees_Genera: genus; Type: Text String
  - Trees_Family: family; Type: Text String
  - Trees_DBH: Diameter at Breast Height (1.3 m); Type: Numeric; Unit: cm
  - Trees_height: tree height; Type: Numeric; Unit: meter
  - WSG: Wood Specific Gravity; Type: Numeric; Unit: unitless
  - CHAVE 2005: carbon stock per tree using CHAVE 2005 allometric equation; Type: Numeric; Unit: Kg per tree
  - MADA I.1: carbon stock per tree using MADA I.1 allometric equation; Type: Numeric; Unit: Kg per tree
  - MADA II.1 V: carbon stock per tree using MADA II.1 V allometric equation; Type: Numeric; Unit: Kg per tree
  - Chave_2014: carbon stock per tree using CHAVE 2014 allometric equation; Type: Numeric; Unit: Kg per tree
  - Field and materials resources: blank cells indicate no data available

- Data quality and interpretation notes
  - Blank cells = no data available
  - The dataset combines measurements (DBH, height, etc.) with multiple allometric models (CHAVE 2005, MADA I.1, MADA II.1 V, CHAVE 2014) to estimate tree-level carbon stock

- Allometric models and outputs
  - CHAVE 2005: carbon stock per tree (kg)
  - CHAVE 2014: carbon stock per tree (kg)
  - MADA I.1: carbon stock per tree (kg)
  - MADA II.1 V: carbon stock per tree (kg)

- References for models
  - CHAVE 2005: Tree allometry and improved estimation of carbon stocks and balance in tropical forests; Oecologia, 145:87-99. DOI: 10.1007/s00442-005-0100-x
  - CHAVE 2014: Improved allometric models to estimate the aboveground biomass of tropical trees; Global Change Biology, 20(10):3177-3190. DOI: 10.1111/gcb.12629

- Use-case considerations for GIS specialists
  - The dataset is designed to support map-based visualization of tree carbon stocks by inventory area, with per-tree measurements and multiple allometric estimates.
  - Enables spatial aggregation (per site or subplot area) and comparison across allometric methods.
  - Suitable for joining to polygonal/site-level GIS layers using Site_ID and Subplot/Area attributes.