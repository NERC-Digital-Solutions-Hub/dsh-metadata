# Basin - Supporting Information

## Purpose and scope
- Describes the study area, generation methods, nature and units of recorded values, quality control, and data structure for land use products under four 2030 scenarios in the Luanhe River Basin (LRB).
- Acknowledges UKRI/NERC TaSE funding for the dataset.

## Study Area
- Luanhe River Basin (LRB): ~45,000 km2 in semi-arid North China (39°10′–42°30′ N, 115°30′–119°15′ E).
- Climate: temperate continental monsoon, semi-arid; 1982–2015 average temp 7.0 ± 2.6°C, precipitation 488.4 ± 80.7 mm; heavy summer rainfall (≈66–76% of annual).
- Land cover gradient: upper region grassland; middle-lower region temperate forest; eastern plains cropland and urban areas.
- Population: ~5.4 million (density ~122 people/km2).

## Methods: CLUMondo framework
- Three-step workflow:
  1) Map land systems for 2000 and 2015 by integrating human–environment datasets.
  2) Derive relationships between land systems and local explanatory factors for 2000; parameterize and calibrate CLUMondo with 2015 map.
  3) Simulate 2015–2030 land system changes under four scenario pathways representing different commodity/service demands.
- Workflow illustrated in Fig. 2.

## Land system classification
- Based on three factors: land use/cover, livestock density, and agricultural intensity.
- Uses China National Land Use and Cover Change (CNLUCC) dataset with six classes: farmland, forestland, grassland, water, urban land, unused land.
- Thresholds determined by natural breaks in data distributions.
- Classification accuracy validated: ~94.3%+ in selected polygons; nationwide county sampling for validation.

## Data inputs and explanatory factors
- Data sources and variables used for delineating land systems and explanatory factors include:
  - Land use: CNLUCC (RESDC)
  - Livestock: Global Livestock data (Robinson et al., 2014)
  - Climatic: mean annual temperature, precipitation, accumulated temperature, moisture index (RESDC)
  - Geographic/Soil: altitude, slope, landforms, sand/silt content, clay, organic content, pH, drainage, soil type (HWSD v1.2; RESDC)
  - Socioeconomic: accessibility, population density, GDP (Verburg et al. 2011; RESDC)
  - Local plans: land greening and afforestation plans (Hebei Province, State Forestry Administration)
- Explanatory factors are organized by category (climatic, soil, socioeconomic, etc.) and units vary by factor.

## Scenarios formulation
- Four scenarios to explore land system evolution and challenges: Trend, Expansion, Sustainability, and Conservation.
- Scenarios reflect different socio-economic development, environmental targets, local policies, and stakeholder input.
- Table 2 (described) provides average annual changes from 2015 to 2030 for:
  - Crop production (ton): Trend 2.1%, Expansion 1.5%, Sustainability 1%, Conservation 1%
  - Livestock numbers (head): Trend 2.7%, Expansion 3.9%, Sustainability 0.9%, Conservation 0.9%
  - Built-up area (km2): Trend 9.6%, Expansion 1.9%, Sustainability 0.7%, Conservation 0.7%
  - Forest area (km2): Trend/Expansion/Sustainability/Conservation as specified (with some n/a)

## Nature and units of recorded values
- Raster representation of land use with nine classes recorded as attributes per cell.

## Quality control
- Validation of 2000–2015 simulations against actual 2015 land systems using:
  - Kappa simulation
  - Kappa transition
  - Kappa transition location
- Overall Kappa simulation: 0.86; Kappa transition: up to 0.99; Kappa transition location: up to 0.99 (overall across classes 0.94–0.99 for several classes; some categories like Built-up lower at 0.41 for simulation, 0.41 for location).
- Results indicate strong overall accuracy and robust spatial allocation accuracy for most land-use changes.

## Data structure
- Four 2030 land use maps corresponding to the four scenarios:
  - Trend_2030.tif
  - Expansion_2030.tif
  - Sustainability_2030.tif
  - Conservation_2030.tif
- Extent: LRB; format: GeoTIFF; coordinate systems: GCS Krasovsky 1940 and Krasovsky_1940_Albers.
- Pixel size: 1 km.
- Nine land use classes and raster values:
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
- Wu et al. 2020; Xu et al. 2018; Zhang et al. 2019 (and related data sources cited throughout).