# Experimental Design/Sampling Regime

- Source and scope: Countryside Survey 2007 data; 591 one-kilometre squares sampled using a stratified random design by land class (geology, soils, etc.); within each square, five large randomly-placed plots (x plots) of 14.14 m × 14.14 m (200 m²) with an inner 2 m × 2 m nest, aligned with plots sampling unenclosed habitats (u plots) and small biotopes (y plots) to capture remnant semi-natural patches.
- Areal focus: Analysis uses only areal features (fields, unenclosed land, small semi-natural patches); excludes coastal and urban habitats from the nectar-pollinator model.
- Objective: Estimate nectar plant diversity as a surrogate for pollinator distribution and model 1 km square nectar plant counts to infer potential pollinator availability.
- Spatial reference: OSGB 1936 / British National Grid (EPSG: 27700)

## Data Attributes

- plantCount: Modelled estimate of the count of all bee nectar plants within a 1 km × 1 km square.
- SEM: Standard error/variance measure for the plantCount attribute.

## Collection Methods

- Vegetation sampling: In each plot, compile a list of all vascular plants and a targeted set of bryophytes and macro-lichens; nomenclature follows Stace (1991) and Watson (1981).
- Abundance estimates: Estimate cover to the nearest 5% for species reaching at least about 5% cover.
- Taxonomic scope: Focus on nectar plant species relevant to bumblebees and solitary bees; Table 1 lists these species (with scientific names and identifiers).
- Habitat classification: Each vegetation plot is assigned a Broad Habitat and a Priority Habitat classification (per Jackson 2000 and Maskell et al. 2008).

## Analytical Methods

- Rationale: Nectar plant diversity is used as a proxy for pollinators based on evidence linking pollinator declines to declines in nectar-rich forage (e.g., Biesmeijer et al. 2006).
- Data preparation: Nectar plant species per plot aggregated to a count per vegetation plot; Dominant Broad Habitat in each 1 km square used to assign mean nectar plant count.
- Model and distribution: Generalised Additive Mixed Model (GAMM) with a Poisson response; 1 km CS square included as a random effect to account for non-independence of plots within the same square.
- Predictors (covariates): Broad Habitat, air temperature, nitrogen deposition, precipitation, and altitude.
- Scale and extrapolation: The model is used to predict nectar plant diversity for 1 km squares not part of the Countryside Survey; scaling relies on the dominant Broad Habitat.
- Limitations: Does not incorporate linear features (hedgerows, streamsides, roadsides) which can be important nectar sources, particularly in large-field, intensive-agriculture areas; scaling is based on Broad Habitat classes from the Land Cover Map and may miss fine-scale habitat features.

## Quality Control

- Compliance: Follow Defra / NERC Joint Codes of Practice throughout data collection and processing.

## References / Supporting Documents

- Key sources include:
  - Biesmeijer et al. (2006) on pollinator-plant relationships
  - Bunce et al. (2007) land classification
  - Carvell et al. (2006) foraging declines of bumblebees
  - Jackson (2000) and Maskell et al. (2008) habitat classifications and mapping
  - Smart et al. (2003, 2008, 2010) vegetation sampling and integrated assessments
  - Stace (1997) flora reference; Watson (1981) bryophyte references

## Table 1: Nectar Plants

- Contains the list of bee nectar plants used in the analysis, including scientific names and associated identifiers (extensive species list).