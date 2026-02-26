# Pollinators in oilseed rape fields in relation to local plant diversity and landscape characteristics.

- Objective
  - Document the number and type of pollinators in winter-sown oilseed rape (Brassica napus L.) and relate them to local plant diversity (in-crop and field margins) and landscape characteristics.
  - Data designed to accompany other Wessex BESS WP4 datasets.

- Study area and field data collection
  - Surveys conducted in 2014 and 2015 across the Wessex region, southern England (12 fields per year).
  - Landscape context: largely arable/intensive grassland with remnant calcareous grassland; coordinates provided for NW and SE corners.
  - Field methods:
    - Two pollinator sampling methods: pan traps and transects.
    - Pan traps: placed at 8 m, 32 m, 58 m into the crop; left for 4 days; targeted solitary bees, hoverflies, and other visitors; collected insects identified to species or family.
    - Transects: three 58 m transects per field; counts of bees visiting flowers within 2 m; transect starts near field edge with stratified placement for hedged and hedgeless margins.
  - Plant diversity and habitat: field-edge margins and cropped areas sampled with quadrats; hedge presence recorded; margin length, width, and plant diversity within margins quantified.
  - Timing and conditions: transects between 10:00–16:00 in suitable weather (temperature > 12°C, light wind); crop growth stage recorded within 2 m of pan traps.
  - Boundaries and buffers: local scale habitat and plant diversity assessed against buffers from 0.5 to 3 km (in 0.5 km increments).

- Landscape context and habitat metrics
  - Derivation of landscape variables via GIS using multiple data sources (within 0.5–3 km radii):
    - Grassland types: semi-improved, restored, species-rich; categories derived from CEH Land Cover Map, PHI, and local NVC surveys; local knowledge used to define restoring category.
    - Habitats: arable land, semi-natural habitats, and grassland patches.
    - Crops nearby: crop species within 1 km buffer recorded.
  - Landscape metrics captured in the landscape survey dataset include areas and distances for various habitat types (intensive grassland, restored grassland, species-rich grassland, semi-natural habitat) and counts/areas of species-rich habitats and oilseed rape within buffers.
  - Additionally, artifacts such as margined habitat features (IP, Margins) and hedge characteristics (length, height, width) were recorded.

- Data structure and files
  - Four data files (CSV) with linkable identifiers:
    - NERCPollinatorSpeciesList.csv: taxonomic details, species codes, functional groups for pollen delivery; notes on missing identifications and gender data.
    - NERCPanTrapData.csv: pan trap counts by PointCode, TransectID, Year, DateSet; includes notes on missing pan trap data due to traps being knocked over.
    - NERCPollTrans.csv: transect-based pollinator counts by date and species codes; linked to species list.
    - NERCPollLandscapeSurvey.csv: landscape and field-level metrics (e.g., IG, RES, SppRich, SN, OSR, TotAr, margins, hedges, and numerous buffer-based area/distance variables).
  - Metadata linkage: consistent identifiers across files (FarmID, FieldID, TransectID, PointCode, SpeciesCode) to enable dataset integration.
  - References and taxonomic standards include growth stage coding and British plant community references for habitat classification.

- Data quality, ethics, and caveats
  - Protocols for field and laboratory data collection followed; training provided; data entered in MS Access with quality checks.
  - Ethics approval obtained from the University of Exeter CLES Penryn Research Ethics Committee (application 2014/622).
  - Noted limitations:
    - Some missing data in pan traps (certain rows/columns lost due to damage).
    - Some taxa only identified to family or superfamily (not always to species); gender data missing for many groups; some functional group assignments missing for rare visitors.
    - Field margins and habitat data rely on multiple datasets with potential differences in classification.
  - The dataset is designed to be used in conjunction with other Wessex BESS WP4 datasets.

- Potential analyses and applications for analysts
  - Explore correlations between pollinator abundance/diversity (Bombus spp., Apis mellifera, other visitors) and:
    - Local plant diversity in margins and cropped areas.
    - Hedge presence and margin structure.
    - Growth stage of oilseed rape near sampling points.
  - Assess how landscape context within 0.5–3 km (grassland types, semi-natural habitats, oilseed rape presence, arable area) influences pollinator assemblages.
  - Build predictive or explanatory models linking pollinator counts to habitat composition, margin features, and landscape configuration.
  - Integrate with other WP4 datasets to examine broader biodiversity and ecosystem service outcomes.

- References
  - Lancashire et al. 1991; Morton et al. 2011; Rodwell 1992; Stace 1997; Toynton & Ash 2002; Walker & Pywell 2000.