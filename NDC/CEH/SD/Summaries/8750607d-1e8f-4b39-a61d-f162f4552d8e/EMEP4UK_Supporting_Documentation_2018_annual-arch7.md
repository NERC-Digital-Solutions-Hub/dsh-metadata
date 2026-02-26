# European Monitoring and Evaluation Program Model for the UK (EMEP4UK) annual surface resistance based atmospheric deposition for 2018

## Overview
- Provides the annual total surface resistance based atmospheric deposition for the UK in 2018.
- Built with EMEP4UK rv4.36 atmospheric chemistry transport model (ACTM) and WRF model v4.2.2 for meteorology.
- Domain includes the EU at 27 × 27 km2 resolution with a nested UK domain at 3 × 3 km2; only UK domain results are included here.
- Temporal scope is annual totals; meteorology is driven by reanalysis data feeding into the model.

## Model design and data sources
- ACTM: EMEP4UK rv4.36 (derived from EMEP MSC-W rv4.36) with 3D meteorology from WRF v4.2.2.
- Meteorology: WRF includes data assimilation (Newtonian nudging) of NWP meteorological reanalysis from NCEP/NCAR GFS at 1° × 1° every 6 hours.
- Emissions: UK NOx, NH3, SO2, primary PM2.5, primary PMcoarse, CO, and non-methane VOCs from 2019 NAEI, rescaled to 2018; non-UK emissions from CEIP at 0.1° × 0.1° resolution.
- Output: annual total deposition data for the UK, including multiple species and deposition pathways.

## Spatial resolution and projection
- Spatial coverage: EU domain at 27 × 27 km2 with a nested UK domain at 3 × 3 km2; only UK results are provided.
- Projection: data on a polar stereographic grid; Proj4 string provided for GIS compatibility: +proj=stere +ellps=sphere +lat_0=90.0 +lon_0=0.0 +x_0=0.0 +y_0=0.0 +units=km +k_0=0.9330127018922193 +no_defs +type=crs.

## Data content, structure, and units
- File format: NetCDF.
- Key variables (examples):
  - Area_Grid_km2: grid area in km2.
  - DDEP_SOX_m2Grid: dry deposition of oxidised sulfur (area weighted) to the grid.
  - DDEP_SOX_m2Conif, DDEP_SOX_m2Seminat, DDEP_SOX_m2Water_D, DDEP_SOX_m2Decid, DDEP_SOX_m2Crops: dry deposition of oxidised sulfur to coniferous forest, semi-natural, water, deciduous forest, and crops, respectively.
  - DDEP_OXN_m2Grid, DDEP_OXN_m2Conif, DDEP_OXN_m2Seminat, DDEP_OXN_m2Water_D, DDEP_OXN_m2Decid, DDEP_OXN_m2Crops: dry deposition of oxidised nitrogen to corresponding land-use categories.
  - DDEP_RDN_m2Grid, DDEP_RDN_m2Conif, DDEP_RDN_m2Seminat, DDEP_RDN_m2Water_D, DDEP_RDN_m2Decid, DDEP_RDN_m2Crops: dry deposition of reduced nitrogen to corresponding land-use categories.
- Coverage and units: the dataset provides area-weighted (grid-wide) and land-use-specific dry deposition components in mgS/m2 or mgN/m2 as applicable, plus grid area in km2.

## Usage guidance for GIS and data users
- Data is designed for map-based visualization and spatial analysis in GIS environments.
- Requires a NetCDF library compatible with R, Python, or FORTRAN; ensure the polar stereographic projection is correctly defined in your GIS workflow using the provided proj4 string.
- Suitable for comparing spatial deposition patterns across land-use types and for integrating with other UK/EU atmospheric or environmental datasets.

## Quality assurance and caveats
- A QA/QC exercise was performed for 2018; detailed QA/QC reports are available on request and not included in this document.
- Content usage is at the user’s risk; no warranty that the data are error-free or fit for a particular purpose.

## Access notes and documentation
- Data compiled and run on the UKCEH POLAR computing cluster.
- Documentation and references provide context for model components, emissions data sources, and methodologies.

## Bibliography (selected references)
- Ge et al. 2021; J. Geosci. Model Dev.; evaluation of EMEP MSCW and WRF model outputs.
- Gu et al. 2021; Science; abating ammonia versus NOx for PM2.5 mitigation.
- Jalkanen et al. 2016; Atmos. Chem. Phys.; ship traffic emissions inventory.
- NCEP/NCAR FNL data; UCAR/NCAR Research Data Archive.
- Simpson et al. 2012; The EMEP MSC-W chemical transport model technical description.
- Skamarock et al. 2019; A Description of the Advanced Research WRF Model Version 4.
- Vieno et al. 2016a,b; Atmos. Chem. Phys. and Environmental Research Letters; UK PM2.5 sensitivities and notable pollution episodes.