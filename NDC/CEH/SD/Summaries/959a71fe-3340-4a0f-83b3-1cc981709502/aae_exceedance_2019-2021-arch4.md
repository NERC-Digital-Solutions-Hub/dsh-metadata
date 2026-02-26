# Introduction

- The document presents 1x1 km raster data sets of Average Accumulated Exceedance (AAE) for acidity and nutrient nitrogen critical loads due to acid and nitrogen deposition for 2019–2021.
- AAE combines exceedances across habitats within each grid square, normalised by the total habitat area in that square.
- AAE is calculated per habitat and then summed across habitats to obtain AE, which is divided by total habitat area to yield AAE (keq ha^-1 year^-1).
- Two data sets are provided:
  - acid_aae_2019-2021.tif: AAE for acidity
  - nutn_aae_2019-2021.tif: AAE for nutrient nitrogen
- Habitat lists differ between acidity and nitrogen datasets; examples include various grasslands, woodlands, bog, montane, dune grassland, saltmarsh, etc.

## What the data represent

- AAE values indicate the potential for long-term, ecosystem-level harm when critical loads are exceeded.
- Exceedances are calculated relative to habitat-specific critical loads for acidity (S and N deposition) and nutrient nitrogen.
- For freshwaters, 1752 locations are reported separately and are not included in the AAE calculations because they use catchment-based data rather than 1x1 km grid squares.

## Datasets included

- acid_aae_2019-2021.tif: AAE for acidity (keq ha^-1 year^-1) across UK habitats (grid-based).
- nutn_aae_2019-2021.tif: AAE for nutrient nitrogen (keq ha^-1 year^-1) across UK habitats.
- Habitats included differ by dataset (acidity vs nutrient nitrogen).

## Methodology overview

- Based on UK methods (Hall et al., 2015) for calculating critical loads and exceedances for habitats sensitive to acidification and eutrophication.
- Inputs:
  - CBED deposition data (deposition estimated from air concentrations and land use).
  - UK CEH Land Cover Map 2019 (1 km summary rasters).
- Outputs are raster datasets in British National Grid (EPSG:27700) with a single band each (acid_aae and nutn_aae).

## How exceedances and critical loads are computed

- Acidity critical loads:
  - Two methods: empirical approach for non-woodland mineral/organomineral soils; simple mass balance (SMB) for woodlands and peat soils.
  - CLmaxS, CLmaxN, CLminN define the critical load function; peat soils use special treatment due to buffering differences.
  - Freshwaters use the catchment-based FAB model (not part of the AAE grid calculations).
- Nutrient nitrogen critical loads:
  - Empirical loads set under the Convention on Long-Range Transboundary Air Pollution, assigned to EUNIS habitat classes; expressed as ranges (e.g., 10–20 kg N ha^-1 yr^-1).
  - Most recent revisions in 2022.
- Exceedances:
  - For nitrogen: exceedance = total N deposition minus the habitat’s (range) critical load.
  - For acidity: exceedance depends on the position relative to CLmaxS, CLminN, CLmaxN; uses the “shortest distance” exceedance concept with a five-region division of the Critical Load Function.
  - The acidity function can be visualised as a diagonal plot of S vs N deposition; in certain regions, the function is shifted to account for long-term N removal processes.
- Units and interpretation:
  - AAE values are in keq ha^-1 year^-1; if deposition is below the critical load, AAE is zero.
  - For nutrient nitrogen, AAE can be converted to kg N ha^-1 year^-1 by multiplying by 14 (1 keq ha^-1 year^-1 = 14 kg N ha^-1 year).
  - Acidity AAE represents a combination of S and N; it cannot be separated into S or N units.

## Inputs and data sources

- Deposition data: CBED (Concentration-Based Estimated Deposition).
- Land cover data: UK CEH Land Cover Map 2019 (1 km summary rasters).
- Freshwater exceedance data are provided separately and are not included in these AAE datasets.

## Data quality, governance and provenance

- Methods aligned with UNECE CLRTAP-based practices; detailed quality assurance and a formal UK Methods Report (Hall et al., 2015) are available.
- Metadata and provenance reflect national/international collaborations; datasets are consistent with ongoing UK trend reporting (e.g., Rowe et al., 2023 Trends Report).

## Use, interpretation and limitations

- AAE indicates potential long-term harm under steady-state or long-term conditions; exceeding critical loads does not imply immediate damage.
- Habitat maps and areas used for calculating critical loads may differ from other national habitat maps, and data are limited to areas with available data for calculation.
- Recovery after reducing deposition below the critical load can be slow; chemical and biological recovery timescales may be long, especially for sensitive ecosystems.
- The two AAE rasters have different UK coverage due to habitat distributions for acidification vs eutrophication.

## Data structure and format

- Two raster files (acid_aae_2019-2021.tif and nutn_aae_2019-2021.tif), each with a single band.
- Projection: British National Grid (EPSG:27700).

## Appendix I (Acidity critical loads for woodland)

- Provides the simple mass balance equation for woodland acidity critical loads and related terms (CLA, ANCw, ANCle(crit), Alle(crit), BCle, Hle(crit), etc.), including how calcium and aluminium fluxes influence the critical load calculation for woodland habitats.

## References

- Comprehensive references to methods, datasets, and supportive studies, including Hall et al. (2015), Henriksen & Posch (2001), Sverdrup & De Vries (1990, 1994), Calver (2003, 2004), Skiba & Cresser (1989), Smith et al. (1992), and others.
- Related datasets and reports: UK Trends Reports (Rowe et al., 2023), UK Land Cover Map 2019 (Morton et al., 2022).