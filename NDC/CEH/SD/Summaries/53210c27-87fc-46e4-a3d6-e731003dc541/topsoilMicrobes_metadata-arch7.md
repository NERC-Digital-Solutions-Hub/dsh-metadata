# Topsoil microbe model estimates [Countryside Survey]

## Overview
- Dataset from the Countryside Survey (CS) representing topsoil microbes in the 0–15 cm layer.
- Includes bacterial community structure (NMDS axis 1 scores) and diversity metrics (Shannon and Simpson).
- Based on 1000 samples across 233 1 km × 1 km squares in Great Britain, collected in 2007.

## Data content and modelling
- Mean values for selected habitat and parent material combinations are modelled across GB using a mixed-model approach.
- Habitat information derived from Land Cover Map 2007 (LCM2007) and parent material from the BGS Soil Parent Material Model (PMM) 2009.
- The parent material characteristic used to drive models is CACO3_RANK (calcium carbonate content) or SOIL_GROUP as applicable.
- Areas not sampled by CS (e.g., urban and littoral rock) have no associated data; some habitat/parent material combinations have insufficient sample sizes to estimate means.

## Variables and modelling output
- LCM_CLASS: Dominant land cover class at a broad habitat level (derived from LCM2007).
- LCM_NUMBER: Integer code (1–23) for LCM2007 class.
- DOM_GRAIN: Qualitative dominant grain size from PMM.
- SOIL_GROUP: Soil texture category (Heavy/Medium/Light) from PMM.
- CACO3_RANK: Carbonate content rank (none/low/medium/high) from PMM.
- NMDS107: Mean axis 1 score of bacterial community structure for the 2007 data, modelled with LCM_CLASS and CAC03_RANK.
- NMDS107_SE: Standard error for NMDS107.
- MSHAN07: Mean Shannon diversity index for bacterial communities (2007), modelled with LCM_CLASS and SOIL_GROUP.
- MSHAN07_SE: Standard error for MSHAN07.
- MSIMP07: Mean Simpson diversity index for bacterial communities (2007), modelled with LCM_CLASS and SOIL_GROUP.
- MSIMP07_SE: Standard error for MSIMP07.

## Sampling, collection, and analysis
- Sampling: 1000 plots within 233 1 km × 1 km squares in 2007 Countryside Survey.
- Collection method: soil microbial measurements taken from a 15 cm long by 4 cm diameter core.
- Analytical methods: microbial communities assessed by tRFLP profiling; NMDS ordination used to quantify community similarities; diversity indices calculated from relative tRFLP peak abundances.
- Quality control: detailed in Griffiths et al. (2011).

## Spatial reference
- Coordinate System: OSGB 1936 / British National Grid (EPSG 27700).

## Data access and references
- Citation: Henrys, P.A.; Keith, A.M.; Robinson, D.A.; Emmett, B.A. (2014). Model estimates of topsoil microbes [Countryside Survey]. NERC Environmental Information Data Centre. https://doi.org/10.5285/53210c27-87fc-46e4-a3d6-e731003dc541
- Used for modelled landscape-scale microbial indicators in GB soils.
- Related technical references: Emmett et al. (2008, 2010), Griffiths et al. (2011), Scott (2008).