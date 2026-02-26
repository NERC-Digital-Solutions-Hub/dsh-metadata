# Sampling design

## Overview for Data Stewards
- Long-running soil monitoring program (Countryside Survey) with repeated sampling across years (1978, 1998, 2007, 2019) and a rolling 2018/2019–2023 expansion.
- Aims to detect significant change in soils and to provide national estimates when accounting for land-class structure; rolling survey targets ~100 squares per year for five years.

## Sampling design and scope
- 5 CS X-plots per square, randomly spaced within each square; X-plots are not replicates due to heterogeneous land use and soil types.
- Squares may be relocated over time due to land use changes or access issues; each location has a unique repeat identifier (e.g., 2RPT1) linking samples to a location.
- Sampling strategy evolves: 256 squares in 1978/1998; all 591 CS squares in 2007; rolling design initiated in 2019 with yearly sample targets.

## Sample location and plot structure
- Within-square sampling uses permanently marked 2 m x 2 m plots; repeat plots locate within proximity (roughly 2–3 m apart) but exact positions can vary.
- Relocations occur when plots are destroyed or access is denied; repeat identifiers maintain continuity of location data.

## Sampling procedures
- Depths: top 15 cm of soil sampled in 1998, 2007, and rolling survey (8 cm for invertebrates); 1978 used a soil pit for the top 15 cm.
- Core-based collection: 1998/2007/rolling surveys use soil cores hammered into the soil and pulled out; 1978 involved pit-based sampling.
- Practical constraints: full 15 cm sometimes not achievable due to stones/shallow soils; core dimensions and photographs recorded in some years (notably 2007).

## Measurements and laboratory analyses
- 1978: pH and loss-on-ignition (LOI) measured; no chemical analyses by horizon.
- 1998/2007/rolling: multiple cores per X-plot; different cores may carry different measurements; homogenization before pH and LOI to standardize subsamples.
- 2007: limited core measurements (e.g., black cores and N mineralization cores) with core photos and dimension data.
- Bulk density: measured in 2007 and 2018/19–2023, but not using ISO whole-core method.
- Notes on data completeness: not all measurements are available for every sample in every year.

## Data processing, quality and provenance
- Some processing decisions (e.g., not using ISO bulk density method) and multi-core sampling per X-plot require careful documentation for comparability.
- Core measurements and displacement (e.g., relocation) introduce potential spatial and temporal biases; metadata should capture core origin, depth, and measurement type per sample.

## Statistical analysis considerations
- Analyses should account for land-class structure to avoid biased population estimates; ignoring land classes yields stock/change of the population rather than national estimates.
- Mixed-model approaches are recommended with square as a random factor to account for multiple X-plots per CS square.
- Design-based interpretation emphasizes dispersed observations for efficiency and broader coverage; bootstrapping is not consistently applied across analyses.
- Users should consult UKCEH and CS publications for previously released analyses and methodological guidance prior to analysis and interpretation.

## Data governance and stewardship implications
- Metadata and lineage: capture sampling design changes over time, plot relocations, and the exact methods used in each year (depths, cores, measurements, and any deviations from ISO methods).
- Provenance and versioning: track per-year methodologies, sample IDs (e.g., 2RPT1), and which measurements were made for each core/location to support cross-year comparability.
- Data quality and completeness: flag samples with partial measurements, missing cores, or deviations (e.g., 1978 pit method) to enable proper filtering and interpretation.
- Standardization and interoperability: document measurement units, depths, and core handling practices; harmonize metadata to support national-scale estimates and role-based data sharing.
- Access, disclosure, and updates: maintain transparency about which data are available, update rolling data annually, and provide guidance on analyses that respect the sampling design and limitations.
- Advisory and governance: data stewards should engage with CS project documentation and UKCEH when planning analyses or disseminating results.

## References
- Emmett, BA, ZL Frogbrook, PM Chamberlain, R Griffiths, R Pickup, B Reynolds, E Rowe, P Rowland, D Spurgeon, J Wilson, CM Wood. Countryside Survey Soils 2007: Method development, power analyses and protocols. Centre for Ecology and Hydrology Project No. C03042/ DEFRA Contact No. CR0334.