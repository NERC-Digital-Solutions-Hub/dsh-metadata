# Geodatabase of ecosystem types and their respective ecosystem services (ES) and disservices (EDS) in the Luanhe River Basin

- Purpose: Describes the study area, generation methods, nature and units of recorded values, quality control, and data structure for a geodatabase linking ecosystem types (ET) with their ecosystem services (ES) and disservices (EDS) in the Luanhe River Basin (LRB). Funded by UKRI/NERC TaSE programme to support sustainable development goals at national and sub-national scales.

## Study Area (LRB context for data governance)

- Location: Luanhe River Basin (LRB), semiarid North China; 39°10'–42°30' N, 115°30'–119°15' E.
- Climate and size: 1982–2015 average temp 7.0 ± 2.6°C; precip 488.4 ± 80.7 mm; area ~45,775 km²; population ~5.4 million; density ~122/km².
- Ecological and socio-economic role: Highly afforested; part of China’s Three-North Shelter Forest Program (since 1978); important ecological barrier against sandstorms; major water resource for Beijing-Tianjin-Hebei region.
- Land use and ES/EDS context: NE pasture, middle-reach reservoirs, southern cropland; provides multiple ES and EDS.

## Data Generation Methods

- ET derivation: Based on China’s National Land Use and Cover Change (CNLUCC) dataset; 30 m × 30 m grid resolution.
- Classification: 6 major land-use/ETs (cropland, forest, grassland, waterbody, built-up, unused) subdivided into 14 ET subcategories.
- ES/EDS inventory: 11 provisioning services (PS), 10 regulating services (RS), 5 cultural services (CS), 7 ecological integrity indicators (EI); 11 ES/EDS added as disservices.
- Capacity scoring: Followed Campagne et al. (2017) guidance; panel of 25 experts across government, research institutes, and regional technical bodies.
- Expert process: Two scoring rounds (Oct 2019 in-person; Aug 2020 online due to Covid-19); explanations of ES/EDS definitions provided; scores 0–5 per ES/EDS capacity; confidence index 1–3 per ES/EDS and ET.
- Panel composition: 8 government, 12 research institutes, 5 regional technical bodies; diverse backgrounds to capture broad expertise.

## Nature and Units of Recorded Values

- Spatial data: Polygons representing ETs with their corresponding ES and EDS.
- Attributes recorded: 14 ET types, 11 PS, 10 RS, 5 CS, 7 EI indicators, 11 EDS.
- Scoring convention: ES/EDS capacity scores for each ET. Confidence indices accompany scores.

## Quality Control

- Overall confidence: Most ES/EDS scores were given with comfort or moderate comfort.
- Low-confidence findings: 5 ES and 11 EDS had low confidence, concentrated largely in ES/EDS from Bare land, rock or gravel (e.g., Biochemicals and medicine, Nutrient regulation, Pollination, Aesthetic, Metabolic efficiency) and several EDS (notably from industrial/traffic and sandy land contexts).
- Interpretation: Some unfamiliarity with certain EDS concepts; bare land contributions to ES often underappreciated.
- Reliability: Despite some low-confidence items, the overall ES/EDS scores were deemed reliable.

## Data Structure

- Data format: Raster-to-vector conversion; ArcGIS shapefile with accompanying .dbf table; designed for broad GIS compatibility.
- Core fields:
  - FID: Unique feature ID
  - Shape: Geometry type (Polygon)
  - ES_Type: Ecosystem type (e.g., irrigated cropland, rainfed cropland, forest, nursery/orchard, grassland, streams/rivers, lakes, reservoirs, beaches, urban/rural land, industrial area/traffic, sandy land, swamp, bare land/rock/gravel)
- Provisioning services (PS): Crops, Livestock, Fodder, Capture_fi (capture fisheries), Aquaculture, Wild_foods, Timber, Wood_fuel, Energy_bi (Exergy/biomass), Biochemica (Biochemicals and medicine), Freshwater
- Regulating services (RS): Local_clim (local climate regulation), Global_cli (global climate regulation), Flood_prot (flood protection), Pests_and (pests and diseases), Droughts, Fires, Floods, Erosion_an (erosion and siltation), Leaching_o (leaching of nutrients)
- Cultural services (CS): Human_dise (human diseases from pathogens), Allergens, Dangerous (dangerous plants/animals), Heat_islan (heat island effect)

## Dataset context and potential uses

- Dataset provides a spatially explicit linkage of ETs with their ES and EDS values, enabling:
  - System-level data-driven planning of land-use and ecosystem service optimization.
  - Co-ownership and collaborative decision-making with policy colleagues and other stakeholders via interpretable ES/EDS outputs.
  - Assessment of data gaps and prioritization for data collection, quality improvement, and standardization.
  - Cross-sector collaboration to support an effective data ecosystem for environmental management.

## Limitations and Considerations for Data Leaders

- Data gaps: Some EDS categories are novel to the basin context; expert familiarity varied.
- Data granularity: ES/EDS scores and metadata may be limited by the 30 m CNLUCC inputs and institutional scoring processes.
- Metadata and standards: Explicit metadata beyond attribute definitions are not detailed here; ensure alignment with organizational data standards for discoverability and interoperability.
- Access and reuse: Data are provided as ArcGIS shapefiles; consider providing metadata and API-access options for broader data discoverability and programmatic use.