# High resolution European Monitoring and Evaluation Program Model for the UK (EMEP4UK) annual surface resistance based atmospheric deposition for 2018

## Overview
- Provides the annual total surface resistance based atmospheric deposition for the UK for 2018.
- Generated with EMEP4UK model rv4.36 and WRF model v4.1.1; domain covers EU at 27×27 km2 with a nested UK domain at 1×1 km2.
- Outputs focus on UK model results; data delivered as annual totals.

## Experimental design / Domain and inputs
- Model: EMEP4UK rv4.36 (an atmospheric chemistry transport model derived from EMEP MSC-W rv4.36).
- Meteorology: Weather Research and Forecasting (WRF) v4.1.1 with data assimilation of NCEP/NCAR GFS reanalysis every 6 hours.
- Domain resolution: EU 27×27 km2 with UK nest 1×1 km2.
- Emissions inputs:
  - UK: NOx, NH3, SO2, primary PM2.5, primary PMcoarse, CO, non-methane VOCs from the 2019 National Atmospheric Emission Inventory (NAEI 2022), rescaled to 2018.
  - Non-UK: emissions from CEIP 0.1° resolution; UK total used for 2018.
- Outputs: annual total atmospheric deposition data for 2018.

## Modelling environment
- Compiled with Intel FORTRAN compiler (version 19.1.3.304, 20200925).
- Calculations run on the UKCEH POLAR compute cluster (CentOS Linux 7.9).

## Nature and units of recorded values
- Data stored in NetCDF with units described in the files.
- Key variables include:
  - Area_Grid_km2: grid area (km2).
  - DDEP_SOX_m2Grid: dry deposition of oxidised sulphur (area weighted).
  - DDEP_SOX_m2Conif / DDEP_SOX_m2Seminat / DDEP_SOX_m2Water_D / DDEP_SOX_m2Decid / DDEP_SOX_m2Crops: dry deposition of oxidised sulphur by land cover types.
  - DDEP_OXN_m2Grid / DDEP_OXN_m2Conif / DDEP_OXN_m2Seminat / DDEP_OXN_m2Water_D / DDEP_OXN_m2Decid / DDEP_OXN_m2Crops: dry deposition of oxidised nitrogen by land cover types.
  - DDEP_RDN_m2Grid / DDEP_RDN_m2Conif / DDEP_RDN_m2Seminat / DDEP_RDN_m2Water_D / DDEP_RDN_m2Decid / DDEP_RDN_m2Crops: dry deposition of reduced nitrogen by land cover types.
- Example structure includes time, i, j dimensions and corresponding longitude/latitude coordinates.

## Guidance for using the data
- Projection: polar stereographic grid with proj4 string provided for compatibility.
- Data access: requires a NetCDF library compatible with R, Python, or Fortran.

## Quality control
- Simple QA/QC performed for 2018; reports available on request.
- Both WRF and EMEP4UK are peer-reviewed models with extensive scientific use.
- QA/QC includes input data checks against official inventories and model output checks (visual time-series and statistical evaluations).
- Usage disclaimer: content provided at user’s risk; no warranty of fitness for purpose.

## Details of the netCDF data structure
- Example NetCDF variable naming includes time, i, j, lon, with detailed metadata preserved (descriptions of units and grid coordinates).

## Data access, limitations, and dissemination
- QA/QC reports available on request; full dataset description is provided here.
- The dataset is intended to support environmental monitoring and evaluation; users should review model assumptions and uncertainties.

## Bibliography / related literature
- Simpson et al. (2012); Vieno et al. (2016a, 2016b); Jalkanen et al. (2016); Skamarock et al. (2019); Ge et al. (2021); Gu et al. (2021); NAEI (2022); additional model and evaluation references.

## Relevance to monitoring framework authors
- Demonstrates end-to-end monitoring workflow:
  - Clear linkage between policy-relevant emissions data and atmospheric transport modeling.
  - Documentation of domain setup, data sources, and data processing pipelines.
  - Transparent data formats (NetCDF) and metadata standards to enable reuse and verification.
  - Use of QA/QC processes and peer-reviewed models to ensure credibility.
  - Guidance for data integration into monitoring dashboards, reports, or policy assessments.
- Practical challenges illustrated:
  - Dependence on multiple data streams (UK emissions, non-UK emissions) with rescaling and harmonization needs.
  - Metadata clarity and data governance considerations for complex, multi-source datasets.
  - Necessity for accessible documentation and potential barriers to data sharing (QA/QC reports available on request).