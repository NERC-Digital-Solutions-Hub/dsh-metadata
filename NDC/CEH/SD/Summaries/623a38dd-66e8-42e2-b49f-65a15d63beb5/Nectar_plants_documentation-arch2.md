Nectar plant diversity as a surrogate for pollinators in Countryside Survey data (GB, 2007)

- Aim
  - Use nectar plant diversity as a surrogate for pollinator distribution to assess environmental health and ecosystem service potential.
  - Leverage Countryside Survey (CS) 2007 data to model nectar plants across Great Britain and support broader environmental monitoring.

- Experimental Design / Sampling Regime
  - Data from Countryside Survey 2007 comprising 591 one-kilometre squares, stratified by land class (geology, soils, etc.).
  - Within each square, five large random plots (x plots) of 14.14 x 14.14 m (200 m2) with an inner 2 m x 2 m nest used for this analysis to align with plots sampling unenclosed habitats (u plots) and small biotopes (y plots).
  - y plots represent remnant semi-natural habitat patches historically more widespread.
  - Areal features sampled; focus on fields, unenclosed land, and small semi-natural patches.

- Spatial Reference
  - Coordinate System: OSGB 1936 / British National Grid (EPSG:27700).

- Data Attributes
  - plantCount: modelled estimate of the count of all bee nectar plants within each 1 km x 1 km square.
  - SEM: standard error (variance measure) for the plantCount attribute.

- Collection Methods
  - In each vegetation plot, compile a list of all vascular plants plus a targeted set of bryophytes and macro-lichens.
  - Nomenclature aligned with Stace (1991) and Watson (1981).
  - Cover estimated to the nearest 5% for species ≥ 5% cover.

- Analytical Methods
  - Nectar plant diversity used as a proxy for pollinator distribution; supported by prior work linking declines in pollinators with declines in nectar plants.
  - Nectar plant species lists for bumblebees and solitary bees created with CEH expert input (sources cited in Carvell et al. 2006; integrated assessment Smart et al. 2010).
  - For each plot, nectar plant species counted to yield a per-plot metric.
  - Each plot assigned a Broad and Priority Habitat classification (per Jackson 2000; Maskell et al. 2008).
  - Coastal and urban habitats excluded due to CS coverage; linear features (hedgerows, streamsides, roadsides) not included in the model but recognized as potential nectar sources.
  - To predict nectar plant counts in 1 km CS squares not part of CS, a Generalised Additive Mixed Model (GAMM) was used:
    - Response: count of nectar plants per plot.
    - Random effect: 1 km CS square to account for within-square non-independence.
    - Distribution: Poisson.
    - Covariates: Broad Habitat, air temperature, nitrogen deposition, precipitation, and altitude.
    - The dominant Broad Habitat in a 1 km square determined the mean nectar plant count for that square.

- Quality Control
  - Adherence to Defra / NERC Joint Codes of Practice throughout.

- Data Use and Integration
  - Outputs include standardized nectar plant counts and habitat classifications suitable for integration with other environmental data.
  - Model framework supports extrapolation to unsampled squares (via GAMM) and potential augmentation with additional data sources.

- References / Supporting Documents
  - Key sources supporting nectar plant–pollinator relationships, habitat classifications, and CS methodologies (e.g., Biesmeijer et al. 2006; Bunce et al. 2007; Carvell et al. 2006; Jackson 2000; Maskell et al. 2008; Smart et al. 2003, 2008, 2010; Stace 1997; Watson 1981).

- Table 1: List of bee nectar plants used in analysis
  - Contains an extensive list of species (e.g., Acer pseudoplatanus, Achillea millefolium, etc.) used to define the nectar plant dataset for pollinator considerations.