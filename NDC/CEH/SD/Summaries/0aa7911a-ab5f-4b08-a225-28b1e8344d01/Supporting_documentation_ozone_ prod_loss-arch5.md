# Modelled annual average production loss due to ozone damage for four global staple crops, 2010-2012.

## Overview
- Global estimation of production losses due to ozone damage for maize, rice, soybean, and wheat.
- Period: 2010–2012; outputs provided as four GIS shapefiles (one per crop) on a 1° by 1° grid.
- Dataset includes production loss in thousand tonnes per grid cell and is designed for broad accessibility and reuse by data stewards and researchers.

## Data collection and generation
- Crop production data sourced from FAO Global Agro-Ecological Zones (GAEZ) for the year 2000; converted to estimates for 2010–2012.
- Grid cell inclusion: only cells with >500 tonnes production considered; each cell labeled as irrigated or non-irrigated.
- Hemisphere classification (North/South) and climate zone assignment via ESDAC/JRC climate zone layer.
- 90-day growing periods defined per climate zone and hemisphere, used to align seasonal windows for modelling.
- Data processing steps documented for each crop to enable reproduction and auditing.

## Methodology and calculations
- Ozone exposure modelling: EMEP MSC-W chemical transport model (version 4.16) used to compute daily ozone flux (POD3 IAM) representing stomatal uptake above 3 nmol m−2 s−1.
- For each grid cell, compute 90-day POD3IAM based on climate- and hemisphere-specific growing periods; generate irrigated vs. rain-limited flux values accordingly.
- Yield loss calculation (common for all crops using wheat-based dose–response as reference):
  - Percent Yield Loss = (POD3IAM − 0.1) × 0.64
  - 0.1 mmol/m2 represents pre-industrial ozone uptake (reference value); 0.64 is the slope of the dose–response relationship.
- Relative ozone sensitivity: crop-specific sensitivity to ozone (via M7 7-hour mean ozone) relative to wheat is used to scale the wheat-based yield loss to maize, rice, and soybean.
  - Crop yield loss per grid cell = wheat-based yield loss × (crop M7 slope ÷ wheat slope)
- Production loss per crop per grid cell: ProductionLoss = CropProduction × (YieldLoss/100)
- Outputs: four separate shapefiles (one per crop) with 1° grid cells and a five-column attribute table.

## Quality control and validation
- Model validation described in Mills et al. 2018b; comparison of modelled vs observed ozone at Global Atmosphere Watch (GAW) sites shows strong correlation (r2 ≈ 0.88–0.93) for seasonal metrics (Dmax and M7) with low scatter.
- Stomatal uptake proxy validation: strong relationship (r2 = 0.63) between AET/PET and POD3IAM/M7, indicating reasonable estimation of stomatal conductance.
- Acknowledges caveats: no maize/rice/soybean flux–response data; approach relies on wheat flux with crop-specific sensitivity adjustments; caveats detailed in supplementary material of Mills et al. 2018a.

## Data structure and access
- Files: four GIS shapefiles (maize, rice, soybean, wheat); each contains 1° by 1° grid cells.
- Attributes (per grid cell): 
  - ID: unique identifier
  - Zone: climate zone
  - Long_Lat: center coordinates (decimal degrees)
  - Hemisphere: Northern, Southern, or Far South (for wheat/maize in Cool temperate)
  - ProdLoss: annual average production loss (thousand tonnes) for 2010–2012
- Only cells with production >500 tonnes are included; Far South classification applies to specific wheat/maize climates.
- Data sources and code references provided, including EMEP model documentation and Mills et al. papers, enabling replication and audit trails.
- Miscellaneous metadata: EMEP MSC-W model version 4.16; crop production and climate zone data sources cited (FAO GAEZ, ESDAC/JRC); model validation details in cited literature.

## Limitations, caveats, and governance considerations
- Species-specific ozone flux relationships are unavailable for maize, rice, and soybean; estimates rely on wheat flux with crop-specific sensitivity scaling.
- Maize data rely on limited varietal data (three older varieties), introducing higher uncertainty for that crop.
- Some regions have multiple growing seasons; only the primary growing period per climate/hemisphere is used.
- Interoperability considerations: data distributed as shapefiles; users should consult the supplementary information for detailed methodological caveats and potential updates.

## References and data sources
- Mills, G. et al. (2018a). Closing the global ozone yield gap: quantification and co-benefits for multi-stress tolerance. Global Change Biology.
- Mills, G. et al. (2018b). Ozone pollution will compromise efforts to increase global wheat production. Global Change Biology.
- CLRTAP 2017. Modelling and Mapping Manual.
- EMEP MSC-W model documentation and updates (Simpson et al. 2012; Simpson et al. 2019).
- FAO GAEZ dataset; European Soil Data Centre (ESDAC) climate zone raster; Global Atmosphere Watch (GAW) ozone data.