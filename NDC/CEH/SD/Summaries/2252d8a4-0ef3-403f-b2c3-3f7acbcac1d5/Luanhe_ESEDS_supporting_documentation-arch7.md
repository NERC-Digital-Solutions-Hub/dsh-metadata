# Geodatabase of ecosystem types and their respective ecosystem services (ES) and disservices (EDS) in the Luanhe River Basin

- Purpose: A GIS-ready geodatabase that maps ecosystem types (ET) and their associated ecosystem services (ES) and disservices (EDS) in the Luanhe River Basin (LRB) to support spatial analysis and decision-making.

## Study Area
- Location: Luanhe River Basin in North China (39°10'–42°30' N, 115°30'–119°15' E).
- Characteristics: Semi-arid region; 45,775 km2 across 27 counties in Hebei, Liaoning, and Inner Mongolia; population ~5.4 million; significant afforestation and ecological role as a sandstorm barrier and water resource for the Beijing-Tianjin-Hebei region.
- Land-use and ES/EDS context: Dominant land uses include pasture in the northeast, major reservoirs mid-reach, and cropland near urban areas; these contribute multiple ES and EDS.

## Generation methods
- ET (ecosystem types) origin: Derived from China's National Land Use and Cover Change (CNLUCC) dataset at 30 m resolution; six major ETs subdivided into 14 subcategories.
- ES/RS/CS/EI/EDS framework: Based on Millennium Ecosystem Assessment (MA) and CICES v5.1; 11 provisioning services (PS), 10 regulating services (RS), 5 cultural services (CS), 7 ecological integrity indicators (EI), and 11 ecosystem disservices (EDS).
- Expert judgment: A panel of 25 experts with diverse backgrounds assessed ES/EDS capacity. Capacity scores (0–5) plus a confidence index (1–3) were recorded; two scoring rounds occurred in Oct 2019 (in-person workshop) and Aug 2020 (online due to Covid-19).
- Scoring approach: Following Burkhard et al. (2009) and Campagne et al. (2017) guidelines; quorum achieved with at least 10 experts per round.

## Nature and units of recorded values
- Data type: Polygons representing ETs with associated ES/EDS values.
- Coverage: 14 ET categories, 11 PS, 10 RS, 5 CS, 7 EI, and 11 EDS recorded per ET.

## Quality control
- Overall confidence: Majority of ES/EDS scores were comfortable to moderately comfortable; only 5 ES and 11 EDS had low confidence.
- Patterns in low confidence: Predominantly associated with ES/EDS from Bare land, rock or gravel (e.g., Biochemicals and medicine, Nutrient regulation, Pollination, Aesthetic, Metabolic efficiency) and some EDS from Industrial area/traffic utilization and Sandy land.
- Interpretation: Some unfamiliarity with certain EDS and the role of unused lands may explain lower confidence; nonetheless, the aggregated scores indicate reliable results.

## Data structure
- Format and accessibility: Data converted from raster to vector; shapefile (ArcGIS-compatible) with accompanying DBF.
- Core attributes:
  - FID: Unique feature ID
  - Shape: Polygon geometry
  - ES_Type: Ecosystem types (e.g., irrigated cropland, rainfed cropland, forest, nursery and orchard, grassland, streams/rivers, lakes, reservoirs/ponds, beach/shore, urban/rural land, industrial area/traffic utilization, sandy land, swamp, bare land/rock/gravel)
  - PS (Provisioning Services): Crops, Livestock, Fodder, Capture_fi (capture fisheries), Aquacultur, Wild_foods, Timber, Wood_fuel, Energy__bi (Exergy/biomass), Biochemica (Biochemicals and medicine), Freshwater
  - RS (Regulating Services): Local_clim (Local climate regulation), Global_cli (Global climate regulation), Flood_prot (Flood protection), Pests_and (Pests and diseases), Droughts, Fires, Floods, Erosion_an (Erosion and siltation), Leaching_o (Leaching of nutrients)
  - Human_dise (Human diseases from pathogens) and Allergens
  - Dangerous (Dangerous plants and animals) and Heat_islan (Heat island effect)
- Coverage of ES/EDS: 11 PS, 10 RS, 5 CS, 7 EI, and 11 EDS recorded across the ETs.
- Notes: Data structure is designed to support map-based visualization and spatial analyses of ES/EDS in relation to ETs.

## References
- Wu, Y., Zhang, X., Fu, Y., Hao, F. and Yin, G., 2020. Response of Vegetation to Changes in Temperature and Precipitation at a Semi-Arid Area of Northern China Based on MultiStatistical Methods. Forests, 11(3): 340.
- Xu, X., Liu, J., Zhang, S., Li, R., Yan, C. and Wu, S., 2018. China's Multi-Period Land Use Land Cover Remote Sensing Monitoring Data Set (CNLUCC). Resource and Environment Data Cloud Platform: Beijing, China.