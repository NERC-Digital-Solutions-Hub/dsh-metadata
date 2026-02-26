# Sampling design

- Context: Describes the Countryside Survey (CS) soils component and its historical sampling across three time points (1978, 1998, 2007), including design decisions, locations, and measurement strategies. Power analyses guided sample numbers (Emmett et al. 2008). Not all measurements were made on every sample.

## Sampling framework and scope

- Years and scope:
  - 1978 and 1998: the same 256 squares sampled.
  - 2007: all 591 CS squares sampled, but not all measurements on every sample.
- Goals for analysis: enable detection of significant change over time with standardized methodologies.
- Data handling note: some measurements and cores vary by year; design aims for broad comparability and national-scale estimates when appropriate.

## Sample location and plotting

- Plot structure: soils are collected from CS x-plots within each CS square; 5 x-plots per square randomly spaced.
- Non-replicate design: x-plots within a square are not treated as replicates due to differing land uses, soils, and conditions.
- Relocation and consistency: x-plots may be relocated over time due to land use changes, permission, or access issues; each location has a unique repeat identifier (e.g., 2RPT1) linking samples to a fixed location concept, though exact sampling points shift ~2–3 m within a fixed 2 m x 2 m plot.
- Sampling locations per square: multiple cores and plots are used to capture spatial variability, with sampling locations deliberately dispersed.

## Sampling method

- Depth: samples collected from the top 15 cm of soil (8 cm for invertebrate samples).
- Techniques:
  - 1998 and 2007: soil cores hammered in and pulled out.
  - 1978: soil pit dug with samples from the top 15 cm of the pit wall.
- Practical notes: stone-rich or shallow soils occasionally prevented full core collection; core dimensions and photographs were recorded in 2007 for some cores.

## Measurements and laboratory analyses

- 1978 measurements: pH and loss-on-ignition (LOI) only.
- Later work:
  - 1990: some soil mapping conducted.
  - 1998 and 2007: multiple cores per x-plot; different cores measured for different variables (refer to Table 1).
- Sample processing: soils are homogenised before pH and LOI analyses; chemical analyses by horizon are not performed.
- Bulk density: measured in 2007 (not via ISO whole-core method due to practical constraints); full methodological implications discussed in Emmett et al. 2008.
- Data disclosure: some measurements are listed as available in CS2007 Table 1; data release restrictions apply (see notes on data availability).

## Measurements by core and data coverage

- Measurements available across years include: pH (in water and CaCl2), LOI, %C, %N, bulk density, core dimensions, photographs, depth of organic layer, texture descriptors, soil moisture, Olsen P, metals, mineralisable N, among others.
- Coverage variability:
  - Some measurements available for all 591 squares in 2007.
  - Some measurements limited to original 256 squares or to a subset of x-plots in each square (e.g., 2 of 5 x-plots) in 2007.
- Data note: the document lists specific measurement availability by core and plot, indicating selective sampling of variables across the sampling framework.

## Statistical analysis and recommended practices

- Key considerations for CS soils data analysis:
  - Land class structure: if not accounted for, results reflect stock and change of the population; if weighted by land classes, estimates reflect national stock and change.
  - Bootstrapping: not universally applied; users should verify methods used in analyses.
  - Model structure: a mixed model is recommended, with square treated as a random factor to account for multiple x-plots within each CS square.
  - Design intent: CS is not primarily focused on spatial structure; a dispersed sampling design improves precision and regional coverage when regional estimates are required.
- Guidance for analysts:
  - Consider the spatial and design context when analyzing CS soils data.
  - Consult CEH prior to analysis, and review published CS outputs available on the CS website to align with established methodologies and interpretations.

## Data release and references

- Data release: some measurements are only released after the Soils Report (November 2009).
- Primary reference: Emmett, B.A., et al. Countryside Survey Soils 2007: Method development, power analyses and protocols (Centre for Ecology and Hydrology, CS Project No. C03042/DEFRA CR0334).