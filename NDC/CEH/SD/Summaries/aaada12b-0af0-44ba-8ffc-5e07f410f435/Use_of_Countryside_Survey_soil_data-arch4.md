# Sampling design

## Overview
- Long-running soils monitoring effort (Countryside Survey) with sampling in 1978, 1998, 2007, and 2019.
- 2019 marks the start of a rolling survey: about 100 squares sampled each year for five years, then repeated.
- Aim: provide a structured dataset for national soil stock and change estimates, with attention to study design and data interpretation.

## Data structure and locations
- Soils sampled from CS x-plots, with 5 x-plots per CS square.
- x-plots are not replicates (they may differ in land use and soil type within a square).
- Each sampling location has a unique repeat identifier (e.g., 2RPT1) to track the same site over time, though exact sampling points may shift by ~2–3 m due to access or destruction of plots.
- Within-square sampling occurs at permanently marked 2m x 2m plots near the corners; precise locations may vary slightly across years.

## Sampling design and sampling units
- Sampling units are the x-plots within CS squares; five per square.
- Relocations occur when plots are destroyed, access is denied, or exact location cannot be confirmed.
- The design emphasizes dispersed sampling across the region rather than focusing on a single fixed location, to enhance regional representativeness.

## Sampling depth and methods
- Soils sampled from the top 15 cm of the profile (8 cm for invertebrate samples).
- 1998, 2007, and 2019 used soil cores hammered into the ground; 1978 used a soil pit.
- In some soils, full cores could not be collected due to stones or shallow soils.
- Core photographs and measurements of core dimensions were recorded in 2007 for some cores.

## Measurements and laboratory analyses
- 1978: only pH and loss-on-ignition (LOI).
- 1998, 2007, 2019: multiple cores per x-plot; different cores may have different measurements.
- No chemical analyses are performed by soil horizons; samples are homogenised before pH and LOI measurements.
- Bulk density measured in 2007 and 2019 (not using ISO bulk density method due to core constraints).
- A full method description and implications are documented in Emmett et al. (2008).

## Data quality, consistency, and gaps
- Measurements across years may vary by core and sampling condition; not all cores have uniform measurements.
- Some lab measurements are limited by method differences (e.g., bulk density not using ISO protocol).
- 1990s soil mapping existed, but not all measurements align across years; careful harmonization is required.

## Statistical analysis considerations
- Analyses should account for land class structure; ignoring it can bias to overall stock/change rather than national estimates weighted by land classes.
- Bootstrapping is not consistently used; recommended to apply mixed models with square as a random factor to account for within-square clustering (up to 5 x-plots per CS square).
- Design-based approaches advocate dispersed sampling to maximize precision and regional coverage; spatial structure is not the primary focus.
- Users should consult CEH prior to analysis and interpretation and review CS publications listed on the CS website for context.

## Data governance, metadata, and access
- Detailed methodological documentation and implications are provided (Emmett et al. 2008).
- References and protocol details available through the CS website and related publications (e.g., Emmett et al. 2007).
- The dataset supports ongoing data products through the rolling survey design and is intended to facilitate national-scale estimates of soil stock and change.

## Practical implications for data leadership
- Ensure robust metadata on plotting, sampling year, core IDs, depths, and measurement types to enable cross-year comparability.
- Maintain unique repeat identifiers and document any relocations or changes in sampling locations.
- Align analyses with the land class structure and adopt mixed-model approaches to appropriately partition variance.
- Plan for data harmonization when integrating data across years, noting method differences (e.g., bulk density protocols, depth, core processing).
- Leverage the rolling design to produce regular, policy-relevant soil status updates while monitoring data gaps and coverage.