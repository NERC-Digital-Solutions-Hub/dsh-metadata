# Basin - Supporting Information

- Study Area
  - Luanhe River Basin (LRB), ~45,000 km2 in North China (39°10′–42°30′ N, 115°30′–119°15′ E)
  - Semi-arid, temperate continental monsoonal climate; 1982–2015 mean temp 7.0 ± 2.6°C, precipitation 488.4 ± 80.7 mm
  - Summer dominates rainfall (200–550 mm, ~66–76% of annual)
  - Land cover: upper reaches grassland; middle–lower reaches temperate forest; eastern plains croplands and urban areas
  - Population ~5.4 million; density ~122 people/km2

- CLUMondo framework
  - Built map of land systems for 2000 and 2015 by integrating human–environment datasets
  - Relationship between land systems and local explanatory factors calculated for 2000
  - CLUMondo model parameterized/calibrated using 2015 land systems map
  - 2015–2030 changes simulated under four scenarios (varying commodity/service demands) to explore land-resource management pathways
  - Workflow illustrated in Figure 2 (not shown)

- Land system classification
  - Based on three factors: land use/cover, livestock, and agricultural intensity
  - Uses China National Land Use and Cover Change (CNLUCC) dataset with six land use/cover categories
  - Classification accuracy validated; ~94.3% in selected polygons
  - Data sources and variables include:
    - Delineate Land systems: land use/cover, potential cropland, livestock density
    - Explanatory factors: climate (temp, precipitation, moisture index, etc.), altitude, slope, soil characteristics (clay, organic content, pH, drainage, soil type), market influence
    - Socioeconomic factors: accessibility, population density, GDP
  - Table 1 lists data used; Table 3 defines land use classes and raster values

- Scenarios formulation
  - Four scenarios: Trend, Expansion, Sustainability, Conservation
  - Driven by different socio-economic development targets, local plans/policies, and stakeholder input
  - Table 2 provides average annual changes 2015–2030 for:
    - Crop production (ton): Trend 2.1%, Expansion 1.5%, Sustainability 1%, Conservation 1%
    - Livestock numbers (head): Trend 2.7%, Expansion 3.9%, Sustainability 0.9%, Conservation 0.9%
    - Built-up land (km2): Trend 9.6%, Expansion 1.9%, Sustainability 0.7%, Conservation 0.7%
    - Forest (km2): Trend/Expansion/Sustainability n/a; Conservation 0.4%
  - Some demand values not specified in the scenario (n/a) and allocated by the CLUMondo model

- Nature and units of recorded values
  - Raster land use map with nine classes
  - Spatial resolution: 1 km
  - Extent: LRB

- Quality control
  - Validation of 2000–2015 simulations against actual 2015 land systems
  - Metrics: Kappa simulation, Kappa transition, Kappa transition location
  - Overall results indicate high accuracy: Kappa simulation = 0.86; Kappa transition location = 0.87; per-class values show strong agreement (many >0.9)
  - Interpretation: CLUMondo provides robust simulations for LRB land-use changes

- Data structure
  - Four 2030 land-use maps corresponding to scenarios:
    - Trend_2030.tif, Expansion_2030.tif, Sustainability_2030.tif, Conservation_2030.tif
  - Extent: LRB; Raster format: GeoTIFF
  - Coordinate systems: GCS Krasovsky 1940; projected Krasovsky 1940 Albers
  - Nine classes and their raster values:
    - 0: Extensive cropland
    - 1: Medium intensive cropland
    - 2: Intensive cropland
    - 3: Forest
    - 4: Grassland with low livestock
    - 5: Grassland with high livestock
    - 6: Water
    - 7: Built-up area
    - 8: Unused land

- References
  - Key sources on climate, land use data, and methodology (e.g., CNLUCC, CLUMondo calibration, and regional studies) used to construct the dataset and validation