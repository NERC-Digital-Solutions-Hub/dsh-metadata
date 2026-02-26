# European Monitoring and Evaluation Program Model for the UK (EMEP4UK) monthly atmospheric deposition of oxidised sulphur, oxidised nitrogen, and reduced nitrogen for 2002-2021

## Overview
- Monthly averaged atmospheric deposition and surface concentration data for the UK from 2002 to 2021.
- Generated with EMEP4UK rv4.36 (an atmospheric chemistry transport model) and WRF model v4.2.2.
- Outputs are gridded NetCDF fields for deposition components and related meteorology on a nested domain: EU domain at 27 × 27 km2 with a UK inner domain at 3 × 3 km2.
- Data are suitable for GIS-based mapping and spatial analysis, with a documented projection and variable definitions.
- QA/QC performed for 2002–2021; usage is at user’s risk; reports available on request.

## Experimental design and data sources
- Model framework: EMEP4UK rv4.36, derived from EMEP MSC-W rv4.36, coupled with WRF v4.2.2 for 3D meteorology.
- Domain and resolution: EU domain at 27 × 27 km2 with a nested UK domain at 3 × 3 km2; only UK-domain results are included.
- Meteorology: WRF data assimilation using Newtonian nudging from NCEP/NCAR GFS reanalysis (1° × 1° every 6 hours).
- Emissions: UK NOx, NH3, SO2, primary PM2.5, primary PMcoarse, CO, and non-methane VOCs from the 2019 NAEI; CEIP 0.1° × 0.1° emissions for non-UK countries; 2020–2021 emissions set to 2019 values.
- Outputs: Monthly-averaged fields from the EMEP4UK model.

## Data products and structure
- NetCDF data containing surface concentration and deposition components:
  - Dry deposition: DDEP_SOX_m2Grid (oxidised sulphur), DDEP_OXN_m2Grid (oxidised nitrogen), DDEP_RDN_m2Grid (reduced nitrogen); units are mgS/m2 or mgN/m2 respectively.
  - Wet deposition: WDEP_SOX, WDEP_OXN, WDEP_RDN (units mgS/m2 or mgN/m2); mapped to WDEP_SOX, WDEP_OXN, WDEP_RDN variables.
  - Rainfall: WDEP_PREC (mm).
  - Grid geometry: Area_Grid_km2 (grid area in km2).
- Example dataset structure item: DDEP_SOX_m2Grid with attributes such as numberofrecords, class (Mosaic), current_date_first, current_date_last.
- Projection and grid: Data projected on a polar stereographic grid; specific proj4 string provided for mapping in GIS applications.
- Time coverage: 2002-01 to 2021-12 (monthly observations).

## Spatial and temporal coverage
- Spatial:
  - European domain: 27 × 27 km2 grid.
  - UK domain: nested 3 × 3 km2 grid for detailed UK results.
- Temporal:
  - Monthly outputs from 2002 through 2021 (12 observations per year).

## Data formats and usage in GIS
- Format: NetCDF files; requires a NetCDF library compatible with R, Python, or Fortran for access and analysis.
- Projection: Polar stereographic projection with the provided proj4 string; users may reproject to their preferred CRS as needed.
- Model provenance: Based on EMEP4UK rv4.36 and WRF v4.2.2 meteorology.
- Handling notes: Data include multiple deposition pathways (wet and dry) for sulphur and nitrogen species; ensure correct interpretation of deposition components when mapping or summing to total deposition.

## Quality assurance, limitations, and usage notes
- QA/QC: Performed for 2002–2021; QA/QC reports available on request; not included in the document.
- Uncertainties: Content is provided “as is” with no warranty; model assumptions and emission inputs (notably 2020–2021 using 2019 emissions) may influence accuracy.
- Data usage caveat: The dataset is intended for analysis and mapping of atmospheric deposition but should be used considering potential uncertainties in emissions and modeling framework.

## Practical guidance for GIS specialists
- Map-ready deposition components: create layers for DDEP_SOX_m2Grid, DDEP_OXN_m2Grid, DDEP_RDN_m2Grid (dry), and WDEP_SOX, WDEP_OXN, WDEP_RDN (wet) to visualize spatial patterns of deposition by species.
- Combine layers to estimate total deposition if needed, paying attention to units (mg/m2) and summation rules for wet and dry components.
- Utilize the polar stereographic grid for regional UK mapping, and reproject to local CRS as required for integration with other GIS layers.
- Leverage rainfall (WDEP_PREC) as a metadata layer to contextualize wet deposition magnitudes where needed.
- Reference the provided proj4 string when configuring GIS software to ensure spatial alignment with other UK datasets.

## References
- Ge, Y., Heal, M. R., Stevenson, D. S., Wind, P., and Vieno, M. (2021). Evaluation of global EMEP MSCW (rv4.34) WRF (v3.9.1.1) model surface concentrations and wet deposition of reactive N and S with measurements. Geosci. Model Dev., 14, 7021-7046.
- Gu, B., et al. (2021). Abating ammonia is more cost-effective than nitrogen oxides for mitigating PM2.5 air pollution. Science, 374, 758-762.
- Jalkanen, J.P., et al. (2016). Inventory of ship traffic exhaust emissions in European sea areas, Atmos. Chem. Phys., 16, 71-84.
- NCEP FNL Operational Model Global Tropospheric Analyses (2000). UCAR/NCAR RDA.
- Simpson, D., et al. (2012). The EMEP MSC-W chemical transport model technical description. Atmos. Chem. Phys., 12, 7825-7865.
- Skamarock, W.C., et al. (2019). A Description of the Advanced Research WRF Model Version 4. UCAR/NCAR.
- Vieno, M., et al. (2016a,b). UK PM2.5 emission sensitivities and 2014 episode analyses. Atmos. Chem. Phys.; Environ. Res. Lett.