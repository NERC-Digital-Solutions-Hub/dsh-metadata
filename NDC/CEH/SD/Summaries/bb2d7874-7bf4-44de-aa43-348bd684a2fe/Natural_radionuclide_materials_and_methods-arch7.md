# Materials and methods for soil, water and sediment data extracted from: Background exposure rates of terrestrial wildlife in England and Wales

## Overview
- Objective: categorize naturally occurring radionuclides in England and Wales according to ICRP reference animals and plants (RAPs) to support dose assessments for non-human species, focusing on terrestrial ecosystems.
- Primary outputs: geospatial data layers of radionuclide activity concentrations in soils, sediments, waters, and associated biota, interpretable in map-based GIS tools.

## Reference animals and plants (RAPs)
- Reference Deer
- Reference Rat
- Reference Duck
- Reference Frog
- Reference Bee
- Reference Earthworm
- Reference Pine Tree
- Reference Wild Grass

## Data sources and data availability
- Data sources include:
  - Grey literature, refereed journal papers, and in-house databases.
  - RIFE (Radioactivity in Food and the Environment) reports (UK-wide data, 1995–2004), including some naturally occurring radionuclides in biota.
  - Centre for Ecology & Hydrology (CEH) analyses of radiocaesium deposition (1986 Chernobyl, Sellafield discharges) with gamma data for 40K.
  - British Geological Survey (BGS) G-BASE geochemical surveys for natural radionuclides in soils, sediments, and waters.
- Data were allocated to RAPs where possible (e.g., Reference Duck: any wild bird; Reference Frog: any amphibian; Reference Bee: any flying insect; Reference Earthworm: any earthworm; Reference Pine Tree: any tree; Reference Wild Grass: any wild grass/grass data).
- Mammalian RAPs: data categorized as “any wild mammalian species” and separately for Deer and Rat.
- Wales data were underrepresented for some taxa; where Wales data were scarce, samples from Wales complemented data from England.

## Sampling and analyses
- Due to limited existing data, targeted sampling was conducted for Duck, Bee, Earthworm, Pine Tree, and Frog.
- Sampling approach combined existing CEH archives with new collections:
  - Flying insects (predominantly moths) from Environmental Change Network sites.
  - Lodgepole pine (Pinus contorta) trunk samples.
  - Grey heron liver samples from Predatory Birds Monitoring Scheme.
  - Earthworms, rabbits, toads, mallards sampled from CEH archives or Wales as needed.
- Fossil and sample types were chosen to improve RAP coverage where data were sparse.

## Sample preparation and analyses
- Preparation steps included cleaning, ashing, freeze-drying, homogenising, and careful handling to avoid contamination.
- Gamma spectrometry using hyperpure germanium detectors determined gamma-emitting radionuclide activity concentrations.
- For total U and Th, samples underwent acid digestion (HNO3, HF) and ICP-MS analysis; secular equilibrium assumptions applied where appropriate:
  - 238U series assumed secular equilibrium with 234U in biological samples.
  - 232Th series assumed equilibrium among its daughters where biologically reasonable.
- Specific activity constants used:
  - 40K, 232Th, and 238U activity per mass values used to derive radionuclide activity concentrations from total element concentrations.
- Sample-specific preparation varied by tissue (e.g., toad analysed fresh before ashing).

## Derivation of soil activity concentrations and spatial data
- Soil activity concentrations based on long-running G-BASE geochemical data (K, U, Th) from England and Wales.
- Sampling density and processing:
  - Soils: about one sample per 2 km2, composite from five holes within a 20 m x 20 m area.
  - Sediments/Waters: approximately one sample per 1.5–2 km2; waters treated with a different approach due to weaker geochemical relationships.
- Normalisation and cross-dataset harmonisation:
  - Normalisation between different analytical techniques and sample types (surface vs subsurface) to enable consistent comparisons.
  - Normalisation between BGS data and Wolfson Atlas (for potassium) via linear quantile transformation in overlapping areas.
  - Extrapolation to cover all England and Wales using bedrock/superficial geology relationships where direct measurements were not available.
- Spatial data products:
  - For soils and sediments: geometric means (GM) on a 5 × 5 km grid (25 km2 cells) using the nearest data points by parent material; both measured means and extrapolated surfaces produced.
  - For waters: GM concentrations where data existed; no extrapolation applied due to weaker geology-concentration relationships.
- Activity concentration calculations:
  - 40K, 232Th, and 238U derived from total element concentrations using published specific activities; assumed approximate equilibrium within decay chains where justified.

## Terrestrial biota data handling and RAP assignment
- Terrestrial biota data compiled with columns covering species name, RAP assignment, location coordinates (eastings/northings), sampling date, and reported activity concentrations.
- RAP attribution approach:
  - Data from various sources mapped to corresponding RAPs (e.g., birds to Reference Duck, amphibians to Reference Frog, insects to Reference Bee, earthworms to Reference Earthworm, trees to Reference Pine Tree, grasses to Reference Wild Grass).
  - For mammals, data separated into “any wild mammalian species” and specific Deer and Rat data.

## GIS implications and data products
- Outputs enable map-based visualization of naturally occurring radionuclide activity across soils, sediments, waters, and biota, aligned to RAPs for non-human dose assessment.
- Data are suitable for integration into GIS workflows to support spatial analyses, exposure modeling, and policy-relevant visualization of radiological risk to wildlife.

## Limitations and considerations
- Data coverage is incomplete across the UK, with notable gaps in Wales for certain RAPs and media.
- Extrapolation introduces uncertainty, particularly for waters where relationships to geology are weak.
- Equilibrium assumptions in decay chains may not hold perfectly for all environmental contexts; results rely on reasonable approximations.
- The work emphasizes data harmonisation across heterogeneous sources to enable robust RAP-based assessments.