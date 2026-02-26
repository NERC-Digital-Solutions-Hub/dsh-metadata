# Supporting documentation for European Monitoring and Evaluation Program Model for the UK (EMEP4UK) daily atmospheric composition and fluxes for UK-SCAPE (1960 - 2020)

- This dataset provides daily averaged atmospheric composition for the UK (1960–2020) for main nitrogen, sulfur, particulate matter, and ozone species, generated using the EMEP4UK rv5.0 atmospheric chemistry transport model and the WRF model v4.4.2.
- Outputs are designed to support analyses of UK air quality and atmospheric chemistry trends over six decades.

## Data scope and main content

- Temporal coverage: 1960 to 2020; daily averaged values.
- Spatial scope: UK results nested within a EU domain (27 × 27 km2) with a higher-resolution UK nested domain (3 × 3 km2).
- Pollutants and variables include:
  - Fine and coarse particulate matter (PM2.5, PMcoarse; PM10 = PM2.5 + PMcoarse)
  - Surface concentrations and related components (e.g., PM2.5 components, dust, sea salt, mineral dust, secondary organic aerosols, nitrate, ammonium)
  - Gaseous species: ozone (O3), nitrogen oxides (NO, NO2, NOx), carbon monoxide (CO), ammonia (NH3), formaldehyde (HCHO), nitric acid (HNO3), various nitrogen/nitrogen oxide and sulfur species
  - Biogenic and organic matter indicators, elemental carbon, black carbon from biomass burning, and related PM fractions
  - Meteorological-like fields and deposition fluxes: mixing height (HMIX), wet/dry deposition terms, rainfall, and related fluxes
- Key NetCDF variable naming and units are described (e.g., SURF_ug_PM25_rh50 for PM2.5 under RH=50%, SURF_ppb_O3 for near-surface ozone in ppbv, etc.).

## Experimental design, domain, and data sources

- Model framework:
  - EMEP4UK rv5.0 (ACTM) derived from EMEP MSC-W rv5.0; meteorology from WRF v4.4.2.
  - 3D meteorology fed by ERA5 via data assimilation (Newtonian nudging) at 0.25° daily updates every 6 hours.
- Spatial setup:
  - European domain at 27 × 27 km2 resolution with a nested UK domain at 3 × 3 km2; only UK-domain results are provided here.
- Emissions sources:
  - UK anthropogenic emissions (NOx, NH3, SO2, primary PM2.5, primary PMcoarse, CO, NMVOCs) from NAEI (year-specific).
  - Non-UK emissions from CEIP at 0.1° × 0.1°; UK total used for the year 1960–2020.
- Output type:
  - Daily averaged atmospheric composition and fluxes for UK-SCAPE (1960–2020).

## Data format, structure, and projection

- Data format: NetCDF files; units and variable mappings are detailed in the documentation.
- Projection and grid:
  - Polar stereographic grid; described by the proj4 string: "+proj=stere +ellps=sphere +lat_0=90.0 +lon_0=0.0 +x_0=0.0 +y_0=0.0 +units=km +k_0=0.9330127018922193 +no_defs +type=crs".
- Required tooling:
  - NetCDF libraries compatible with R, Python, and FORTRAN (for reading and analysis).
- Example data note:
  - An example 1960 output is shown for SURF_ug_PM25_rh50 (PM2.5 with RH 50%).

## Data quality, provenance, and caveats

- Quality control:
  - QA/QC has been conducted for 1960–2020; QA/QC reports are available on request (not included in the document).
- Usage caveat:
  - Use of the dataset is at the user’s own risk; no warranty or guarantee of error-free content or fitness for a specific purpose.
- Documentation scope:
  - The document provides extensive mappings between NetCDF variables and physical pollutants, including numerous SURF_ variables for near-surface concentrations and related deposition and flux terms.

## Guidance for data users and potential data products

- How to use:
  - Leverage the detailed variable mapping and the polar stereographic projection to integrate with UK-specific datasets, trend analyses, or scenario assessments.
  - Combine with other data sources (e.g., ground-based monitors, emissions inventories) for validation or enrichment.
- Data product opportunities:
  - Create dashboards or reports showing long-term trends in PM and ozone, spatial distribution maps, and exposure assessments at 3 × 3 km UK resolution.
  - Develop reproducible analysis pipelines using the NetCDF outputs, with attention to the specified projection and unit conventions.
- Access and references:
  - Data is supported by a bibliography of model evaluations and methodological references (e.g., Simpson et al., Vieno et al., Skamarock et al., Ge et al., etc.).
  - For QA/QC reports and further methodological details, contact the data providers.