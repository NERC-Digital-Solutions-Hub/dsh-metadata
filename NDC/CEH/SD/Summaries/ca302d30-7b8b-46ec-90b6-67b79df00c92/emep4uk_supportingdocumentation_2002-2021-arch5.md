# Supporting documentation for European Monitoring and Evaluation Program Model for the UK (EMEP4UK) daily atmospheric composition and fluxes for UK-SCAPE (2002 - 2021)

## Overview
- Dataset provides daily averaged atmospheric composition for the UK (2002–2021) for major nitrogen, sulphur, particulate organic matter, and ozone species.
- Based on EMEP4UK rv4.36 (ACTM) with meteorology from WRF v4.2.2; UK domain nested within EU domain (27 × 27 km2; 3 × 3 km2 for the UK).
- Daily model outputs are included; emissions and meteorology are sourced and processed to produce UK-focused results.

## Experimental design, data sources, and processing
- Model framework:
  - EMEP4UK rv4.36 atmospheric chemistry transport model (derived from EMEP MSC-W rv4.36).
  - Weather calculations via WRF v4.2.2 with data assimilation (Newtonian nudging) of NCEP/NCAR GFS reanalysis meteorology (1° × 1°, every 6 hours).
- Domain and resolution:
  - EU domain at 27 × 27 km2 with UK nested domain at 3 × 3 km2; results reported for the UK domain.
- Emissions:
  - UK emissions (NOx, NH3, SO2, primary PM2.5, primary PMcoarse, CO, NMVOCs) from 2019 National Atmospheric Emission Inventory (NAEI), rescaled to each year 2002–2019.
  - Non-UK emissions from CEIP 0.1° × 0.1° grid; UK total used for 2002–2019; 2020–2021 emissions based on 2019 data.
- Computation:
  - Model compiled with Intel FORTRAN compiler; calculations run on the UKCEH POLAR compute cluster.
- Documentation and QA:
  - QA/QC performed for 2002–2021; QA/QC reports available on request (not included in this document). Content is provided “as-is” and users assume risk.

## Data products and variable definitions
- Temporal coverage: daily averaged data for 2002–2021.
- Variables (examples of surface concentrations and related metrics):
  - PM2.5 (SURF_ug_PM25_rh50) and PMcoarse (SURF_ug_PMCOARSE or equivalent in dataset).
  - PM10 defined as PM2.5 + PMcoarse.
  - Gaseous species: ozone near surface (SURF_ppb_O3; units ppbv), various nitrogen and sulfur species, ammonia (SURF_ug_NH3), nitric/nitrous acids (SURF_ug_HNO3, SURF_ug_HONO), etc.
  - Particulate constituents: black carbon, organic matter, elemental carbon, sea salt, mineral dust, secondary organic aerosols (SOA), primary PM fractions, etc. Variables are named with SURF_ug_* or SURF_ppb_* conventions as listed in the documentation.
  - Other outcomes: mixing layer height (HMIX, units m).
- Units: specified per variable in NetCDF files (e.g., µg m-3 for particulates; ppbv for ozone; m for mixing height).
- Geography and projection:
  - Data on a polar stereographic grid; projection details provided (proj4 string: +proj=stere +ellps=sphere +lat_0=90.0 +lon_0=0.0 +x_0=0.0 +y_0=0.0 +units=km +k_0=0.9330127018922193 +no_defs +type=crs).
  - Users may need to specify this projection in their applications.

## Data structure and usage guidance
- File format: NetCDF (with explicit variable names and units documented in the dataset).
- Example included for SURF_ug_PM25_rh50 (illustrative of NetCDF structure; detailed structure is described in the accompanying documentation).
- Usage guidance:
  - Compatible with common NetCDF-supporting tools (R, Python, FORTRAN).
  - Ensure correct handling of the polar stereographic grid and the specified proj4 string when integrating into analyses or visualizations.

## Quality assurance, limitations, and caveats
- QA/QC:
  - Conducted for 2002–2021; full QA/QC reports are available on request.
- Limitations and disclaimers:
  - Content use is at the user’s own risk; no warranty or guarantee that content is error-free or fit for a particular purpose.
  - Emissions data for 2020–2021 rely on 2019 emission estimates, which may affect year-specific accuracy.
  - The dataset reflects model outputs and associated assumptions (e.g., emissions inventories, data assimilation inputs) and may not capture all real-world variations.
- Documentation and references:
  - Bibliography includes key model descriptions and related studies (e.g., Simpson et al. 2012; Vieno et al. 2016; Skamarock et al. 2019).

## Governance, access, and reuse
- Dataset stewardship:
  - Was prepared to provide a consistent, traceable UK-focused atmospheric composition record, with clear provenance from EMEP4UK rv4.36 and WRF meteorology.
  - Documentation covers model design, data sources, variable definitions, and data structure to facilitate proper interpretation and reuse.
- Data sharing and cataloguing:
  - Guidance in the surrounding documentation emphasizes that such data can be uploaded to appropriate data portals and catalogues to enhance discoverability (where applicable in the hosting workflow).
- Metadata and discoverability:
  - Detailed variable names, units, and definitions are provided within the NetCDF structure and accompanying documentation to support discoverability and appropriate reuse by data stewards, researchers, and data users.

## References and further information
- Key references include:
  - Ge et al. 2021; Gu et al. 2021; Jalkanen et al. 2016; Simpson et al. 2012; Skamarock et al. 2019; Vieno et al. 2016a, 2016b; and related methodological papers on EMEP MSC-W and WRF model descriptions.