# IMOGEN: Energy Balance Model Parameters and Pattern Data for CMIP3 GCMs

- This dataset provides the parameters used in the Integrated Model Of Global Effects of climatic aNomalies (IMOGEN) impacts modelling system. It supports testing new land surface parameterisations before full GCM implementation and making projections for future emission scenarios not yet run in GCMs.
- IMOGEN employs pattern-scaling to emulate GCMs, assuming local monthly meteorological changes scale linearly with global land warming. An Energy Balance Model (EBM) links evolving radiative forcing to land warming, accounting for oceanic thermal delays.

## Data Description

- EBM calibration parameters (per GCM)
  - λ_l: climate sensitivity over land (W m^-2 K^-1)
  - λ_o: climate sensitivity over ocean (W m^-2 K^-1)
  - κ: ocean effective thermal diffusivity (W m^-1 K^-1)
  - ν: constant ratio of mean land and ocean SST warming (dimensionless)
  - f: ocean fraction (1 minus land fraction, including Antarctica)
- Calibrated against 22 GCMs from CMIP3 (Meehl et al., 2007) with tabled values for each GCM (e.g., BCCR-BCM2.0, CGCM3.1(T47), CNRM-CM3, etc.)
- Local and monthly patterns
  - Patterns are downloadable ASCII files for each GCM and month.
  - Each GCM is remapped to a common HadCM3 grid of 2.5° x 3.75° (1631 land points).
  - Each monthly file (jan–dec) contains a header followed by 1631 data points describing changes per degree global warming:
    1) Longitude
    2) Latitude
    3) Temperature change per degree warming [K per K]
    4) Relative humidity change per degree warming [% per K]
    5) Wind change per degree warming [m s^-1 per K]
    6) Unused
    7) Longwave change per degree warming [W m^-2 per K]
    8) Shortwave change per degree warming [W m^-2 per K]
    9) Unused
    10) Precipitation change per degree warming [mm day^-1 per K]
    11) Unused
    12) Pressure change per degree warming [hPa per K]
    13) Unused
- Coupling and related work
  - IMOGEN is routinely coupled to the JULES land surface model (examples in Huntingford et al., 2010; JULES described in Best et al., 2011 and Clark et al., 2011).

## Data Structure

- 22 directories named pattRelPR_d2_<GCM>, one per GCM.
- Inside each directory: monthly ASCII files jan through dec.
- Each GCM is re-mapped to the common HadCM3 grid; results cover 1631 land points per month.
- Each file includes one header line followed by 1631 data points as described above.

## Purpose, Usage, and Context

- Used to calibrate and test IMOGEN’s EBM parameters and pattern responses against a multi-model ensemble (CMIP3).
- Enables exploration of land surface parameterisations and their responses to different GCM-sourced patterns.
- Provides a scalable approach to project future warming scenarios for which full GCM runs are not available, by linking local changes to global forcing via pattern scaling.
- IMOGEN’s integration with JULES allows applying these patterns within a land-surface modelling framework.

## Quality Control

- Patterns are part of a beta program extending IMOGEN EBM and pattern parameterisation beyond the UK, currently validated against CMIP3.
- A new version is being developed to emulate CMIP5 models, with emphasis on full traceability and UK ISO standards.

## Acknowledgement

- Acknowledges modeling groups, PCMDI, WGCM, and WCRP for CMIP3 data.
- Support provided by the U.S. Department of Energy.

## References

- Best, M.J. et al. 2011. The Joint UK Land Environment Simulator (JULES), model description - Part 1: Energy and water fluxes.
- Clark, D.B. et al. 2011. The Joint UK Land Environment Simulator (JULES), model description - Part 2: Carbon fluxes and vegetation dynamics.
- Huntingford, C. et al. 2010. IMOGEN: an intermediate complexity model to evaluate terrestrial impacts of a changing climate.
- Huntingford, C. & Cox, P.M. 2000. An analogue model to derive additional climate change scenarios from existing GCM simulations.
- Meehl, G.A. et al. 2007. The WCRP CMIP3 multimodel dataset.
- Zelazowski, P., Huntingford, C., Mercado, L.M., and Schaller, N. (2016) Climate pattern scaling set for an ensemble of 22 GCMs – adding uncertainty to the IMOGEN impacts system (In Prep).