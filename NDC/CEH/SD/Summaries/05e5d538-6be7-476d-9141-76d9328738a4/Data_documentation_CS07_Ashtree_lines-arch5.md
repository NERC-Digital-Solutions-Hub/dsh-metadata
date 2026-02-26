# Countryside Survey: Ash tree distribution in woody linear features 2007

## Overview
- Provides estimates of ash trees within woody linear features across Great Britain, derived from Countryside Survey 2007 data.
- Documented as CS07_Ashtree_Linears; data are © NERC - Centre for Ecology & Hydrology.
- Used to support data governance, accessibility, and reuse within large dataset environments.

## Dataset Details
- File: CS07_Ashtree_Linears
- Purpose: national estimates of ash within lines of trees and belts derived from Countryside Survey 2007.
- Based on: Countryside Survey 2007 methodology and sampling framework.
- Associated datasets:
  - ITE Land Classification (2007)
  - Countryside Survey (www.countrysidesurvey.org.uk)

## Data Model and Columns
- LC2007: Land Class (numeric)
- LC2007_COD: Land Class (text)
- LC_2007: Land Class (text; same as LC2007 with no code where no hedges occur)
- Area of Land Class: Area in square meters (from original land classification file; may differ from default Area)
- Size_of_LC: Area of Land Class (reference value)
- WNS_km: Woody linear feature, Natural shape, length of ash in km (by land class)
- WUS_km: Woody linear feature, Unnatural shape, length of ash in km (by land class)
- Belt_km: Belt of trees, length of ash in km (by land class)
- All_WLF_km: Total of WNS_km, WUS_km, and Belt_km (in land class)
- Mean_km_km: Mean length of all linear features in km per km2

## Spatial and Temporal Scope
- Resolution: 1 km
- Coordinate system: British National Grid
- Projection: Transverse Mercator
- Extent: Great Britain
- Projection reference: OSGB1936

## Methodology and Estimation Approach
- Sampling framework: Countryside Survey uses a stratified random sample of 1 km squares across GB, based on land classes representing major ecological gradients.
- Linear features recorded: features less than 5 m wide; minimum length 20 m; may include gaps up to 20 m.
- Woody Linear Features (WLFs):
  - Natural Shape: lines of trees and belts of trees
  - Unnatural Shape: hedgerows
- Species data:
  - In Natural Shape WLFs, proportion of ash recorded against each species present (with bands: <10%, 10-25%, 25-50%, 50-75%, 75-95%, 95-100%, Individual Tree)
  - In Unnatural Shape WLFs, ash proportion derived from different data streams and methods (e.g., mixture categories and >50% hawthorn/other)
- Ash estimation process:
  - For lines: calculate length of ash per 1 km square using proportion band midpoints (e.g., 5%, 17.5%, 37.5%, 62.5%, 85%, 97.5%, 100%).
  - Obtain a 1 km mean length of ash in lines per sampling stratum; multiply by the Land Class area to scale to national estimates.
  - For belts: apply the same methodology, including belts of trees and belts of scrub.
  - For WLFs with unnatural shape: use D plots (vegetation diversity plots adjacent to hedges) to inform species composition; calculate mean percentage cover for ash and multiply by total hedge length in all sampled 1 km squares within the stratum.
- Derivation of national totals:
  - 1 km square means per stratum multiplied by Land Class area, then summed across strata/country.

## Data Governance and Documentation
- Version: Document Version 1:19-8-2013
- Rights: Countryside Survey data © NERC - Centre for Ecology & Hydrology
- Metadata considerations:
  - Clear linkage to Land Classification and Countryside Survey methodologies
  - Documentation of methods for ash estimation, including handling of bands and D plots
  - Notes on data interpretation differences between Natural vs Unnatural shapes and belt vs line features
- Accessibility and reuse:
  - Dataset and associated documentation are linked to broader Countryside Survey outputs and UK results (2007)
  - Methods and references provided for reproducibility and methodological audit

## Related Reading and References
- Distribution of Ash trees (Fraxinus excelsior) in Countryside Survey data (Maskell et al., 2013)
- Countryside Survey: UK Results from 2007 (Carey et al., 2008)
- LCM2007 and related land cover mapping resources
- Sampling strategies and land classification frameworks for Countryside Survey