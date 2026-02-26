# High resolution European Monitoring and Evaluation Program Model for the UK (EMEP4UK) annual surface resistance based atmospheric deposition for 2018

## Overview
- Provides the annual total surface resistance based atmospheric deposition for the UK for 2018.
- Generated with EMEP4UK model rv4.36 and WRF model v4.1.1.
- Domain combines a 27×27 km2 EU domain with a nested UK domain at 1×1 km2; only UK results are included.
- Atmosphere chemistry transport modeling to simulate deposition of pollutants (N and S species) on an area-weighted basis.

## Model components and inputs
- Atmospheric chemistry transport model: EMEP4UK rv4.36 (derived from EMEP MSC-W rv4.36).
- Meteorology: WRF v4.1.1 with data assimilation of NCEP/NCAR GFS reanalysis every 6 hours at 1°×1° resolution.
- Emissions: UK NOx, NH3, SO2, primary PM2.5, PMcoarse, CO, NMVOCs from 2019 NAEI, rescaled to 2018; non-UK emissions from CEIP 0.1°×0.1° data using UK total for 2018.
- Model compiler and computing: FORTRAN Intel compiler 19.1.3.304; run on UKCEH POLAR cluster.

## Experimental design and data production
- Purpose: produce annual surface deposition data (dry deposition for oxidised/reduced N and S) and related metrics.
- Grid and variables: results provided on a 1×1 km UK grid; multiple deposition components (e.g., DDEP_SOX_m2Grid, DDEP_OXN_m2Grid, DDEP_RDN_m2Grid, and equivalents for other land covers such as coniferous forest, semi-natural, water, deciduous forest, crops).
- NetCDF data: annual totals stored in NetCDF with specific variable names and units; example structure includes time, i (x-coordinate), j (y-coordinate), lon, lat, and deposition variables.
- Projection: data on a polar stereographic grid; proj4 string provided for proper reprojection.

## Data structure and units
- NetCDF variables are labeled with clear names (e.g., Area_Grid_km2, DDEP_SOX_m2Grid, DDEP_OXN_m2Conif, etc.).
- Units: area in km2; dry deposition values in mgS/m2 or mgN/m2 depending on species and target (e.g., coniferous forest, water, deciduous forest, crops).
- Example snippet shown for 2018 output (DDEP_SOX_m2Grid) illustrating dimensions (time, i, j) and spatial coordinates (lon, lat).

## Quality assurance and limitations
- QA/QC conducted for 2018; details available on request (not fully included in the document).
- Processes include: comparing country totals against EMEP inventories; visual and statistical evaluation of model outputs versus observations.
- WRF and EMEP4UK are peer-reviewed and widely used.
- User guidance includes a standard disclaimer: results come with no warranty and are used at the user’s own risk.

## Guidance for use
- Data are described on a polar stereographic grid; users should apply the provided proj4 string for proper projection in their tools.
- NetCDF compatibility: data can be read with common libraries in R, Python, FORTRAN, etc.
- Documentation and references provide context for model evaluation and supporting sources.

## Outputs and interpretation
- Production of annual deposition totals for key sulfur and nitrogen species and their deposition to different land-cover types.
- Outputs suitable for reporting environmental health and policy performance over time, consistent with standard monitoring practices.
- Encourages integration with other datasets to increase value and support broader data accessibility.

## References and related work
- Key methodological and evaluative references for EMEP4UK, WRF, and emissions data (e.g., Simpson et al. 2012; Vieno et al. 2016a,b; Skamarock et al. 2019; Ge et al. 2021; Gu et al. 2021; NAEI 2022).