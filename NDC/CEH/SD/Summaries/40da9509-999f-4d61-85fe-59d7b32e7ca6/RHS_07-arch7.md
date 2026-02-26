# River Habitat Survey (RHS) data 2007 [Countryside Survey] Dataset  description

- Purpose and scope
  - An assessment of the physical structure of freshwater streams and rivers using standardized 500 m sampling units.
  - Designed to support GIS-based mapping and analysis of habitat features and riverine environments.
  - Data suitable for map-based visualisations and spatial analyses to inform policy, planning, and conservation.

- Data collection and quality control
  - Surveyors must be accredited; recording follows standard protocols to ensure consistency.
  - Data collected on field tablet computers (2007) and uploaded to a central CEH database.
  - Extensive data audit and quality checks performed after collection.
  - Data usage requires explicit acknowledgement:
    - Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology
    - Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.

- Data structure and primary data tables
  - STREAM_RHS_SURVEY_main_07.csv
    - Site and location identifiers: SQUARE (1 km square code), SITE_ID, CS_SURVEY (year), COUNTRY, COUNTY07.
    - Land classification and environment: LC07, LC07_NUM, EZ_DESC_07, HYDRO_UNIT, ENVIRONMENTAL context such as ALTITUDE, SLOPE.
    - Spatial and hydrological context: STREAM_OR_DRAIN, DISTANCE_FROM_SOURCE, CATCHMENT_AREA, STRAHLER_ORDER, SOLID_GEOLOGY, DRIFT_GEOLOGY, SURVEY_DATE, PART_OF_RIV_OR_ART.
    - Channel and habitat attributes: various measures of valley form, riffles, pools, bends, weirs/sluices, bridges, culverts, bankfull indicators, and bed/topography related fields.
    - Geomorphology and hydraulics: BANKFULL_LEFT/RIGHT, WATER_WIDTH/DEPTH, BKTOP_HT_LEFT/RIGHT, EMBANKED_HT_LEFT/RIGHT, BKFULL_WIDTH, WATER_DEPTH, etc.
    - Bed and channel material: BED_MATERIAL, BED_MATERIAL_DESC, MEASURE_LOCATION, MEASURE_OTHER, BED_SUB- and CHANNEL_SUB related fields.
    - Channel features and condition: BRAIDED_CHANNEL, SIDE_CHANNEL, FLOOD/WEIR/DEFLECT/REVET metrics, CH_REALIGN, CH_OVER_DEEP, WAT_IMP_DAM, FORDS, DEFLECT/REVET/WEIRS across classifications.
    - Vegetation and woody features: TREES_L, TREES_R, C_WOODY_DEB, EXTENT and presence indicators for woody debris and shading.
    - Habitat quality and modification: HQA_SCORE (Habitat Quality Score), HMS_CLASS (Habitat Modification Scores).
    - Other features of interest: MAJ_IMP, L_MANAGE, ANIMALS, ALDERS, and related health/disease indicators.
  - STREAM_RHS_SURVEY_spotcheck_07.csv
    - Spot-check data (sections E, F, G): Year, SQUARE, LC07/LC07_NUM, COUNTRY/COUNTY, SPOT, LB_MAT and LB_MAT_DESC, LB_MD1/2 and descriptions, LB_FE1/2 and descriptions, CH_SUB and CH_SUB_DESC, C_SUB1/2/3 and descriptions, CH_FLW/CH_FLW_DESC, CH_MD1/2 and descriptions, CH_FE1/2 and descriptions, RB_MAT and RB_MAT_DESC, bank-related land-use and vegetation fields, and numerous descriptive spot-check fields.
  - STREAM_RHS_SURVEY_bank_07.csv
    - Bank section data (sections H and I): Year, SQUARE, LC07/LC07_NUM, COUNTRY/COUNTY, BANK (left/right), and an extensive set of bank vegetation, substrate, and modification descriptors, including vegetation types, banktop/bankface features, land use within 5 m of banktop, and banktop structure descriptions.
  - All data tables use standardized codes and descriptive fields to support GIS attribute joins and thematic mapping.

- Content focus and example field types
  - Location and context: 1 km square sampling sites, hydrological unit, land class, environmental zone, and country/region.
  - Physical habitat and geomorphology: stream/drain designation, distance from source, altitude, slope, catchment area, Strahler stream order, valley form, presence of riffles/runs/glides/pools, bedrock/gravels, bank topology (banktop/bankfull), embankments, and channel width/depth.
  - Substrates and bed materials: bed material code, bed material descriptions, and measurement locations.
  - Flow and hydraulics: flow category, water depth, and related hydraulics descriptors.
  - Structure and modification: major/minor weirs, sluices, bridges, culverts, deflectors, revetments, embankments, channel realignment, and artificial modifications.
  - Vegetation and habitat features: trees (left/right bank), coarse woody debris, shading, and a broad set of bank/shore vegetation types and related descriptors.
  - Habitat quality and modification indicators: Habitat Quality Score (HQA), HMS class, and overall site characterisation.
  - Spot-check and bank-specific attributes: supplementary details on substrates, channel modifications, bank features, and land use in proximity to banks.

- How this aligns with GIS Specialist workflows
  - Rich, multi-layered attribute data suitable for thematic mapping, habitat suitability analyses, and landscape-scale hydromorphology studies.
  - Structured around 1 km squares and hydrological units, enabling integration with other geospatial datasets (e.g., land cover, soils, topography, hydrology layers).
  - Extensive feature types support detailed map legends and graduated symbology (quantitative metrics and qualitative descriptors).

- Usage notes and constraints
  - Data were collected in 2007; consider temporal context when comparing with modern datasets.
  - Acknowledge data provenance and copyright in all outputs and publications.

- Accessibility and attribution
  - Data are owned by NERC - Centre for Ecology & Hydrology; use requires the specified acknowledgement text in outputs and presentations.