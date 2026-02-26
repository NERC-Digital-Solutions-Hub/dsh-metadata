# Emissions of Ammonia (NH 3 ) from Agriculture in South Asia in 2015

## Overview
- Dataset of annual NH3 emissions from agricultural sources in SAARC for 2015.
- Units: grams of NH3 flux per square metre per year (g m^-2 yr^-1); data are gridded at 0.1° x 0.1°.
- Domain: Afghanistan, Bangladesh, Bhutan, India, Maldives, Nepal, Pakistan, and Sri Lanka; cells outside these countries are NA.
- Purpose: to better represent NH3 emissions in South Asia with regional data (e.g., sub-national fertiliser statistics) for improved inventories.

## Data content
- Emissions are represented by five sub-sectors:
  - crop residue burning (CRB)
  - crop residues left in fields (CRR)
  - livestock management (housing, storage of manures & slurries, yarding)
  - livestock grazing and manure applications (GRM/MNM)
  - application of synthetic fertilisers (SFA)
- Data are bottom-up calculations using activity data and emission factors (EFs), following EDGARv6.1, IPCC 2006 Guidelines, IPCC 2019 Refinement, and EMEP/EEA guidebooks.
- Each sub-sector is mapped to a GeoTIFF:
  - NH3_CRB_SouthAsia_2015_gm2_0.1.tif
  - NH3_CRR_SouthAsia_2015_gm2_0.1.tif
  - NH3_GRM_SouthAsia_2015_gm2_0.1.tif
  - NH3_MNM_SouthAsia_2015_gm2_0.1.tif
  - NH3_SFA_SouthAsia_2015_gm2_0.1.tif
- Outputs are designed to reflect regional specifics (e.g., crop burning fractions vary by country, with India-specific burn crop sets).

## File format and naming
- Format: GeoTIFF (geospatial raster format).
- File names encode sector, region, year, and resolution as shown above.

## Spatial and temporal coverage
- Spatial: SAARC region with WGS84 coordinate reference system; extent xmin 60.5°, xmax 97.4°, ymin -0.7°, ymax 38.5°; resolution 0.1° x 0.1°.
- Temporal: annual emissions for the year 2015.
- Production timeframe: data produced in 2022–2023.

## Input data and methodology
- Input data sources include:
  - Crop harvest distributions (EarthStat 0.1° grids)
  - National and sub-national crop area and yield data (FAOSTAT 2023; India/Nepal specifics)
  - Crop residue parameters and burning practices
  - Fertiliser use by type and total N content (FAOSTAT 2023)
  - Livestock populations, distributions, and management practices (FAOSTAT 2023; global livestock distributions)
  - Topsoil properties (pH)
  - Nitrogen application and crop-specific N data
- Methodological framework:
  - EDGARv6.1-based calculations for agricultural soils and livestock emissions
  - IPCC 2006 Guidelines and 2019 Refinement
  - EMEP/EEA guidebooks (2019, 2023)
  - Region-specific data incorporation (country/region data as per inputs)
  - Sub-sector specific treatment (e.g., EF adjustments for India, crop-specific burn fractions, and N-flow approach for livestock)
- Output emission surfaces are spatially distributed and reweighted to FAOSTAT totals and country-specific data.

## Quality control
- Checks for outliers and NA values.
- Totals for NH3 by sector/sub-sector computed and sense-checked; spatially distributed to GeoTIFFs.
- Sector totals validated against non-spatial calculations and compared with other NH3 agricultural emission estimates.

## Usage and notes
- The dataset provides spatially explicit NH3 emission fluxes suitable for regional atmospheric modelling and policy analyses.
- Sub-sector details enable targeted analyses (e.g., burning practices, synthetic fertiliser applications, livestock management phases).
- Users should be aware of country-specific assumptions (e.g., crop burning sets, emission factors, and reweighting steps) and consider local data updates where available.

## References
- Methodological and data-source references include EDGARv6.1, IPCC Guidelines (2006, 2019 Refinement), EMEP/EEA guidebooks (2019, 2023), FAOSTAT, EarthStat, and various country- and crop-specific studies and datasets cited in the accompanying documentation.