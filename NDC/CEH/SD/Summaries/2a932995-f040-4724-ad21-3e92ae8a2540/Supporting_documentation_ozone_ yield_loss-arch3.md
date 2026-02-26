# Modelled annual average percentage yield loss due to ozone damage for four global staple crops, 2010-2012 version 2.

## Objective and Scope
- Models and maps annual average percentage yield loss due to ozone for maize, rice, soybean, and wheat.
- Timeframe: 2010–2012; version 2.
- Aimed at informing environmental health monitoring, policy scrutiny, and future decision-making.

## Methodology: Grid Creation and Data Sources
- Grid: 1° by 1° cells created in ArcMap (v10.3).
- Crop production data: FAO Global Agro-Ecological Zones (GAEZ) dataset (year 2000) with irrigated and non-irrigated classifications.
- Filtering: include grid cells with >500 tonnes production per crop.
- Classification: each cell labeled by hemisphere and climate zone using ESCDAC/JRC data.
- Growing periods: 90-day periods defined per climate zone/hemisphere using USDA/FAO references.

## Yield Loss Calculation
- Wheat baseline: POD3IAM (phytotoxic ozone dose above 3 nmol m-2 s-1) used with CLRTAP dose-response.
- Equation: Percent Yield Loss = (POD3IAM − 0.1) × 0.64.
  - 0.1 mmol/m2 represents pre-industrial/natural ozone uptake.
  - Slope 0.64 reflects the wheat dose-response.
- Other crops (maize, rice, soybean): lack species-specific flux-response data; use relative ozone sensitivity by comparing each crop’s M7 (7-hour mean ozone) response to wheat.
  - Final crop yield loss = wheat-based yield loss × crop’s relative sensitivity.
- Output: four 1°×1° GIS shapefiles (one per crop) with yield-loss values.

## Quality Control and Validation
- Model: EMEP MSC-W chemical transport model (v4.16) for POD3IAM.
- Validation: comparison against Global Atmosphere Watch (GAW) observations; good correlation for Dmax and M7 (r2 = 0.88–0.93).
- Stomatal uptake proxy: strong (r2 = 0.63) between actual evapotranspiration/potential evapotranspiration and POD3IAM/M7 ratio.
- Caveats: no crop-specific ozone flux–yield relationships for maize, rice, and soybean; uncertainties stronger for maize due to limited data; only the most important growing period per climate was used in multi-season climates.

## Data Structure and Accessibility
- Outputs: four GIS shapefiles (one per crop), 1°×1° grid.
- Attributes per grid cell: ID, Zone (climate), Long_Lat, Hemisphere, Yloss (annual average % yield loss for 2010–2012).
- Data governance and sharing: notes that publicly sharing underlying datasets can be a barrier; metadata completeness and data-management standards are emphasized, highlighting the need for clear data provenance and governance.

## Data Sources, Tools, and Documentation
- Modeling framework: EMEP MSC-W CT model; ArcMap 10.3 for grid construction.
- Crop and climate data: FAO GAEZ; ES DAC climate zone raster layer; USDA and FAO growing-period guidance.
- Supporting references: Mills et al. (2018a, 2018b) on ozone yield loss, CLRTAP dose-response methodology, and model validation; GAW network data for validation.
- Public references and data:
  - EMEP model descriptions and updates
  - CLRTAP modelling manual
  - FAO/GAEZ data and ES DAC climate zone layer

## Implications for Monitoring Frameworks
- Demonstrates integrating atmospheric chemistry models with agricultural yield response to produce spatially explicit health-relevant indicators.
- Highlights data governance needs: metadata completeness, data sharing barriers, and the importance of open data for monitoring.
- Emphasizes transparent handling of uncertainties, especially when species-specific flux data are unavailable.
- Suggests future improvements as species-specific ozone flux data become available and multiple growing seasons are better represented.