# Supporting documentation for European Monitoring and Evaluation Program Model for the UK (EMEP4UK) daily atmospheric composition and fluxes for UK-SCAPE (1960 - 2020)

## Overview
- Provides daily averaged atmospheric composition for the UK (1960–2020) for main nitrogen, sulfur, particulate organic matter, and ozone.
- Generated with EMEP4UK model version rv5.0 and Weather Research and Forecasting (WRF) model version 4.4.2.

## Data scope and content
- Scope: UK-scale daily averages, derived from an ACTM (atmospheric chemistry transport model) with EU domain resolution and a nested UK domain.
- Spatial resolution: EU domain at 27 × 27 km2 with a nested UK domain at 3 × 3 km2; only UK model results are included.
- Temporal coverage: 1960–2020.
- Emissions inputs: UK emissions from NAEI (NOx, NH3, SO2, primary PM2.5, primary PMcoarse, CO, NMVOCs) for a given year; non-UK emissions at 0.1° × 0.1° from CEIP; UK total is used for the year 1960–2020.
- Meteorology: 3D meteorology from WRF with ERA5 data assimilation (Newtonian nudging) at 0.25° × 0.25° every 6 hours.

## Experimental design and provenance
- Model lineage: EMEP4UK rv5.0 derived from EMEP MSC-W rv5.0, configured to simulate hourly to daily atmospheric composition and deposition.
- Domain and grid details: UK domain results extracted from the EU-wide 27 × 27 km2 grid; 3 × 3 km UK nest.
- Computational environment: Fortran Intel compiler 19.1.3.304; calculations performed on the UKCEH POLAR cluster (CentOS 7).

## Data products and variables
- Key species and products include: surface concentrations for PM2.5, PMcoarse, PM10; ozone; isoprene; carbon monoxide; ammonia; nitric/nitric acid; NOx; NH3; HCHO; dust (and natural/coarse/fine components); black carbon and organic matter (various forms); and mixing layer height (HMIX).
- NetCDF conventions: variables have designated NetCDF names (e.g., SURF_ug_PM25_rh50, SURF_ppb_O3, HMIX, SURF_MAXO3, SURF_PM25water, etc.) with corresponding units described in the documentation.
- Units: surface concentrations in µg m−3 or ppbv, with many fields explicitly defined (e.g., PM2.5, PM10, gases like O3, NO2, CO, NH3, HNO3, etc.). Detailed naming conventions and equivalents are provided in the supporting text.

## Data format, access, and usage
- Format: NetCDF files; data described by detailed variable lists and units.
- Grid projection: Polar stereographic projection; proj4 string provided for use in applications.
- Compatibility: NetCDF libraries compatible with R, Python, and FORTRAN.
- Use guidance: Users should configure their software to the specified CRS and NetCDF conventions; data quality control has been performed, but it is provided with a disclaimer of use "at your own risk."

## Quality assurance and limitations
- QA/QC: Conducted for 1960–2020; QA/QC reports available on request; not included in the document.
- Limitations and warranty: Content use is at the user’s own risk; no warranty or guarantee of error-free data or fitness for a particular use.

## Guidance for data users and governance considerations
- Dataset is a long-term, high-resolution UK atmospheric composition product suitable for policy analysis, environmental modelling, and cross-network data integration.
- Provenance is clearly described (model versions, data assimilation, emission inputs, and computing environment), supporting reproducibility and traceability.
- The dataset is historical (1960–2020) with no explicit ongoing updates documented in this file.

## References and sources
- Ge et al. (2021), evaluation of global EMEP MSC-W and WRF models for surface concentrations and wet deposition.
- Gu et al. (2021), findings on ammonia vs. NOx mitigation costs for PM2.5.
- Jalkanen et al. (2016); Simpson et al. (2012); Skamarock et al. (2019); Vieno et al. (2016a, 2016b) – foundational methodological references for EMEP4UK, WRF, and UK PM2.5 studies.
- NAEI (National Atmospheric Emission Inventory) and CEIP contributions for UK and non-UK emissions inputs.
- The dataset is published with a comprehensive bibliography accompanying the model documentation.