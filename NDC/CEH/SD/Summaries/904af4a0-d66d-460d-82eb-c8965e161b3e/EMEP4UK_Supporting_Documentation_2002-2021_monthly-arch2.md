# European Monitoring and Evaluation Program Model for the UK (EMEP4UK) monthly atmospheric deposition of oxidised sulphur, oxidised nitrogen, and reduced nitrogen for 2002-2021

## Overview
- Provides monthly averaged atmospheric deposition of oxidised sulphur, oxidised nitrogen, and reduced nitrogen for the UK from 2002 to 2021.
- Produced with the EMEP4UK rv4.36 atmospheric chemistry transport model (ACTM) and the WRF model (v4.2.2) for meteorology.
- Aimed at monitoring environmental health and informing policy performance over time using standardized outputs.

## Data and Methods
- Model components:
  - EMEP4UK rv4.36 ACTM (derived from EMEP MSC-W rv4.36) simulating hourly to annual deposition and surface concentrations.
  - Meteorology from WRF v4.2.2 with data assimilation (Newtonian nudging) of NCEP/NCAR GFS reanalysis at 1°x1° every 6 hours.
- Domain and resolution:
  - EU domain at 27×27 km2, nested UK domain at 3×3 km2; only UK model results are included.
- Emissions inputs:
  - Anthropogenic NOx, NH3, SO2, primary PM2.5, primary PMcoarse, CO, and NMVOC from 2019 National Atmospheric Emission Inventory (NAEI); UK 2002–2019 emissions rescaled to yearly totals.
  - Non-UK emissions from CEIP at 0.1°×0.1°, with UK totals used for 2002–2019; 2020–2021 emissions use 2019 data.
- Computation and infrastructure:
  - Calculations run on the UKCEH POLAR cluster.
- Data products:
  - Monthly averaged deposition fields including dry and wet deposition for oxidised sulphur (SOx), oxidised nitrogen (OXN), and reduced nitrogen (RDN).

## Spatial and Temporal Coverage
- Time period: 2002–2021 (monthly data).
- Spatial focus: United Kingdom, derived from a European grid but limited to UK results.

## Variables and Units
- Surface concentration and deposition components include:
  - Dry deposition of oxidised sulphur (SO2) and oxidised nitrogen (OXN) per area (mg S/m2, mg N/m2).
  - Dry deposition of reduced nitrogen (RDN) per area (mg N/m2).
  - Wet deposition of oxidised sulphur (SOx), oxidised nitrogen (OXN), and reduced nitrogen (RDN) per area (mg S/m2 or mg N/m2 as indicated).
  - Rainfall (WDEP_PREC) in mm.
  - Grid area (Area_Grid_km2).
- Data files are stored in NetCDF with specified variable names (e.g., DDEP_SOX_m2Grid, WDEP_SOX, WDEP_OXN, WDEP_RDN).

## Data Structure and Access
- Data are projected on a polar stereographic grid; use the Proj4 description: +proj=stere +ellps=sphere +lat_0=90.0 +lon_0=0.0 +x_0=0.0 +y_0=0.0 +units=km +k_0=0.9330127018922193 +no_defs +type=crs.
- NetCDF library compatibility required (works with R, Python, Fortran).
- Example netCDF data structure snippet provided for 2002 output (DDEP_SOX_m2Grid):
  - DDEP_SOX_m2Grid:numberofrecords = 12 ;
  - DDEP_SOX_m2Grid:class = "Mosaic" ;
  - DDEP_SOX_m2Grid:current_date_first = 2002, 2, 1, 0 ;
  - DDEP_SOX_m2Grid:current_date_last = 2003, 1, 1, 0 ;
- Example section also includes an illustrative placeholder for code block, emphasizing the structure of monthly records.

## Quality Assurance and Limitations
- QA/QC performed for 2002–2021; QA/QC reports available on request (not included in the document).
- Content usage is at the user’s own risk; no warranty that outputs are error-free or fit for a particular purpose.
- 2020–2021 emissions use 2019 UK emissions data due to data availability.

## Usage Guidance
- Data are organized on a polar stereographic grid; ensure projection alignment in analyses.
- Requires NetCDF support; compatible with common data analysis environments (R, Python, Fortran).
- Suitable for standardized environmental health monitoring and policy performance assessment over time.
- Can be combined with other datasets to enrich environmental monitoring (considerations noted in related monitoring challenges).

## References and Bibliography
- Foundational model and methodology references for EMEP4UK and WRF, including:
  - Simpson et al. (2012) on EMEP MSC-W chemistry transport model.
  - Vieno et al. (2016a, 2016b) on UK PM2.5 mitigation sensitivities and 2014 PM episodes.
  - Skamarock et al. (2019) on WRF model description.
  - Ge et al. (2021) on evaluation of EMEP MSC-W and WRF model performance.
  - Gu et al. (2021) on ammonia vs NOx for PM2.5 mitigation.
  - Jalkanen et al. (2016) on ship emissions inventory.
  - NCEP/NCAR reanalysis data and related sources used for meteorology.