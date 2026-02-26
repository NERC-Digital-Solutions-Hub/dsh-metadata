# European Monitoring and Evaluation Program Model for the UK (EMEP4UK) monthly atmospheric deposition of oxidised sulphur, oxidised nitrogen, and reduced nitrogen for 2002-2021

## Overview
- Monthly averaged atmospheric deposition data for the UK, covering oxidised sulphur (SOx), oxidised nitrogen (NOx), and reduced nitrogen (RDN) from 2002 to 2021.
- Produced with the EMEP4UK rv4.36 chemical transport model and the WRF model v4.2.2.
- Data are suitable for supporting UK air quality and deposition studies and model evaluation.

## Experimental design and data creation
- Model framework: EMEP4UK rv4.36 atmospheric chemistry transport model (ACTM), derived from EMEP MSC-W rv4.36.
- Meteorology: 3D meteorology from the Weather Research and Forecasting Model (WRF) v4.2.2 with Newtonian nudging of NWP reanalysis from NCEP/NCAR GFS (1°x1°) every 6 hours.
- Domain and resolution: EU domain at 27 × 27 km^2, nested UK domain at 3 × 3 km^2; results extracted for the UK domain.
- Emissions: UK NOx, NH3, SO2, primary PM2.5, PMcoarse, CO, and NMVOC emissions from 2019 NAEI; UK total scaled to each year 2002–2019. Non-UK emissions from CEIP at 0.1° × 0.1°; for 2020–2021, emissions are taken from 2019 data.
- Output: Monthly averaged deposition fields included in the dataset.
- Technical setup: Compiled with the Intel Fortran compiler (19.1.3.304); computations run on the UKCEH POLAR cluster.

## Data structure and content
- File format: NetCDF with multiple deposition and related fields.
- Key variables and units (examples):
  - Rainfall: WDEP_PREC (mm)
  - Grid area: Area_Grid_km2 (km^2)
  - Dry deposition, oxidised sulphur: DDEP_SOX_m2Grid (mgS/m2)
  - Dry deposition, oxidised nitrogen: DDEP_OXN_m2Grid (mgN/m2)
  - Dry deposition, reduced nitrogen: DDEP_RDN_m2Grid (mgN/m2)
  - Wet deposition, oxidised sulphur: WDEP_SOX (mgS/m2)
  - Wet deposition, oxidised nitrogen: WDEP_OXN (mgN/m2)
  - Wet deposition, reduced nitrogen: WDEP_RDN (mgN/m2)
- Example structure snippet (notional):
  - DDEP_SOX_m2Grid contains 12 monthly records per year
  - DDEP_SOX_m2Grid uses a Mosaic class, with time bounds 2002-02-01 to 2003-01-01
- Projection and grid: Data projected on a polar stereographic grid; Proj4 string provided for integration into analysis tools.

## Quality, provenance, and caveats
- Quality assurance: QA/QC performed for 2002–2021; QA/QC reports available on request (not included in the document).
- Usage note: Content use is at the user’s risk; no warranty or guarantee of correctness or fitness for purpose.
- Metadata and provenance: Model versions, emission inventories, and data sources clearly documented; 2020–2021 rely on 2019 emissions data.

## Access, usage, and guidance
- Projection details: Proj4 string provided for correct spatial handling. Requires a NetCDF-compatible library (R, Python, FORTRAN, etc.).
- Data discovery and reuse: Dataset is described with model versions, domain, emissions sources, and temporal coverage (2002–2021) to support traceability and reproducibility.
- Recommendations for users: Align interpretation with stated model frameworks and emission data sources; consult QA/QC reports for confidence assessment.

## Version history / data lineage
- Core model: EMEP4UK rv4.36 (ACTM) building on EMEP MSC-W rv4.36 framework.
- Meteorology: WRF v4.2.2 with NCEP/NCAR GFS reanalysis nudging.
- Emissions: UK 2019 NAEI data (rescaled 2002–2019); CEIP non-UK emissions; 2020–2021 emissions based on 2019 data.
- Data product: Monthly atmospheric deposition fields for 2002–2021.

## References
- Ge et al. (2021) Evaluation of EMEP MSC-W and WRF models with measurements.
- Gu et al. (2021) Costs of ammonia vs. NOx abatement for PM2.5 mitigation.
- Jalkanen et al. (2016) Ship traffic emissions inventory.
- NCEP FNL Operational Model (2000) and UCAR/NCAR data archive.
- Simpson et al. (2012) EMEP MSC-W model description.
- Skamarock et al. (2019) WRF model description.
- Vieno et al. (2016a, 2016b) UK PM2.5 emission sensitivities and 2014 PM episode analysis.