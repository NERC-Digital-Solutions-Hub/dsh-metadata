# Geodatabase of ecosystem types and their respective ecosystem services (ES) and disservices (EDS) in the Luanhe River Basin

## Study Area
- Luanhe River Basin (LRB): 39°10'–42°30' N, 115°30'–119°15' E; semiarid North China
- Climate (1982–2015): average temperature 7.0 ± 2.6°C; precipitation 488.4 ± 80.7 mm
- Area and population: ~45,775 km2; ~5.4 million people; density ~122 persons/km2
- Ecological context: heavily afforested; part of China’s Three-North Shelter Forest Program (since 1978); key ecological barrier against sandstorms; important water resource for Beijing–Tianjin–Hebei region
- Land-use context: northeast dominated by pasture; middle reach contains major reservoirs; south around urban areas is cropland
- Data source for land use: China's National Land Use and Cover Change (CNLUCC)

## Generation methods
- Land uses (ecosystem types, ET) derived from CNLUCC at 30 m × 30 m resolution
- Six major ETs, subdivided into 14 ET subcategories
- Ecosystem Services (ES) and Disservices (EDS) framework:
  - 11 provisioning services (PS)
  - 10 regulating services (RS)
  - 5 cultural services (CS)
  - 7 Ecological integrity indicators (EI)
  - 11 ecosystem disservices (EDS)
- Capacity assessment:
  - Follow Campagne et al. (2017) guidance; panel of 25 experts (diverse expertise) to gather broad knowledge
  - Two scoring periods: Oct 2019 (in-person workshop) and Aug 2020 (online due to Covid-19)
  - Expert composition: 8 from government, 12 from research institutes, 5 from regional technical bodies
  - Scoring: capacity scores 0–5 with a confidence index 1–3
  - Objective: quantify the capacity of each ET to provide ES/EDS and capture score confidence
- Process details:
  - Experts were trained on ES/EDS definitions; scoring was individual
  - Data collection occurred in two rounds with differing modalities (in-person vs online)

## Nature and units of recorded values
- Data representation: polygons for ETs and their corresponding ES/EDS
- Recorded attributes: 14 ETs, 11 PS, 10 RS, 5 CS, 7 EI, 11 EDS

## Quality control
- Most ES/EDS scores were deemed comfortable or moderately comfortable
- Total of 616 ES/EDS capacities; low confidence on 5 ES and 11 EDS
- Higher prevalence of low-confidence scores associated with Bare land, rock or gravel (≈75%)
  - Affected ES: Biochemicals and medicine, Nutrient regulation, Pollination, Aesthetic, Metabolic efficiency; all EDS except Droughts, Floods, Erosion and siltation, Heat island effect
- Low-confidence also noted for EDS: Human diseases from pathogens and Allergens (from Industrial area/traffic utilization and Sandy land)
- Observed unfamiliarity with certain EDS concepts; bare land often overlooked in ES
- Reported average ES/EDS score for Bare land with low confidence: 0.8
- Overall conclusion: expert-derived ES/EDS scores are considered reliable despite some low-confidence items

## Data structure
- Data were converted from raster to vector; provided as ArcGIS shapefile with readable accompanying tabular data (.dbf)
- Key attributes:
  - FID: unique feature ID
  - Shape: polygon geometry
  - ES_Type: ET category (examples include irrigated cropland, rainfed cropland, forest, nursery/orchard, grassland, streams/rivers, lakes, reservoirs, beaches, urban/rural land, industrial area/traffic utilization, sandy land, swamp, bare land/rock/gravel)
  - PS (Provisioning services): Crops, Livestock, Fodder, Capture_fi, Aquaculture, Wild_foods, Timber, Wood_fuel, Energy_bi, Biochemica, Freshwater
  - RS (Regulating services): Local_clim, Global_cli, Flood_prot, Pests_and, Droughts, Fires, Floods, Erosion_an, Leaching_o
  - CS (Cultural services): [categories not exhaustively listed in the summary]
  - EI (Ecological integrity indicators)
  - EDS (Disservices): 11 categories including human health-relevant disservices
- Purpose: enable GIS-enabled exploration and analysis of ES/EDS by ET; supports data-driven policy and planning

## References
- Wu, Y., Zhang, X., Fu, Y., Hao, F. and Yin, G., 2020. Response of Vegetation to Changes in Temperature and Precipitation at a Semi-Arid Area of Northern China Based on Multi-Statistical Methods. Forests, 11(3): 340.
- Xu, X., Liu, J., Zhang, S., Li, R., Yan, C. and Wu, S., 2018. China's Multi-Period Land Use Land Cover Remote Sensing Monitoring Data Set (CNLUCC). Resource and Environment Data Cloud Platform: Beijing, China.

## Funding acknowledgment
- Funded by the UK Research and Innovation (UKRI) through the Natural Environment Research Council's TaSE program (Grant NE/S012427/1) for the project on river basins as living laboratories for sustainable development goals.