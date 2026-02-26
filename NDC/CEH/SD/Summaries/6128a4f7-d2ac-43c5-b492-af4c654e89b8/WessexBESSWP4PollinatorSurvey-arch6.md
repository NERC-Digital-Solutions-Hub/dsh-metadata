# Pollinators in oilseed rape fields in relation to local plant diversity and landscape characteristics.

- Overview
  - Dataset describing pollinator communities in winter-sown oilseed rape (Brassica napus) fields, examined in relation to local plant diversity (in-crop and field margins) and landscape characteristics.
  - Part of the Wessex BESS project; funded under NERC Biodiversity and Ecosystem Service Sustainability program.
  - Collected in 2014 and 2015 across the Wessex region in southern England; data can be used with other Wessex BESS WP4 datasets.

- Study area and timeframe
  - Location: Wessex region, southern England (NW corner: 51.415482 N, -2.2892761 W; SE corner: 51.087135 N, -1.5037537 W).
  - Landscape context: largely arable and intensive grassland with remnant calcareous grassland, including Salisbury Plain area.
  - Spatial scale for landscape variables: within 0.5 to 3 km radii around collection points (buffered areas at 0.5 km intervals).

- Data collection methods
  - Pollinators collected using two methods:
    - Pan traps (15 cm diameter) for non-bee visitors and some bees/hoverflies.
    - Transect walks to observe flower visitors (bumblebees, Apis mellifera) within 2 m of observers.
  - Field data collection:
    - 12 fields surveyed per year; three 58 m transects per field set perpendicular to field edge with stratified random selection for hedge/margin presence.
    - Local plant diversity: five 1 m² quadrats within 20 m of transect start (margin diversity) and quadrats in cropped areas (in-crop diversity).
    - Plant species identified (Stace 1997); percent cover recorded.
  - Temporal constraints: transect surveys conducted between 10:00 and 16:00 under favorable weather (temp > 12°C, wind < 6–8 m/s).
  - Documentation of growth stage of oilseed rape within 2 m of pan traps (Lancashire growth staging system).
  - Taxonomic resolution: bees and hoverflies identified to species where possible; other groups to family level.

- Local habitat and plant diversity (within-field and margins)
  - Field-edge structure and plant diversity measured (length of field edge, hedge proportion, field margin proportion and width).
  - Margin plant diversity assessed with quadrats around transect start.
  - Crop plant diversity recorded within sampling points.

- Landscape characteristics (buffer-based)
  - Derived from GIS using CEH Land Cover Map 2007, Natural England Priority Habitats Inventory, and local NVC surveys.
  - Grassland classification: semi-improved, species-rich, restored, and improved grasslands (CG2, CG3, CG6, MG5; MG1, MG4, MG6; MG7).
  - Additional habitat categories: semi-natural habitat, arable land, oilseed rape, etc.
  - Variables computed as area or proportion within buffers from 0.5 to 3 km (e.g., IG, RES, SppRich, SN, OSR, TotAr, margins, hedges).

- Data quality assurance and ethics
  - Standardized field and lab protocols; data entered in MS Access; QA checks for anomalies.
  - Training provided by R. Shaw.
  - Ethics approval: CLES Penryn Research Ethics Committee (application 2014/622).

- Datasets and linking structure
  - Files (4):
    - NERCPollinatorSpeciesList.csv: taxonomic details, species codes, and links to other datasets.
    - NERCPanTrapData.csv: pan trap counts by species/codes across points and transects; notes on missing data.
    - NERCPollTrans.csv: transect survey counts by date and species codes.
    - NERCPollLandscapeSurvey.csv: landscape and margin/edge metrics associated with transects, including numerous radii-based covariates.
  - Linking keys: FarmID, FieldID, TransectID, PointCode, SpeciesCode (consistent across WP4 datasets to enable data integration).

- Data limitations and caveats
  - Pan trap data: some traps knocked over; missing data in several points (e.g., 3.2.C, 1.2.G, etc.).
  - Taxonomic resolution: some taxa identified only to family or superfamily; species-level data limited for certain groups.
  - Gender data: assigned only for Apoidea; missing for other groups.
  - Some columns and fields are provided with technical descriptions; users should refer to the CSV metadata for precise definitions and units.

- Potential uses and integration
  - Enables analysis of relationships between pollinator communities, local plant diversity (margin and crop), and landscape context.
  - Can be combined with other Wessex BESS WP4 datasets for broader ecosystem service and biodiversity analyses.
  - Suitable for creating dashboards or self-serve data products to explore pollinator patterns across fields, margins, and landscapes.