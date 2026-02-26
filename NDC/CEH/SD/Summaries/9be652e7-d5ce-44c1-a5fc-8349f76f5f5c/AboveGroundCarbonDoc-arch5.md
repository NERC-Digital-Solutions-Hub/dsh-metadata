# Carbon stock in the vegetation of Great Britain

## Overview for Data Stewards
- Purpose: Estimate the national vegetation carbon stock for Great Britain using updated data sources and a consistent methodology aligned with Milne & Brown (1997).
- Primary data sources:
  - Countryside Survey (CS) 2007 field data and habitat mapping (Norton et al., 2012)
  - 2007 Land Cover Map (LCMGB) derived from satellite imagery (Morton et al., 2011)
  - National Inventory of Woodland and Trees (2003)
  - Supporting literature and previous benchmarks (Milne & Brown; Carey 2008)
- Output: A dataset labeled “Carbon” representing above-ground vegetation carbon density (tonnes per hectare).

## Data sources and sampling design
- Countryside Survey (CS) started in 1978 with 256 one-kilometre squares, sampled using a stratified design by land classes to ensure unbiased national estimates.
- The CS framework provides spatially explicit habitat types and area extents that underpin national upscaling.
- The 2007 LC Map adds higher-spatial-resolution habitat mapping (approximately 25 m) to improve spatial coherence in mapping carbon stock.

## Carbon density assignment and data preparation
- Non-woodland vegetation: carbon density values are adopted from Milne & Brown and related literature for different land cover types.
- Woodland carbon density: density depends on species and age class because biomass (and thus carbon) scales with tree age.
  - For woodland species, carbon density for each age class is combined into a net density (CDs) using a weighted mean:
    CDs = sum over age classes of (CD_sa × A_sa) / A_sT
    where CD_sa is the density for species s in age class a, A_sa is the area of age class a for species s, and A_sT is the total area covered by species s.
- Age-class and species densities come from Milne & Brown (Table 4) and are combined with species-area distributions from the 2003 National Inventory of Woodlands and Trees.

## Up-scaling methodology (design-based and stratified approach)
- For each land class l, calculate total stock for a given vegetation group by multiplying densities by the land-class-specific relative area (RA_s_l):
  - CSc,l, CSb,l, CSo,l represent total carbon stock in conifers, broadleaves, and other vegetation within land class l, respectively.
  - CS_GB is obtained by summing across land classes: CS_GB = sum_l CS_l, where CS_l is the sum of the different vegetation components in that land class.
- Relative area RA_s_l and total land-class areas are derived from CS 2007 habitat mapping and the Land Cover Map to enable nationwide upscaling.

## Mapping and spatial weighting
- Spatial distribution is refined by weighting the total vegetation carbon stock within each land class by the habitat composition from the 2007 Land Cover Map.
- Conversion ratios adjust densities to align with differences between Countryside Survey extents and Land Cover Map extents, ensuring the sum of stock across the map matches the total from the stratified calculation.
- The resulting maps illustrate higher carbon stock in areas with woodland dominance (e.g., Thetford, Langdale, Kielder forests) and lower stock in areas like the Fens.

## Key results
- Total carbon stock in vegetation across GB: 169.1 Mt C.
- Breakdown by major groups (approximate, from the results table interpretation):
  - Broadleaved woodland: ~106.9 Mt C (about 63% of total)
  - Coniferous woodland: ~40.8 Mt C
  - Other vegetation: ~21.4 Mt C
- Woodland (broadleaves + conifers) accounts for about 87% of total vegetation carbon stock.
- The data are presented per land class across 45 categories, with totals shown for each group and a final GB total.

## Uncertainty and quality assessment
- Uncertainty sources:
  - Habitat area extents from CS 2007 (uncertainty accounted via Carey 2008)
  - Density estimates themselves (woodland densities with an assumed standard error of ±10 t ha^-1 for woodland)
  - Ratios used to weight mapping (conversion factors between CS extents and LC map extents)
- Uncertainty propagation is integrated into the final variance estimates, and standard statistical formulae are used to combine components.

## Data outputs and accessibility
- Output data: “Carbon” dataset representing the carbon density (t C per hectare) stored in above-ground vegetation.
- The approach emphasizes reproducibility by following the Milne & Brown framework, applying explicit equations and transparent data sources.

## Practical implications for data governance
- Provenance and versioning:
  - Data are built from multiple national datasets (CS 2007, LCMGB 2007, NIT 2003); maintain clear provenance and versioned releases as inputs change.
- Metadata and documentation:
  - Document data sources, sampling design, age-class and species density sources, stratification method, and mapping steps, including uncertainty components.
- Reproducibility and stewardship:
  - Provide reproducible workflows (equations and steps) so future updates (new CS years, updated land cover) can be integrated consistently.
- Update and maintenance:
  - Plan for re-calibration when new national inventories or habitat maps become available; ensure conversion ratios and weighting schemes are revisited to maintain consistency with total stock totals.
- Policy and discovery:
  - The dataset supports policy-oriented carbon stock estimation and spatial planning; ensure discoverability within data catalogs with clear usage constraints and data lineage.

## References (data context)
- Milne & Brown (1997) framework for carbon density by land cover and woodland species
- Norton et al. (2012) CS 2007 field survey measurements and habitat mapping
- Morton et al. (2011) Final Report for LCM2007 – high-resolution land cover map
- Carey (2008) CS 2007 headline messages and uncertainty discussion
- Smith & Gilbert (2003) National Inventory of Woodland & Trees
- Other referenced works on habitat classification, allometry, and carbon density literature