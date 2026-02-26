# Experimental Design/Sampling Regime

- Data source: Countryside Survey 2007, surveying 591 1km squares across Great Britain (GB) using stratified random sampling by land class (geology, soils, etc.).
- Plot design: Within each square, five large randomly placed plots (14.14 m × 14.14 m; 200 m²) with an inner 2 m × 2 m nest for analysis of unenclosed habitats; includes y plots representing remnant semi-natural habitats.
- Scope: Areal features sampled (fields, unenclosed land, small semi-natural biotope patches); focuses on habitats not covered by other plot types.
- Spatial reference: OSGB 1936 / British National Grid (EPSG:27700)

## Data Attributes

- plantCount: modelled estimate of the count of all bee nectar plants within a 1 km × 1 km square.
- SEM: standard error of the mean for the plantCount attribute (variance measure).

## Collection Methods

- Flora surveying: In each vegetation plot, a list of all vascular plants was recorded; a subset of bryophytes and macro-lichens was sampled.
- Nomenclature: Followed Stace (1991) and Watson (1981).
- Abundance estimates: Cover estimated to the nearest 5% for species with at least ~5% cover.

## Analytical Methods

- Purpose: Nectar plant diversity used as a surrogate for pollinator distribution.
- Species lists: Nectar plant species for bumblebees and solitary bees curated with CEH expert input; sources summarized in associated references.
- Plot-level metric: Nectar plant count per vegetation plot; plots classified by Broad and Priority Habitat (Jackson 2000; Maskell et al. 2008).
- Habitat exclusions: Coastal and urban habitats excluded due to limited CS coverage; linear features (hedgerows, streamsides, roadsides) not included in the scaling framework but may be important.
- Modelling: Generalised additive mixed Model (GAMM) to predict nectar plant diversity for non-CS 1 km squares.
  - Response: Count of nectar plants per plot.
  - Random effect: 1 km square to account for non-independence of plots within the same square.
  - Distribution: Poisson.
  - Covariates: Broad Habitat, air temperature, nitrogen deposition, precipitation, and altitude.
  - Prediction: Dominant Broad Habitat in a 1 km square used to assign mean nectar plant count.

## Quality Control

- Adherence to Defra / NERC Joint Codes of Practice throughout data collection and processing.

## Data Availability and Limitations

- Limitations and caveats:
  - Exclusion of coastal and urban habitats may affect representativeness for those environments.
  - Scaling based on Land Cover Map excludes linear features (hedgerows, streamsides, roadsides) which can be important nectar sources, especially in intensively farmed landscapes.
  - Potential incompleteness in meeting user needs due to data availability from a single survey year (2007) and the focus on areal, not linear, features.
- Data handling notes:
  - Data are prepared at plot and square levels with modelled square counts and associated uncertainty (SEM); provenance and references are documented.

## References / Supporting Documents

- Key sources include: Bunce et al. 2007; Smart et al. 2003, 2008; Jackson 2000; Maskell et al. 2008; Carvell et al. 2006; Biesmeijer et al. 2006; and the integrated assessment work (Smart et al. 2010). The dataset includes a long list of bee nectar plant species used in the analysis.