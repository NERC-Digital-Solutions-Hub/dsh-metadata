# Modelled annual average production loss due to ozone damage for four global staple crops, 2010-2012.

## Aim
- Present a methodology to estimate annual production losses for maize, rice, soybean, and wheat due to ozone exposure (2010–2012).
- Provide production-loss data on a global 1°×1° grid for monitoring and policy evaluation purposes.

## Data sources and collection
- Crop production data: FAO Global Agro-Ecological Zones (GAEZ) dataset (year 2000 baseline, 0.0833° resolution) used to derive 1°×1° grid production totals; irrigated vs. non-irrigated classification.
- Climate and growing periods: Global Climate Zone GIS layer from ESDAC/JRC; 90-day growing periods per climate zone and hemisphere (based on USDA/FAO data).
- Ozone and flux data: EMEP MSC-W chemical transport model (v4.16) providing daily ozone flux metrics (POD3 IAM) for irrigated and rain-limited conditions.
- Validation data: Global Atmosphere Watch (GAW) network observations for model performance; evapotranspiration data (AET/PET) as a proxy for stomatal conductance.

## Methods and calculations
- Ozone-impact metric: use POD3 IAM (phytotoxic ozone dose) as the uptake-based measure; convert to yield loss using a wheat-specific dose–response relationship.
- Yield-loss calculation for wheat: Percent Yield Loss = (POD3IAM − 0.1) × 0.64.
- Cross-crop adjustment: derive relative ozone sensitivity for maize, rice, and soybean by comparing their M7 (7-hour mean ozone) response slopes to that of wheat; final crop yield loss = wheat yield loss × relative sensitivity.
- Production loss per grid cell: Production Loss = Crop Production (from 2010–2012) × (Percent Yield Loss / 100).
- Outputs: four GIS shapefiles (one per crop), each at 1°×1° resolution with grid-cell attributes.

## Data structure and outputs
- Shapefiles: four, one per crop (maize, rice, soybean, wheat).
- Attributes per grid cell: ID, Zone (climate zone), Long_Lat (cell center coordinates), Hemisphere (N/S/Far South), ProdLoss (annual average production loss in thousand tonnes for 2010–2012).

## Quality control and validation
- Model validation against GAW site data shows good spatial/temporal alignment; r² values between 0.88 and 0.93 for Dmax and M7 comparisons in 2012.
- Stomatal-conductance proxy correlation (AET/PET vs. POD3IAM/M7) yields r² = 0.63, supporting reasonable estimation of stomatal uptake.
- Caveats acknowledged:
  - Lack of species-specific ozone-flux to yield relationships for maize, rice, and soybean; reliance on wheat-based dose–response with crop-specific sensitivity adjustment.
  - Limited maize data (only three older varieties); higher uncertainty for maize.
  - In multi-season climates (e.g., India), only the primary growing period was used.

## Monitoring framework implications
- Demonstrates an end-to-end monitoring workflow: data identification, grid-based integration, model-based exposure assessment, bias checks, and production-loss estimation.
- Emphasizes the importance of data provenance, model validation, and transparent transformation steps for policy-relevant indicators.
- Provides a replicable data product (GIS shapefiles) suitable for dashboards, reports, or governance processes.

## Data governance, openness, and metadata
- Data are generated from public datasets (GAEZ, FAO, USDA, GAW, CLRTAP-related methods) and produced as open GIS shapefiles.
- Metadata and methodological transparency are addressed through references to detailed methodology in Mills et al. 2018a and 2018b, including supplementary information and validation figures.
- Public sharing considerations acknowledged in the broader monitoring context (data-sharing barriers highlighted in the archetype overview), though explicit sharing policies for these outputs are not detailed in the document.