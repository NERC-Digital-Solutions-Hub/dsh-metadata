## Geodatabase of ecosystem types and their respective ecosystem services (ES) and disservices (EDS) in the Luanhe River Basin

- Purpose and scope
  - A geodatabase detailing ecosystem types (ET) and their associated ecosystem services (ES) and disservices (EDS) in the Luanhe River Basin (LRB) to support environmental monitoring and policy evaluation.
  - Builds a standardized, comparable dataset suitable for scrutiny of environmental health and policy performance over time.

- Study Area
  - Location: Luanhe River Basin, North China (39°10'–42°30' N, 115°30'–119°15' E).
  - Area and demographics: ~45,775 km²; ~5.4 million people; population density ~122/km².
  - Key characteristics: highly afforested, important ecological barrier against Mongolian sandstorms, major water resource for Beijing-Tianjin-Hebei region.
  - Land uses: pasture in the northeast, large reservoirs mid-reach, cropland around urban areas; multiple ES/EDS linked to these land uses.

- Generation methods and data sources
  - Land uses (ET) derived from China's National Land Use and Cover Change (CNLUCC) dataset (30 m resolution), with six major ETs subdivided into 14 subcategories.
  - Conceptual framework: links to Millennium Ecosystem Assessment (MA) and Common International Classification of Ecosystem Services (CICES) v5.1; 11 provisioning services (PS), 10 regulating services (RS), 5 cultural services (CS), and 7 ecological integrity indicators (EI); 11 EDS added.
  - Capacity matrix: filled following Campagne et al. (2017); expert panel composed of 25 experts across government, research institutes, and regional technical bodies.
  - Expert process: two scoring rounds (Oct 2019 in-person; Aug 2020 online due to COVID-19); each expert rated ES/EDS capacity for ETs on a scale 0–5 and provided a confidence index (1–3).
  - Panel composition: 8 government, 12 research institutes, 5 regional technical bodies; diverse disciplinary backgrounds.

- Recorded values and units
  - Data are polygon-based, representing 14 ETs, 11 PS, 10 RS, 5 CS, 7 EI, and 11 EDS.
  - Each ET-ES/EDS combination carries a capacity score and a confidence/uncertainty assessment.

- Quality control and confidence
  - Overall high comfort level: most ES/EDS scores deemed reliable; low confidence observed for 5 ES and 11 EDS.
  - Lower confidence largely associated with ES/EDS from Bare land, rock or gravel (e.g., biochemicals, nutrient regulation, pollination, aesthetic value, metabolic efficiency) and some EDS (e.g., human diseases from pathogens, allergens) linked to industrial/traffic and sandy land.
  - Unfamiliarity with some EDS concepts noted as a factor; nonetheless, the dataset demonstrates overall reliability of scores.

- Data structure and accessibility
  - Data converted from raster to vector for ease of calculation and integration.
  - Output format: ArcGIS shapefile (readable in most GIS tools) with accompanying .dbf table.
  - Key attributes:
    - FID: feature ID; Shape: geometry (Polygon).
    - ES_Type: ET category (e.g., irrigated cropland, forest, grassland, water bodies, urban/rural land, industrial area/traffic, sandy land, bare land/rock/gravel, etc.).
    - PS (Provisioning Services): Crops, Livestock, Fodder, Capture_fi, Aquaculture, Wild_foods, Timber, Wood_fuel, Energy_bi, Biochemica, Freshwater.
    - RS (Regulating Services): Local_clim, Global_cli, Flood_prot, Pests_and, Droughts, Fires, Floods, Erosion_an, Leaching_o.
    - EI (Ecological Integrity indicators): (listed as applicable).
    - EDS: Human_dise, Allergens, Dangerous, Heat_islan, and other disservices (11 total; includes outputs like pathogens-related diseases and allergens).
  - All data are prepared to support integration with GIS-based monitoring and analysis workflows.

- Funding and references
  - Funded by UK Research and Innovation (UKRI) through the Natural Environment Research Council's TaSE programme (Grant NE/S012427/1).
  - Key references informing methods: Wu et al. (2020); Xu et al. (2018); Campagne et al. (2017); Burkhard et al. (2009); Campagne et al. (2017).

- Relevance for environmental monitoring
  - Provides standardized, auditable ES/EDS capacity data aligned with established classifications, enabling temporal comparisons and policy performance assessments.
  - Uses broadly accessible data sources (CNLUCC) and GIS-ready formats to facilitate reuse, sharing, and integration with broader environmental datasets.
  - Addresses challenges of data value and accessibility by documenting confidence levels and ensuring datasets are stored and retrievable for ongoing monitoring and decision-making.