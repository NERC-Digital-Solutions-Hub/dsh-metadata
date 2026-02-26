# Supporting documentation for European Monitoring and Evaluation Program Model for the UK (EMEP4UK) daily atmospheric composition and fluxes for UK-SCAPE (2001 - 2015)

## Overview
- Provides daily averaged atmospheric composition and fluxes for the UK (2001–2015) focusing on main nitrogen, sulphur, particulate organic matter, and ozone.
- Generated with EMEP4UK rv4.17 ACTM, derived from EMEP MSC-W rv4.17; meteorology from WRF v3.7.1.
- Model domain: EU at 0.5°×0.5° with a nested UK domain at ~5×6 km (0.05°×0.055°); only UK-domain results included.
- Meteorology uses data assimilation (Newtonian nudging) of NCEP/NCAR GFS reanalysis at 1°×1° every 6 hours.
- Emissions and inputs are sourced and scaled to cover 2001–2015 (see Emissions section); daily averaged model outputs are provided in NetCDF format.

## Data content and variables
- Daily averaged outputs include:
  - Surface concentrations for pollutants (e.g., nitrogen, sulphur species, PM2.5, PMcoarse, ozone, VOCs, organics, etc.).
  - Deposition fluxes and related dry/wet deposition terms for multiple species (e.g., HNO3, NH3, NO2, NO3, PM components, SO2, SO4, etc.).
  - Meteorological and atmospheric state variables (e.g., mixing height, near-surface pollutants, temperatures, and related diagnostics).
- Particulate matter definitions:
  - PM2.5 (fine), PMcoarse (2.5–10 μm), PM10 (PM2.5 + PMcoarse).
  - Specific compositions and conversions defined for PM components.
- Units and NetCDF mapping are provided in the document (e.g., mgN/m² for deposition, mg/m² for deposition fluxes, ppbv for some gas concentrations, etc.).
- A comprehensive, but extensive, set of NetCDF variable names and their mappings is included (examples and definitions illustrated in the document).

## Experimental design and data sources
- EMEP4UK rv4.17 ACTM, derived from EMEP MSC-W rv4.17; 3D meteorology from WRF v3.7.1.
- UK anthropogenic emissions (NOx, NH3, SO2, PM2.5, PMcoarse, CO, NMVOC) based on 2015 NAEI estimates, rescaled to 2001–2015 annually.
- Non-UK emissions and UK total references:
  - CEIP EMEP emission estimates (0.5°×0.5°) for non-UK emissions; UK total used for 2001–2015.
  - NAEI UK emissions rescaled by year using UK totals (versions v2015 for 2001–2013, v2016 for 2014, v2017 for 2015).
- Shipping emissions (FMI, 2011) with adjustments:
  - NMVOC = 0.029 × NOx, PM2.5 = 0.95 × PM, PMcoarse = 0.05 × PM.
  - No annual rescaling applied to FMI shipping emissions.
- Daily averaged EMEP4UK outputs are included for UK-SCAPE (2001–2015).

## Data quality, QA/QC, and limitations
- QA/QC conducted for 2001–2015; QA/QC reports are available on request (not embedded in the document).
- Data use is at the user’s own risk; no warranty or guarantee of error-free data or fitness for a particular purpose.
- Certain complex emission rescalings and imports (e.g., FMI shipping adjustments) introduce methodological nuances that may affect comparability with other datasets.
- The document includes detailed notes on data structure and variable definitions to aid interoperability and discovery.

## Data formats, structure, and provenance
- Output format: NetCDF data files containing a wide range of atmospheric composition and flux variables.
- Model and computation details:
  - FORTRAN Intel compiler 2013_sp1.3.174 used for model compilation.
  - Computations executed on the CEH NEMSIS computing cluster.
- Data structure examples:
  - The document provides an example NetCDF variable mapping (e.g., WDEP_PM25ONS) to illustrate data organization.
- Documentation and references:
  - Bibliography includes key methodological sources (e.g., Simpson et al. 2012; Jalkanen et al. 2016; Skamarock 2019; Vieno et al. 2016a,b; etc.), establishing model lineage and validation context.

## Provenance and stewardship considerations
- Clear lineage from EMEPMSC-W and WRF models to UK-SCAPE daily outputs; explicit versioning (rv4.17, WRF v3.7.1) and emission-assembly versions/manipulations.
- Emission data provenance and rescaling approach documented (NAEI, CEIP, FMI shipping adjustments).
- Data governance aspects for Data Stewards:
  - Versioned inputs and model configurations enable reproducibility and auditability.
  - Extensive metadata support through variable definitions and units facilitates discoverability and reuse.
  - QA/QC status available on request supports assessment of data quality for governance and transparency.

## Practical implications for reuse and discovery
- Suitable for benchmarking UK atmospheric composition and deposition fluxes (2001–2015) within data catalogs and research workflows.
- Requires handling of large NetCDF files and understanding of NetCDF variable mappings for proper interpretation.
- Users should account for emission rescaling and shipping adjustment methodologies when integrating with other datasets or conducting trend analyses.
- Consider requesting QA/QC reports for detailed quality assessments and any dataset-specific caveats prior to reuse.