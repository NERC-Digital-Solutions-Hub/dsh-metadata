# Collection/generation methods

## Purpose and scope
- Assess yield potential and soil carbon impacts of large-scale Miscanthus bioenergy across three models: MiscanFor, JULES, and IMAGE.
- Use a single climate/social pathway: SSP2-RCP2.6, with IMAGE-derived land-use maps defining bioenergy crop expansion.
- Focus areas: tropics (25°N–25°S) during 2040–2049 and Europe (roughly 15°W–40°E, >35°N) during 2090–2099.
- Primary outputs: bioenergy yield and soil carbon changes, key drivers of life-cycle carbon balance.

## Data sources and modelling frameworks
- Models: MiscanFor (Miscanthus-specific crop model), JULES (DGVM), IMAGE (IAM).
- Climate driving data: HadGEM2-ES RCP2.6 for MiscanFor and JULES (downscaled and bias-corrected to 1960–1999 climatology for 2006–2099); IMAGE uses MAGICC-derived pathway downscaled to grid level.
- Bioenergy expansion dynamics: global area increases in 2020s–2040s, peaking near 300 Mha around 2040, with a maximum expansion rate of 24 Mha/yr (under SSP2-RCP2.6).
- Data focus includes two strategic purposes: early low-cost renewable energy scaling, and later biomass with CCS considerations.

## Data structure and units
- File naming: {model}_{variable}_{period}.csv
- Grid and coverage: 6,858 grid cells on a global 0.5° grid; represents ~11% of global land area (Antarctica excluded); 89% of grid cells not modeled due to no bioenergy land use in the scenario.
- Data formats: MiscanFor outputs CSV; JULES and IMAGE outputs NetCDF, then converted to CSV; regridded to 0.5° grid; unit conversions applied.
- Contents: each file has three columns—latitude, longitude, value.
- Units and nuances:
  - Yield: tonnes dry matter (DM) per hectare of planted area per year (MiscanFor provides DM; JULES/IMAGE provide biomass in t C, converted to DM assuming 48% carbon content).
  - Soil carbon change: t C per hectare per year; MiscanFor per planted area, JULES/IMAGE per gridbox (includes other land cover/environmental change effects).
- Data completeness: NaN represents missing data; not all models provide data for all cells/periods in every file.

## Provenance, quality, and documentation
- Quality: models are state-of-the-art and validated across multiple sites; robust numerical stability and accuracy requirements.
- Data provenance: raw model outputs underpin the referenced publication Littleton et al. (2022) in GCB Bioenergy.
- Model versions and code: JULES version used (r12164_biotiles_harvest) is cited; JULES code is publicly accessible; model details and related references provided (Littleton et al. 2020; 2022; Doelman et al. 2019; others).
- Documentation: explicit notes on units, grid alignment, and the distinction between per planted area vs per gridbox for soil carbon outputs.

## Data accessibility and reuse considerations
- Uniform file structure across models but selective spatial coverage per file and period; 6,858 cells common across files.
- Regridding to a common 0.5° resolution facilitates cross-model comparisons.
- Clear metadata on units, grid centers, and carbon content assumption (48%) supports reproducibility and interpretation.
- The dataset represents a specific scenario (SSP2-RCP2.6) and defined focus regions, which should be considered when applying to broader analyses.

## Implications for data leadership and governance
- Demonstrates the importance of harmonizing multi-model outputs with consistent grids, units, and naming conventions to enable integration and comparability.
- Highlights need for robust provenance tracking, including model versions, climate drivers, and downscaling methods, to ensure reproducibility.
- Underlines the value of linking data assets to their underlying code and publications for traceability.
- Points to considerations around data scope and coverage (limited to grid cells with bioenergy land use) and handling of missing data in multi-model ensembles.