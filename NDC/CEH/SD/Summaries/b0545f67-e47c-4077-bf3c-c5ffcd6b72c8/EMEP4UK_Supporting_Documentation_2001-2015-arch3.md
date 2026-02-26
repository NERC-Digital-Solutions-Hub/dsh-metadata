# Supporting documentation for European Monitoring and Evaluation Program Model for the UK (EMEP4UK) daily atmospheric composition and fluxes for UK-SCAPE (2001 - 2015)

## Overview
- Provides daily averaged atmospheric composition and fluxes for the UK for 2001–2015, focusing on main nitrogen, sulphur, particulate organic matter, and ozone.
- Generated with EMEP4UK model rv4.17 coupled to the WRF meteorology model (v3.7.1), using high-level emissions inputs and data assimilation.
- UK-focused domain at 0.5° × 0.5° resolution with a nested UK domain at approximately 5 × 6 km2 (0.05° × 0.055°).
- Daily averaged outputs are included for various atmospheric species, deposition processes, and related metrics.

## Experimental design and data sources
- Modeling framework: Atmospheric chemistry transport model (ACTM) based on EMEP MSC-W rv4.17, combined with WRF meteorology and data assimilation (Newtonian nudging) using NCEP/NCAR reanalysis inputs at 1° × 1° every 6 hours.
- Emissions inputs:
  - UK anthropogenic emissions (NOx, NH3, SO2, primary PM2.5, primary PMcoarse, CO, NMVOC) from the 2015 National Atmospheric Emission Inventory (NAEI), rescaled to 2001–2015 years.
  - Non-UK emissions from CEIP (EMEP emissions estimates, 0.5° × 0.5° resolution) used for all non-UK contributions; UK total used for 2001–2015 scaling.
  - Shipping emissions from FMI (2011) with post hoc rescaling to NMVOC and PM components based on EMEP estimates.
- Model compilation and execution: Fortran compiler (Intel 2013) on the CEH NEMSIS cluster; computations run on the CEH computing environment.
  
## Data products and structure
- Outputs include daily averaged fields for:
  - Atmospheric composition: NOx, NH3, NO3, NO2, O3, NMVOC, CO, SO2, PM2.5, PMcoarse, PM10, various inorganic and organic aerosol components, and related tracers.
  - Deposition fluxes: Dry and wet deposition fluxes to multiple land cover types (coniferous forest, crops, deciduous forest, desert, semi-natural, water, grid-weighted, etc.) for species such as nitrate, ammonium, nitric acid, nitrite, ammonia, nitrogen deposition components, sulphur species, elemental carbon, organic matter, PM components, and oxidised/reduced nitrogen.
  - Surface and near-surface metrics: Near-surface concentrations of gases and particulates, mixing layer height, mean daily maximum ozone, and related surface/atmospheric variables.
  - Specific deposition and gas/particle fields are defined with detailed NetCDF variable names (e.g., DDEP_HNO3_m2Conif, SURF_MAXO3, WDEP_NO3_F, etc.).
- Data format and accessibility: Outputs are provided as NetCDF files; an example of a NetCDF data structure is indicated in the documentation.

## Quality control and documentation
- QA/QC has been performed for 2001–2015; QA/QC reports exist upon request but are not included in the core document.
- Documentation notes that use of the dataset is at the user’s risk; no warranty or guarantee of error-free content or fitness for purpose is provided.
- A short example of the NetCDF data structure is included, illustrating how data might be accessed or interpreted.

## Practical considerations for monitoring frameworks
- Data provenance and integration:
  - Combines UK-sited emissions data (NAEI) with regional/global emissions (CEIP) and FMI-shipping emissions, enabling evaluation of both local and international emission contributions.
  - Daily averages provide policy-relevant temporal resolution for monitoring trends and evaluating emission-control scenarios.
- Metadata and interoperability:
  - The dataset relies on NetCDF with numerous derived variables and custom naming conventions; users will require detailed metadata (variable definitions, units, spatial/temporal references) to ensure correct interpretation and integration into monitoring dashboards or frameworks.
- Data accessibility and governance:
  - Although QA/QC is documented, full QA/QC details and perhaps some metadata are available on request, implying potential access barriers for some users.
  - The documentation emphasizes that the data are provided without warranty, and users should validate suitability for specific monitoring objectives.
- Applicability to policy evaluation:
  - Enables assessment of UK atmospheric composition, deposition fluxes, and ozone-related metrics over 2001–2015, supporting retrospective policy analysis and informing future strategies on air quality and deposition-related environmental health aspects.

## References
- Jalkanen, J.P., Johansson, L., and Kukkonen, J. (2016). A comprehensive inventory of ship traffic exhaust emissions in European seas (Atmos. Chem. Phys.).
- National Centers for Environmental Prediction (NCEP) reanalysis references.
- Simpson et al. (2012); Vieno et al. (2016a, 2016b) – EMEP MSC-W model technical descriptions and UK PM2.5 episode studies.
- Skamarock et al. (2019) – WRF Model Description.
- Vieno et al. (2016a, 2016b) – UK PM2.5 mitigation sensitivities and related case studies.