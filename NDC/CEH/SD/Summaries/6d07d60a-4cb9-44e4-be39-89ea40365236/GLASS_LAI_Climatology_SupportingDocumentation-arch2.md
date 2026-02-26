# Global gridded monthly mean Leaf Area Index (LAI) for five Plant Functional Types (PFTs) derived from the Global LAnd Surface Satellite (GLASS) products for the period 2000-2014

## Summary
- Global monthly LAI climatology for five Plant Functional Types (PFTs) derived from GLASS, covering 2000–2014, intended for use in JULES and the UK Met Office Unified Model.
- Improves upon previous JULES_LAI_current data by providing correct seasonality and consistent spatial distribution; LAI is partitioned into PFTs using CCI Land Cover fractions.
- Data are provided as CF-compliant NetCDF files on a 0.5° × 0.5° grid, with accompanying PFT/land-cover fractions, suitable for model initialization, validation, and evaluation.

## Data and Variables
- GLASS_LAI_Global_0.5deg.nc
  - Variables: LAI (unitless) and canopy height (m)
  - Dimensions: month, pft (Broad Leaf, Needle Leaf, C3 Grass, C4 Grass, Shrub), lat, lon
  - Description: Monthly LAI climatology (2000–2014) derived from GLASS MODIS data, plus canopy height per grid cell
- Land_Cover_Frac_LC-CCI.nc
  - Variables: canopy height (m) and land_cover_class (%)
  - Dimensions: month, pft, lat, lon (plus pseudo_lat/pseudo_lon)
  - Description: Fractional distribution of PFTs and land cover classes per grid cell from ESA CCI data
- Grid/Format
  - 0.5° latitude/longitude grid
  - NetCDF format, CF conventions v1.6
  - Monthly climatology (12 timesteps)

## Methodology
- LAIGLASS is partitioned into five PFT LAIs using fixed relative weights: Broad Leaf = 4, Needle Leaf = 3, C3 Grass = 2, C4 Grass = 4, Shrub = 1 (relative weights were previously used in JULES configurations).
- The GLASS LAI product (2000–2014 MODIS data; 1981–1999 AVHRR data not used here) is voxelized to 0.5° grid via ANTS and Iris, then distributed to PFTs according to the CCI PFT fractions.
- Validation against GLASS LAI demonstrates that the segregated PFT LAIs preserve overall LAI seasonality with negligible data loss/gain during segregation; the resulting PFT-specific seasonality is more realistic globally than the previously used JULES_LAI_current product.
- The approach emphasizes improving LAI seasonality and model-consistency for use in climate and land-surface models.

## Applications and Use
- Primary use: initialization, validation, and evaluation of land-surface and earth-system models (e.g., JULES, UKMO Unified Model).
- Facilitates dynamic vegetation representation by providing monthly LAI per PFT and corresponding canopy height.

## Data Quality and Limitations
- GLASS LAI dataset (2000–2014) chosen for this product due to better temporal and spatial homogeneity and validation against high-resolution references.
- The relative PFT weights are fixed across space and time; spatially/temporally varying weights were not implemented.
- The integration process shows good agreement with GLASS LAI; any minor discrepancies are attributed to small differences in CCI-derived PFT fractions and data handling during segregation.

## Access and Format
- CF-compliant NetCDF v1.6 files
- Datasets are provided as a pair of files in the same resource and can be downloaded jointly:
  - GLASS_LAI_Global_0.5deg.nc
  - Land_Cover_Frac_LC-CCI.nc
- Available via the EIDC catalogue as part of the dataset titled “Global gridded monthly mean Leaf Area Index (LAI) for five Plant Functional Types (PFTs) derived from the GLASS products for 2000-2014.”

## Acknowledgements
- Supported by the NERC VER A project (NE/M003574/1) and published under the NERC HydroJULES project (NE/S017389/1).
- Authors: Semeena, Taylor, Folwell, Hartley; CEH and UK Met Office.