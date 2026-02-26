# Model estimates of expected diversity of positive plant habitat condition indicators

## Aims and scope
- Estimate the diversity of positive plant habitat condition indicators for different Broad Habitats.
- Provide a model-based approach to predict positive habitat indicators in 1 km squares not directly surveyed, supporting monitoring and decision-making.

## Experimental design and sampling regime
- Data source: Countryside Survey 2007, surveying 591 1 km squares across Great Britain using stratified random sampling by land class (geology, soils, etc.).
- Plot types and placement: Within each 1 km square, five large randomly placed plots (x plots) of 14.14 m × 14.14 m (200 m²) with an inner 2 m × 2 m nest; plots chosen to be consistent with unenclosed habitats (u plots) and small semi-natural habitat patches (y plots). This setup helps sample remnant semi-natural habitats not covered by other plot types.
- Habitat indicators: A list of characteristic indicator species for priority habitats was developed from JNCC guidance and BSBI consultation. Indicator identity reflects the Priority Habitats within the Broad Habitat. Some Broad Habitats required alternative indicator lists when published CSM lists were unavailable.

## Indicators and habitat classification
- Indicator metric: percentCSM = (number of CSM plant species in a plot for the habitat type) / (number of characteristic plant species identified for that habitat) × 100.
- SEM: Standard error of the percentage (variance of percentCSM).
- Habitat classification: Each plot assigned to Broad Habitat and Priority Habitat classifications; coastal and urban habitats excluded due to limited CS coverage; linear features (hedgerows, streamsides, roadsides) not included in scaling from the Land Cover Map.

## Spatial reference and data attributes
- Coordinate system: OSGB 1936 / British National Grid (EPSG:27700).
- Data attributes: percentCSM (proportion of positive indicators per plot) and SEM (uncertainty around percentCSM).

## Collection methods and measurement
- Vegetation survey: Within each plot, a list of all vascular plants plus easily identifiable bryophytes and macro-lichens; nomenclature aligned with Stace (1991) and Watson (1981).
- Abundance estimates: Cover for each species estimated to the nearest 5% for species with at least 5% cover.
- Plot classification: Each plot assigned to Broad and Priority Habitat categories (Jackson 2000; Maskell et al. 2008).

## Analytical methods
- In-plot aggregation: Positive habitat indicators summed per plot to produce a count used for analysis.
- Exclusions: Coastal and urban habitats excluded; scaling based on Land Cover Map excludes linear features that may act as refugia.
- Predictive modeling for non-surveyed squares: Generalised additive mixed Model (GAMM) with the response variable as the percentage of positive CSM indicators per plot. 1 km CS square included as a random effect to account for non-independence of plots within the same square; Poisson distribution specified.
- Covariates: Broad habitat, Temperature, Precipitation, Nitrogen deposition, Sulphur deposition, SSSI presence/absence.
- Mapping: Dominant broad habitat within a 1 km square used to create the predictive map of positive habitat indicators.

## Quality control and governance
- Adherence to Defra/NERC Joint Codes of Practice throughout the study and data handling.

## Data limitations and choices
- Some Broad Habitats lacked published CSM lists; for these, alternative “desirable” species lists were used.
- The approach does not account for linear features and excludes certain habitat types (coastal/urban) due to limited coverage.
- Metadata completeness and reliance on originator data are implicit barriers in broader data sharing and verification contexts.

## Outputs and applications
- Model outputs include predicted percentages of positive plant habitat indicators per 1 km square, along with associated uncertainty (SEM).
- Results support monitoring of habitat condition, prioritisation of conservation actions, and informing policy decisions at landscape scales through mapped predictions.

## References and supporting documents
- JNCC guidance, Byfield & Wilson (2005), Jackson (2000), Maskell et al. (2008), Smart et al. (various years), Bunce et al. (2007), Stace (1991), Watson (1981) among others.