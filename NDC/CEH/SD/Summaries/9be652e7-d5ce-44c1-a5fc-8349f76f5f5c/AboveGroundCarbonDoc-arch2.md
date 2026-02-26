# Carbon in the vegetation and soils of Great Britain

## Introduction
- This work follows the approach of Milne and Brown (1997), updating base carbon density estimates with the latest data from Countryside Survey 2007, Land Cover Map (2011), and National Forest Inventory (2003).
- Objective: produce a consistent, comparable estimate of vegetation carbon stock for Great Britain to assess change and policy relevance.

## Data and methods
- Countryside Survey (CS): initiated in 1978 to nationally audit countryside; used 256 one-km squares as sampling units across GB with stratified land classes to ensure unbiased estimates; repeat surveys in 1984, 1990, 1998, and 2007 (CS 2007 was the largest).
- Carbon density assignment:
  - Non-woodland densities drawn from literature.
  - Woodland carbon density treated by species and age class due to biomass effects; older trees store more carbon.
  - For woodland species s, net density CDs calculated as a weighted mean across age classes: CDs_s = sum(CD_sa * As_a) / As_T.
  - Density estimates for woodland then combined with densities for other land cover types to upscale to GB stock.
- Up-scaling to GB:
  - Use relative area by land class (RAs_l) from CS 2007 to weight densities.
  - Compute carbon stock per land class for conifers, broadleaves, and other vegetation; sum across land classes to obtain total GB stock.
  - Uncertainty: combine habitat area uncertainty (from Carey 2008) with density uncertainties; woodland density uncertainty assumed ±10 t ha^-1.
- Mapping approach:
  - Spatially weight total vegetation carbon stock within land classes using the 2007 Land Cover Map (25 m resolution) to reflect actual habitat makeup.
  - Apply conversion ratios to align densities with Land Cover Map estimates, ensuring that mapped totals equal stratified estimates.

## Results
- Total vegetation carbon stock in GB: 169 million tonnes (Mt) of carbon.
- Category contributions:
  - Broadleaved woodland: the largest share, contributing about 63% of the total stock.
  - Woodlands (broadleaves + conifers): collectively about 87% of the total stock.
  - Conifers and other vegetation contribute smaller shares (details presented per land class in the full results).
- Spatial pattern: high vegetation carbon in forested areas (e.g., Thetford Forest, Langdale Forest, Kielder Forest) and low carbon in open flatlands such as the Fens.

## Conclusion
- By replicating the Milne & Brown analytical framework with updated datasets, the study estimates GB vegetation carbon stock at 169 Mt, reinforcing the primacy of woodland vegetation in national carbon stocks.

## Output Data
- Carbon: the carbon density (tonnes per hectare) stored in above-ground vegetation.