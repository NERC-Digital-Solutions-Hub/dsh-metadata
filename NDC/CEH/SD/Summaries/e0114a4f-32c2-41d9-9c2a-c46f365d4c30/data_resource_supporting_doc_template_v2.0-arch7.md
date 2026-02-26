# Emissions of Ammonia (NH 3 ) from Agriculture in South Asia in 2015.

## Overview
- Gridded, bottom-up estimates of annual NH3 emissions from agricultural sources in SAARC for 2015.
- Spatial resolution: 0.1° x 0.1°; domain masked to Afghanistan, Bangladesh, Bhutan, India, Maldives, Nepal, Pakistan and Sri Lanka.
- Data format: GeoTIFF; units are grams per square metre per year (g m^-2 yr^-1); NA values indicate outside the domain.
- Five sub-sectors are represented: crop residue burning, crop residues left in fields, livestock management, livestock grazing and manure applications, and application of synthetic fertilisers.
- Methodology follows EDGARv6.1, IPCC 2006 Guidelines, IPCC 2019 Refinement, and EMEP/EEA guidebooks (2019, 2023) with region-specific data to improve representation.

## Data Files and Naming
- NH3_CRB_SouthAsia_2015_gm2_0.1.tif — Emissions from crop residue burning.
- NH3_CRR_SouthAsia_2015_gm2_0.1.tif — Emissions from crop residues left in fields.
- NH3_GRM_SouthAsia_2015_gm2_0.1.tif — Emissions from livestock grazing and manure applications.
- NH3_MNM_SouthAsia_2015_gm2_0.1.tif — Emissions from livestock management (housing, storage of manures & slurries, yarding).
- NH3_SFA_SouthAsia_2015_gm2_0.1.tif — Emissions from synthetic fertiliser application.
- All files are gridded GeoTIFFs with the same spatial footprint; non-domain cells are NA.

## Spatial and Temporal Coverage
- Spatial: SAARC country domain with coordinates xmin 60.5°, xmax 97.4°, ymin -0.7°, ymax 38.5°; World Geodetic System 1984 (WGS84) CRS.
- Resolution: 0.1° x 0.1°.
- Temporal: annual emissions for the year 2015.
- Data production: generated during 2022–2023.

## Methodology
- Emissions are computed using a bottom-up approach combining activity data with emission factors (EFs) per sector.
- Sub-sector specifics:
  - Crop residue burning (CRB): fraction of crops burnt; India-specific burning crop sets; EF as mean of seven MCE values; distributed over EarthStat surfaces reweighted to country totals.
  - Crop residues left in field (CRR): fraction left in field; EF linked to above-ground dry matter and country-specific pH-related EF.
  - Livestock sources (GRM, MNM): N-flow approach; N excretion per head by livestock type; losses by management stage; distributed on country-lot livestock surfaces.
  - Synthetic fertilisers (SFA): total N application by country; N distribution by crop and fertiliser type; emissions computed from EF by fertiliser type and surface pH data; India-specific updates for Urea EF.
- Important regional details:
  - India uses a restricted set of burnt crops (maize, rice, sugar cane, wheat) versus a broader set for other SAARC members.
  - Spatial distribution tied to reweighted EarthStat surfaces and FAOSTAT national totals.
- Quality control: checks for extreme values and NA locations; totals recalculated by sector and cross-validated against non-spatial calculations and other NH3 agriculture estimates.

## Input Data and Sources (Representative Categories)
- Crop harvest distributions (EarthStat; gridded 0.1° x 0.1°).
- Country- and crop-level fertiliser use (FAOSTAT 2023; nitrogen content by fertiliser type).
- State- and country-level crop data (e.g., India 2012/13, Nepal 2014/15).
- Crop residues and management practices (inputs from FAO, IPCC guidance, and region-specific studies).
- Livestock populations, distributions, and management practices (FAOSTAT 2023; global livestock distributions).
- Topsoil pH and related soil data (Batjes et al., 2024; related soil datasets).
- Emission factors and methodological references (EEA EMEP guidebooks 2019/2023; IPCC 2006/2019; EDGARv6.1).

## Reproducibility and Data Quality
- Sectoral totals checked against non-spatial calculations; spatially distributed back to GeoTIFF format for consistency.
- Comparisons made with other NH3 agricultural emission estimates to ensure plausibility.
- Data quality assurance includes validation of extreme values and domain masking.

## GIS Usage and Practical Notes
- Suitable for map-based analyses and regional policy/applications within SAARC.
- Use per-sector GeoTIFFs for layered visualization; combine for total NH3 emissions.
- Be mindful of the India-specific burnt-crop rule when aggregating or comparing with other regions.
- NA values correctly mask areas outside SAARC coverage; ensure alignment with other geospatial layers using WGS84.

## References
- Key methodological references include EDGARv6.1, IPCC Guidelines (2006, 2019), and EMEP/EEA Guidebooks (2019, 2023); supporting data sources span FAOSTAT, EarthStat, FAO/IRRI datasets, and region-specific studies.