# Collection/generation methods

- Purpose and scope
  - Evaluates yield potential and soil carbon impacts of large-scale Miscanthus bioenergy production.
  - Uses three models: MiscanFor (Miscanthus-specific crop growth), JULES (Dynamic Global Vegetation Model), and IMAGE (Integrated Assessment Model).
  - All models run under a single climate/social pathway: SSP2-RCP2.6.
  - Focus areas illustrate two 21st-century Bioenergy roles: inexpensive renewable energy expansion (2020s–2030s) and sustainable bioenergy with carbon capture and storage (BECCS) later in the century.
  - Key outputs: bioenergy yield and soil carbon changes, central to life-cycle carbon balance.

- Data structure and file organization
  - Data consist of 6,858 grid cells on a 0.5-degree grid, selected from global coverage where bioenergy land use occurs.
  - Files are organized per model, variable, and period: {model}_{variable}_{period}.csv.
  - Data sources and formats:
    - MiscanFor: CSV
    - JULES and IMAGE: NetCDF, then converted to CSV
  - After processing, data are regridded to a common 0.5-degree grid, with unit conversions applied, and written as new CSVs.
  - Each file contains three columns: latitude, longitude, value.
  - Grid cells are in the same order across all files, but some cells have NaN (missing) values.

- Coverage and grid details
  - The 6,858 grid cells cover about 11% of global land area (excluding Antarctica); the remaining 89% are not modeled for bioenergy land use in this scenario.
  - MiscanFor data coverage is regionally limited within Europe for 2090–2099 and outside Europe for 2040–2049; other cells may be NaN.

- Focus areas and time periods
  - Tropics: lat ±25° for the decade 2040–2049.
  - Europe: long 15°W to 40°E and lat >35°N for the decade 2090–2099.
  - These focus areas illustrate early bioenergy expansion and later BECCS-related feedstock use.

- Variables, units, and interpretation
  - Yield:
    - MiscanFor: tonnes dry matter (DM) per hectare of planted area per year (direct output).
    - JULES/IMAGE: biomass in tonnes of carbon, converted to DM using 48% carbon content.
  - Soil carbon change:
    - Units: tonnes C per hectare per year.
    - MiscanFor: per hectare of planted area.
    - JULES/IMAGE: per hectare of the entire grid box (includes other land covers/environmental change effects).
  - Units are defined at grid-box centroids for 0.5-degree cells; latitude/longitude denote grid-centre coordinates.

- Climate driving data and modeling details
  - MiscanFor and JULES: HadGEM2-ES downscaled to 0.5° and bias-corrected to WATCH climatology (1960–1999) to produce 2006–2099 climate time series (ISIMIP-based).
  - IMAGE: climate pathway aligned with RCP2.6, downscaled using MAGICC and HadGEM2-ES data (ISIMIP framework).

- Data quality and provenance
  - Models represent state-of-the-art approaches and have undergone rigorous validation across sites.
  - Version references:
    - JULES: Littleton et al., 2020
    - MiscanFor: Shepherd et al., 2020
    - IMAGE: Daioglou et al., 2019; Doelman et al., 2019
  - This dataset provides raw model output underpinning the publication:
    - Littleton, E.W. et al. 2022, GCB Bioenergy
  - JULES model code is publicly available in the Met Office repository (require registration); specific version used: r12164_biotiles_harvest.

- Usage notes for GIS and mapping
  - Data are gridded and suitable for map-based analyses and visualisation of spatial patterns in yield and soil carbon.
  - Be mindful of NaN values representing cells not modeled or lacking data in the scenario.
  - When combining across models, apply the same 0.5-degree grid and ensure consistent unit interpretation (DM vs carbon-based yield).
  - Refer to Littleton et al. (2022) for methodological context on data interpretation and differences in reporting units.

- File naming, formats, and access
  - File naming convention: {model}_{variable}_{period}.csv
  - Periods correspond to decades: 2040–2049 and 2090–2099 (two focus areas).
  - Source formats: MiscanFor CSV; JULES/IMAGE NetCDF converted to CSV; data regridded to 0.5-degree grid.

- References
  - Littleton, E.W., Shepherd, A., Harper, A.B. et al. (2022). Uncertain effectiveness of Miscanthus bioenergy expansion for climate change mitigation explored using land surface, agronomic and integrated assessment models. GCB Bioenergy, 15, 303-318.
  - Supporting model and methodology references: Littleton et al. (2020); Shepherd et al. (2020); Daioglou et al. (2019); Doelman et al. (2019); Hempel et al. (2013).