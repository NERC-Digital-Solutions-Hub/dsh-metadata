# Global gridded monthly mean Leaf Area Index (LAI) for five Plant Functional Types (PFTs) derived from the Global LAnd Surface Satellite (GLASS) products for the period 2000-2014

## Overview
- Global monthly LAI climatology on a 0.5-degree grid, intended for use in JULES and the UK Met Office Unified Model.
- Derived from GLASS LAI time series (MODIS data for 2000-2014) and partitioned into five Plant Functional Types (PFTs).
- Two accompanying files provide LAI/canopy height and PFT/land-cover fractional distributions; CF-compliant NetCDF format.

## Data Content
- LAI and canopy height (H) variables in GLASS_LAI_Global_0.5deg.nc (monthly climatology, 2000-2014).
- PFTs: Broad Leaf, Needle Leaf, C3 Grass, C4 Grass, Shrub (pft dimension 1-5).
- Land cover fractions by PFT/land-cover class in Land_Cover_Frac_LC-CCI.nc (monthly, similarly structured).
- Land cover classes include 5 PFTs plus Urban, Inland Water, Bare Soil, Snow/Ice (pseudo dimension 1-9).
- Units and roles:
  - LAI: unitless (important for energy/water/CO2 balance in models).
  - Canopy height: meters.
- Grid and format:
  - 0.5-degree global grid, CF v1.6 netCDF format.
  - Dimensions: month, pft, lat, lon for LAI and H; month, pseudo, lat, lon for land-cover fractions.

## Processing Methodology
- Base LAI time series drawn from GLASS (1981-2014); this dataset uses GLASS-derived LAI for 2000-2014.
- Partitioning LAI into 5 PFTs using CCI Land Cover fractional data per grid box.
- Fixed relative weights to allocate total LAI to PFTs: Broad Leaf 5, Needle Leaf 4, C3 Grass 2, C4 Grass 4, Shrub 1.
- ANTs toolkit (Python-based) used to segregate GLASS LAI into 5 PFTs; Iris aggregated results to 0.5-degree grid.
- Validation against GLASS LAI shows close agreement; JULES_LAI_current (earlier product) underestimates LAI and misrepresents seasonality in several regions.
- Purpose-built to improve seasonality and spatial distribution of LAI for model initialization and evaluation.

## Data Quality and Validation
- GLASS LAI used for validation; comparison indicates negligible data loss/gain during PFT segregation.
- LAI seasonality of PFT components aligns more realistically with expected global patterns than previous products.
- Consistency with in situ and satellite-based measurements supports dataset reliability for model applications.
- Some minor discrepancies attributed to cases with negligible vegetation fraction in CCI data.

## File Formats and Access
- Files included in the dataset package:
  - GLASS_LAI_Global_0.5deg.nc: LAI and canopy height, monthly climatology, 0.5-degree grid.
  - Land_Cover_Frac_LC-CCI.nc: Fractional distribution of land cover classes (PFTs and others), monthly, 0.5-degree grid.
- Both files are NetCDF CF-compliant (v1.6) and intended to be downloaded together from the dataset resource in the EIDC catalog.

## Usage Guidance for Data Support
- Primary use: initialize and validate land-surface models (e.g., JULES, UKMO MO) with realistic LAI seasonality split by PFT.
- How to use:
  - Combine GLASS_LAI_Global_0.5deg.nc LAI per grid cell with Land_Cover_Frac_LC-CCI.nc fractions to reconstruct PFT-specific LAI values.
  - Use fixed PFT weights to distribute total LAI across PFTs for each grid cell and month.
  - Ensure CF-compliant access and transformation to the model’s native grid if needed.
- Model applicability:
  - Suitable for global to regional climate/land-surface modelling and validation of vegetation dynamics.
- Validation posture:
  - Leverages GLASSLAI as the reference; aims to improve seasonality and inter-annual consistency over previous products.

## Limitations and Considerations
- PFT LAI partition uses fixed relative weights across time and space; not dynamically varying by region or season.
- Temporal scope is a climatology over 2000-2014 (monthly means), not daily or interannual variability beyond the 2000-2014 window.
- 0.5-degree resolution may be coarse for very fine-scale applications.
- Potential caveats related to fraction data in CCI and the assumption of immutable PFT weights in all grid cells.

## Provenance and Acknowledgments
- Based on the GLASS LAI data lineage; produced under the VER A project (NERC) and published within the HydroJULES framework.
- Acknowledges contributions and guidance from collaborators.

## Summary
- This dataset provides a well-documented, open global LAI climatology at 0.5-degree resolution (2000-2014), partitioned into five PFTs using FA-weighted, fixed ratios and linked to land-cover fractions. It improves the realism of LAI seasonality for climate and land-surface models and has undergone validation against GLASS LAI, with acknowledged benefits over prior products.