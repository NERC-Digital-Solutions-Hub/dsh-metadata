# Model estimates of expected diversity of positive plant habitat condition indicators

## Overview
- A dataset and modeling approach to estimate the diversity of positive plant habitat condition indicators (CSM indicators) across Great Britain.
- Based on Countryside Survey 2007 data, covering 591 1km squares with stratified random sampling by land class.

## Experimental Design / Sampling Regime
- Plots were located within each 1km square using restricted randomisation to reduce aggregation.
- Plot types:
  - x plots: five large randomly placed plots (14.14 x 14.14 m; ~200 m²) per square.
  - Inner nest within x plots: 2 m x 2 m used for analysis to align with unenclosed habitats.
  - u plots and y plots: used to sample unenclosed habitats and small semi-natural patches; y plots often remnant historic habitat patches.
- Targeted habitats focus on areal, not linear features, and exclude coastal and urban habitats from analysis.

## Spatial Reference
- Coordinate System: OSGB 1936 / British National Grid (EPSG: 27700)

## Data Attributes
- percentCSM: percentage of positive CSM plant species in a plot, normalized by the number of characteristic species for the habitat type.
- SEM: standard error / variance measure for percentCSM.
- Each plot is classified by Broad Habitat and Priority Habitat (as per Jackson 2000, Maskell et al. 2008).

## Indicator Species and Habitat Classification
- Indicator species selected from JNCC guidance and BSBI consultations aligned with Priority Habitats within the Broad Habitat.
- Broad Habitat examples include Upland/Lowland Heath (Dwarf Shrub Heath), Arable/Horticulture, Broadleaved/Mixed/Yew Woodland, etc.
- Some Broad Habitats may include non-priority areas; some had alternative species lists when CSM lists were unavailable.
- The Improved Grassland Broad Habitat lacks CSM guidance but indicators for neutral grassland were calculated.

## Collection Methods
- In each vegetation plot, a list of vascular plants plus a selection of easily identifiable bryophytes and macro-lichens was created.
- Nomenclature aligned with Stace (1991) and Watson (1981).
- Cover estimates recorded to the nearest 5% for species with ≥5% estimated cover.

## Analytical Methods
- Positive habitat indicators summed per plot; each plot assigned Broad and Priority Habitat classifications.
- Exclusions: coastal and urban habitats; scaling based on the Land Cover Map excludes linear features (e.g., hedgerows, streamsides, roadsides).
- For unsampled 1km squares, predictions used a Generalised Additive Mixed Model (GAMM):
  - Response: percentage of positive CSM indicators per plot.
  - Random effect: 1km CS square to account for non-independence within squares.
  - Distribution: Poisson.
  - Covariates: broad habitat, Temperature, Precipitation, Nitrogen deposition, Sulfur deposition, SSSI presence.
  - Model uses the dominant broad habitat within a 1km square to create the map.

## Quality Control
- Processes followed the Defra / NERC Joint Codes of Practice.

## Limitations / Caveats for GIS Use
- Linear features and landscape connectivity not included in the scaling (potentially important refugia sites).
- Exclusion of coastal and urban habitats limits applicability to those areas.
- Predictions rely on the dominant broad habitat per square; finer-scale heterogeneity within squares may be underrepresented.
- Data completeness and resolution constrained by the Countryside Survey 2007 framework and available CSM guidance lists.

## References / Supporting Documents
- Bunce et al. 2007; ITE land classification of Great Britain 2007.
- Byfield & Wilson 2005; JNCC guidance on CSM for vascular plants.
- Jackson 2000; Maskell et al. 2008; Field Mapping Handbook.
- Smart et al. (2003, 2006, 2008) on vegetation sampling and landscape relationships.
- Stace 1997; Watson 1981 on plant nomenclature.