# Supporting documentation for European Monitoring and Evaluation Program Model for the UK (EMEP4UK) daily atmospheric composition and fluxes for UK-SCAPE (1960 - 2020)

- Dataset provides daily averaged atmospheric composition for the UK, covering main nitrogen, sulfur, particulate organic matter, and ozone for 1960–2020.
- Based on EMEP4UK model rv5.0 and Weather Research and Forecasting (WRF) model v4.4.2.
- Daily outputs are suitable for GIS-oriented analyses and map-based visualisations.

## Overview of the modelling and data generation

- Experimental design
  - ACTM-based modelling (EMEP4UK rv5.0) derived from EMEP MSC-W rv5.0, simulating hourly to annual concentrations and deposition.
  - 3D meteorology from WRF v4.4.2; data assimilation (Newtonian nudging) of ERA5 at 0.25°×0.25° every 6 hours.
  - Spatial domain includes EU-wide 27×27 km2 resolution with a nested UK domain at 3×3 km2; only UK model results are provided.
- Emissions and inputs
  - UK anthropogenic emissions (NOx, NH3, SO2, primary PM2.5, primary PMcoarse, CO, non-methane VOC) from NAEI for specific years.
  - Non-UK emissions and UK total (1960–2020) from CEIP at 0.1°×0.1° resolution.
- Computational details
  - FORTRAN Intel compiler 19.1.3.304; calculations run on the UKCEH POLAR cluster.

## Spatial coverage, grid, and GIS readiness

- Coverage and resolution
  - UK-focused outputs on a 3×3 km2 nested domain; EU-wide background at 27×27 km2.
- Grid and projection
  - Data projected on a polar stereographic grid.
  - Proj4 string: '+proj=stere +ellps=sphere +lat_0=90.0 +lon_0=0.0 +x_0=0.0 +y_0=0.0 +units=km +k_0=0.9330127018922193 +no_defs +type=crs'.
- NetCDF format and GIS integration
  - Outputs are NetCDF files; compatible with major GIS and data-science tools (R, Python, FORTRAN).
  - Guidance provided to specify the CRS in applications for correct spatial alignment.

## Nature, units, and key variables

- Species and surface concentrations
  - Near-surface concentrations for a wide set of pollutants including NOx, NO, NO2, O3, CO, HNO3, NH3, NH4, PM2.5, PMcoarse, PM10, dust (various size fractions), sea salt, elemental and organic carbon, secondary organic aerosols, and others.
- PM definitions and composition
  - PM2.5 defined as PM2.5 including water and various components (examples given: SURF_ug_PM25_rh50, SURF_PM25water).
  - PMcoarse defined and used to compute PM10 (PM2.5 + PMcoarse).
  - Variables include both primary emitted and secondary components (e.g., biomass burning, sea salt, dust, SIA, SOA).
- NetCDF variable naming conventions (examples)
  - Near-surface ozone: SURF_ppb_O3
  - NO, NO2: SURF_ppb_NO, SURF_ppb_NO2
  - PM2.5: SURF_ug_PM25_rh50
  - PM2.5 water content: SURF_PM25water
  - Nitric acid: SURF_ppb_HNO3 or SURF_ug_HNO3 depending on context
  - Ammonia: SURF_ppb_NH3 or SURF_ug_NH3
  - Organic and elemental carbon: SURF_ug_ECCOARSE, SURF_ug_ECFINE
  - Dust: SURF_ug_DUST (and NAT_C, NAT_F for natural coarse/fine dust)
  - VOC/biomass burning tracers, sea salt, SIA, NOx, deposition fluxes, and more (see full variable list in documentation)
- Fluxes and depositional terms
  - Wet and dry deposition variables (e.g., WDEP_HNO3, DDEP_OXN_m2Grid)
  - Wet deposition of oxidised/reduced nitrogen, precipitation, and related fluxes.

## Data quality, documentation, and caveats

- Quality assurance
  - QA/QC conducted for 1960–2020; detailed QA/QC reports available on request.
  - Usage is at user’s risk; no warranty or guarantee of error-free content.
- Documentation and example structure
  - Includes examples of NetCDF outputs (e.g., SURF_ug_PM25_rh50 for 1960).
  - Comprehensive guidance on dataset usage and projection details provided.

## How this data can be used in GIS workflows

- Map-based visualization of UK air quality and atmospheric composition over time (1960–2020) at 3×3 km UK resolution, with finer resolution context from the EU domain.
- Integration with other GIS data by aligning to the polar stereographic grid and using the provided proj4 string.
- Time-series and trend analyses of key pollutants at the national scale, with potential downscaling or overlay with emission and deposition datasets.
- Potential for combining with policy-relevant layers (policy colleagues, clients, public) to illustrate historical air quality changes and attribution.

## References and further reading

- Ge, Y., Heal, M. R., Stevenson, D. S., Wind, P., and Vieno, M. (2021). Evaluation of global EMEP MSCW (rv4.34) WRF (v3.9.1.1) model surface concentrations and wet deposition of reactive N and S with measurements. Geoscientific Model Development, 14, 7021-7046.
- Gu, B., et al. (2021). Abating ammonia is more cost-effective than nitrogen oxides for mitigating PM2.5 air pollution. Science, 374, 758-762.
- Jalkanen, J.P., Johansson, L., Kukkonen, J. (2016). Inventory of ship traffic exhaust emissions in European seas. Atmospheric Chemistry and Physics, 16, 71-84.
- NCEP/NOAA/UCAR data references and related model descriptions cited in the documentation.
- Simpson, D., et al. (2012); Vieno, M., et al. (2016a, 2016b); Skamarock, W.C., et al. (2019) for modelling framework and methodology.