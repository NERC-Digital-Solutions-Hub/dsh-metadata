# Global gridded monthly mean Leaf Area Index (LAI) for five Plant Functional Types (PFTs) derived from the Global LAnd Surface Satellite (GLASS) products for the period 2000-2014

- Global monthly LAI climatology derived from GLASS products, intended for use with JULES and the UK Met Office Unified Model (UKMO).
- Covering 2000–2014, with data originally from MODIS surface reflectance (1 km) for 2000–2014, interpolated to a 0.5° × 0.5° grid on a geographic projection.
- LAI is partitioned into five Plant Functional Types (PFTs): Broad Leaf, Needle Leaf, C3 Grass, C4 Grass, Shrub; a second file provides PFT fractions and other land cover classes (Urban, Inland Water, Bare Soil, Snow/Ice) based on ESACCI LC (CCI dataset).
- The dataset is designed to support land-surface models, primarily JULES, by providing PFT-specific LAI and canopy height, along with land-cover fractions required for model initialization and validation.

## Dataset contents and file structure

- Two NetCDF files at 0.5° spatial resolution:
  - GLASS_LAI_Global_0.5deg.nc: variables include Leaf Area Index (LAI) and Canopy Height (H) with dimensions month, pft, lat, lon.
  - Land_Cover_Frac_LC-CCI.nc: variables include Canopy Height (m) and land_cover_class fractions (%), with dimensions month, pseudo, lat, lon (pft = 1–5; pseudo = 1–9 representing land cover classes).
- Data are provided as monthly climatologies (12 timesteps) for 2000–2014.
- CF conventions v1.6 compliance; designed for joint download as a single data resource in the EIDC catalogue.

## Methodology and data processing

- LAI_GLASS data are partitioned from total GLASS LAI into five PFT LAIs using fixed relative weights across space and time: Broad Leaf = 5, Needle Leaf = 4, C3 Grass = 2, C4 Grass = 4, Shrub = 1.
- Partitioning relies on per-grid-cell PFT fractional coverage from the ESACCI LC-CCI dataset to determine PFT shares.
- Process workflow:
  - Use ANTs (Ancillary Tools and Suites) to segregate GLASS LAI into 5 PFTs.
  - Aggregate to 0.5° grid using Iris.
  - Combine with LC-CCI fractions to produce PFT-specific LAI and total LAI (for quality checks).
- Canopy height (H) is included for each grid box/PFT; accompanying Land_Cover_Frac_LC-CCI.nc provides the fractions for the 9 land-cover classes (5 PFTs + 4 other classes).
- Validation and comparison:
  - The GLASS-derived LAI shows improved seasonality and spatial consistency compared with the previous JULES_LAI_current product, which had implausible seasonality in some regions (notably Africa).
  - The JULES_LAI_GLASS product aligns closely with GLASS LAI time series, indicating negligible loss/gain during the PFT segregation process.
  - Comparisons with in-situ and satellite data support the reliability of GLASS LAI over the 2000–2014 period.

## Purpose and use cases

- Primary use: initialization, validation, and evaluation of land-surface and climate models, particularly JULES and UKMO configurations that require:
  - Monthly LAI per grid cell for each PFT.
  - Canopy height information for each grid cell.
  - Fractional distribution of PFTs and other land cover classes to support model parameterization and scaling.
- While developed for JULES, the dataset is suitable for other global/regional land-surface and hydrological model applications needing spatially and temporally resolved LAI by PFT.

## Data quality, standards, and limitations

- Data quality: improved seasonality and spatial distribution of LAI relative to older products; strong agreement with GLASS LAI time series after PFT segregation.
- Limitations:
  - PFT LAI ratios (the relative weights among PFT LAIs) are fixed (5, 4, 2, 4, 1) and may not reflect temporal or spatial variability; future work could implement varying weights.
  - The provenance of the fixed PFT weighting is unclear; the approach represents a pragmatic solution focused on seasonality correction.
  - The dataset provides a 15-year climatology (2000–2014) rather than full time-series variability beyond this period.
- Metadata and provenance are documented, with acknowledgments to the VER A project and related funding; data described as open and documented for reproducibility.

## Format, access, and usability

- NetCDF (CF v1.6) format; monthly climatologies stored as:
  - GLASS_LAI_Global_0.5deg.nc: LAI and Canopy Height by month, PFT, lat, lon.
  - Land_Cover_Frac_LC-CCI.nc: Canopy Height and land_cover_class fractions by month, pseudo (land-cover classes), lat, lon.
- Data are provided as a single dataset/resource in the EIDC catalogue; designed for joint download of both files to facilitate model use.
- Documentation supports model integration, including dimension definitions (month, pft, lat, lon; pseudo for land-cover classes) and variable units.

## Summary and implications for data stewardship

- This dataset delivers a robust, PFT-split LAI climatology (2000–2014) and associated land-cover fractions to support climate and land-surface models with improved seasonal dynamics and spatial realism.
- Governance implications:
  - Clear provenance: GLASS-derived LAI with PFT partitioning based on CCI LC-CCI fractions; open, CF-compliant NetCDF deliverables.
  - Documentation of methodology, including fixed PFT weights and data processing steps using ANTS/Iris, supports reproducibility and auditability.
  - Accessible via a centralized data portal (EIDC) with associated metadata facilitating discovery and reuse.
- Data Stewards should track versioning, ensure metadata remains aligned with CF standards, and consider updating weighting schemes as new PFT weighting approaches become available to maintain accuracy across changing land cover and vegetation dynamics.