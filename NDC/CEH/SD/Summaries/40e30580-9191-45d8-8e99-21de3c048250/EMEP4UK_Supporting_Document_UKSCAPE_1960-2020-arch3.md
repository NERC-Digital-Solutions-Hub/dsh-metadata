# Supporting documentation for European Monitoring and Evaluation Program Model for the UK (EMEP4UK) daily atmospheric composition and fluxes for UK-SCAPE (1960 - 2020)

## Overview
- Daily averaged atmospheric composition for the UK, 1960–2020, covering major nitrogen, sulphur, particulate matter, and ozone species.
- Generated with EMEP4UK model rv5.0 (an atmospheric chemistry transport model, ACTM) and the WRF model v4.4.2 for meteorology.
- UK domain results extracted from a EU-scale 27 × 27 km2 grid with a nested UK domain at 3 × 3 km2.
- Meteorology includes data assimilation (Newtonian nudging) of ERA5 reanalysis data (0.25° × 0.25°, every 6 hours).

## Modelling framework and data inputs
- Emissions:
  - UK: NOx, NH3, SO2, primary PM2.5, primary coarse PM, CO, non-methane VOCs from the National Atmospheric Emission Inventory (NAEI).
  - Non-UK emissions: 0.1° × 0.1° data from CEIP; UK totals used for year 1960–2020.
- Model components:
  - ACTM derived from EMEP MSC-W rv5.0; UK results produced from this framework.
  - WRF meteorology with ERA5 nudging.
- Computing environment:
  - FORTRAN Intel compiler; calculations performed on the UKCEH POLAR cluster.

## Nature and units of recorded values
- PM definitions:
  - PM2.5: aerodynamic diameter < 2.5 μm (various constituent definitions provided, including sulfate, nitrate, ammonium, sea salt, mineral dust, secondary organics, and water).
  - PMcoarse: aerodynamic diameter 2.5–10 μm.
  - PM10: PM2.5 + PMcoarse.
- Surface concentration variables are stored in NetCDF files; units and NetCDF variable names are documented (e.g., SURF_ug_PM25_rh50, HMIX, SURF_MAXO3, etc.).
- A wide set of near-surface gas and particle species are included (e.g., NOx, NO, NO2, CO, HNO3, NH3, O3, SO2, dust components, elemental carbon, organic matter, PM fractions, wet/dry deposition fluxes, and related hydrometeorographic variables).

## Data structure and conversion guidance
- Projection: data are projected on a polar stereographic grid.
- Proj4 description: '+proj=stere +ellps=sphere +lat_0=90.0 +lon_0=0.0 +x_0=0.0 +y_0=0.0 +units=km +k_0=0.9330127018922193 +no_defs +type=crs'.
- Compatibility: NetCDF libraries required; data usable with R, Python, and FORTRAN.

## Data products and outputs
- Daily averaged atmospheric composition and fluxes, including:
  - Surface concentrations for a broad suite of species (gas-phase and PM-related).
  - Deposition fluxes (wet and dry deposition) for various species.
  - Meteorological and derived quantities such as mixing height.
- Representative variable naming examples (NetCDF variable names) illustrate the data structure and content.

## Quality control and limitations
- QA/QC completed for the 1960–2020 period; reports available on request.
- The dataset comes with no warranty; use of the content is at the user’s risk.
- Some metadata and supporting documentation are extensive; the provided document notes that QA/QC reports are not included directly.

## Guidance for use and caveats
- The dataset is designed for evaluating environmental health policies and informing decision-making.
- Users should consider the stated assumptions, data sources, and potential uncertainties in emissions, meteorology assimilation, and model chemistry when interpreting results.
- Clear communication of complex model outputs is encouraged, consistent with the aims of monitoring frameworks.

## Bibliography / references
- Ge et al. (2021), Geosci. Model Dev.
- Gu et al. (2021), Science
- Jalkanen et al. (2016), Atmos. Chem. Phys.
- National Centers for Environmental Prediction/NWS/NOAA (2000)
- Simpson et al. (2012), Atmos. Chem. Phys.
- Skamarock et al. (2019), AR WRF Model
- Vieno et al. (2016a, 2016b), Atmos. Chem. Phys. / Environ. Res. Lett.