# The Concentration-Based Estimation of Deposition (CBED) Methodology

- Provides 5x5 km resolution gridded estimates of deposition flux for nitrogen (NOx, NHx, Ntot), sulphur (SOx, xSOx), hydrogen ions (H), calcium (Ca), magnesium (Mg), and chloride (Cl) across the UK.
- Based on measured concentrations of gases and PM in air, plus ions in precipitation, using observations from the UK Eutrophying and Acidifying Pollutants (UKEAP) network.
- Interpolates observations to create maps of air and precipitation concentrations; combines with precipitation data and land-cover-specific deposition velocities to estimate dry and wet deposition.

- Dry deposition
  - Uses gas/PM concentration maps and spatially distributed land-cover deposition velocities for five land-cover categories: forest, moorland, grassland, arable, and urban.
  - Deposition to each grid cell is a weighted mix based on land-cover proportions within the 5x5 km grid square.

- Wet deposition
  - Includes deposition from precipitation and occult deposition (direct deposition of cloud droplets to vegetation).
  - Separates anthropogenic (non-seasalt) and total sulphur and calcium components using sea-water ion ratios.
  - Applies an orographic enhancement factor for upland precipitation concentrations (seeder-feeder effect).

- Temporal context and uncertainty
  - Significant inter-annual variability and interpolation uncertainty due to sparse monitoring; results are averaged over three-year periods to smooth variability.
  - Earlier years have greater uncertainty due to missing components (e.g., aerosols) and retrospective estimation using long-term fractions.

- Implementation
  - Originally written in Genstat; re-implemented in R. The R version has small numerical differences in spatial interpolation (kriging) and whether the long-term mean/orographic factor is recalculated yearly.

- Data provenance and quality control
  - Data undergo extensive quality assurance, peer review, and cross-year mass-balance checks; part of Defra model inter-comparison efforts.
  - Documentation and version control are maintained; results widely published in peer-reviewed literature.

- Data outputs and structure
  - Data exported from raster format to comma-separated text (xyz) format as 3-year means for the current and two preceding years (e.g., 2012 represents 2010–2012).
  - Coverage: 1986–2012; deposition calculated for five land-cover categories; grid-squares averaged to provide a mean per 5x5 km cell.

- Files and variables (example outputs)
  - rCBED_Fdep_gm2y_1986-2012_gridavg.csv – mean deposition weighted by land-cover fractions.
  - rCBED_Fdep_gm2y_1986-2012_forest.csv – deposition to forest (assuming full forest cover per grid cell).
  - rCBED_Fdep_gm2y_1986-2012_moor.csv – deposition to moorland (assuming full moorland cover per grid cell).
  - Common fields: year (end-year of the 3-year period), easting, northing (OS Great Britain grid, metres), and deposition components: H (hydrogen ions), NOx (oxidised nitrogen), NHx (reduced nitrogen), Ntot (total nitrogen), SOx (sulphur), xSOx (non-marine sulphur), Ca, Mg, CaMg (calcium + magnesium), Cl (chloride).

- Spatial reference
  - Coordinates based on the OS Great Britain grid; units in metres.
  - Deposition flux units: grams per square metre per year (g m-2 year-1).

- Notes for GIS use
  - Grid-based outputs are suitable for map-based visualisation and spatial analyses; three 3-year aggregates provide more stable temporal signals.
  - Users should be aware of uncertainties in earlier years and the differences between the Genstat and R implementations when comparing historical results.

- Access and references
  - Supporting information and data descriptions are linked to UK pollutant deposition resources and Defra/UK-AIR networks; data are tied to UKEAP and related modelling literature.