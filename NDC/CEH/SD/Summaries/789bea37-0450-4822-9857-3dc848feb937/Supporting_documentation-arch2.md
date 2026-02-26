# Ensemble of JULES simulations for 1km GB grid cells (2001–2010): GPP by plant functional types and emulator training/testing data

- An ensemble of Joint UK Land Environment Simulator (JULES) simulations across select 1km × 1km grid cells in Great Britain, spanning 2001–2010.
- Outputs Gross Primary Productivity (GPP) for five plant functional types (PFTs) plus a weighted total: gpp_BT, gpp_NT, gpp_C3g, gpp_SH, gpp_Cr, and gpp_gb (total GPP).
- Parameter-space sampling with different parameter values for each grid cell; data are prepared for emulation using sparse Gaussian processes.

## Data scope and purpose

- Designed to support emulation of high-resolution land surface models (JULES) with a focus on predicting GPP by PFTs.
- Data are split into training and testing sets to fit and validate the emulator described in the referenced study.
- Data are provided in standardised form with clear scaling/unscaling instructions to ensure reproducibility and comparability over time.

## Data structure and files

- Training_Data_standardised.csv
  - 91 columns: unique run identifier, grid cell coordinates (lon, lat, X, Y), and a comprehensive set of input parameters for each PFT (e.g., alpha_io, dqcrit_io_*, f0_io_*, g_grow_io_*, lai_max_io_*, nmass_io_*, rootd_ft_io_*, tleaf_of_io_*, tlow_io_*, tupp_io_*, vsl_io_*), plus time and environmental variables and GPP outputs (gpp_BT, gpp_NT, gpp_C3g, gpp_SH, gpp_Cr, gpp_gb), dayofyear, and year.
  - Input columns are scaled to [0, 1]; unscale using Tr_max.csv and Tr_min.csv.
  - Output columns gpp_XX (excluding gpp_gb) are standardised to mean 0 and std 1; unscale using mean_and_stddev.csv.
- Testing_Data_standardised.csv
  - Identical structure to Training_Data_standardised.csv, used for validation of the emulator.
- Tr_max.csv
  - 75 columns: maximum values for a subset of input variables to reverse scaling.
- Tr_min.csv
  - 75 columns: minimum values for a subset of input variables to reverse scaling.
- mean_and_stddev.csv
  - 10 columns: means and standard deviations used to standardise gpp_BT, gpp_NT, gpp_C3g, gpp_SH, gpp_Cr (excluding gpp_gb).

## Experimental design and data quality

- Data are generated from an ensemble of JULES runs with diverse parameter settings across 1km GB grid cells (2001–2010).
- Runs that failed or did not converge were discarded (quality control).
- The dataset is designed to support building emulators (e.g., sparse Gaussian process models) to predict high-resolution GPP outputs efficiently.

## Data content details (selected parameter groups)

- Inputs related to photosynthesis and carbon assimilation:
  - alpha_io (photosynthetic quantum efficiency)
  - dqcrit_io_* (critical humidity deficit for BT, NT, C3g, SH, Cr)
  - f0_io_* (Ci/Ca when dq = 0)
  - g_grow_io_* (rate of leaf growth)
  - lai_max_io_* (maximum leaf area index)
  - nmass_io_* (top leaf N content)
  - time-varying environmental drivers (time, dtr, huss, precip, psurf, rlds, rsds, sfcWind, tas)
- Plant functional types (PFTs) distribution and fractions:
  - BT, NT, C3g, SH, Cr fractions per grid cell
- Soil and root properties:
  - slope, hcon1/hcon2, satcon1/satcon2, vcrit1/vcrit2, vast1/vsat2, vwilt1/v wilt2
  - rootd_ft_io_* (root decay with depth)
- Temperature and radiation parameters:
  - tleaf_of_io_*, tlow_io_*, tupp_io_* (leaf drop temperature, lower/upper photosynthesis temp bounds)
- GPP outputs:
  - gpp_BT, gpp_NT, gpp_C3g, gpp_SH, gpp_Cr
  - gpp_gb (total GPP)
- Temporal resolution:
  - dayofyear and year indicating the 8-day averaged timestep within 2001–2010.

## How to use (for environment-monitoring analysts)

- Use Training_Data_standardised.csv to fit emulator models; use Testing_Data_standardised.csv to validate predictive performance.
- To revert scaling for inputs:
  - Apply scaling ranges from Tr_min.csv and Tr_max.csv to transform standardized inputs back to their original scale.
- To revert scaling for outputs:
  - Use mean_and_stddev.csv to unstandardise gpp_BT, gpp_NT, gpp_C3g, gpp_SH, gpp_Cr; note gpp_gb is provided as a derived total and excluded from standardisation.
- Consider the five-file data resource as a consistent, QA-filtered set of high-resolution JULES simulations suitable for constructing and evaluating data-driven emulators in environmental monitoring workflows.
- References for model description:
  - Best et al. 2011; Clark et al. 2011 (JULES model descriptions, energy/water fluxes and carbon fluxes/vegetation dynamics).

## References

- Best, M. J., et al. The Joint UK Land Environment Simulator (JULES), model description-Part 1: energy and water fluxes. Geoscientific Model Development, 2011.
- Clark, D. B., et al. The Joint UK Land Environment Simulator (JULES), model description-Part 2: carbon fluxes and vegetation dynamics. Geoscientific Model Development, 2011.