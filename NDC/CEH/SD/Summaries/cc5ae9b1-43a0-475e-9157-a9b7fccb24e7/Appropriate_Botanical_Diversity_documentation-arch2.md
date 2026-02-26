# Model estimates of expected diversity of positive plant habitat condition indicators

## Purpose and scope
- Provide a standardized, model-based estimate of positive plant habitat condition across Great Britain by using Countryside Survey (CS) data.
- Enable monitoring of environmental health and policy performance over time through comparable indicators.

## Data and sampling design
- Data source: Countryside Survey 2007, across 591 1km squares using stratified random sampling by land class.
- Plot scheme within each square:
  - Five large plots (x plots): 14.14 m × 14.14 m (200 m2) with an inner 2 m × 2 m nest for analysis.
  - Included areal plots located in fields, unenclosed land, and small semi-natural biotope patches (u and y plots) to capture unenclosed habitats and remnant patches.
- Target habitats: vegetation within Broad Habitats and associated Priority Habitats; some broad habitats lacked CSM lists and used alternative indicators.

## Indicators and habitat classification
- Indicator species aligned with Priority Habitats and Broad Habitat classifications (e.g., AWI for Ancient Woodland, guidance from JNCC/Byfield & Wilson for arable habitats).
- For some Broad Habitats, no explicit CSM lists were available; alternative "desirable" species lists were used.
- Proportion of positive indicators (percentCSM) computed per plot as:
  - percentCSM = (number of CSM indicator species in the plot for that habitat) / (number of characteristic species for that habitat in the plot) × 100
- Data exclude coastal and urban habitats due to CS coverage and scaling basis.

## Spatial reference
- Coordinate System: OSGB 1936 / British National Grid (EPSG:27700)

## Data attributes
- percentCSM: percentage of positive CSM indicator species in a plot for its Broad Habitat.
- SEM: standard error of the percentCSM estimate.
- Each plot classified by Broad Habitat and Priority Habitat.

## Collection methods
- In each plot, all vascular plants and a targeted range of bryophytes and macro-lichens were recorded.
- Nomenclature aligned with Stace (1991) and Watson (1981).
- Cover estimated to the nearest 5% for species with at least 5% cover.

## Analytical methods
- Positive habitat indicators summed per plot; plots assigned Broad and Priority Habitat classifications.
- Exclusions: Coastal and urban habitats; linear features (hedgerows, streamsides, roadsides) not included due to Land Cover Map limitations.
- Model to predict positive plant habitat condition for non-CS 1km squares:
  - Generalised additive mixed Model (GAMM) with percentCSM as response.
  - 1km CS square included as a random effect to account for non-independence of plots within the same square.
  - Distribution: Poisson.
  - Covariables: broad habitat, Temperature, Precipitation, Nitrogen deposition (N dep), Sulphur deposition (S dep), SSSI presence (0/1).
  - Dominant broad habitat within a 1km square used to generate the map.

## Quality control
- Followed Defra/NERC Joint Codes of Practice throughout data handling and analysis.

## Data access and stewardship
- Datasets are produced under standardized monitoring workflows; underlying data are curated and stored for reproducibility and potential reuse in cross-study analyses.

## Supporting references
- Key sources for classifications, indicators, and methodology include JNCC guidance, Byfield & Wilson, Maskell et al., and Smart et al. (various CS-related technical reports and handbooks).