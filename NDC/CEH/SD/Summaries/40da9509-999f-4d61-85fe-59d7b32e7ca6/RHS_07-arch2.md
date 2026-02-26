# River Habitat Survey (RHS) data 2007 [Countryside Survey] Dataset  description

- Context and aim for analysts monitoring environmental health
  - RHS provides a standardized assessment of the physical structure of freshwater streams and rivers.
  - Based on a standard 500m sampling unit; designed for consistency across sites and time to support trend analysis and policy monitoring.
  - Surveyors must be accredited; recording follows established protocols; data are quality assured and stored for reuse.

- What the dataset contains and how it is organized
  - Main RHS dataset: STREAM_RHS_SURVEY_main_07.csv
    - Site-level details for each 1km square: SQUARE, SITE_ID, CS_SURVEY (year), COUNTRY, COUNTY07, environmental zone, stream or drain type, distance from source, altitude, slope, flow category, catchment area, Strahler order, geology (solid/drift), hydrological unit, height measures, and a wide range of channel and bed characteristics.
    - Channel morphology and features: bankfull height/width, water depth, flow types, riffles/pools/glides/runs, debris, bed/material descriptors, channel realignment, dams/sluices, bridges and culverts, fords, deflectors, and other artificial features.
    - Vegetation and habitat indicators: trees, bank vegetation, woody debris, shading, and other in-channel and riparian features.
    - Habitat assessment and quality indicators: Habitat Quality Score (HQA), Habitat Modification Scores (HMS), and overall habitat characteristics.
  - Spot-check dataset: STREAM_RHS_SURVEY_spotcheck_07.csv
    - Sections E, F, and G data capturing spot-check observations at the 500m site (e.g., environmental zone, land class, bank/substrate observations, flow, and spot-check-specific descriptors).
  - Bank-focused dataset: STREAM_RHS_SURVEY_bank_07.csv
    - Sections H and I data detailing bank-side conditions:
      - Bank and banktop properties, land use within 5m of banktop, vegetation descriptions, bank materials and modifications, embankments, and banktop/bankface structure.
      - Channel vegetation types and spot-checks across right and left banks (numerous variables for vegetation categories and descriptions).
      - Additional notes on major bank features, land use, and habitat interactions near banks.
  - All CS data usage requires acknowledgement; data compiled from 2007 Countryside Survey with DOIs and classification references.

- Data collection, entry and quality assurance
  - Data collected in the field using tablet computers in 2007; uploaded to a central CEH database.
  - Extensive audit and quality checks performed after data capture.
  - Data sources and method references include the Countryside Survey Freshwater Manual (Murphy & Weatherby, 2008) and Headwater Streams Report (2010).

- Related materials and acknowledgements
  - Supporting documents: Freshwater Manual (CS Technical Report No.5/07), Headwater Streams Report (CS Technical Report No. 8/07).
  - Official RHS website and viral references for land classification (ITE Land Classification of Great Britain 2007).
  - Acknowledgement and copyright requirement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology; Countryside Survey ©; all uses must include the specified acknowledgement text.

- Practical notes for analysts
  - Data are time-stamped to 2007; designed for longitudinal analyses when combined with other RHS or Countryside Survey years.
  - Expect substantial attribute detail and many coded fields (numerical codes for land class, environmental zones, etc.), with some fields having missing values (-9 or similar codes).
  - The dataset supports comprehensive assessment of river habitat structure, bank condition, and related ecological indicators, enabling evaluation of environmental health and policy performance over time.