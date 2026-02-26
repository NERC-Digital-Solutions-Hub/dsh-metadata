# Methods

- The Concentration-Based Estimation of Deposition (CBED) methodology generates 5x5 km resolution gridded estimates of deposition flux for nitrogen, sulphur, and base cations. It uses measured concentrations of gases and particulate matter in air and measured ion concentrations in precipitation from the UK Eutrophying and Acidifying Pollutants (UKEAP) network, which are interpolated to UK-wide concentration maps (in air and precipitation) to produce deposition estimates.

- Dry deposition is derived by combining gas and PM concentration maps with land-cover–specific deposition velocities for five land cover categories (forest, moorland, grassland, arable, urban). Deposition to each grid square is a weighted mix based on land-cover composition.

- Wet deposition is mapped from precipitation deposition and direct deposition to vegetation (occult deposition). It includes sulphate, ammonium, nitrate, calcium, magnesium, and acidity (hydrogen ion). Anthropogenic versus total deposition components are separated for sulphur and calcium using sea-water ion ratios; orographic enhancement factors are applied for upland regions.

- Key gas components include NO2 (via the PCM model), NH3 (via FRAME plus UKEAP observations for local variability), and SO2 (from rural measurements plus an urban enhancement factor). Wet deposition accounts for precipitation deposition and occult deposition.

- There is substantial inter-annual uncertainty due to data sparsity and natural weather variability. To reduce year-to-year noise, CBED estimates are averaged over three-year periods; reliability for individual years remains uncertain, especially pre-1996 when some components were not measured.

- Implementation: originally written in Genstat and re-implemented in R. Differences between versions arise from the spatial interpolation algorithm (kriging) and the use of long-term means versus recalculation each year. Earlier years have higher uncertainty because some components (e.g., aerosols) were not measured and are retrospectively estimated using long-term fractions.

- Data quality and governance: CBED data follow QA procedures aligned with government model QA practices, have undergone extensive peer review, were part of the Defra model inter-comparison, and include mass-balance checks for numerical consistency across years.

- Data products and structure: Data are exported from a raster format to comma-separated text files in xyz format. Values represent 3-year means for the current and two preceding years (e.g., 2012 represents 2010–2012), covering 1986–2012. Deposition is provided for five land-cover categories, with an average deposition to each grid square computed as a land-cover-weighted mean.

- Three data files are provided:
  - rCBED_Fdep_gm2y_1986-2012_gridavg.csv – mean deposition weighted by land-cover fractions
  - rCBED_Fdep_gm2y_1986-2012_forest.csv – deposition to forest (assuming full forest cover in each grid cell)
  - rCBED_Fdep_gm2y_1986-2012_moor.csv – deposition to moorland (assuming full moorland cover in each grid cell)

- File format and fields (example fields across all files): year; easting; northing; H (hydrogen ions); NOx (oxidised nitrogen); NHx (reduced nitrogen); Ntot (total nitrogen); SOx (sulphur); xSOx (non-marine sulphur); Ca (calcium); Mg (magnesium); CaMg (calcium + magnesium); Cl (chloride). Units are g m^-2 year^-1 or equivalent per field description. Each file provides data for corresponding grid squares and variables.

- Data coverage and time frame: deposition values correspond to 3-year means for 1986–2012, expressed per square metre per year (g m^-2 year^-1). The results are presented on 5x5 km grid squares across Great Britain.

- References and resources: CBED methodology and validation are documented in literature (e.g., Smith et al., Fowler et al.) with supporting materials and network information available via provided URLs.