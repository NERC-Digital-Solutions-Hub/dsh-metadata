# Supporting documentation for European Monitoring and Evaluation Program Model for the UK (EMEP4UK) daily atmospheric composition and fluxes for UK-SCAPE (2002 - 2021)

## Overview
- Daily averaged atmospheric composition for the UK (2002–2021) focusing on major nitrogen, sulphur, particulate organic matter, and ozone.
- Based on the EMEP4UK rv4.36 atmospheric chemistry transport model (ACTM), derived from EMEP MSC-W rv4.36, coupled with the WRF model (v4.2.2) for 3D meteorology.
- UK-domain results are provided within a larger EU domain (27 × 27 km2) with a nested UK domain at 3 × 3 km2.

## Experimental design and data sources
- Meteorology: 3D fields from WRF v4.2.2 with data assimilation (Newtonian nudging) of NWP reanalysis from NCEP/NCAR GFS (1° × 1° every 6 hours).
- Emissions: UK NOx, NH3, SO2, primary PM2.5, primary PMcoarse, CO, and NMVOCs from the 2019 National Atmospheric Emission Inventory (NAEI); non-UK emissions from CEIP at 0.1° × 0.1°. For 2020–2021, UK total emissions use 2019 estimates.
- Model framework: EMEP4UK rv4.36 coupled to WRF; computations performed on the UKCEH POLAR cluster using the Intel FORTRAN compiler.

## Spatial, temporal coverage and data scope
- Temporal: daily averaged data for 2002–2021; includes daily fluxes and surface concentrations.
- Spatial: EU domain at 27 × 27 km2 with a nested UK domain at 3 × 3 km2; only UK-domain results are provided here.
- Variables: surface concentrations and related meteorological variables (e.g., mixing height) on a polar stereographic grid; NetCDF outputs with specified variable names.

## Data products and structure
- Primary outputs are NetCDF files containing:
  - Surface concentrations for pollutants and particulate matter (e.g., PM2.5, PM10, O3, NH3, NOx, SO2, various organic and inorganic aerosols, black carbon, nitrate/nitrite species, sea salt, mineral dust, etc.).
  - Example variable naming includes SURF_ug_PM25_rh50 for fine PM and SURF_ppb_O3 for near-surface ozone; HMIX for mixing layer height; diverse SURF_ug_ and SURF_ppb_ variables for different species.
  - PM definitions:
    - PM2.5: aerodynamic diameter < 2.5 µm (with composition terms defined in the documentation).
    - PMcoarse: 2.5–10 µm fraction.
    - PM10: PM2.5 + PMcoarse.
- Data are documented with units in NetCDF attributes; guidance includes a proj4 string for the polar stereographic projection and notes on NetCDF compatibility with R, Python, and FORTRAN.

## Quality control and caveats
- QA/QC performed for 2002–2021; QA/QC reports are available on request.
- Content comes with no warranty; usage is at the user’s own risk and suitability is not guaranteed.
- Example data snippet (e.g., 2001 SURF_ug_PM25_rh50) is provided in the supporting docs but not fully displayed here.

## Usage, access, and interoperability
- Projection and geospatial specifics:
  - Polar stereographic grid with provided Proj4 string; users may need to configure this in their applications.
- Software compatibility:
  - NetCDF libraries compatible with R, Python, and FORTRAN are suitable for dataset access and analysis.
- Documentation and references:
  - Bibliography includes key papers detailing the EMEPMSC-W model, WRF integration, and related PM2.5 mitigation work, establishing context for model validation and interpretation.

## Practical implications for data leadership
- Comprehensive UK-focused, long-term atmospheric composition data: enables organisation-wide data strategy around environmental modelling, policy-support analytics, and cross-domain data integration.
- Demonstrates end-to-end data pipeline: from emissions and meteorology inputs (NAEI, CEIP, NCEP/NCAR GFS) to daily UK-specific concentration outputs, with explicit spatial resolution, data formats, and required processing tools.
- Emphasizes governance and discoverability needs:
  - Clear metadata in NetCDF and documented variable definitions facilitate discoverability and reuse.
  - QA/QC processes exist but require formal access requests for full reports, highlighting data governance considerations.
- Data stewardship considerations:
  - Emissions inputs for 2020–2021 rely on 2019 data; users should be aware of potential temporal inconsistencies when analyzing trends across edge years.
  - Availability of model methodology and references supports traceability and potential collaboration with the wider data community for system-wide improvements.