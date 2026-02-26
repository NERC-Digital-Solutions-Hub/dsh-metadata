# Global gridded monthly mean Leaf Area Index (LAI) for five Plant Functional Types (PFTs) derived from the Global LAnd Surface Satellite (GLASS) products for the period 2000-2014

## Scope and Purpose
- Provides global monthly LAI climatology for use in land surface models (primarily JULES and UKMO Unified Model) and related earth-system modelling.
- Derived from GLASS LAI time series (2000-2014) based on MODIS surface reflectance data; supports initialization, validation, and evaluation of climate and ecological models.
- Includes a partitioning of total LAI into five Plant Functional Types (PFTs) using fractional PFT cover from the ESA CCI Land Cover product.

## Data Description
- Files and variables
  - GLASS_LAI_Global_0.5deg.nc: monthly LAI and canopy height (H) on a 0.5° grid.
  - Land_Cover_Frac_LC-CCI.nc: fractional coverage for the 5 PFTs and 4 other land-cover classes.
- Spatial and temporal coverage
  - Global domain at 0.5° resolution, monthly climatology for 2000-2014 (15-year GLASS period).
- Variables
  - LAI: Leaf Area Index (dimensionless; related to canopy foliage).
  - H: Canopy height (m; spatially varying, temporally fixed for PFTs).
  - PFT fractions: Broad Leaf, Needle Leaf, C3 Grass, C4 Grass, Shrub; plus Urban, Inland Water, Bare Soil, Snow/Ice for land-cover classes.
- Format and standards
  - NetCDF files conforming to CF conventions (v1.6).
  - Documentation and metadata align with dataset tables (dimensions: month, pft/pseudo, lat, lon).

## Motivation and Rationale
- Addresses need for a high-quality, open, well-documented global LAI dataset with correct seasonality for climate modelling.
- Prior JULES_LAI_current (2000-2009) exhibited implausible seasonality in several regions (e.g., Africa) due to handling of missing data and segmentation of total LAI into PFTs.
- GLASS LAI (2000-2014 MODIS-based; validated as temporally and spatially homogeneous) provides more reliable seasonality and distribution, improving model initialisation and evaluation.

## Methodology
- Partitioning framework
  - Each grid cell is divided into 5 vegetation PFTs and 4 other land-cover classes (total 9 classes).
  - GLASS LAI is partitioned into PFT LAIs using fixed relative weights across the season and geography: Broad Leaf = 5, Needle Leaf = 4, C3 Grass = 2, C4 Grass = 4, Shrub = 1.
  - PFT LAIs are computed from total LAI via proportional weighting, then aggregated back to total LAI for verification.
- Use of ancillary data
  - PFT fractions per grid box come from the ESA Climate Change Initiative (CCI) Land Cover data (Poulter et al., 2015).
- Processing workflow
  - ANTs (Ancillary Tools and Suites) in Python to segregate 5k GLASS LAI data into 5 PFTs.
  - Iris used to regrid aggregated PFT LAIs to a 0.5° grid.
- Validation and quality
  - Compared JULES_LAI_GLASS (ancillary LAI for JULES) to GLASS LAI; found strong agreement in seasonality and distribution.
  - JULES_LAI_current showed underestimation and incorrect seasonality in many regions; segregation losses during processing were negligible.
- Outputs and applications
  - Dataset supports improved initialization/validation of JULES and UKMO models and can serve broader land-surface and hydrological applications.

## Data Format and Access
- Files
  - GLASS_LAI_Global_0.5deg.nc: LAI (monthly, 0.5° grid, by PFT) and canopy height.
  - Land_Cover_Frac_LC-CCI.nc: PFT fractional distributions and land-cover classes (monthly, 0.5° grid).
- Access and integration
  - Both files are distributed as part of a single dataset/resource in the EIDC catalogue; designed for joint download.
- Dimensions and variables
  - month, pft (1-5) or pseudo (1-9), lat, lon; with CF-compliant naming and units.

## Summary and Implications for Monitoring
- LAI is a key vegetation structural variable driving energy, water, and carbon fluxes in climate models; accurate seasonality and spatial distribution are essential for reliable Earth system simulations.
- The GLASS-based LAI climatology, partitioned into 5 PFTs, provides more realistic, seasonally consistent vegetation dynamics globally.
- The methodology preserves total LAI while delivering PFT-specific LAIs, enabling better representation of vegetation types in model configurations and scenario analyses.
- The approach demonstrates that careful data processing and governance (data provenance, open access, metadata) can yield usable, policy-relevant environmental health indicators for monitoring and decision-support.

## Data Governance, Metadata, and Barriers (Relevance to Monitoring Frameworks)
- Open data and clear provenance are maintained; data are CF-compliant NetCDF, facilitating verification, replication, and reuse.
- Metadata richness supports data quality assessment and auditability; however, fixed PFT weights and reliance on ancillary fractions may warrant future refinements for spatial/temporal variability.
- The workflow relies on cross-institutional data (GLASS, MODIS, ESA CCI) and tooling (ANTS, Iris); governance and collaboration are essential to maintain data quality and timeliness.
- Timeliness: dataset covers 2000-2014; ongoing monitoring would benefit from extended temporal coverage and updates.

## Acknowledgments and References
- Acknowledges the VER A project (NE/M003574/1) and HydroJULES (NE/S017389/1).
- References include key GLASS, CCI, MODIS, and JULES literature and related validation studies.