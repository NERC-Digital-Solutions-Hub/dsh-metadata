# Experimental Design/Sampling Regime

- Study basis: Countryside Survey 2007; 591 one-kilometre squares sampled across Great Britain using a stratified random design by land class (geology, soils, etc.).
- Plot design within each square:
  - Five large random plots (x plots) measuring 14.14 m × 14.14 m (200 m²).
  - Inner nest within each plot of 2 m × 2 m used for this analysis to align with unenclosed habitats.
  - Additional plots (y plots) target semi-natural habitats and small biotopes; y plots often represent remnant habitats historically more widespread.
- Focus: areal features (fields, unenclosed land, small semi-natural biotope patches).

## Spatial Reference

- Coordinate System: OSGB 1936 / British National Grid (EPSG:27700)

## Data Attributes

- plantCount: modeled estimate of the count of all bee nectar plants within a 1 km × 1 km square.
- SEM: standard error/variance measure of the plantCount attribute.

## Collection Methods

- Within each vegetation plot:
  - List all vascular plants and a targeted set of bryophytes and macro-lichens.
  - Nomenclature aligns with Stace (1991) and Watson (1981).
  - Cover estimates recorded to the nearest 5% for species with estimated cover of at least 5%.

## Analytical Methods

- Nectar plant diversity used as a surrogate for pollinator distribution.
- Nectar plant species per plot summed to yield a count; each 1 km CS square treated as a random effect to account for non-independence of plots within the same square.
- Modeling approach:
  - Generalised Additive Mixed Model (GAMM) with Poisson distribution.
  - Covariates: Broad Habitat, air temperature, nitrogen deposition, precipitation, and altitude.
  - The dominant Broad Habitat in a 1 km square used to assign the mean nectar plant count.
- Habitat classification:
  - Each plot assigned a Broad and Priority Habitat classification (Jackson 2000; Maskell et al. 2008).
  - Coastal and urban habitats excluded due to limited coverage by Countryside Survey data.

## Data Scope, Limitations and Assumptions

- Scaling to non-CS 1 km squares uses the GAMM with square as random effect.
- Limitations due to data sources:
  - Scaling relies on Land Cover Map Broad habitats; linear features (hedgerows, streamsides, roadsides) are not included, potentially omitting important nectar sources in agricultural areas.
  - Coastal and urban habitats are excluded, possibly omitting relevant nectar plant diversity in some landscapes.
- Linear features and fine-scale habitat connectivity not captured by Broad Habitat classification.

## Quality Control

- Adherence to Defra / NERC Joint Codes of Practice throughout data handling and processing.

## References / Supporting Documents

- Key literature supporting methodology and habitat classifications (e.g., Biesmeijer et al. 2006; Bunce et al. 2007; Carvell et al. 2006; Jackson 2000; Maskell et al. 2008; Smart et al. various; Stace 1997; Watson 1981).

## Table 1: Table of bee nectar plants used in analysis

- Comprehensive list of nectar plant species used (example taxa provided, including numerous tree, herb, shrub, and herbaceous species such as Acer pseudoplatanus, Achillea millefolium, Cardamine pratensis, Helianthus annuus, Vicia sativa, Trifolium pratense, and many others).