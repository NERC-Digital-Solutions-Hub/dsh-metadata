# disservices (EDS) in the Luanhe River Basin, China

- Study Area
  - Luanhe River Basin (LRB): 39°10'–42°30' N, 115°30'–119°15' E; semiarid North China
  - Periodic climate: 1982–2015 average temp 7.0 ± 2.6°C, precipitation 488.4 ± 80.7 mm
  - Area: ~45,775 km2; population ~5.4 million; density ~122 people/km2
  - Key features: most afforested basin in North China; part of Three-North Shelter Forest Program; ecological barrier against Mongolian sandstorms; important water resource for Beijing–Tianjin–Hebei (BTH) region
  - Land uses: dominant pasture in NE, major reservoirs (Panjiakou, Daheiting) mid-reach, cropland near urban areas
  - Data basis: land-use/cover data from China’s CNLUCC (30 m resolution); figure showing 2018 ecosystem types

- Generation methods
  - Land uses (ecosystem types, ET) derived from CNLUCC (30 m × 30 m) with 6 major ETs, subdivided into 14 subcategories
  - ES/EDS framework: 11 provisioning services (PS), 10 regulating services (RS), 5 cultural services (CS), 7 ecological integrity indicators (EI), plus 11 ecosystem disservices (EDS)
  - Expert-driven capacity scoring: based on Campagne et al. (2017); quorum of at least 10 experts
  - Expert panel: total 25 experts (8 government, 12 research institutes, 5 regional technical bodies) across two rounds; October 2019 (in-person) and August 2020 (online due to Covid-19)
  - Scoring: ES/EDS capacities ranked 0–5; each score accompanied by a confidence index (1–3)
  - Process: individual scoring after standard definitions; diverse expertise to cover local environment and policy context

- Nature and units of recorded values
  - Data consist of polygons for ETs and their ES/EDS
  - Attributes include 14 ET categories, 11 PS, 10 RS, 5 CS, 7 EI, and 11 EDS

- Quality control
  - Most experts reported comfort or moderate comfort with scores
  - Low confidence on 5 ES and 11 EDS (roughly 616 ES/EDS capacity entries)
  - Lower confidence largely associated with ES/EDS from Bare land, rock or gravel and some EDS from industrial/traffic and sandy land
  - Unfamiliarity with EDS concept noted as part of novelty in LRB context; unused lands often overlooked in ES assessments
  - Average mean score for ES/EDS from Bare land with low confidence ~0.8
  - Overall, confidence patterns suggest the scores are broadly reliable

- Data structure
  - Vector data created by converting from raster; ArcGIS shapefile for broad GIS compatibility
  - Tabular data (.dbf) accompanying shapefile for attribute access
  - Key attributes:
    - ES_Type: ET category (e.g., irrigated cropland, forest, grassland, water bodies, urban/industrial areas, sandy land, bare land, etc.)
    - PS: provisioning services (Crops, Livestock, Fodder, Capture_fi, Aquaculture, Wild_foods, Timber, Wood_fuel, Energy_bi, Biochemica, Freshwater)
    - RS: regulating services (Local_clim, Global_cli, Flood_prot, Pests_and, Droughts, Fires, Floods, Erosion_an, Leaching_o)
    - CS: cultural services (not exhaustively listed in extract)
    - EI: ecological integrity indicators
    - EDS: ecosystem disservices (various categories including human diseases from pathogens, allergens, dangerous species, etc.)
  - Data source references: Wu et al. (2020); Xu et al. (2018)

- Funding and acknowledgments
  - Funded by UK Research and Innovation (UKRI) through NERC TaSE programme
  - Project: River basins as “living laboratories” for sustainable development goals; Grant NE/S012427/1

- References
  - Wu, Y.; Zhang, X.; Fu, Y.; Hao, F.; Yin, G. (2020). Response of Vegetation to Changes in Temperature and Precipitation at a Semi-Arid Area of Northern China Based on Multi-Statistical Methods. Forests, 11(3): 340
  - Xu, X.; Liu, J.; Zhang, S.; Li, R.; Yan, C.; Wu, S. (2018). China’s Multi-Period Land Use Land Cover Remote Sensing Monitoring Data Set (CNLUCC). Resource and Environment Data Cloud Platform: Beijing, China