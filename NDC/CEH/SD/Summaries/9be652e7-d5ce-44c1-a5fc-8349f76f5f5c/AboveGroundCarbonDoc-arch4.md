# Carbon stock in the vegetation of Great Britain

- This document updates previous Milne & Brown approaches to estimate vegetation carbon stock in Great Britain using the latest available data: Countryside Survey 2007, Land Cover Map 2007, and the 2003 National Inventory of Woodland and Trees.
- The goal is to produce a comparative, design-based estimate of carbon stored in above-ground vegetation across GB and to map its spatial distribution.

## Data sources and approach

- Data sources
  - Countryside Survey of Great Britain (initial 1978 survey with repeated surveys in 1984, 1990, 1998, 2007)
  - 2007 Countryside Survey habitat mapping for land-cover types and relative areas
  - 2007 Land Cover Map (high-resolution satellite-derived habitat mapping)
  - 2003 National Inventory of Woodland and Trees (woodland extent and age-class information)
- Methodology
  - Follow Milne & Brown’s design-based framework to assign carbon density (t/ha) to land cover types
  - Woodland carbon  
    - Treat broadleaved and conifer species separately
    - For each species, compute age-class–specific carbon density and combine using the area proportion of each age class
    - Net per-species density (CDs) is a weighted mean over age classes
  - Up-scaling to GB totals
    - Use land-class strata from Countryside Survey to weight densities by the relative area of each land class and species within each class (RAs_l)
    - Multiply density by relative areas and sum across species and land classes to obtain total vegetation carbon stock by land class, then sum for GB total
  - Mapping refinement
    - Use the 2007 Land Cover Map to spatially weight stock within each land class, enhancing spatial coherence
    - Apply conversion ratios to harmonize densities with the Land Cover Map extents
- Uncertainty
  - Standard errors include habitat-area uncertainty (from CS 2007) and density estimate uncertainty
  - Woodland density uncertainty assumed as ±10 t/ha
  - Variance components combined to produce overall uncertainty

## Carbon densities by cover type

- Carbon densities are provided for broadleaved, coniferous, and other vegetation types, and are used to derive a full GB stock when weighted by habitat distribution.
- The approach accounts for the greater carbon storage in older woodland trees by using age-class–specific densities rather than a single woodland value.

## Spatial mapping and visualization

- Spatial distribution is produced by weighting total vegetation carbon stock within each land class according to the 2007 habitat makeup.
- The resulting maps highlight high-carbon areas (e.g., Thetford Forest, Langdale Forest, Kielder Forest) and low-carbon areas (e.g., fen areas around the Wash).
- Mapping also ensures the sum across mapped areas equals the total stock estimated from land-class data.

## Results

- Total vegetation carbon stock in Great Britain: 169 million tonnes of carbon (Mt C)
  - Broadleaf woodland contributed about 63% of the total stock
  - Woodlands (broadleaf + conifers) accounted for about 87% of the total stock
- Stocks are broken down by land class and vegetation type (detailed per-class totals provided in the study), consistent with the design-based upscaling approach.

## Conclusion

- Using the same analytical framework as Milne & Brown and the updated data sources, the study estimates GB vegetation carbon stock at 169 Mt C.
- The approach provides a transparent, repeatable method for estimating stock and change, with spatially coherent mapping aligned to current land-cover data.

## Output Data

- Carbon: the carbon density (tonnes per hectare) stored in above-ground vegetation, available for policy and planning use.

## References

- Key sources include Milne & Brown (1997), Emerson and colleagues on Countryside Survey methods, Norton et al. (2012) for CS 2007, Morton et al. (2011) for LCM2007, Carey (2008) on 2007 headline messages, and related woodland carbon density studies.