# Basin - Supporting Information

## 1. Study Area
- Luanhe River Basin (LRB): ~45,000 km2 in semi-arid North China (39°10′–42°30′ N, 115°30′–119°15′ E)
- Climate: temperate continental monsoonal, semi-arid; mean 7.0 ± 2.6 °C; precipitation 488.4 ± 80.7 mm (1982–2015)
- Seasonal rainfall: heavy in summer (≈200–550 mm; 66–76% of annual)
- Land use distribution: upper reaches grassland; middle-lower reaches temperate forest; eastern plains cropland and urban areas
- Population: ~5.4 million; density ~122 people/km2

## 2. CLUMondo framework (methodology)
- Three-step workflow to generate 2030 land-use maps:
  1) Map land systems for 2000 and 2015 by integrating human–environment datasets
  2) Parameterise and calibrate CLUMondo model using the 2015 land systems map
  3) Simulate 2015–2030 changes under four scenarios (alternative commodity/service demands)
- Model workflow visually summarized in Fig. 2
- Classification and drivers:
  - Land system factors: land use/cover, livestock density, agricultural intensity
  - Explanatory factors: climate (Temp, Precipitation, Growing-period metrics), altitude, slope, landforms, soil characteristics, market/accessibility, population density, GDP
  - Data sources: RESDC CNLUCC (China), Global Distribution of Livestock, NASA SRTM, HWSD v1.2, Verburg et al. socioeconomics

## 3. Land system classification
- Based on three main categories: land use/cover, livestock, and agricultural intensity
- Data inputs: China National Land Use and Cover Change (CNLUCC) dataset
- Land-use classes used for delineation (nine classes in total; table of inputs and thresholds derived from data distribution)

## 4. Scenarios formulation
- Four scenarios to explore future trajectories: Trend, Expansion, Sustainability, Conservation
- Scenarios reflect different socio-economic development targets, environmental goals, local plans
- Parameterised by average annual demand changes (2015–2030) for:
  - Crop production (ton/yr): Trend 2.1%, Expansion 1.5%, Sustainability 1%, Conservation 1%
  - Livestock numbers (head/yr): Trend 2.7%, Expansion 3.9%, Sustainability 0.9%, Conservation 0.9%
  - Built-up land (km2/yr): Trend 9.6%, Expansion 1.9%, Sustainability 0.7%, Conservation 0.7%
  - Forest area (km2/yr): Trend/Expansion/Sustainability/Conservation vary (Conservation 0.4%)
- Average changes are detailed in Table 2

## 5. Nature and units of recorded values
- Raster land use maps with nine classes
- Spatial extent: LRB
- Data format: raster (GeoTIFF)
- Resolution: 1 km
- Coordinate systems: GCS Krasovsky 1940; projected Krasovsky 1940 Albers

## 6. Quality control
- Validation against actual 2015 land systems
- Metrics reported:
  - Kappa simulation (overall): 0.86
  - Kappa transition (overall): 0.99
  - Kappa transition location (overall): 0.87
- Class-specific Kappa values indicate strong accuracy for most classes (e.g., Forest, Grasslands, Water, Built-up) with some lower accuracy for Built-up in certain metrics

## 7. Data structure
- Four 2030 land-use rasters (GeoTIFF):
  - Trend_2030.tif
  - Expansion_2030.tif
  - Sustainability_2030.tif
  - Conservation_2030.tif
- Extent: LRB
- Raster values encode nine land-use classes:
  - 0: Extensive cropland
  - 1: Medium intensive cropland
  - 2: Intensive cropland
  - 3: Forest
  - 4: Grassland with low livestock
  - 5: Grassland with high livestock
  - 6: Water
  - 7: Built-up area
  - 8: Unused land

## 8. Data sources and references
- Land-use inputs: CNLUCC (China National Land Use and Cover Change)
- Livestock distribution: Global Distribution of Livestock
- Climate/topography/ soils: RESDC datasets, HWSD v1.2, NASA SRTM
- Socioeconomics and scenario parameters informed by regional plans and stakeholder input
- Related methodological references: CLUMondo framework development and validation studies