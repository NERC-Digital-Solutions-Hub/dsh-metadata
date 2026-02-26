# Emissions of Ammonia (NH 3 ) from Agriculture in South Asia in 2015.

## Scope and purpose
- Provides 2015 annual NH3 emissions from agricultural sources in SAARC, representing total emissions at a 0.1° x 0.1° grid.
- Aims to better represent NH3 emissions in South Asia by incorporating regionally specific information (e.g., sub-national fertiliser statistics) beyond standard international inventories.
- Emissions are estimated using bottom-up calculations based on activity data and emission factors, following established methodologies.

## Spatial and temporal coverage
- Domain: SAARC countries – Afghanistan, Bangladesh, Bhutan, India, Maldives, Nepal, Pakistan, Sri Lanka.
- Spatial resolution: 0.1° x 0.1°; CRS: WGS84; domain extents xmin 60.5°, xmax 97.4°, ymin -0.7°, ymax 38.5°.
- Temporal coverage: annual emissions for the year 2015.
- Data production period: 2022–2023.
- NA cells are used for areas outside the specified countries.

## Data format and file naming
- File format: GeoTIFF.
- Sub-sector files:
  - NH3_CRB_SouthAsia_2015_gm2_0.1.tif — crop residue burning
  - NH3_CRR_SouthAsia_2015_gm2_0.1.tif — crop residues left in fields
  - NH3_GRM_SouthAsia_2015_gm2_0.1.tif — livestock grazing and manure applications
  - NH3_MNM_SouthAsia_2015_gm2_0.1.tif — livestock management (housing, storage, slurries)
  - NH3_SFA_SouthAsia_2015_gm2_0.1.tif — synthetic fertiliser application
- Units: grams of NH3 flux per square metre per year (g m^-2 yr^-1).

## Sub-sectors and emission categories
- Crop residue burning (CRB): fraction of crops burnt post-harvest; India-specific burn sets applied.
- Crop residues left in fields (CRR): fraction left in field; emissions depend on above-ground dry matter and EFs.
- Livestock management (GRM) and livestock grazing/manure (MNM): nitrogen-flow approach using per-animal excretion rates and management-stage losses to derive NH3 fluxes.
- Synthetic fertilisers (SFA): total N application by crop/country per year; converted to NH3 using fertiliser-type-specific EFs and field pH data.

## Methodology and standards
- Based on EDGARv6.1, IPCC 2006 Guidelines, IPCC 2019 Refinement, and EMEP/EEA guidebooks (2019, 2023).
- Incorporates country/region-specific data for improved regional accuracy.
- Emissions are computed per sector/sub-sector and spatially distributed onto country-adjusted EarthStat surfaces; then reweighted to FAOSTAT totals.
- Specific treatment:
  - CRB and CRR use burn/left-in-field fractions with sector-specific emission factors.
  - GRM/MNM use a nitrogen-flow approach across management stages.
  - SFA distributes total N application by crop and country, allocating fertiliser types and applying EF with pH considerations; Urea EF updated in this dataset.

## Input data and sources
- Crop distributions and production data (EarthStat, FAOSTAT, India/Nepal state-level data).
- Crop residue parameters and burning practices (IPCC-based studies; regional literature).
- Emission factors for crops, fertilisers, and livestock (EEA Guidebooks, IPCC references, regional studies).
- Livestock populations, distributions, and management practices (FAOSTAT, global livestock datasets).
- Soil pH and related factors (topsoil data and related sources).
- Nitrogen application data by crop and country (FAOSTAT, 2023).

## Quality control and validation
- Checks for extreme values and NA locations; consistency of sector totals with non-spatial calculations.
- Spatial totals validated against original (non-spatial) calculations and compared with other NH3 agriculture estimates.

## Access, storage, and interoperability
- Data are stored as GeoTIFFs for each sub-sector, enabling integration with GIS workflows and cross-comparison with other emission inventories.
- The methodology emphasizes transparency and reproducibility by aligning with widely used guidelines and incorporating region-specific inputs.

## Relevance to environmental monitoring and policy
- Supports consistent, time-stamped evaluation of agricultural NH3 emissions in South Asia, enabling trend analyses and policy impact assessments.
- Addresses the need to increase dataset value by enabling cross-dataset analyses (e.g., linking NH3 fluxes to fertiliser usage, livestock density, and crop patterns) and facilitating access to underlying data for broader use.
- Provides a granular spatial framework suitable for regional air quality and environmental health assessments, as well as cross-border policy considerations within SAARC.