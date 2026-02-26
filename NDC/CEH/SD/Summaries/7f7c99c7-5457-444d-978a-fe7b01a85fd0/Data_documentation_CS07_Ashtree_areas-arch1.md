# Countryside Survey: Ash tree distribution in areas <5ha,  2007

## Summary
- Dataset: CS07_ashtree_areas, estimates of ash trees for Great Britain within broadleaved woodland areas smaller than 5 hectares, based on Countryside Survey 2007.
- Purpose: Provide national estimates of the areal extent of ash in small broadleaved woodlands.
- Resolution and extent: 1 km resolution, extent across Great Britain; coordinate system OSGB36 (British National Grid), projection Transverse Mercator.
- Data structure: Associated with ITE Land Classification (1990) and Land Cover Map 2007 (1 km raster); the Countryside Survey dataset framework.
- Key result representation: Each 1 km square is assigned a band (Gridcode 1–7) indicating the estimated hectares of ash per km square (Ha_per_km) using seven categories: 0-0.2, 0.2-0.4, 0.4-0.6, 0.6-0.8, 0.8-1, 1-5, >5.

## Data details and structure
- Columns:
  - Gridcode: Code for band interval related to ash hectares per km square (1–7).
  - Ha_per_km: Estimated hectares of ash per km square, stored in seven bands (0-0.2, 0.2-0.4, 0.4-0.6, 0.6-0.8, 0.8-1, 1-5, >5) (text).
- Data origin: Based on Countryside Survey measurements (2007) in areas of broadleaved woodland <5 ha.
- Associated datasets:
  - ITE Land Classification (1990)
  - Land Cover Map 2007 (1 km raster)
  - Countryside Survey (www.countrysidesurvey.org.uk)

## Methods and calculation approach
- Sampling framework: Countryside Survey samples 1 km squares across GB using stratified random sampling by land classes derived from ecological gradients.
- Habitat mapping within squares: Each square is mapped to Broad or Priority Habitat; dominant species recorded by percentage cover categories (e.g., <10%, 10–25%, 25–50%, 50–75%, 75–95%, 95–100%).
- Scope within woodland: Analyses focus on woodlands <0.5 ha to avoid duplication with Forestry Commission data.
- Calculation process:
  - Use the mid-point of ash percentage cover within each 1 km square by land class to derive mean ash woodland area.
  - Multiply the mean ash area by the land class area, then sum across land classes to yield a national hectare estimate for ash extent in GB.
  - Land classification basis: 1990 ITE Land Classification with 32 land classes.
  - Scaling: Means per land class are weighted by the proportion of Broadleaved Woodland in each 1 km square as per Land Cover Map 2007.

## Scope, scale, and limitations
- Temporal scope: Estimates reflect ash distribution in 2007.
- Spatial scope: GB-wide, limited to broadleaved woodland areas <5 ha per the dataset description.
- Scale and detail considerations: 1 km grid resolution; reliance on mid-point cover categories which may mask finer-scale variation.
- Data integration: Uses multiple datasets (ITE Land Classification, LCM2007) for weighting and scaling; potential limitations in harmonising across datasets and scales.
- Notes on accessibility and analysis: The dataset is designed for national estimation and may require access to associated CS resources for full methodological context.

## Access, references, and further reading
- Primary source: Countryside Survey: Ash tree distribution in areas <5ha, 2007 – CEH/Lancaster
- Further reading and methodological references:
  - Distribution of Ash trees (Fraxinus excelsior) in Countryside Survey data (2013) – Maskell et al.
  - Countryside Survey: UK Results from 2007 – Carey et al. (CEH)
  - CS Technical Report No 11/07: Final Report for LCM2007 – Morton et al.
  - ITE Merlewood Land Classification of Great Britain – Bunce et al. (1996)
  - CS Sampling Strategy revisions and related documents – Barr, Wood, et al.
- Access portals: Countryside Survey outputs and related datasets via the Countryside Survey website and NERC CEH resources.