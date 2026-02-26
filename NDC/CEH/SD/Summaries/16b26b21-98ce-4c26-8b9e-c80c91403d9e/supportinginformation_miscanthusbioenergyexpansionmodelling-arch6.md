# Collection/generation methods

- Objective and scope
  - Assess yield potential and soil carbon impacts of large-scale Miscanthus bioenergy production.
  - Compare outputs from three models: MiscanFor (crop growth), JULES (Dynamic Global Vegetation Model), and IMAGE (Integrated Assessment Model).
  - Use a single climate and social-development pathway: SSP2-RCP2.6.

- Models and climate forcing
  - MiscanFor: Miscanthus-specific crop growth model.
  - JULES: Global land surface model with bioenergy crop representation.
  - IMAGE: Integrated assessment framework with land-use and bioenergy pathways.
  - Climate driving data: HadGEM2-ES RCP2.6 (ISIMIP) downscaled and bias-corrected for MiscanFor and JULES; IMAGE climate pathway downscaled via MAGICC/HadamGEM2-ES outputs.
  - Bias correction: MiscanFor and JULES calibrated to WATCH climatology (1960–1999).

- Focus areas and purposes
  - Tropics: 2040–2049 (latitude ±25°) to illustrate early bioenergy scale-up.
  - Europe: 2090–2099 (Europe-focused grid) to illustrate bioenergy as sustainable feedstock with CCS.

- Outputs of interest
  - Yield and soil carbon projections are the chosen focal outputs due to their importance for life-cycle carbon balance.
  - Outputs produced in three formats per model: yield (DM ha−1 yr−1) or biomass carbon, and soil carbon change (t C ha−1 yr−1).

- Data structure and file organization
  - Files named as {model}_{variable}_{period}.csv.
  - Data sourced from MiscanFor (CSV) or JULES/IMAGE (NetCDF), then regridded to a common 0.5° grid and units standardized.
  - Grid coverage: 6,858 grid cells selected from the global 0.5° grid, representing about 11% of global land area with bioenergy land use; remaining 89% not modeled due to no bioenergy land use in this scenario.
  - Missing data: NaN values where a model did not cover certain cells (e.g., MiscanFor only covers specific Europe 2090–2099 cells and non-Europe 2040–2049 cells).

- Units and data interpretation
  - Latitude/longitude: degrees north/east, centered on 0.5° grid boxes.
  - Yield:
    - MiscanFor: directly in tonnes DM per hectare of planted area per year.
    - JULES/IMAGE: biomass in tonnes C; converted to DM using 48% carbon content.
  - Soil carbon change:
    - MiscanFor: t C per hectare of planted area per year.
    - JULES/IMAGE: t C per hectare of the entire gridbox (includes other land cover/environmental changes).
  - Consistency note: Differences in denominator (planted area vs gridbox) discussed in Littleton et al. (2022).

- Data quality and provenance
  - Models are state-of-the-art; validated across multiple sites; robust numerical behavior.
  - Detailed model version references: Littleton et al. (2020, 2022) and related methodological papers; JULES code available publicly (repository link provided).

- Use cases and context
  - Provides raw model outputs underpinning the cited publication: Littleton et al. (2022) on the uncertain effectiveness of Miscanthus bioenergy expansion.
  - Enables cross-model comparisons of bioenergy yield and soil carbon outcomes under a consistent climate pathway.
  - Useful for reanalysis, data integration, and constructing data products (e.g., dashboards, maps) that explore bioenergy potential and soil carbon responses.