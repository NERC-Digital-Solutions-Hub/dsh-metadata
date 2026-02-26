# DATA HEADER information for Tree_carbon_stock.csv

## Overview
- Dataset records the carbon stock of the big tree cluster.
- Related to ESPA programme and P4GES project.
- DOI: https://doi.org/10.5285/cbeea40f-8e35-4875-8b49-815e04f0cbd9
- Acknowledgement required for products derived from these data: Laboratoire des Radio Isotopes, Université d'Antananarivo.

## Data structure and fields
- Site_ID: code of the site where the inventory was conducted (Text String).
- Subplot: relative size of the circle in which the inventory was conducted (Categorical: Small, Medium, Large; values S, M, L).
- Area: area of the inventory circle (Numeric, m²).
- Trees-local_name: vernacular name of the tree (Text String).
- Trees_Scientific_name: scientific name of the tree (Text String).
- Trees_Genera: genus of the tree (Text String).
- Trees_Family: family of the tree (Text String).
- Trees_DBH: Diameter at Breast Height (1.3 m) (Numeric, cm).
- Trees_height: height of the tree (Numeric, m).
- WSG: Wood Specific Gravity of the wood species (Numeric, unitless).
- CHAVE 2005: carbon stock of the tree according to the CHAVE 2005 allometric equation (Numeric, Kg per tree).
- MADA I.1: carbon stock of the tree according to the MADA I.1 allometric equation (Numeric, Kg per tree).
- MADA II.1 V: carbon stock of the tree according to the MADA II.1 V allometric equation (Numeric, Kg per tree).
- Chave_2014: carbon stock of the tree according to the CHAVE 2014 allometric equation (Numeric, Kg per tree).

- Information, Variable type, Unit, and Field and materials ressources accompany each field as noted in the dataset header (mostly textual descriptors; some fields have no specific units).

## Provenance and access
- Data linked to a specific inventory methodology and allometric models (CHAVE 2005, CHAVE 2014, MADA I.1, MADA II.1 V) for estimating aboveground carbon stocks.
- References provided for the allometric models used.

## Methods for carbon stock estimation
- Carbon stock per tree estimated using multiple allometric equations:
  - CHAVE 2005
  - CHAVE 2014
  - MADA I.1
  - MADA II.1 V

## Notes on data quality and completeness
- Notes: blank cells mean no data available.

## References
- CHAVE 2005: Tree allometry and improved estimation of carbon stocks and balance in tropical forests. Oecologia, 145:87-99. DOI: 10.1007/s00442-005-0100-x
- Chave_2014: Improved allometric models to estimate the aboveground biomass of tropical trees. Global Change Biology, 20(10):3177-3190. DOI: 10.1111/gcb.12629