# Countryside Survey Soils 2007: Method development, power analyses and protocols

## Executive summary
- The Countryside Survey (CS) soils dataset spans 1978, 1998, and 2007, with a shift from 256 squares in earlier years to 591 squares in 2007.
- Sampling design includes five x-plots per CS square; x-plots are not true replicates due to varied land uses and soils, and plots can be relocated over time.
- Data encompass a range of soil measurements collected from multiple cores, with some measurements limited to certain years or plots.
- Analyses must account for land class structure and spatial design; mixed models with square as a random factor are recommended for proper inference.
- Data governance notes include partial data release timelines and guidance to consult CEH and CS publications for proper use.

## Sampling design and locations
- Soils sampled in 1978, 1998, and 2007; 256 squares were used in 1978/1998, 591 squares in 2007.
- Each CS square contains 5 randomly spaced x-plots; x-plots are not replicates across different land uses or soil types.
- Plot relocations occurred when plots were destroyed or access denied; each location has a unique repeat identifier (e.g., 2RPT1).
- Sampling locations within a square are around a permanently marked 2m x 2m plot, with sampling around the four corners (2–3 m apart).

## Sampling methods
- Soil collected from the top 15 cm (8 cm for invertebrates); 1998/2007 used a soil core, hammered in and pulled out; 1978 used a soil pit.
- In some soils, full core collection was not possible due to stones or shallow soils.
- Core photographs and measurements of core dimensions were made in 2007 on a subset of cores.

## Measurements and data attributes
- 1978: pH and loss-on-ignition (LOI) only.
- 1990: some soil mapping conducted.
- 1998 and 2007: multiple cores per x-plot; different cores have different measurements (Table 1).
- No chemical analyses by soil horizon; samples are homogenised before pH and LOI measurements.
- Bulk density measured in 2007 (not using ISO bulk density method).
- In 2007, a comprehensive set of measurements was recorded per core: pH (in water and CaCl2), %C, %N, bulk density, core dimensions, photographs, depth of organic layer, texture (hand), soil moisture, Olsen P, metals, mineralisable N, etc.
- Data coverage varies: some measurements apply to all 591 squares; others limited to the original 256 squares; data release notes indicate some measurements released after November 2009.

## Statistical analysis and interpretation
- Analyses should consider land class structure; ignoring land classes yields stock/change of the population, while including them yields national estimates weighted by land classes.
- Bootstrapping is not consistently used across analyses.
- A mixed-effects approach is advised: square as a random factor to account for up to five x-plots per square.
- Design-based approaches with dispersed observations can improve regional precision and coverage when estimating regional metrics.
- Users are encouraged to consult CEH prior to analysis and review CS publications on data usage and methods (CS website).

## Data governance, provenance, and access
- Primary methodological reference: Emmett et al. 2008 (Method development, power analyses, protocols).
- Soils report published November 2009 notes data release and measurement specifics.
- Data availability varies by year and measurement; notable guidance to refer to CS website for published analyses and data releases.