# European Monitoring and Evaluation Program Model for the UK (EMEP4UK) annual surface resistance based atmospheric deposition for 2018

## Overview
- Provides the annual total surface-resistance based atmospheric deposition for the UK for 2018.
- Built from EMEP4UK model rv4.36 (an atmospheric chemistry transport model) with WRF v4.2.2 for meteorology; EU domain at 27×27 km2 with a nested UK domain at 3×3 km2 (only UK results included).
- meteorology assimilates NCEP/NCAR GFS reanalysis data every 6 hours.
- UK emissions inputs derived from the 2019 National Atmospheric Emission Inventory (NAEI), rescaled to 2018; non-UK emissions supplied by CEIP (0.1° resolution).
- Outputs include annual total deposition and multiple related deposition variables in NetCDF format.

## Data production and experimental design
- Modeling chain: EMEP4UK rv4.36 coupled with WRF v4.2.2; both compiled with Intel FORTRAN and run on the UKCEH POLAR cluster.
- Domain and resolution: EU domain 27×27 km2; UK nest 3×3 km2; only UK results reported.
- Emissions inputs:
  - UK: NOx, NH3, SO2, primary PM2.5, primary PMcoarse, CO, non-methane VOC from NAEI 2019, rescaled to 2018 UK totals.
  - Non-UK: CEIP emissions (0.1°×0.1°) and UK total used for 2018.
- Outputs captured include annual totals and various deposition components by species and land-cover categories.

## Data content and structure
- File format: NetCDF with explicit units described in metadata.
- Recorded species/components include:
  - Dry deposition of oxidised sulphur and nitrogen (area-weighted and land-cover specific such as coniferous forest, semi-natural, water, deciduous forest, crops).
  - Dry deposition of reduced nitrogen (area-weighted and land-cover specific).
  - Grid area (km2) and multiple DDEP and related deposition variables (with NetCDF variable names like DDEP_SOX_m2Grid, DDEP_OXN_m2Grid, DDEP_RDN_m2Grid, etc.).
- Grid and projection: data projected on a polar stereographic grid; proj4 description provided for compatibility with GIS/analysis tools.

## Data quality, governance, and access
- Quality Control: QA/QC performed for 2018; QA/QC reports available on request (not included in this document).
- Legal/usage note: dataset use is at the user’s risk; no warranty or guarantee stated regarding errors or fitness for purpose.
- Documentation and metadata: NetCDF metadata includes units and variable mappings; an example for a variable (e.g., DDEP_SOX_m2Grid) is provided, illustrating structure.
- Accessibility: Requires a NetCDF library compatible with R, Python, and FORTRAN; guidance is provided for data usage and integration.

## Usage considerations and limitations
- Temporal scope: 2018 only.
- Emissions uncertainty: UK emissions are rescaled from 2019 NAEI estimates to 2018, which may introduce uncertainties.
- Interoperability: Data described on a polar stereographic grid; users may need to regrid or adapt to their analysis framework.
- Documentation: QA/QC reports available on request; full methodological details are supported by cited literature.

## References
- Ge, Y., Heal, M. R., Stevenson, D. S., Wind, P., and Vieno, M. (2021). Evaluation of global EMEP MSC-W (rv4.34) WRF (v3.9.1.1) model surface concentrations and wet deposition of reactive N and S with measurements. Geosci. Model Dev., 14, 7021-7046.
- Gu, B. et al. (2021). Abating ammonia is more cost-effective than nitrogen oxides for mitigating PM2.5 air pollution. Science, 374, 758-762.
- Jalkanen, J.P. et al. (2016). Inventory of ship traffic exhaust emissions in European seas. Atmos. Chem. Phys., 16, 71-84.
- NCEP FNL Operational Model Global Tropospheric Analyses (2000). UCAR/NCAR RDA.
- Simpson, D. et al. (2012). The EMEP MSC-W chemical transport model technical description. Atmos. Chem. Phys., 12, 7825-7865.
- Skamarock, W.C. et al. (2019). A Description of the Advanced Research WRF Model Version 4. UCAR/NCAR.
- Vieno, M. et al. (2016a). The sensitivities of emissions reductions for UK PM2.5 mitigation. Atmos. Chem. Phys., 16, 265-276.
- Vieno, M. et al. (2016b). The UK PM2.5 episode of March-April 2014. Environ. Res. Lett., 11, 044004.