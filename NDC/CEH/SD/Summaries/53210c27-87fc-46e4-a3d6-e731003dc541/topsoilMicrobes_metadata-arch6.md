# Topsoil microbe model estimates [Countryside Survey]

- Overview
  - GB-wide dataset describing topsoil (0–15 cm) bacterial community structure and diversity (Shannon and Simpson) from the Countryside Survey (CS).
  - Represented by NMDS axis 1 scores and diversity indices, linked to habitat and parent material characteristics.
  - Data derived from 1,000+ samples across 233 1 km × 1 km squares, collected in 2007.

- What is modeled
  - Estimated mean values within habitat/parent material combinations, based on:
    - Land Cover Map 2007 (dominant habitat characteristics)
    - BGS Soil Parent Material Model (2009)
  - Model selection via minimizing AIC; some areas (urban, littoral rock) are not sampled and have no data.
  - Outputs include model-estimated means for:
    - Bacterial community structure (NMDS axis 1 scores)
    - Shannon diversity index
    - Simpson diversity index

- Data attributes and variables
  - Spatial reference: OSGB 1936 / British National Grid (EPSG:27700)
  - Key attributes (observed/derived):
    - LCM_CLASS, LCM_NUMBER: Land Cover Map 2007 Class and code
    - DOM_GRAIN: Dominant grain size from Soil PMM
    - SOIL_GROUP: General soil texture (Heavy/Medium/Light)
    - CACO3_RANK: Carbonate content ranking in parent material
    - NMDS107, NMDS107_SE: Mean NMDS axis 1 scores and standard error (07)
    - MSHAN07, MSHAN07_SE: Mean Shannon diversity and standard error (07)
    - MSIMP07, MSIMP07_SE: Mean Simpson diversity and standard error (07)

- Data collection and analysis
  - Sampling: >1,000 plots within 233 CS 1 km × 1 km squares (2007)
  - Collection method: Soil cores (15 cm long, 4 cm diameter)
  - Laboratory analysis: Molecular profiling of bacterial communities via tRFLP; diversity indices calculated from tRFLP peak relative abundances
  - Data quality/validation: Detailed quality control described in Griffiths et al. (2011)

- Modeling approach
  - Mixed-model framework using habitat (LCM_CLASS) and parent material (CACO3_RANK/SOIL_GROUP) characteristics
  - Derives means for each habitat × parent material combination
  - Based on auxiliary data sources: Land Cover Map 2007 and Soil Parent Material Model (2009)
  - Notes: Some habitat/parent material combinations have insufficient samples to estimate means

- Access and references
  - Data citation: Henrys, P.A.; Keith, A.M.; Robinson, D.A.; Emmett, B.A. (2014). Model estimates of topsoil microbes [Countryside Survey]. NERC Environmental Information Data Centre. DOI provided
  - Related resources: Countryside Survey technical reports and primary literature (sampling, methods, and ecological context)

- Practical considerations for data users
  - Useful for mapping and comparing microbial structure and diversity across GB in relation to habitat type and soil parent materials
  - Enables exploration of associations with other soil parameters (e.g., pH, carbon) and biotic features like plant diversity via correspondence with NMDS axis 1
  - Be mindful of limitations:
    - Areas without sampling data (urban, littoral rock) cannot be modeled here
    - Some habitat/parent material combinations lack sufficient data to estimate means
    - Model outputs are estimates based on habitat and parent material proxies rather than direct sampling in every category
  - When integrating with other datasets, align with OSGB coordinates and consider using Land Cover Map 2007 and Soil PMM inputs for cross-cutting analyses