# A modelled dataset derived from national datasets, describing the distribution of woody linear feature boundaries in Great Britain

## What this dataset is
- A nationally scaled predictive dataset describing the distribution of woody linear features (hedges and lines of trees) in Great Britain.
- Output derived from existing national datasets to provide coverage where field mapping would be costly/time-consuming.

## Why woody linear features matter
- They are important boundaries that connect and enclose habitats, buffer land management, and enhance biodiversity in changing landscapes.
- Their linear nature and data gaps have historically limited inclusion in landscape-function models.

## How the model was built
- Based on a simplified version of OS MasterMap within the Land Cover Map 2007 framework.
- Areas unlikely to contain woody features or difficult to detect were masked out: land >350 m, urban, wooded, or coastal tide-washed areas.
- Boundary height information came from a 5 m NEXTMap Digital Terrain Model; woody features were identified along boundaries using vegetation height thresholds:
  - minimum vegetation height: -0.13 m (accounts for adjacent ditch)
  - maximum vegetation height: 58 m (upper limit for GB trees)
  - mean vegetation height: 0.58 m (accounts for gaps)
- The dataset includes only linear features with a high likelihood of being woody.

## Validation and quality control
- Model outputs at national and other scales are concordant with published statistics and are spatially consistent with Countryside Survey results.
- Further details available in Scholefield et al. (2016).

## Dataset structure and content
- Features are linear (polyline) with geometry stored in SHAPE and SHAPE_LENGTH reported in metres.
- Data sources include:
  - OS MASTERMAP, OS LAND-FORM PANORAMA
  - NEXTMAP digital elevation data
  - Countryside Survey 2007 mapped estimates of linear feature lengths in Great Britain
- Acknowledges licensing and sources from 2016 (OS, NEXTMAP) and related publications.

## How to use this dataset
- Combine with other biodiversity, land-use, or ecological datasets to analyze hedgerow extent, connectivity, and landscape function.
- Useful for predicting impacts of land management actions, policy scenarios, or environmental change at national to local scales.
- May help fill data gaps where field mapping is impractical, aiding models that require woody linear boundary information.

## Limitations and caveats
- Excludes areas masked during modelling, so woody features in those areas are not represented.
- Based on data from different years and modelling thresholds, which may introduce some uncertainties in exact locations and extents.
- Thresholds and methods may not capture all local variations in vegetation structure.