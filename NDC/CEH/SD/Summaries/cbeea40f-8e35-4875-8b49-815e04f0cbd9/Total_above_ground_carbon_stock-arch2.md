# DATA HEADER INFORMATION for Total_above_ground_carbon_stock.csv

## Overview
- The dataset summarizes carbon stocks on each site and each subplot for the total above-ground biomass pool.
- Included components: trees (>5 cm DBH), saplings (>1.3 m height and <5 cm DBH), understorey, standing dead wood, lying dead wood, and litter.
- Related programme and project: ESPA program and P4GES project.
- DOI: https://doi.org/10.5285/cbeea40f-8e35-4875-8b49-815e04f0cbd9
- Acknowledgement required: Labouratoire des Radio Isotopes, Université d'Antananarivo for products derived from these data.
  
## Data structure and fields
- Site_ID: P4GES site code; Information = Site_ID; Site_ID type = Text; Site_ID Unit = (no specific unit)
- subplot: Subsample location; Information = subplot; Variable type = Categorical; Unit = S1 / S2 / S3 / S4

### Carbon stock variables (all numeric)
- tree_carbon_stock: Carbon stock of trees >5 cm DBH; Unit = Mg.ha-1 (milligrams per hectare); Variable type = Numeric
- saplings_carbon_stock: Carbon stock of saplings (>1.3 m height and DBH <5 cm); Unit = Mg.ha-1; Variable type = Numeric
- standing_dead_wood_carbon_stock: Carbon stock of standing dead wood; Unit = Mg.ha-1; Variable type = Numeric
- lying_dead_wood_carbon_stock: Carbon stock of lying dead wood; Unit = Mg.ha-1; Variable type = Numeric
- understorey_carbon_stock: Carbon stock of herbaceous biomass and small trees <1.3 m; Unit = Mg.ha-1; Variable type = Numeric
- litter_carbon_stock: Carbon stock of litter (leaf litter and root mat); Unit = Mg.ha-1; Variable type = Numeric

## Notes on data
- Notes field indicates missing data: "Notes - means no data available."