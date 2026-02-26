# Global gridded monthly mean Leaf Area Index (LAI) for five Plant Functional Types (PFTs) derived from the Global LAnd Surface Satellite (GLASS) products for the period 2000-2014

- Global monthly LAI climatology for five PFTs (Broad Leaf, Needle Leaf, C3 Grass, C4 Grass, Shrub) and canopy height (H), derived from GLASS MODIS data.
- Time coverage: 2000–2014 (15 years); spatial resolution: 0.5° x 0.5° global grid; projection: geographic latitude/longitude (lat/lon).
- LAI partitioned into PFTs using fixed relative weights and PFT fractional coverage from ESA CCI Land Cover data.
- Two data files in NetCDF CF v1.6 format:
  - GLASS_LAI_Global_0.5deg.nc: contains LAI and canopy height variables.
  - Land_Cover_Frac_LC-CCI.nc: contains fractional distribution of PFTs and other land cover classes (9 classes total).
- Dataset intended for initialization/validation of JULES and UKMO Unified Model, with focus on improved LAI seasonality and spatial distribution.

## Data content and structure

- GLASS_LAI_Global_0.5deg.nc
  - Variables: Leaf Area Index (LAI) and Canopy Height (H) on a 0.5° grid.
  - Dimensions: month, pft, lat, lon.
  - LAI is unitless; H is in meters.
- Land_Cover_Frac_LC-CCI.nc
  - Variable: land_cover_class Fractions and Canopy Height per grid cell.
  - Dimensions: month, pft, lat, lon (plus a pseudo dimension for land cover classes).
  - PFTs correspond to five vegetation classes; other land cover classes included (Urban, Inland Water, Bare Soil, Snow/Ice).
- File format: NetCDF with CF conventions (v1.6); monthly climatological fields.

## Methodology

- Data sources:
  - LAI derived from GLASS MODIS surface reflectance (2000–2014; 1 km MODIS, regridded to 0.5° grid).
  - PFT fractions derived from ESA CCI Land Cover data (fractional coverage per grid cell).
- LAI partitioning:
  - Total GLASS LAI per grid cell is distributed among the five PFTs using fixed relative weights: Broad Leaf = 5, Needle Leaf = 4, C3 Grass = 2, C4 Grass = 4, Shrub = 1.
  - Equation basis: LAI_GLAS S = sum(PFT_fraction_i * LAI_PFT_i); fixed weights applied to derive LAI per PFT.
- Processing tools:
  - ANTs (Ancillary Tools and Suites) used to segregate GLASS LAI into 5 PFTs.
  - Iris used to regrid/seal data to 0.5°.
- Validation:
  - Compared JULES_LAI_GLASS (PFT-segregated LAI) with GLASS LAI; found close agreement, validating the segregation procedure.
  - Demonstrated that the new GLASS-based LAI climatology improves seasonality relative to the older JULES_LAI_current dataset, which underestimated LAI in many regions.

## Spatial and temporal coverage

- Global domain with monthly resolution.
- Time period: 2000–2014 (15 years) for the LAI climatology.
- Spatial grid: 0.5° latitude × 0.5° longitude.

## Using in GIS and related applications

- Suitable for:
  - Initializing and validating land surface and climate models (e.g., JULES, UKMO Unified Model).
  - Map-based analyses of LAI by Plant Functional Type and by land cover class.
  - Exploring seasonal dynamics of canopy structure and its regional variations.
- How to use:
  - Load GLASS_LAI_Global_0.5deg.nc for LAI and canopy height per PFT.
  - Use Land_Cover_Frac_LC-CCI.nc to map PFT fractional coverage and land cover classes per grid cell.
  - Combine to produce per-grid LAI by land cover type, or total LAI by PFT for model inputs or GIS visualizations.

## Data quality, limitations, and notes

- Strengths:
  - GLASS LAI provides temporally and spatially homogeneous long time-series; validated against in situ and satellite measurements.
  - Improved LAI seasonality compared with previous JULES_LAI_current dataset.
- Limitations:
  - PFT LAI partitioning uses fixed, globally uniform weights; provenance of these ratios is not temporally/spatially varying.
  - Segregation relies on CCI PFT fractions; potential uncertainties in areas with low data quality or missing values.
  - Although GLASS covers 1981–2014, this product uses only 2000–2014 MODIS-based LAI for the climatology.
- Data handling considerations:
  - Missing data handling in the original MODIS LAI could influence LAI values in certain regions, though the aggregation to PFTs aims to minimize impact.

## Access, provenance, and related resources

- Data is published under the VER A project (NERC) and linked to HydroJULES; downloadable as a combined dataset from the EIDC catalogue.
- Acknowledges contributions from UK Met Office ANTS/Iris tools and related collaborators.

## Summary

- The dataset provides a globally consistent, 0.5° grid, monthly LAI climatology for five PFTs plus canopy height, derived from GLASS MODIS data (2000–2014) and partitioned using ESA CCI land cover fractions with fixed PFT weights.
- It replaces older, less accurate LAI datasets by offering improved seasonality and spatial distribution, suitable for initializing and validating climate and land surface models.
- Delivered as two CF-compliant NetCDF files, enabling integrated GIS analyses and model applications.