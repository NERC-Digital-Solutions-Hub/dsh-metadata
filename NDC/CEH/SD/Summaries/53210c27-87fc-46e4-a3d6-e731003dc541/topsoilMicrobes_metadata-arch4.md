# Topsoil microbe model estimates [Countryside Survey]

- Overview
  - Dataset of topsoil microbes (0–15 cm) across Great Britain from the 2007 Countryside Survey.
  - Includes bacterial community structure (ordination axis 1 scores) and diversity indices (Shannon, Simpson).
  - >1000 samples across 233 1 km × 1 km squares; GB-wide estimates of mean values within selected habitat and parent-material combinations.
  - Modelling links microbial metrics to habitat characteristics from Land Cover Map 2007 and the British Geological Survey Parent Material Model (2009); some areas/samples not covered.

- Data content and attributes
  - Key variables (attributes):
    - LCM_CLASS, LCM_NUMBER: dominant land cover from LCM2007.
    - DOM_GRAIN: dominant grain size from the Soil Parent Material Model.
    - SOIL_GROUP: general soil texture (Heavy/Medium/Light).
    - CACO3_RANK: carbonate content (none/low/medium/high).
    - NMDS107, NMDS107_SE: mean axis 1 scores for bacterial community structure and standard error.
    - MSHAN07, MSHAN07_SE: mean Shannon diversity index and standard error.
    - MSIMP07, MSIMP07_SE: mean Simpson diversity index and standard error.
  - Modelling approach:
    - Means estimated for habitat/parent material combinations, based on dominant habitat and material characteristics.
    - Model selection uses the Area-Under-Information-Criterion (AIC) approach to choose relevant parent-material characteristics.

- Methods
  - Sampling: microbial measurements in 1,000+ plots within 233 1 km squares (2007 CS).
  - Collection: soil cores (15 cm long, 4 cm diameter) following standard field protocol.
  - Laboratory/analysis: bacterial communities via tRFLP; NMDS ordination to assess similarities; diversity indices calculated from relative peak abundances.
  - Quality control and references: detailed in Griffiths et al. (2011); supporting technical reports by Emmett et al. (2008, 2010) and Scott (2008).

- Spatial and data considerations
  - Spatial reference: OSGB 1936 / British National Grid (EPSG: 27700).
  - Data access: cited dataset available through the NERC Environmental Information Data Centre; DOI provided.
  - Data limitations:
    - Urban and littoral rock areas are not sampled and have no associated data.
    - Some habitat/parent material combinations have insufficient sample sizes to estimate means.
    - Reflects 2007 conditions; applicability to current conditions may require additional contextual metadata.

- Implications for data strategy and use
  - Provides a stratified view of soil microbial structure and diversity linked to habitat and parent material, useful for soil health and biodiversity assessments.
  - Supports data-driven decision-making when integrating microbial metrics with other soil parameters (e.g., pH, carbon, plant diversity).
  - Emphasizes the importance of data discoverability, metadata completeness, and explicit documentation of gaps (e.g., unsampled areas and limited combinations) for planning future data collection and analyses.

- Access and references
  - Henrys, P.A.; Keith, A.M.; Robinson, D.A.; Emmett, B.A. (2014). Model estimates of topsoil microbes [Countryside Survey]. NERC Environmental Information Data Centre. DOI https://doi.org/10.5285/53210c27-87fc-46e4-a3d6-e731003dc541
  - Spatial and methodological references: Emmett et al. (2008, 2010); Griffiths et al. (2011); Scott (2008); Morton et al. (2011) and related technical reports.