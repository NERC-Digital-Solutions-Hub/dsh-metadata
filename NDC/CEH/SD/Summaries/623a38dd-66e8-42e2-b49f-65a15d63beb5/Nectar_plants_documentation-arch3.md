# Experimental Design/Sampling Regime

- Objective and scope
  - Use nectar plant diversity as a surrogate for pollinator distribution to assess environmental health and inform policy decisions.
  - Based on Countryside Survey 2007 data, focusing on areal, unenclosed habitats (fields, unenclosed land, small semi-natural patches).

- Sampling design and plots
  - Countryside Survey 2007 sampled 591 one-kilometre squares, stratified by land class.
  - Within each square, five large randomly placed plots (14.14 m x 14.14 m; 200 m²) with an inner 2 m x 2 m nest are used for analysis.
  - Plot types include x plots (large random plots) and y plots (targeted area habitats in small biotopes; often remnants of semi-natural habitats).
  - The sampling emphasizes unenclosed habitats; coastal and urban habitats are excluded.

- Spatial reference
  - Coordinate System: OSGB 1936 / British National Grid (EPSG:27700).

- Data attributes
  - plantCount: modeled estimate of the count of all bee nectar plants within each 1 km² square.
  - SEM: standard error (variance measure) for plantCount.

- Collection methods
  - In each vegetation plot, compile a list of all vascular plants and a subset of bryophytes and macro-lichens.
  - Nomenclature follows Stace (1991) and Watson (1981).
  - Cover estimates are recorded to the nearest 5% for species with at least ~5% cover.

- Analytical methods
  - Nectar plant diversity is used as a proxy for pollinator distribution.
  - Nectar plant lists for bumblebees and solitary bees developed with CEH experts; sources cited from Carvell et al. (2006) and related studies.
  - For each plot, nectar plant species are counted; plots receive Broad Habitat and Priority Habitat classifications (Jackson 2000; Maskell et al. 2008).
  - Exclusions: coastal/urban habitats are omitted; linear features (hedgerows, streamsides, roadsides) are not included in the model due to Land Cover Map limitations.
  - To predict nectar plant diversity for squares outside Countryside Survey, a Generalised Additive Mixed Model (GAMM) is used with:
    - Response: count of nectar plants per plot (Poisson distribution).
    - Random effect: 1 km square (to account for non-independence of plots within the same square).
    - Covariates: Broad Habitat, air temperature, nitrogen deposition, precipitation, and altitude.
  - Dominant Broad Habitat per 1 km square is used to assign the mean nectar plant count.

- Quality control
  - Methods follow the Defra / NERC Joint Codes of Practice throughout the study.

- References / Supporting documents
  - The document cites multiple methodological and species references (e.g., Biesmeijer et al. 2006; Bunce et al. 2007; Carvell et al. 2006; Jackson 2000; Maskell et al. 2008; Smart et al. 2003, 2008, 2010; Stace 1997; Watson 1981) and includes a table (Table 1) listing the bee nectar plants used in the analysis.