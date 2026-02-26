# European Monitoring and Evaluation Program Model for the UK (EMEP4UK) monthly atmospheric deposition of oxidised sulphur, oxidised nitrogen, and reduced nitrogen for 2002-2021

## Overview
- Provides monthly averaged atmospheric deposition data for the UK from 2002 to 2021.
- Generated using EMEP4UK rv4.36 atmospheric chemistry transport model (ACTM) and WRF model version 4.2.2.
- Includes surface concentrations and deposition metrics for oxidised sulphur, oxidised nitrogen, and reduced nitrogen.
- Data stored as NetCDF files with explicit variable names and units.

## Data Scope and Temporal Coverage
- Time period: 2002–2021 (monthly data).
- Spatial domain: EU-wide 27 × 27 km2 model grid with a nested 3 × 3 km2 UK domain; only UK-domain results are included.
- Variables cover rainfall, grid area, and depositions:
  - Dry deposition: oxidised sulphur (SOx), oxidised nitrogen (OXN), reduced nitrogen (RDN).
  - Wet deposition: oxidised sulphur (SOx), oxidised nitrogen (OXN), reduced nitrogen (RDN).
  - Rainfall and grid area metadata.

## Methodology, Data Production, and Provenance
- Modelling framework:
  - ACTM: EMEP4UK rv4.36 (derived from EMEP MSC-W rv4.36).
  - Meteorology: Weather Research and Forecasting Model (WRF) v4.2.2 with data assimilation from NCEP/NCAR GFS reanalysis (1° × 1°, every 6 hours).
- Emissions:
  - UK emissions (NOx, NH3, SO2, primary PM2.5, primary PMcoarse, CO, NMVOC) from 2019 National Atmospheric Emission Inventory (NAEI), rescaled to 2002–2019 yearly totals.
  - Non-UK emissions from CEIP 0.1° × 0.1° data; UK total used for 2002–2019.
  - For 2020–2021, emissions are based on 2019 data.
- Technical details:
  - Software stack compiled with Intel FORTRAN compiler (19.1.3.304) and run on the UKCEH POLAR cluster (CentOS 7).
  - Projections and grid information described for data usage and interoperability.

## Data Structure, Formats, and Variables
- Format: NetCDF files.
- Projection: Polar stereographic grid; proj4 description provided.
- Key variables and names:
  - DDEP_SOX_m2Grid (dry deposition of oxidised sulphur, area-weighted)
  - DDEP_OXN_m2Grid (dry deposition of oxidised nitrogen, area-weighted)
  - DDEP_RDN_m2Grid (dry deposition of reduced nitrogen, area-weighted)
  - WDEP_SOX (wet deposition of oxidised sulphur)
  - WDEP_OXN (wet deposition of oxidised nitrogen)
  - WDEP_RDN (wet deposition of reduced nitrogen)
  - WDEP_PREC (rainfall)
  - Area_Grid_km2 (grid area)
- Example metadata snippet (for DDEP_SOX_m2Grid):
  - numberofrecords = 12
  - class = "Mosaic"
  - current_date_first = 2002, 2, 1, 0
  - current_date_last = 2003, 1, 1, 0
- Data usage requirements:
  - NetCDF libraries required; compatible with R, Python, and FORTRAN.

## Quality Assurance and Limitations
- QA/QC performed for 2002–2021; QA/QC reports available on request (not included in the document).
- Usage is at the user’s own risk; no warranty or guarantee that content is error-free or fit for purpose.

## Access, Use, and Guidance
- Projection details and coordinate system guidance provided; users should apply the included proj4 string as needed.
- Data discovery and reuse supported via NetCDF format with explicit variable names and units.
- Documentation references and bibliography supplied for model descriptions and methodological context.

## Provenance, Reproducibility, and Documentation
- Full bibliographic references for model components and related methodological work (EMEP MSC-W, WRF, emission inventories, etc.).
- Clear lineage: EMEP4UK rv4.36 ACTM + WRF v4.2.2, 1° NCEP/NCAR GFS nudging, UK emissions from NAEI (2019) scaled, CEIP non-UK emissions, 2020–2021 using 2019 UK emissions.
- Computational environment and compiler details provided to support reproducibility.