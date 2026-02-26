# DATA HEADER information for Tree_carbon_stock.csv

## Overview
- The dataset records carbon stock for a big tree cluster as part of ESPA (Project P4GES) activities.
- Data provenance includes acknowledgement requirements for products derived from these data (Laboratoire des Radio Isotopes, Université d'Antananarivo).
- Related reference materials and manuals are noted (Manual 1_Classical_Survey).

## Key variables and data types
- Site_ID: code of the site where the inventory was conducted; Information = Text String; Unit = .
- Subplot: relative size/category of the inventory circle (5m–10m Small, 10m–20m Medium, etc.); Variable type = Categorical; Unit = L/M/S.
- Area: area of the inventory circle; Numeric; Unit = m².
- Trees-local_name: vernacular name of the tree; Text String.
- Trees_Scientific_name: scientific name of the tree; Text String.
- Trees_Genera: genera of the tree; Text String.
- Trees_Family: family of the tree; Text String.
- Trees_DBH: Diameter at Breast Height (1.3 m); Numeric; Unit = cm.
- Trees_height: height of the tree; Numeric; Unit = meter.
- WSG: Wood Specific Gravity of the wood species; Numeric; Unit = Unitless.
- CHAVE 2005: carbon stock of the tree according to the CHAVE 2005 allometric equation; Numeric; Unit = Kg per tree.
- MADA I.1: carbon stock according to the MADA I.1 allometric equation; Numeric; Unit = Kg per tree.
- MADA II.1 V: carbon stock according to the MADA II.1 V allometric equation; Numeric; Unit = Kg per tree.
- Chave_2014: carbon stock according to the CHAVE 2014 allometric equation; Numeric; Unit = Kg per tree.
- Notes: blank cells indicate no data available.

## Allometric models used
- CHAVE 2005: allometric model for estimating aboveground carbon stocks in tropical trees.
- CHAVE 2014: updated allometric models for tropical tree aboveground biomass.
- MADA I.1: allometric approach variant for carbon stock estimation.
- MADA II.1 V: another allometric variant for carbon stock estimation.
- Each model yields carbon stock values in kilograms per tree (Kg per tree).

## Data provenance, quality, and usage notes
- Data are associated with a specific inventory methodology (Classical Survey) and linked to a manual (Manual 1_Classical_Survey).
- Blank cells signify missing data, which can affect cross-model comparisons or aggregation.
- Field and materials resources indicate contributors (e.g., botanist) and indicate the provenance of taxonomic information.
- The dataset includes multiple units and requires careful alignment of inputs (e.g., DBH, WSG) for model calculations.
- Metadata management practices include tracking data sources and making datasets discoverable with metadata.

## References
- CHAVE 2005. Tree allometry and improved estimation of carbon stocks and balance in tropical forests. Oecologia, 145:87-99. DOI: 10.1007/s00442-005-0100-x
- Chave 2014. Improved allometric models to estimate the aboveground biomass of tropical trees. Global Change Biology, 20(10):3177-3190. DOI: 10.1111/gcb.12629

## Additional notes for analysts
- Use Site_ID, Subplot, and Area to contextualize carbon stock at the spatial scale of the inventory (circle area and subplot size).
- Leverage Trees_DBH and Trees_height along with WSG to compute or validate CHAVE 2005/2014 or MADA model estimates.
- Compare carbon stock outputs across models (CHAVE 2005 vs CHAVE 2014 vs MADA variants) to assess model sensitivity.
- Be mindful of missing data (blanks) when aggregating at site, subplot, or tree level.
- Ensure proper data provenance and acknowledgments are maintained when using or publishing derived results.