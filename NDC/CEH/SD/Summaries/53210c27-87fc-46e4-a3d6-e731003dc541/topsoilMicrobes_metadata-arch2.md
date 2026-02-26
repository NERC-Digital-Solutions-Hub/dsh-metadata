# Topsoil microbe model estimates [Countryside Survey]

## Purpose and scope
- Represents 0–15 cm soil depth microbial data from the Countryside Survey (CS), focusing on bacterial community structure (NMDS axis 1), Shannon diversity, and Simpson diversity.
- Aims to provide standardized, monitorable outputs that relate microbial patterns to habitat and soil context across Great Britain (GB).

## Sampling design and spatial coverage
- Data from over 1000 soil samples collected across 233 1 km × 1 km squares in GB during 2007.
- Sampling supports estimation of mean microbial metrics within selected habitat and parent material combinations.

## Modelling framework and inputs
- Estimates means by habitat/parent material using mixed-model approaches.
- Habitat characteristics derived from Land Cover Map 2007 (LCM2007); parent material characteristics from the British Geological Survey Soil Parent Material Model (2009).
- Parent material variable selected to minimise AIC in each model.
- Some areas (e.g., urban, littoral rock) are not sampled by CS and have no associated data; certain habitat/parent material combos have insufficient samples for mean estimation.

## Key variables and outputs
- Bacterial community structure: NMDS axis 1 scores (NMDS107) with standard error (NMDS107_SE).
- Bacterial diversity: Shannon diversity index (MSHAN07) with SE (MSHAN07_SE); Simpson diversity index (MSIMP07) with SE (MSIMP07_SE).
- Clickable data attributes include Land Cover Map class (LCM_CLASS, LCM_NUMBER), soil group (SOIL_GROUP), and calcium carbonate content ranking (CACO3_RANK).

## Data collection and analysis methods
- Collection: soil microbial measurements using a 15 cm long, 4 cm diameter core following the CS field protocol.
- Analysis: molecular profiling of bacterial communities via tRFLP; community similarities assessed with two-dimensional NMDS; diversity indices calculated from relative tRFLP peak abundances.
- Quality control guided by Griffiths et al. (2011).

## Data attributes and sourcing
- Dataset attributes include:
  - LCM_CLASS, LCM_NUMBER: dominant land cover from LCM2007.
  - SOIL_GROUP: broad soil texture category (Heavy/Medium/Light).
  - CACO3_RANK: carbonate content category (none/low/medium/high).
  - NMDS107, NMDS107_SE; MSHAN07, MSHAN07_SE; MSIMP07, MSIMP07_SE.
- Spatial reference: OSGB 1936 / British National Grid (EPSG:27700).

## Access, references, and provenance
- Data cited as: Henrys et al. (2014). Model estimates of topsoil microbes [Countryside Survey]. NERC Environmental Information Data Centre. DOI provided.
- Related methods and context available in:
  - Emmett et al. 2008/2010 CS technical reports (Soils Manual; Soils Report 2007).
  - Griffiths et al. 2011 (bacterial biogeography of British soils).
  - Scott 2008 (CS Technical Report: Statistical Analysis).
- Data and technical resources accessible via Countryside Survey and associated data portals.

## Practical implications for environmental monitoring
- Provides standardized microbial indicators linked to habitat and parent material, enabling temporal trend analyses and cross-site comparisons.
- Outputs can be integrated with other soil parameters (pH, carbon, plant diversity) to monitor environmental health and inform policy performance.
- Emphasizes the value of making underlying data accessible to stakeholders (data portals) to support broader analyses and reuse.