# Model estimates of expected diversity of positive plant habitat condition indicators

## Overview
- Analyzes Countryside Survey 2007 data to estimate expected diversity of positive plant habitat condition indicators (CSM) across Great Britain.
- Aims to predict positive habitat indicators for 1 km squares not part of Countryside Survey using a statistical model and to map by dominant broad habitat.
- Uses a combination of plot-level data and habitat classifications to produce a self-contained data product for broader use.

## Data and Sampling Design
- Source: Countryside Survey 2007 with 591 1 km squares across GB, stratified by land class.
- Plot types within squares: five large randomly placed plots (x plots), with an inner 2 m x 2 m nest; supplemented by y plots and unenclosed habitat plots (u plots) to capture semi-natural patches.
- Habitat indicators: selected from Joint Standards Monitoring (JNC/ BSBI guidance) reflecting Priority Habitats within each Broad Habitat.
- Exclusions: coastal and urban habitats; linear features (hedgerows, streamsides, roadsides) not included due to Land Cover Map limitations.

## Data Attributes
- percentCSM: percentage of positive CSM indicator species per plot, calculated as (number of CSM species for habitat) / (number of characteristic species for that habitat) × 100.
- SEM: standard error of the percentCSM for each plot.
- Spatial reference: OSGB 1936 / British National Grid (EPSG:27700).

## Data Collection Methods
- Vegetation plots recorded all vascular plants and a select range of bryophytes and macro-lichens.
- Nomenclature aligned with Stace (1991) and Watson; cover estimates recorded to the nearest 5% for species ≥5% cover.

## Analytical Methods
- Aggregation: Positive habitat indicators summed per plot; each plot assigned Broad and Priority Habitat classifications.
- Mapping consideration: dominant broad habitat within a 1 km square used for visualization.
- Modelling approach: Generalised Additive Mixed Model (GAMM) to predict percentCSM in non-CS 1 km squares.
  - Response: percentCSM per plot.
  - Random effect: 1 km CS square to account for non-independence of plots within the same square.
  - Distribution: Poisson.
  - Covariates: broad habitat, Temperature, Precipitation, Nitrogen deposition, Sulfur deposition, SSSI presence/absence.
- Output: model-based predictions used to create habitat-condition maps aligned with the dominant broad habitat.

## Quality Control and Governance
- Adherence to Defra/NERC Joint Codes of Practice throughout the study.

## Data Limitations and Scope
- Limitations: exclusion of coastal/urban habitats; scaling based on Land Cover Map that omits linear features; potential non-independence addressed via random effects but still subject to patchy data and varying data quality across plots.
- Scope note: model predictions apply to 1 km squares not covered by Countryside Survey and rely on broad habitat classification and environmental covariates.

## Potential Data Products and Uses (Data Support Perspective)
- Spatial maps of predicted positive habitat-condition indicators by 1 km square and dominant broad habitat.
- Plot-level dataset of percentCSM and SEM for each vegetation plot, with habitat classifications.
- Model parameterizations (GAMM inputs and covariates) for reproducing or updating predictions with new data.
- Dashboards or reports summarizing habitat-condition indicators across regions to support policy or conservation planning.

## References / Supporting Documents
- Bunce et al. 2007; Byfield & Wilson 2005; Jackson 2000; Maskell et al. 2008; Smart et al. 2003, 2006, 2008; Stace 1991; Watson 1981.