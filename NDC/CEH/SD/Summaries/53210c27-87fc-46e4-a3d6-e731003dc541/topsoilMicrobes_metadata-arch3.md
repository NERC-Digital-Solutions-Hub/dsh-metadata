# Topsoil microbe model estimates [Countryside Survey]

## Overview
- Dataset provides model estimates of topsoil microbial metrics (0–15 cm depth) from the Countryside Survey (CS) in Great Britain.
- Fields bacterial community structure (NMDS axis 1), Shannon diversity, and Simpson diversity.
- Based on >1000 samples from 233 one-km squares collected in 2007.

## Data scope and spatial coverage
- Spatial framework: OSGB 1936 / British National Grid (EPSG:27700).
- Coverage: GB land areas sampled in 2007; areas such as urban and littoral rock are not represented (no associated data).

## Key variables and attributes
- LCM_CLASS, LCM_NUMBER: Derived from Land Cover Map 2007 (habitat classification).
- SOIL_GROUP, CACO3_RANK: Derived from BGS Soil Parent Material Model (soil type and carbonate content).
- NMDS107: Mean axis-1 scores of bacterial community structure (modelled by LCM_CLASS and CACO3_RANK).
- NMDS107_SE: Standard error for NMDS axis-1 scores.
- MSHAN07, MSIMP07: Mean Shannon and Simpson diversity indices (modelled by LCM_CLASS and SOIL_GROUP).
- MSHAN07_SE, MSIMP07_SE: Standard errors for the diversity indices.

## Modelling approach
- Estimates are produced as mean values for habitat/parent material combinations.
- Modelling uses dominant habitat from LCM2007 and parent material from the Soil PMM (2009); the parent material variable chosen to minimize AIC in each model.
- Some areas (e.g., urban, littoral rock) have no data; some habitat/parent material combinations have insufficient sample sizes.

## Methods and experimental design
- Sampling: >1000 plots within 233 1-km squares as part of the 2007 CS.
- Collection: Soil cores (15 cm long, 4 cm diameter) following CS field protocols.
- Analytical methods: Molecular community profiling via tRFLP; bacterial community similarities assessed with 2D NMDS ordination.
- Diversity metrics computed from relative abundances of tRFLP peaks.

## Data access and provenance
- Dataset citation: Henrys et al. (2014). Model estimates of topsoil microbes [Countryside Survey].
- Access via NERC Environmental Information Data Centre (EIDC): https://doi.org/10.5285/53210c27-87fc-46e4-a3d6-e731003dc541
- References for methods and context: Emmett et al. (2008), Griffiths et al. (2011), Scott (2008), Emmett et al. (2010), and related CS technical reports.
- Coordinate and data source links: Land Cover Map 2007; Soil PMM (British Geological Survey).

## Quality control and limitations
- Quality control details are provided in Griffiths et al. (2011); further methodological details in Emmett et al. (2008, 2010) and related CS reports.
- Limitations for monitoring use:
  - Spatial gaps: urban and some habitat/parent material combinations are not represented.
  - Temporal gap: data are from 2007; applicability to current monitoring requires consideration of change over time.
  - Modelling uncertainty: relies on AIC-driven selection and represents mean estimates with associated standard errors.

## Implications for monitoring frameworks
- Demonstrates a framework for producing large-scale, habitat- and material-specific microbial indicators.
- Illustrates integration of field sampling, molecular analyses, and multivariate ordination into actionable monitoring outputs.
- Highlights governance considerations relevant to monitoring frameworks:
  - Metadata linkage between land cover, parent material, and microbial metrics.
  - Data accessibility and openness via public data centres.
  - Need for clear documentation of data provenance, methods, and uncertainty.
  - Constraints when sharing underlying data and ensuring dataset quality at the source.