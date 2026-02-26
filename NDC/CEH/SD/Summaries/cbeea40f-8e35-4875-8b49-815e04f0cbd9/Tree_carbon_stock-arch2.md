# DATA HEADER information for Tree_carbon_stock.csv

## Purpose and context
- Records the carbon stock of a big tree cluster.
- Associated with the ESPA programme and the P4GES project.
- Requires acknowledgment of the Laboratoire des Radio Isotopes, Université d'Antananarivo for products derived from these data.
- Reference to Manual 1_Classical_Survey as part of data collection and handling.
- Data are intended for standardised environmental monitoring and comparisons over time.

## Data structure and fields
- Site_ID: code of the inventory site; Text String; used to identify location.
- Subplot: relative size category of the circle where the inventory was conducted (Small, Medium, Large) with radii 5m, 10m, 20m; Variable type = Categorical; Unit = L/M/S.
- Area: area of the inventory circle; Numeric; Unit = m².
- Trees-local_name: vernacular name of the tree; Text String.
- Trees_Scientific_name: scientific name of the tree (if available); Text String.
- Trees_Genera: genus of the tree; Text String.
- Trees_Family: family of the tree; Text String.
- Trees_DBH: Diameter at Breast Height (1.3 m); Numeric; Unit = cm.
- Trees_height: height of the tree; Numeric; Unit = meter.
- WSG: Wood Specific Gravity of the wood species; Numeric; Unit = Unitless.
- CHAVE 2005: carbon stock of the tree according to the CHAVE 2005 allometric equation; Numeric; Unit = Kg per tree.
- MADA I.1: carbon stock of the tree according to the MADA I.1 allometric equation; Numeric; Unit = Kg per tree.
- MADA II.1 V: carbon stock of the tree according to the MADA II.1 V allometric equation; Numeric; Unit = Kg per tree.
- Chave_2014: carbon stock of the tree according to the CHAVE 2014 allometric equation; Numeric; Unit = Kg per tree.
- Notes: blank cells indicate no data available.

## Allometric approaches and outputs
- Multiple allometric models are used to estimate carbon stock per tree:
  - CHAVE 2005
  - MADA I.1
  - MADA II.1 V
  - CHAVE 2014
- These allow cross-comparison of carbon stock estimates for the same trees.

## Data provenance and references
- CHAVE 2005: Tree allometry and improved estimation of carbon stocks and balance in tropical forests. Oecologia 145:87-99. DOI: 10.1007/s00442-005-0100-x
- Chave_2014: Improved allometric models to estimate the aboveground biomass of tropical trees. Global Change Biology 20(10):3177-3190. DOI: 10.1111/gcb.12629

## Data quality, handling, and storage
- Notes indicate that blank cells mean data are not available, emphasizing the need for data verification, quality assurance, cleaning, and transformation as part of the monitoring workflow.
- Standardised data handling aligned with environmental monitoring practices, including storage and portal uploads of created datasets.