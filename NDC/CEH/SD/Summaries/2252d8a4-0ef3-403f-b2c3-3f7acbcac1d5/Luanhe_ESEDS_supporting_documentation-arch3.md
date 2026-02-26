# Geodatabase of ecosystem types and their respective ecosystem services (ES) and disservices (EDS) in the Luanhe River Basin

## Purpose and scope
- Describes the study area, generation methods, nature and units of recorded values, quality control, and data structure for a geodatabase of ecosystem types (ET) and their ecosystem services (ES) and disservices (EDS) in the Luanhe River Basin (LRB).
- Supports assessment of environmental health measures to scrutinize and inform policy and future decisions.
- Funded by UKRI/NERC under the TaSE programme; project focuses on treating river basins as living laboratories for sustainable development goals.

## Study Area
- Luanhe River Basin (LRB): 39°10'–42°30' N, 115°30'–119°15' E; semiarid North China.
- Area around 45,775 km²; population ~5.4 million; density ~122 people/km².
- Coverage across 27 counties in Hebei, Liaoning, and Inner Mongolia Autonomous Region.
- Notable for afforestation (Three-North Shelter Forest Program since 1978), ecological barrier against sandstorms, and importance as a water resource for Beijing–Tianjin–Hebei (BTH) region.
- Land-use context includes cropland, forest, grassland, waterbodies, built-up areas, and unused land contributing ES/EDS.

## Generation Methods
- Land uses (ET) derived from China's National Land Use and Cover Change (CNLUCC) dataset at 30 m × 30 m resolution.
- Six major ETs defined (cropland, forest, grassland, waterbody, built-up land, unused land) with 14 subcategories.
- Based on Millennium Ecosystem Assessment (MA) and Common International Classification of Ecosystem Services (CICES) v5.1, 11 provisioning services (PS), 10 regulating services (RS), 5 cultural services (CS), and 7 ecological integrity indicators (EI) identified; 11 ecosystem disservices (EDS) added.
- Capacity matrix completed following Campagne et al. (2017); expert panel of 25 consulted to gather diverse perspectives.
- Scoring process: ES/EDS capacities rated on a 0–5 scale; each score accompanied by a confidence index (1–3).
- Two scoring rounds: October 2019 (in-person workshop in Tianjin) and August 2020 (online due to Covid-19); participants included government, research institutes, and regional technical bodies.

## Nature and units of recorded values
- Spatial data: polygons representing ETs with attributes for 14 ETs, 11 PS, 10 RS, 5 CS, 7 EI, and 11 EDS.
- Scoring outputs: capacity scores (0–5) for how well each ET provides each ES/EDS, plus confidence indices for each score.

## Quality control
- Overall high self-reported comfort with scores; 616 ES/EDS capacities scored.
- Low confidence identified for 5 ES and 11 EDS; most low-confidence scores associated with:
  - Bare land, rock or gravel (unutilized land) as ES sources (e.g., biochemicals/medicine, nutrient regulation, pollination, aesthetics, metabolic efficiency) and nearly all EDSs except for droughts, floods, erosion/siltation, and heat island effect.
  - Some EDSs related to human health (pathogens, allergens) from industrial/traffic and sandy land.
- Unfamiliarity with certain EDS concepts and underestimation of bare/unutilized lands’ contributions noted; nonetheless overall scores deemed reliable.

## Data structure
- Data converted from raster to vector for easier calculation of ES/EDS values.
- Output format: ArcGIS shapefile (readable by most GIS software) with accompanying tabular data (.dbf).
- Key attributes:
  - FID: unique feature ID
  - Shape: geometry type (Polygon)
  - ES_Type: ecosystem type (e.g., irrigated cropland, forest, grassland, waterbody, urban/rural land, industrial area and traffic utilization, sandy land, bare land, rock or gravel, etc.)
  - PS: Provisioning services (Crops, Livestock, Fodder, Capture_fi, Aquaculture, Wild_foods, Timber, Wood_fuel, Energy__bi, Biochemica, Freshwater)
  - RS: Regulating services (Local_clim, Global_cli, Flood_prot, Pests_and, Droughts, Fires, Floods, Erosion_an, Leaching_o)
  - CS: Cultural services (not explicitly itemized in the excerpt beyond PS/RS/CS headers)
  - EI: Ecological integrity indicators (not itemized in the excerpt beyond EI header)
  - EDS: Ecosystem disservices (e.g., Human_dise, Allergens, Dangerous)
  - Additional fields correspond to the listed ES/EDS categories (e.g., Heat_islan, etc.)
- Data structure designed to support analysis and reporting of ES/EDS capacities across ETs.

## References
- Wu Y., Zhang X., Fu Y., Hao F., Yin G. (2020). Response of Vegetation to Changes in Temperature and Precipitation at a Semi-Arid Area of Northern China Based on Multi-Statistical Methods. Forests, 11(3): 340.
- Xu X., Liu J., Zhang S., Li R., Yan C., Wu S. (2018). China's Multi-Period Land Use Land Cover Remote Sensing Monitoring Data Set (CNLUCC). Resource and Environment Data Cloud Platform: Beijing, China.