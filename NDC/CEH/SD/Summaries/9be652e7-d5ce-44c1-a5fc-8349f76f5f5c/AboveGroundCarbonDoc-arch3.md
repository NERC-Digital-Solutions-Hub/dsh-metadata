# Carbon in the vegetation of Great Britain

- Objective and approach
  - Update national estimates of carbon stored in vegetation across Great Britain using Milne and Brown’s framework, with updated data from the 2007 Countryside Survey (CS), the 2007 Land Cover Map (LCM2007), and the 2003 National Inventory of Woodlands and Trees.
  - Follow the design-based, stratified sampling approach to enable unbiased national estimates and assess change over time.

- Data and sampling design
  - Countryside Survey (GB) since 1978: 256 one-km squares randomly located within land-class strata to capture environmental heterogeneity; repeated surveys in 1984, 1990, 1998, and 2007.
  - Land-class stratification ensures representative sampling across environments and enables upscaling to national totals.

- Carbon density estimation
  - Non-woodland vegetation: assign carbon density values from the literature (consistent with Milne & Brown, 1997).
  - Woodland: account for tree biomass by species and age class, using age-class specific carbon densities and area proportions from the 2003 National Inventory of Woodlands and Trees.
  - Net carbon density for each woodland species is calculated as a weighted mean across age classes:
    CDs_s = sum_a (CD_sa * A_sa) / A_sT
    where CD_sa is density for species s, age class a; A_sa is area of age class a; A_sT is total area of species s.
  - Combine woodland densities with densities for other land-cover types to obtain full vegetation carbon densities for each land-cover type.

- Upscaling to national stock
  - Use habitat mapping data from the 2007 Countryside Survey to derive relative areas by land class (RAs_l) and compute total carbon stock per land class and per vegetation type.
  - Core equations relate density estimates to land-class areas and sum across land classes to obtain GB totals:
    CS_c,l = X_c,l * sum over conifers of (CD_s * RA_sl)
    CS_b,l = X_b,l * sum over broadleaves of (CD_s * RA_sl)
    CS_o,l = X_o,l * sum over other vegetation of (CD_nu * RA_nl)
    CS_GB = sum_l CS_l = sum_l (CS_c,l + CS_b,l + CS_o,l)
  - Standard error incorporates uncertainty in habitat extents (CS2007) and density estimates; a cross-component standard error of ±10 t ha^-1 for woodland density is applied and combined with other variance components.

- Mapping and spatial refinement
  - Initial maps reflect land-class stock distributions, which can yield abrupt boundaries.
  - Refined spatial distribution by weighting stock estimates with the high-resolution (25 m) Land Cover Map GB (LCM2007) to reflect actual habitat occurrences, enhancing spatial coherence.
  - Apply conversion ratios to align densities with habitat extents between CS field data and the Land Cover Map, ensuring the mapped total matches the summed land-class estimate.

- Results
  - Total vegetation carbon stock in GB: 169 million tonnes of carbon (MtC).
  - By vegetation category (across 45 land classes)
    - Broadleaf woodland contributes about 63% of total stock.
    - All woodlands (broadleaf + conifers) account for roughly 87% of total stock.
  - Spatial pattern highlights: high stocks in large forested areas (e.g., Thetford Forest, Langdale Forest, Kielder Forest); lower stocks in fen and low-vegetation areas.

- Conclusion
  - Reproduction of Milne & Brown’s analytical framework with updated datasets confirms a GB vegetation carbon stock of 169 MtC, illustrating how design-based sampling, species-age structuring for woodland, and spatial weighting with high-resolution habitat maps yield robust national estimates.

- Output data
  - "Carbon" – carbon density (tonnes per hectare) stored in above-ground vegetation.