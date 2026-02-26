# Experimental Design/Sampling Regime

- Based on Countryside Survey 2007
- Survey of 591 one-kilometre squares across Great Britain, stratified by land class (geology, soils, etc.)
- Within each square, five large vegetation plots (x plots) measuring 14.14 m × 14.14 m (200 m2) with an inner 2 m × 2 m nest
- The inner nest plots are used for consistency with other plot types (u plots and y plots)
- Y plots represent remnant semi-natural habitat patches not sampled by other plot types
- Restricted randomisation to reduce aggregation and spatial clustering
- Only areal features (fields, unenclosed land, small semi-natural biotopes) sampled for this analysis

## Spatial Reference

- Coordinate System: OSGB 1936 / British National Grid (EPSG:27700)

## Data Attributes

- plantCount: modelled estimate of the count of all bee nectar plants within a 1 km × 1 km square
- SEM: standard error (variance) of the plantCount attribute

## Collection Methods

- In each vegetation plot, compile a list of all vascular plants
- Include a selected range of easily identifiable bryophytes and macro-lichens
- Nomenclature follows Stace (1991) and Watson (1981)
- Cover estimates recorded to the nearest 5% for species with at least ~5% cover

## Fieldwork and Laboratory Instrumentation

- Not applicable (N/A)

## Calibration Steps and Values

- Not applicable (N/A)

## Analytical Methods

- Nectar plant diversity used as a surrogate for pollinator distribution
- Nectar plant species lists for bumblebees and solitary bees compiled from CEH experts and sources (Carvell et al. 2006; referenced in Smart et al. 2010)
- For each plot, nectar plant species counted to yield a plot-level count
- Each 1 km square assigned Broad and Priority Habitat classifications (Jackson 2000; Maskell et al. 2008)
- Coastal and urban habitats excluded due to limited CS coverage; scaling based on the Land Cover Map excludes linear features (hedgerows, streamsides, roadsides)
- To predict nectar plant diversity for non-CS squares, a Generalised Additive Mixed Model (GAMM) with Poisson distribution
  - Response: count of nectar plants per plot
  - Random effect: 1 km CS square to account for non-independence of plots within the same square
  - Covariables: Broad Habitat, air temperature, nitrogen deposition, precipitation, altitude
  - Outcome: mean nectar plant count per square based on the dominant Broad Habitat

## Quality Control

- Adherence to Defra/NERC Joint Codes of Practice throughout

## References / Supporting Documents

- Key sources include: Biesmeijer et al. (2006); Bunce et al. (2007); Carvell et al. (2006); Jackson (2000); Maskell et al. (2008); Smart et al. (2003, 2008, 2010); Stace (1997); Watson (1981)

## Table 1: List of Bee Nectar Plants Used in Analysis

- Comprehensive species list provided (including species names with BRC identifiers)
- Used to tabulate nectar plant diversity per plot for the analyses