# Introduction

## Purpose and use
- Provides updated parameters and monthly climatologies for the Integrated Model Of Global Effects of climatic aNomalies (IMOGEN) impacts modelling system.
- Used to test new land surface parameterisations before implementation in full General Circulation Models (GCMs) and to make projections for future emission scenarios beyond what GCMs have simulated.
- IMOGEN uses pattern-scaling to emulate GCM responses, linking local monthly meteorology changes to global land warming via an Energy Balance Model (EBM).

## Pattern-scaling and model framework
- Pattern-scaling assumes local changes scale linearly with global temperature increase over land.
- EBM relates evolving radiative forcing to land warming while accounting for oceanic thermal delays.
- Original calibration relied on CMIP3 (22 GCMs); the updated dataset uses CMIP5 (34 GCMs).
- References discuss CMIP3/CMIP5 contexts and the integration with IMOGEN and JULES.

## Data content: EBM parameters
- Five EBM parameters calibrated per GCM:
  - λ_land: climate sensitivity over land (W m^-2 K^-1)
  - λ_ocean: climate sensitivity over the ocean (W m^-2 K^-1)
  - ν: constant ratio of mean land and ocean SST warming
  - κ: ocean effective thermal diffusivity (W m^-1 K^-1)
  - f: ocean fraction (unitless; one minus land fraction including Antarctica)
- Table 1 lists these values for each of the 34 CMIP5 GCMs (model and centre).

## Data source and CMIP5 context
- Based on CMIP5 multi-model ensemble; includes multiple centres/models (e.g., BCC-CSM1-1, CCSM, GISS, IPSL, HadGEM, etc.).
- Provides a consolidated calibration set to support IMOGEN’s pattern-scaling calculations.

## Data structure and file layout
- Local and monthly pattern files are downloadable ASCII files.
- For each GCM, directory structure: CEN_<Centre>_MOD_<Model> (34 directories).
- Within each directory: monthly files named jan, feb, ..., dec (one for each month).
- Each GCM is remapped to a common grid: 2.5° latitude × 3.75° longitude (HadCM3 original grid), resulting in 1631 land points.
- Each monthly file contains:
  - 1 header line
  - 1631 data lines with columns:
    1. Longitude
    2. Latitude
    3. Temperature change per degree global warming (K per K)
    4. Relative humidity change per degree global warming (% per K)
    5. Wind change per degree global warming (m s^-1 per K)
    6. Unused (0.0)
    7. Longwave change per degree global warming (W m^-2 per K)
    8. Shortwave change per degree global warming (W m^-2 per K)
    9. Unused (0.0)
    10. Precipitation change per degree global warming (mm day^-1 per K)
    11. Unused (0.0)
    12. Pressure change per degree global warming (hPa per K)
    13. Unused (0.0)

## Access, provenance, and metadata
- IMOGEN is routinely coupled to the JULES land surface model; coupling examples are described in associated literature.
- Calibration against CMIP5 models with full numerical code documentation and traceability on demand.
- Open-access software and ISO-standard practices are employed for numerical model development.

## Quality control and governance
- Emphasizes traceability, documented workflows, and reproducibility.
- Calibrations and data preparation align with established CMIP5 procedures and related literature.

## Acknowledgments and references
- Acknowledges CMIP5 data providers, PCMDI, WGCM, and U.S. Department of Energy support.
- References key works on IMOGEN, JULES, pattern-scaling, and CMIP5 context (e.g., Huntingford et al. 2010; Best et al. 2011; Taylor et al. 2012).