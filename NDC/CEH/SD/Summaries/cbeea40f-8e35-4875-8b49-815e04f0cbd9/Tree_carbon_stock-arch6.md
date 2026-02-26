# DATA HEADER information for Tree_carbon_stock.csv

## Overview
- The dataset records the carbon stock of the big tree cluster, with per-tree measurements and calculated carbon stock using multiple allometric equations.
- Associated project and program: ESPA (Programme) and P4GES (Project).
- Includes guidance that acknowledgement of the Laboratoire des Radio Isotopes, Université d'Antananarivo is required for products derived from these data.
- References to additional manuals: Manual 1_Classical_Survey.

## Data provenance and access
- DOI for the dataset: https://doi.org/10.5285/cbeea40f-8e35-4875-8b49-815e04f0cbd9
- Source programmes: ESPA http://www.espa.ac.uk/; Project P4GES https://www.p4ges.org
- Acknowledgement requirement: Laboratoire des Radio Isotopes, Université d'Antananarivo.

## Variables and structure
- Site_ID
  - Information: code of the site where the inventory was conducted
  - Type: Text String
  - Unit: .
- Subplot
  - Information: Relative size of the circle inside which the inventory was conducted
  - Type: Categorical
  - Unit: L (Large) / M (Medium) / S (Small)
  - Notes: Subplot information includes size categories with radii (5m–10m for Small, 10m–20m for Medium, 20m+ for Large)
- Area
  - Information: area of the inventory circle
  - Type: Numeric
  - Unit: m²
- Trees-local_name
  - Information: vernacular name of the tree
  - Type: Text String
  - Unit: .
- Trees_Scientific_name
  - Information: scientific name of the tree (if available)
  - Type: Text String
  - Unit: .
- Trees_Genera
  - Information: genera of the tree
  - Type: Text String
  - Unit: .
- Trees_Family
  - Information: family of the tree
  - Type: Text String
  - Unit: .
- Trees_DBH
  - Information: Diameter at Breast Height (1.3 m)
  - Type: Numeric
  - Unit: Centimeter
- Trees_height
  - Information: height of the tree
  - Type: Numeric
  - Unit: meter
- WSG (Wood Specific Gravity)
  - Information: wood density for the species
  - Type: Numeric
  - Unit: Unitless
- CHAVE 2005
  - Information: carbon stock of the tree according to the CHAVE 2005 allometric equation
  - Type: Numeric
  - Unit: Kg per tree
- MADA I.1
  - Information: carbon stock according to the MADA I.1 allometric equation
  - Type: Numeric
  - Unit: Kg per tree
- MADA II.1 V
  - Information: carbon stock according to the MADA II.1 V allometric equation
  - Type: Numeric
  - Unit: Kg per tree
- Chave_2014
  - Information: carbon stock according to the CHAVE 2014 allometric equation
  - Type: Numeric
  - Unit: Kg per tree

## Data notes
- Notes: blank cells mean no data available.

## Allometric references for carbon stock
- CHAVE 2005: Tree allometry and improved estimation of carbon stocks and balance in tropical forests. Oecologia, 145: 87-99. DOI: 10.1007/s00442-005-0100-x
- Chave_2014: Improved allometric models to estimate the aboveground biomass of tropical trees. Global Change Biology, 20(10): 3177-3190. DOI: 10.1111/gcb.12629

## Usage considerations for data use and product development
- The dataset enables per-tree carbon stock calculations using multiple allometric models (CHAVE 2005, CHAVE 2014, MADA I.1, MADA II.1 V) for comparative analysis.
- Suitable for creating self-serve data products (e.g., dashboards, pivot tables) by site, subplot size, species group, area, and carbon stock per tree.
- Data can be aggregated at plot/site level to produce area-based carbon stock estimates and species- or family-level summaries.
- Missing data (blank cells) should be treated as not available; careful handling is needed for analyses requiring complete-case data.
- Proper attribution is required when using outputs derived from these data.

## References
- CHAVE 2005. Tree allometry and improved estimation of carbon stocks and balance in tropical forests. Oecologia. DOI: 10.1007/s00442-005-0100-x
- CHAVE 2014. Improved allometric models to estimate the aboveground biomass of tropical trees. Global Change Biology. DOI: 10.1111/gcb.12629