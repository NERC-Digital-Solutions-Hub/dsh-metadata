# Global gridded monthly mean Leaf Area Index (LAI) for five Plant Functional Types (PFTs) derived from the Global LAnd Surface Satellite (GLASS) products for the period 2000-2014

## Overview
- Global monthly LAI climatology derived from GLASS products, intended for use in JULES and the UK Met Office Unified Model.
- LAI data span 2000–2014, using MODIS-based observations (1 km) interpolated to a 0.5° x 0.5° grid; includes canopy height (H).
- Total LAI is partitioned into five Plant Functional Types (PFTs): Broad Leaf, Needle Leaf, C3 Grass, C4 Grass, and Shrub, using PFT fractions from the ESACCI Climate Change Initiative (CCI) land cover product.
- Provides ancillary fields and is designed to improve seasonality and spatial distribution of LAI in land-surface models, addressing limitations of prior JULES_LAI datasets.

## Data Content
- Two NetCDF files at 0.5° spatial resolution:
  - GLASS_LAI_Global_0.5deg.nc
    - Variables: Leaf Area Index (LAI) and Canopy Height (H) for each PFT.
    - Dimensions: month, pft, lat, lon (12 months, 5 PFTs, global grid).
  - Land_Cover_Frac_LC-CCI.nc
    - Variables: Fractional distribution of land cover classes corresponding to the 5 PFTs plus 4 other classes (total of 9 classes).
    - Dimensions: month, pseudo (class index 1–9), lat, lon.
- PFTs and classes:
  - PFTs: Broad Leaf, Needle Leaf, C3 Grass, C4 Grass, Shrub.
  - Other classes: Urban, Inland Water, Bare Soil, Snow/Ice.
- Purpose: deliver monthly LAI for each grid cell by PFT and the corresponding fractions of land cover PFTs to support model configurations that use PFT-based LAI.

## Methodology
- LAI_GLASS is partitioned into 5 PFT LAIs using fixed relative weights between PFT LAIs: Broad Leaf, Needle Leaf, C3 Grass, C4 Grass, Shrub with weights 5, 4, 2, 4, 1 respectively.
- Weights determine how total LAI is distributed among PFTs within each grid cell and month.
- Process involves:
  - Segregating GLASS LAI into PFT components using CCI-PFT fractions.
  - Aggregating segregated PFT LAIs to the 0.5° grid.
  - Utilizing ANTs (Ancillary Tools and Suites) and Iris (Python-based tools) for data processing and interpolation.
- Rationale: improve the seasonality and geographical realism of LAI used in JULES, addressing prior issues with JULES_LAI_current (notably implausible seasonality in several regions).

## File Format and Datasets
- Format: NetCDF, CF convention v1.6; monthly climatology (12 timesteps).
- Dataset descriptions:
  - GLASS_LAI_Global_0.5deg.nc
    - Variables: leaf area index (LAI), canopy height (H)
    - Dimensions: month, pft, lat, lon
  - Land_Cover_Frac_LC-CCI.nc
    - Variables: canopy height? and land_cover_class (%)
    - Dimensions: month, pseudo, lat, lon
- Usage note: both files are part of the same dataset resource and can be downloaded jointly; designed for integration into climate and land-surface models.

## Validation and Comparison
- GLASS LAI has been validated as a higher-quality, more homogeneous long-term dataset (1981–2014) compared with other LAI products.
- JULES_LAI_GLASS (this dataset segregated into PFTs) is shown to align closely with GLASS LAI, with negligible data loss/gain during PFT partitioning.
- Compared to the previous JULES_LAI_current (MODIS-based 2000–2009 climatology), JULES_LAI_GLASS exhibits correct seasonality (e.g., stronger summer LAI in regions like West Africa) and improved temporal consistency.
- Across locations, the total LAI from JULES_LAI_GLASS matches GLASS LAI closely; JULES_LAI_current underestimates LAI globally.

## Applications and Use
- Primary use: initialization, validation, and evaluation of earth system models, particularly JULES and UKMO Unified Model, for regional and global simulations.
- Enables modelers to represent vegetation canopies as 5 PFTs with monthly LAI and canopy height, consistent with 5-PFT JULES configurations.
- Facilitates better coupling between vegetation structure and energy, water, and carbon flux calculations in climate and land-surface studies.

## Limitations and Notes
- Relative weights for distributing GLASS LAI among PFTs are fixed; spatially/temporally varying weights were not implemented, which could influence some grid-cell-specific dynamics.
- The dataset relies on CCI-PFT fractions; accuracy depends on the underlying land-cover classifications and their applicability to LAI partitioning.
- Some descriptions in the accompanying text may contain minor typographical inconsistencies (e.g., variable naming in the Land_Cover_Frac file), but the overall methodology and dataset structure are consistent with the stated aims.

## Access and Acknowledgments
- Acknowledges support from NERC VERa project and HydroJULES, with contributions from listed authors and collaborators.
- Dataset intended for dissemination via the EIDC catalogue, enabling joint download of both GLASS_LAI and Land_Cover_Frac files.