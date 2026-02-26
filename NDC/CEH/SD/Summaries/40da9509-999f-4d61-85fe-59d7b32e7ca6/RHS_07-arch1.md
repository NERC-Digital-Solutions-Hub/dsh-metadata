# River Habitat Survey (RHS) data 2007 [Countryside Survey] Dataset  description

## Overview and purpose
- RHS is a standardized assessment of the physical structure of freshwater streams and rivers using 500m sample units.
- Recording relies on accredited surveyors and documented protocols to ensure consistency.
- The dataset supports analyses of habitat structure, geomorphology, hydrology, and associated factors across Britain.

## Data collection and quality control
- Field data were collected in 2007 using tablet computers and uploaded to a central CEH database.
- An extensive audit and quality checks followed data capture.
- Foundational references for methods include Murphy & Weatherby (2008) Freshwater Manual and related Countryside Survey reports.

## Datasets and structure
- STREAM_RHS_SURVEY_main_07.csv
  - Primary site-level table with sections A, B, C, D, J, K, L, M, N, O, P, Q.
  - Key fields include:
    - Spatial identifiers and context: SQUARE (1km grid), SITE_ID, CS_SURVEY (year), COUNTRY, COUNTY07, LC07 (land class 2007 codes).
    - Hydromorphology and geomorphology: STREAM_OR_DRAIN, DISTANCE_FROM_SOURCE, ALTITUDE, SLOPE, FLOW_CATEGORY, CATCHMENT_AREA, STRAHLER_ORDER, SOLID_GEOLOGY, DRIFT_GEOLOGY, HYDRO_UNIT, HEIGHT_SOURCE, SURVEY_DATE, PART_OF_RIV_OR_ART, and numerous channel and valley descriptors.
    - Channel and bed features: BANKFULL_LEFT/RIGHT, BKTOP_HT_LEFT/RIGHT, BKFULL_WIDTH, WATER_WIDTH, WATER_DEPTH, BED_MATERIAL, MEASURE_LOCATION, BED_MATERIAL_DESC, CH_REALIGN, WAT_IMP_DAM, and extensive tagged feature counts (e.g., RIFFLES, RUNS, POOLS, CASCADES, RAPIDS, etc.).
    - Vegetation, bank/top features, and habitat indicators: TREES_L/R, SH_CHANNEL, OVERHANG, EX_B_ROOTS, UW_T_ROOTS, FALLEN_TREES, C_WOODY_DEB, and a wide range of other structural and ecological indicators.
    - Habitat quality and modification: HQA_SCORE (Habitat Quality Score) and HMS_CLASS (Habitat Modification Scores Class).
    - Spatially-referenced attributes for land use, vegetation, and bank features.
- STREAM_RHS_SURVEY_spotcheck_07.csv
  - Spot-check data covering RHS sections E, F, G.
  - Includes Year, SQUARE, LC07, COUNTRY/COUNTY07, and spot-check specific descriptors (LB_MAT, LB_MD1/2, CH_SUB, CH_FLW, CH_MD1/2, CH_FE1/2, bank/shoreline features, and various descriptions).
- STREAM_RHS_SURVEY_bank_07.csv
  - Banktop and bankface attributes for RHS sections H and I.
  - Contains Year, SQUARE, LC07, COUNTRY, COUNTY07, BANK (left/right), and extensive variables for bank materials, vegetation, land use within bankside buffers, and banktop/bankface structure (USE5_L/R, L_BTOP/L_BFAC, CV_* vegetation types, etc.).
- STREAM_RHS_SURVEY_bank_07.csv (continued)
  - Additional bank-related fields capturing land-use within 5m of banktop, and detailed channel-bank interactions.
- All Countryside Survey data usage
  - Acknowledgement is required: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology; data are © and rights reserved.

## Key concepts and variables for analysis
- Spatial and contextual variables: SQUARE, SITE_ID, HYDRO_UNIT, STRAHLER_ORDER, LAND CLASS (LC07), COUNTRY, COUNTY07.
- Hydromorphology and channel form: VALLEY_FORM, VALLEY_TERR, NO_RIFFLES, NO_WIRSMAJOR, WEIRSMINOR, BRIDGEMAJ/BRIDGEINT/BRIDGEMIN, CULVERTS, SLUICES, BANKFULL_LEFT/RIGHT, BKTOP_HT_LEFT/RIGHT, BKFULL_WIDTH, WATER_WIDTH, WATER_DEPTH.
- Substrate and bed/material descriptors: BED_MATERIAL and BED_MATERIAL_DESC; MEASURE_LOCATION and MEASURE_OTHER.
- Channel features and structures: WEIRS/OUTFALLS/DEFLECTS/REVETMENTS/EMBANK etc., including major/intermediate/minor classifications.
- Habitat indicators and vegetation: TREES_L/R, CV_* vegetation codes and descriptions (within 5m of banktop), HQA_SCORE (Habitat Quality), HMS_CLASS (Habitat Modification).
- Hydrology and flow: FLOW_CATEGORY, RUNS/RIFfLES/POOLS, WAT_IMP_DAM, PONDED_REACH, NOFLOW, etc.
- Spot-check and bank attributes provide finer-resolution context on bankmaterials, substrate, channel modification, and vegetation in spot-checks.

## Intended usage and analytical opportunities
- Correlate habitat structure and channel form with land use, geology, and hydrology to understand drivers of river habitat quality.
- Compute and compare Habitat Quality Score (HQA) across sites and assess drivers (natural features vs. modifications captured by HMS_CLASS).
- Build spatial analyses and predictive models of river habitat condition using RHS variables (e.g., Strahler order, land class, valley form, presence of major/moderate bank modifications).
- Assess the impact of artificial structures (weirs, sluices, embankments, channel realignment) on habitat complexity and flow regimes.
- Cross-tabulate 500m RHS units with broader landscape data (HYDRO_UNIT, CATCHMENT_AREA) for regional habitat assessments.

## Practical considerations and limitations
- Data represent 500m sample units and are most appropriate for landscape- to regional-scale analyses; local-scale interpretation may require finer-scale data.
- Data availability and scale may pose challenges for local decision-making; some attributes are extensive and require careful interpretation.
- Data access and interpretation may require familiarity with the Countryside Survey methodology and related manuals; consult Murphy & Weatherby (2008) and headwater streams report for context.
- Data integration requires attention to coding schemes (LC07, environmental zones, etc.) and metadata for correct joins and interpretations.
- All uses must include the specified acknowledgement language due to copyright and data ownership.

## Documentation and references
- Core data and methods: River Habitat Survey (RHS) and Countryside Survey materials; Murphy, J.; Weatherby, A. 2008; Dunbar et al. 2010 Headwater Streams Report; RHS official website.
- Acknowledgement and copyright notice must accompany all outputs: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology; Countryside Survey ©; all rights reserved.