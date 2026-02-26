# Basin - Supporting Information

- This document documents the study area, data generation methods, value units, quality control, and data structure for Land use products under four scenarios in 2030 in the Luanhe River Basin (LRB). It is part of a UKRI/NERC TaSE project on river basins as living laboratories for sustainable development.

## 1. Study Area
- Luanhe River Basin (LRB) area: ~45,000 km2 in semi-arid North China.
- Location: 39°10′–42°30′ N, 115°30′–119°15′ E; temperate continental monsoonal climate.
- Climate: 1982–2015 average 7.0 ± 2.6 °C; precipitation 488.4 ± 80.7 mm; summer is the wettest (~200–550 mm; 66–76% of annual rainfall).
- Land system gradient: upper reaches grassland; middle-lower reaches temperate forests; eastern plains croplands and urban areas.
- Population: ~5.4 million; density ~122 people/km2.

## 2. CLUMondo framework
- Three-step workflow:
  - Map land systems for 2000 and 2015 by integrating multiple human–environment datasets.
  - Relate land systems to local explanatory factors for the initial year (2000); parameterise and calibrate CLUMondo using the 2015 land systems map.
  - Simulate land-system changes from 2015 to 2030 under four scenarios representing different commodity/service demands and management pathways.
- Process overview illustrated in the study (Fig. 2).

## 3. Land system classification
- Based on three main factors:
  - Land use/cover
  - Livestock
  - Agricultural intensity
- Data source: China National Land Use and Cover Change (CNLUCC) dataset from RESDC; six land-use/land-cover categories: farmland, forestland, grassland, water, urban land, unused land.
- Classification approach:
  - Thresholds determined by natural breaks in variable distributions.
  - Explanatory and auxiliary factors include climate (mean temperature, precipitation, ≥10°C, accumulated temperature, moisture index), topography (altitude, slope, landforms, sand/silt content), soils (clay content, organic matter, pH, drainage, soil type), and socioeconomic factors (accessibility, population density, GDP, market influence).
  - Data sources for factors span RESDC, NASA SRTM, and HWSD; units include various percent, temperature (°C), and other indices.
- Data products and provenance are detailed in Table 1.

## 4. Scenarios formulation
- Four scenarios to explore future land-system trajectories: Trend, Expansion, Sustainability, and Conservation.
- Scenario design reflects different socio-economic development paths, environmental targets, local plans, policies, and stakeholder input.
- Parameters:
  - Table 2 provides average annual percentage change (2015–2030) for:
    - Crop production (ton): Trend 2.1%; Expansion 1.5%; Sustainability 1%; Conservation 1%.
    - Livestock numbers (head): Trend 2.7%; Expansion 3.9%; Sustainability 0.9%; Conservation 0.9%.
    - Built-up land (km2): Trend 9.6%; Expansion 1.9%; Sustainability 0.7%; Conservation 0.7%.
    - Forest (km2): Trend/Expansion/Sustainability unspecified; Conservation 0.4%.
  - Some values are “n/a” where not specified and allocated by the model.

## 5. Nature and units of recorded values
- Raster land-use maps with nine classes representing the landscape.
- Spatial resolution: 1 km cells.
- File format: GeoTIFF rasters.

## 6. Quality control
- Validation approach: calibrate 2000–2015 CLUMondo results against the actual 2015 land-use map.
- Metrics:
  - Kappa simulation: overall 0.86 (high agreement).
  - Kappa transition: overall ~1.00-0.99 (strong agreement on the quantity of transitions).
  - Kappa transition location: overall ~0.87 (strong spatial allocation accuracy).
- Per-class results (examples):
  - High accuracy for forest, grassland, water, and cropland transitions.
  - Built-up and unused land show comparatively lower but acceptable accuracy.
- These metrics indicate strong model performance and applicability for predicting 2030 scenarios.

## 7. Data structure
- Four land-use maps for 2030 corresponding to each scenario:
  - Trend_2030.tif
  - Expansion_2030.tif
  - Sustainability_2030.tif
  - Conservation_2030.tif
- Coverage: entire LRB; format: raster GeoTIFF.
- Coordinate system:
  - Geographic: GCS_Krasovsky_1940
  - Projected: Krasovsky_1940_Albers
- Nine land-use classes (values 0–8):
  - 0: Extensive cropland
  - 1: Medium intensive cropland
  - 2: Intensive cropland
  - 3: Forest
  - 4: Grassland with low livestock
  - 5: Grassland with high livestock
  - 6: Water
  - 7: Built-up area
  - 8: Unused land
- The class-to-value mapping is detailed in Table 3.

## 8. References
- Key data sources and validation studies include:
  - RESDC data portal and CNLUCC dataset (Liu et al., Xu et al., 2018)
  - CLUMondo methodology and validation studies (Van Asselen and Verburg; Jin et al.; Liu et al.)
  - Supplementary climate and soil references (Wu et al. 2020; Zhang et al. 2019; others)