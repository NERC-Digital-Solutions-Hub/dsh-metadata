# Model estimates of expected diversity of positive plant habitat condition indicators

## Overview
- Describes a Generalised Additive Mixed Model (GAMM) approach to estimate the percentage of positive plant habitat condition indicators (CSM indicators) per 1km square using Countryside Survey 2007 data.
- Uses a hierarchical sampling Design across GB: 591 1km squares with multiple vegetation plots to capture habitat-specific indicator species.

## Experimental Design / Sampling Regime
- Data source: Countryside Survey 2007; stratified random sampling by land class (geology, soils, etc.).
- Plot types within each 1km square:
  - x plots: five large randomly-placed plots (14.14 x 14.14 m; 200 m2) with an inner 2 m x 2 m nest for consistency with unenclosed habitats.
  - u plots: located in fields, unenclosed land, and small semi-natural biotope patches.
  - y plots: targeted area habitat plots in small biotopes not covered by other plot types.
- Indicator species: selected as characteristic indicators for priority habitats based on JNCC guidance and BSBI consultation; defined to reflect Broad Habitat composition and its Priority Habitats.
- Some Broad Habitats required alternative indicator lists when published CSM lists were absent.
- Spatial reference: OSGB 1936 / British National Grid (EPSG:27700).

## Data Attributes
- percentCSM: percentage of positive CSM indicator species per plot relative to the characteristic species list for that habitat type.
- SEM: standard error/variance of the percentCSM estimate.
- Other attributes: each plot assigned a Broad Habitat and Priority Habitat classification; dataset includes a list of CSM species by habitat.

## Collection Methods
- Within each plot, all vascular plants counted; a subset of easily identifiable bryophytes and macro-lichens recorded.
- Nomenclature aligned with Stace (1991) and Watson (1981); cover estimates recorded to the nearest 5% for species with ≥ 5% cover.

## Analytical Methods
- Response variable: percentCSM per vegetation plot.
- Model: Generalised Additive Mixed Model (GAMM) with 1km square as a random effect to account for non-independence of plots within the same square; Poisson distribution specified.
- Covariates: broad habitat, Temperature, Precipitation, Nitrogen deposition (N dep), Sulphur deposition (S dep), SSSI presence/absence.
- Mapping: the dominant broad habitat within each 1km square used to generate the spatial map of predicted positive habitat indicators.
- Exclusions and scaling: Coastal and urban habitats excluded; scaling based on the Land Cover Map which omits linear features (hedgerows, streamsides, roadsides) that may act as refugia in certain landscapes.

## Quality Control
- Adherence to Defra/NERC Joint Codes of Practice throughout.

## References / Supporting Documents
- Bunce et al. 2007; Byfield & Wilson 2005; Jackson 2000; Maskell et al. 2008; Smart et al. 2003, 2006, 2007, 2008; Stace 1997; Watson 1981.