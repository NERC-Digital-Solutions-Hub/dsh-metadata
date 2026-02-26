# Carbon density of vegetation in Great Britain

## Aim
- Estimate the carbon stock stored in vegetation across Great Britain (GB) by updating Milne and Brown’s approach with recent data.
- Use base-level carbon density estimates by land cover type and age-class–specific woodland data to enable upscaling to national totals and mapping.

## Data sources
- Countryside Survey (CS) of Great Britain: since 1978, sampling 256 one-km squares with stratified land-class design to enable unbiased national estimates; surveys conducted in 1984, 1990, 1998, and 2007 (the largest to date).
- Land Cover Map (LCM) 2007 and its habitat mapping to derive spatial extents and relative areas.
- 2003 National Inventory of Woodlands and Trees for woodland extent and age-class distribution.
- Supplementary data and literature to assign carbon densities to non-woodland land covers and to woodland age classes (per Milne & Brown).

## Methodology
- Non-woodland carbon densities: taken from published literature; used for most land-cover types with relatively low carbon storage.
- Woodland carbon densities: require age-class–dependent treatment because biomass (and thus carbon) increases with tree age. For each woodland species and age class, carbon density is taken from Milne & Brown and updated with 2007 CS and 2003 woodland inventory data.
- Net density for woodland species s is computed as a weighted mean over age classes a:
  CDs_s = sum over a of (CD_sa * Asa) / AsT
  where CD_sa is the density for species s in age class a, Asa is the area of age class a for species s, and AsT is the total area of species s.
- Upscaling to GB stock:
  - Use relative area by land class (RAs_l) from the 2007 CS habitat mapping.
  - Compute per-land-class stocks for conifers, broadleaves, and other vegetation:
    CS_c,l = X_c,l * sum over species of (CD_s * RA_sl)
    CS_b,l = X_b,l * sum over broadleaves of (CD_s * RA_sl)
    CS_o,l = X_o,l * sum over other vegetation of (CD_nu * RA_nu,l)
    where X_c,l, X_b,l, X_o,l are the total areas of conifers, broadleaved woodland, and other vegetation in land class l.
  - Total per land class: CS_l = CS_c,l + CS_b,l + CS_o,l
  - GB total: CS_GB = sum over all land classes l of CS_l
- Uncertainty: combine CS2007 habitat-area uncertainty (Carey 2008) and density estimate uncertainty; for woodland densities, assume ±10 t/ha as a standard error.
- Mapping refinement: weight GB stock by the 2007 LC Map to produce a spatially coherent distribution; apply conversion ratios to align density estimates with LCMap extents so the map’s total matches the upscaled total.

## Mapping approach
- Visualize spatial distribution by land-class stock, then refine with LC Map (25 m resolution) to reflect actual habitat occurrences.
- Use density conversion factors to ensure the mapped total equals the mapped-area total.

## Results
- Estimated total stock of carbon stored in GB vegetation: 169 million tonnes of carbon (Mt C).
- Woodland contribution:
  - Broadleaved woodland accounts for about 63% of the total stock.
  - All woodland (broadleaved + coniferous) accounts for about 87% of the total stock.
- Distribution across land classes and species is detailed in CS output, with the total GB stock combining broadleaved, coniferous, and other vegetation across 45 land classes.

## Output data
- "Carbon" dataset: carbon density (tonnes per hectare) stored in above-ground vegetation, by cover type, suitable for mapping and further analysis.

## Conclusion
- By applying Milne & Brown’s analytical framework with updated data (CS 2007, LC Map 2007, and 2003 woodland inventory), GB vegetation carbon stock is estimated at 169 Mt.
- The approach validates the previous methodology while incorporating newer datasets, enabling spatially explicit mapping and policy-relevant stock-change assessments.

## References (selected)
- Milne, R. & Brown, T.A. (1997). Carbon in the vegetation and soils of Great Britain.
- Norton, L.R. et al. (2012). Measuring stock and change in the GB countryside for policy—key findings from the Countryside Survey 2007.
- Carey, P.D. (2008). Countryside Survey: UK headline messages from 2007.
- Morton, D. et al. (2011). Final Report for LCM2007—UK land cover map.
- Smith, S. & Gilbert, J. (2003). National Inventory of Woodland & Trees.