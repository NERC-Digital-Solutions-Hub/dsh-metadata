# Carbon in the vegetation of Great Britain

## Purpose and approach
- Builds on Milne and Brown’s approach to estimate vegetation carbon using updated data sources (Countryside Survey, Land Cover Map) to produce a comparable GB-wide stock estimate.
- Focuses on above-ground vegetation carbon density by land cover type, with woodland carbon density treated by species and age class due to biomass–carbon relationships.

## Data and sampling framework
- Countryside Survey of Great Britain (started 1978) used 256 one-km squares as sampling units to map all features within each square and derive national estimates.
- Stratified sampling by land classes to ensure representative coverage across environments; repeat surveys occurred in 1984, 1990, 1998, and 2007, with 2007 providing the latest data used here.
- Relative area by land class (RA_s,l) derived from 2007 habitat mapping to weight density estimates spatially.

## Carbon density estimation (woodlands and other types)
- Non-woodland and woodland carbon densities established by land cover type; woodland carbon requires age-class adjustments because tree carbon scales with biomass.
- For woodlands, carbon density for each broadleaved and coniferous species is calculated using age-class specific densities weighted by the area covered by each age class.
- Net carbon density for each woodland species (CD_s) computed as a weighted mean across age classes:
  CD_s = sum_a (CD_sa * A_sa) / A_sT
- The full suite of density estimates combines woodland (broadleaf and conifer), and other vegetation types to produce national stock estimates.

## Spatial mapping and weighting
- Initial upscaling uses land-class stratification to estimate total stock per class, then summed to GB total.
- To produce spatially coherent maps, the 2007 Land Cover Map (LCM2007) is used to weight stock within each land class by actual habitat distribution, improving spatial realism and continuity.
- Conversion ratios adjust densities to reflect differences between Countryside Survey extents and land-cover map extents, ensuring consistency between map-weighted stock and class totals.

## Results
- Estimated total vegetation carbon stock in Great Britain: 169 million tonnes of carbon (MtC).
- Woodland contribution: Broadleaf woodlands account for about 63% of the total; woodlands overall (including conifers) account for about 87% of the stock.
- The spatial weighting highlights higher stock in woodland-dense areas (e.g., Thetford Forest, Langdale Forest, Kielder Forest) and lower stock in open agricultural/grassland areas (e.g., Fens).
- Uncertainty: standard errors incorporated from habitat area estimates (CS2007) and density estimates; woodland density uncertainties approximated at ±10 t/ha for consistency with Milne & Brown.

## Output data
- Data product: “Carbon” representing the carbon density (tonnes per hectare) stored in above-ground vegetation.

## Implications for GIS and policy
- Demonstrates how to integrate stratified field data with high-resolution land-cover maps to produce spatially explicit carbon stock maps.
- Provides a reproducible framework for updating GB vegetation carbon stocks as new survey data become available.
- Maps enable policy and planning analyses by identifying high-carbon areas and monitoring spatial patterns in vegetation carbon stock.

## References (key influences)
- Milne, R. & Brown, T.A.; Countryside Survey data (1990 and 2007); Norton et al. 2012; LCM2007; Chave et al. 2005; Carey 2008; and related design-based estimation approaches.