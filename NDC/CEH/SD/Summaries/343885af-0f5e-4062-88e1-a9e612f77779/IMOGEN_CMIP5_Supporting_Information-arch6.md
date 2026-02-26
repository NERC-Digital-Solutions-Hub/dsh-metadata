# This dataset represents the updated parameters and monthly climatologies used in the Integrated Model Of Global Effects of climatic aNomalies (IMOGEN) impacts modelling system (Huntingford et al., 2010)

## Purpose and context
- Provides updated parameters and monthly climatologies for the IMOGEN impacts modelling system, used to test land surface parameterisations before integration into full General Circulation Models (GCMs) and to project future emission scenarios.
- Built on pattern-scaling: local monthly changes in meteorology scale linearly with global land temperature increases.
- Uses an Energy Balance Model (EBM) to relate evolving radiative forcing to land warming, incorporating oceanic thermal delays.
- Updated dataset based on CMIP5 (34 GCMs) for improved coverage over the original CMIP3-based set (22 GCMs).

## Key data components (EBM parameters)
For each GCM, five EBM parameters are calibrated:
- λ land: climate sensitivity over land (W m⁻² K⁻¹)
- λ ocean: climate sensitivity over ocean (W m⁻² K⁻¹)
- ν: constant ratio of mean land and ocean surface (SST) rate of warming
- κ: ocean effective thermal diffusivity (W m⁻¹ K⁻¹)
- f: ocean fraction (unitless; 1 minus land fraction including Antarctica)

- The dataset includes these parameters for 34 GCMs, with their modelling centre and model name listed (e.g., BCC, BNU-ESM, CanESM2, etc.).

## Data structure and access
- Local monthly patterns are downloadable in ASCII format.
- Organization: for each GCM, a directory named CEN_<Centre>_MOD_<Model> (as in Table 1). Inside, monthly files jan to dec.
- Spatial grid: re-mapped to a common 2.5° x 3.75° grid (HadCM3 origin), yielding 1631 land points.
- Each monthly file contains a header line followed by 1631 data lines with columns:
  1) Longitude
  2) Latitude
  3) Temperature change per degree global warming (K per K)
  4) Relative humidity change per degree warming (% per K)
  5) Wind change per degree warming (m s⁻¹ per K)
  6) Unused (0.0)
  7) Longwave change per degree warming (W m⁻² per K)
  8) Shortwave change per degree warming (W m⁻² per K)
  9) Unused (0.0)
  10) Precipitation change per degree warming (mm d⁻¹ per K)
  11) Unused (0.0)
  12) Pressure change per degree warming (hPa per K)
  13) Unused (0.0)
- IMOGEN is routinely coupled to the JULES land surface model (references provided).

## Methodology and model details
- IMOGEN supports testing terrestrial climate impacts through pattern-scaling, enabling rapid evaluation of potential changes across regions and times.
- The dataset links local climate responses to a global warming signal via the five EBM parameters, with patterns provided for each month and GCM.
- Coupled usage with JULES allows integration with an established land surface model framework.

## Quality, provenance, and references
- Calibration against CMIP5 models with full numerical documentation, traceability on demand, and scripts using open-access software.
- Meets ISO standards for numerical model building.
- Acknowledges CMIP5/CMIP3 modeling groups, PCMDI, and WGCM; supported by the U.S. Department of Energy.
- Key references include Huntingford et al. (2010), Huntingford & Cox (2000), Best et al. (2011), Clark et al. (2011), and related CMIP5/CMIP3 literature.