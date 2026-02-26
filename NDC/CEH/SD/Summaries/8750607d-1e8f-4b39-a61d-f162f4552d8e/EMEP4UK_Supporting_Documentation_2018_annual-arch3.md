# European Monitoring and Evaluation Program Model for the UK (EMEP4UK) annual surface resistance based atmospheric deposition for 2018

## Purpose and scope
- Provides the 2018 annual total of surface resistance based atmospheric deposition for the UK.
- Generated using EMEP4UK model rv4.36 and the Weather Research and Forecasting (WRF) model v4.2.2.
- Aims to support environmental monitoring of atmospheric deposition and inform policy and decision-making.

## Experimental design and domain
- Uses the EMEP MSC-W chemical transport model rv4.36 (ACTM) for hourly to annual deposition/atmospheric composition.
- 3D meteorology from WRF v4.2.2 with data assimilation (Newtonian nudging) of NCEP/NCAR GFS reanalysis at 1°×1° every 6 hours.
- Spatial domain covers the EU at 27×27 km, with a nested UK domain at 3×3 km; only UK-domain results are reported.
- Includes UK emissions (NOx, NH3, SO2, primary PM2.5, PMcoarse, CO, NMVOCs) from the 2019 NAEI, rescaled to 2018; non-UK emissions from CEIP at 0.1°×0.1° resolution.

## Data sources and emissions
- UK anthropogenic emissions: NAEI 2019 estimates scaled to 2018 total for UK contributions.
- Non-UK emissions: CEIP data used for all non-UK emissions.
- All emissions drive the deposition and concentration fields within the model framework.

## Model and computation
- Model compilers: WRF and EMEP4UK compiled with the Intel FORTRAN compiler (version 19.1.3.304).
- Computations performed on the UKCEH POLAR computing cluster (CentOS Linux 7).

## Output, units, and recorded values
- Data are provided as NetCDF files with grid-based variables.
- Grid area: km^2 (Area_Grid_km2).
- Dry deposition components include oxidised and reduced nitrogen and oxidised sulphur, with area-weighted and land-use specific deposition (e.g., coniferous forest, deciduous forest, semi-natural, water, crops).
- Examples of NetCDF variable names include DDEP_SOX_m2Grid (dry deposition of oxidised sulfur, area-weighted) and DDEP_OXN_m2Conif (dry deposition of oxidised nitrogen to coniferous forest), among others for various species and land categories.
- Units are specified within the NetCDF files (e.g., mgS/m2 or mgN/m2) and described for each depositional pathway.

## Quality assurance and governance
- A QA/QC exercise was conducted for the year 2018; QA/QC reports are available on request but not included in the document.
- The document contains a disclaimer: use of the dataset is at the user’s risk; no warranty of error-free content is provided.
- Data provenance includes model versions and input inventories; governance processes for sharing underlying data are not detailed beyond the QA/QC note and data sharing constraints.

## Data structure and usage guidance
- Data are projected on a polar stereographic grid; a proj4 string is provided to describe the coordinate reference system.
- Users may need to specify this projection in their applications.
- NetCDF libraries compatible with R, Python, and FORTRAN are suitable for accessing the data.
- An illustrative example of the 2018 output for DDEP_SOX_m2Grid is provided in the documentation (formatting shown in the document).

## Relevance to monitoring frameworks
- Demonstrates end-to-end monitoring data production: from emissions inventories and meteorology assimilation to an atmospheric deposition output suitable for policy analysis.
- Emphasizes traceability of data provenance (model versions, emissions sources, meteorology data) and the importance of QA/QC.
- Highlights data governance considerations, including openness of QA/QC reports and the requirement to acknowledge the risk of use without complete in-document QA details.

## References and context
- Key technical references for the EMEP MSC-W model rv4.36 and its integration with WRF, emission inventories, and related methodologies are cited (e.g., Simpson et al. 2012; Vieno et al. 2016; Skamarock et al. 2019; Ge et al. 2021; various reviews on emissions and PM2.5 mitigation).