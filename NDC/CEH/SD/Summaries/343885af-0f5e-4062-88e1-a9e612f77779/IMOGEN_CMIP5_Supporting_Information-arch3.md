# Introduction

- The dataset represents updated parameters and monthly climatologies used in the Integrated Model Of Global Effects of climatic aNomalies (IMOGEN) impacts modelling system.
- IMOGEN is used to test new land surface parameterisation before implementation in a full General Circulation Model (GCM) and to make projections for future emission scenarios not simulated by the GCMs.
- IMOGEN uses pattern-scaling to emulate GCMs: local monthly changes in meteorology scale linearly with global land warming; an Energy Balance Model (EBM) relates evolving atmospheric radiative forcing to land warming while accounting for oceanic thermal delays.
- The dataset updates the original CMIP3-based set (22 GCMs) to a CMIP5-based ensemble (34 GCMs). A description of the updated dataset is provided in Comyn-Platt et al. (Nature Geoscience, 2018, accepted).

## Data Description

- The EBM is parameterised by five values for each GCM:
  - 1) λ_land (land climate sensitivity; W m^-2 K^-1)
  - 2) λ_ocean (ocean climate sensitivity; W m^-2 K^-1)
  - 3) ν (constant ratio of mean land and ocean surface warming)
  - 4) κ (ocean effective thermal diffusivity; W m^-1 K^-1)
  - 5) f (ocean fraction; unitless)
- Table 1 lists these five parameters for each of the 34 GCMs, including the modeling centre and model name (and the corresponding values for each parameter).
- Examples of parameter values are provided for multiple models (illustrating variation across centres).

## Data Structure

- Local and monthly pattern data are downloadable in ASCII format.
- For each GCM, there is a directory named CEN_<Centre>_MOD_<Model> (34 directories in total).
- Within each directory, monthly files jan through dec exist.
- All GCMs are remapped to a common grid of 2.5° latitude × 3.75° longitude (1631 land points).
- Each monthly file contains:
  - One header line, followed by 1631 lines with columns:
    1) Longitude
    2) Latitude
    3) Temperature change per degree global warming (Kelvin × Kelvin^-1)
    4) Relative humidity change per degree warming (% change × Kelvin^-1)
    5) Wind change per degree warming (m s^-1 × Kelvin^-1)
    6) Unused (0.0)
    7) Longwave change per degree warming (W m^-2 × Kelvin^-1)
    8) Shortwave change per degree warming (W m^-2 × Kelvin^-1)
    9) Unused (0.0)
    10) Precipitation change per degree warming (mm day^-1 × Kelvin^-1)
    11) Unused (0.0)
    12) Pressure change per degree warming (hPa × Kelvin^-1)
    13) Unused (0.0)
- IMOGEN is routinely coupled to the JULES land surface model (with references to JULES literature and models).

## Quality Control

- Calibration against CMIP5 models includes full numerical code documentation and traceability on demand, with scripts based on open-access software.
- The process meets ISO standards for numerical model building.

## Acknowledgements

- The authors acknowledge modeling groups, PCMDI, and WCRP WGCM for CMIP5/CMIP3 data, and support from the U.S. Department of Energy.

## References

- Best, M.J. et al., 2011: The Joint UK Land Environment Simulator (JULES), model description.
- Clark, D.B. et al., 2011: JULES model description – carbon fluxes and vegetation dynamics.
- Comyn-Platt, E. et al., 2018: Carbon budgets for 1.5 and 2°C targets with natural wetland and permafrost feedbacks.
- Huntingford, C. et al., 2010: IMOGEN—an intermediate complexity model to evaluate terrestrial impacts of climate change.
- Huntingford, C. and Cox, P.M., 2000: An analogue model to derive additional climate change scenarios from existing GCM simulations.
- Meehl, G.A. et al., 2007: The CMIP3 multimodel dataset.
- Taylor, K.E., Stouffer, R.J. and Meehl, G.A., 2012: CMIP5 overview and experiment design.
- Zelazowski, P. et al., 2016: Climate pattern-scaling set for CMIP ensembles and uncertainty in IMOGEN v2.0.