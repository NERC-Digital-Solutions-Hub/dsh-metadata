# Basin - Supporting Information

- Purpose and scope: Describes the study area, generation methods, nature and units of recorded values, quality control, and data structure for land use products under four scenarios in 2030 in the Luanhe River Basin (LRB). Funded by UKRI/NERC TaSE program.

## Study Area
- Luanhe River Basin (LRB): ~45,000 km² in semi-arid North China; temperate continental monsoonal climate; average 1982–2015 temp 7.0 ± 2.6°C and precipitation 488.4 ± 80.7 mm with strong summer concentration.
- Land cover gradient: upper reaches grassland; middle-lower reaches temperate forests; eastern plains more cropland and urban areas.
- Population: ~5.4 million; density ~122 people/km².

## CLUMondo framework
- Three-step approach:
  - Map land systems for 2000 and 2015 by integrating multiple human–environment datasets.
  - Parameterise and calibrate CLUMondo model using the 2015 land systems map.
  - Simulate land system changes from 2015 to 2030 under four scenarios representing different commodity/services demands and management pathways.
- Workflow illustrated in a referenced figure.

## Land System Classification
- Based on three main factors: land use/cover, livestock, and agricultural intensity.
- Data source: China National Land Use and Cover Change (CNLUCC) dataset with six land use categories (farmland, forestland, grassland, water, urban, unused).
- Classification approach: thresholds determined by natural breaks in variable distributions.
- Accuracy: CNLUCC validated with nationwide field checks; selected polygons >94.3% accuracy.

## Data Inputs and Explanatory Variables
- Land systems: delineated by land use, cropland production potential, and livestock density.
- Explanatory factors (climatic, geographic, soil, socioeconomic):
  - Climate: mean annual temperature, annual precipitation, accumulated temperature, moisture index.
  - Geography/Soils: altitude, slope, landforms, sand/silt content, soil clay content, organic content, pH, drainage, soil type.
  - Socioeconomic: accessibility, population density, GDP, market influence.
- Data sources include RESDC (Chinese Academy of Sciences), Global Livestock Distribution data, NASA SRTM, HYDROMAPS (HWSD v1.2), and literature (Verburg et al., 2011) and regional plans (Hebei province, State Forestry Administration).

## Scenarios Formulation
- Four scenarios: Trend, Expansion, Sustainability, Conservation.
- Purpose: Explore land system evolution trajectories and major future challenges under different development and environmental targets.
- Parameters: average annual changes in demand (2015–2030) for crops, livestock, built-up land, and forest, varying by scenario. Some values are not specified in the scenario formulation and are allocated by CLUMondo.

## Nature and Units of Recorded Values
- Output data are rasters representing land use maps with nine classes.

## Quality Control and Validation
- Validation approach: compare 2000–2015 simulated results with actual 2015 land system map.
- Accuracy metrics:
  - Kappa simulation (overall and by class) to measure agreement of simulated vs. actual transitions.
  - Kappa transition (overall and by class) for the quantity of transitions.
  - Kappa transition location (overall and by class) for spatial allocation accuracy.
- Results (LRB 2015 assessment): overall Kappa simulation = 0.86; Kappa transition ≈ 0.99; Kappa transition location ≈ 0.87–0.99 across classes, indicating strong agreement, especially in the spatial allocation and transition quantities. Overall Kappa values above 0.8 indicate good accuracy.

## Data Structure and Outputs
- Four 2030 land use maps produced per scenario: Trend_2030.tif, Expansion_2030.tif, Sustainability_2030.tif, Conservation_2030.tif.
- Coverage: entire LRB.
- File format: GeoTIFF raster.
- Coordinate systems: Geographic CRS Krasovsky 1940 (GCS_Krasovsky_1940) and projected Krasovsky_1940_Albers.
- Grid resolution: 1 km.
- Land use classes and raster values:
  - 0: Extensive cropland
  - 1: Medium intensive cropland
  - 2: Intensive cropland
  - 3: Forest
  - 4: Grassland with low livestock
  - 5: Grassland with high livestock
  - 6: Water
  - 7: Built-up area
  - 8: Unused land

## References
- Data sources and validation references for land use, climate, soils, and model performance are provided (e.g., Xu et al. 2018; Wu et al. 2020; Zhang et al. 2019; van Asselen & Verburg 2013; van Vliet et al. 2011).