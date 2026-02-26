This data is an ensemble of JULES (Best et al. (2011), Clark et al. (2011)) simulations, ran for a select set of 1kmx1km grid cells in Great Britain, each with a different set of parameter values, from 2001 to 2010.

## Overview and aim for monitoring frameworks
- Purpose: Provide training and testing data for emulating high-resolution land surface models (JULES) to inform environmental monitoring decisions, model evaluation, and policy-relevant insights.
- Use case for monitoring authors: calibrate and validate environmental health models, assess how parameter choices influence primary productivity estimates, and support transparent, data-driven decision making.

## Data content and scope
- Outputs:
  - Gross Primary Productivity (GPP) by five plant functional types: gpp_BT (Broadleaf trees), gpp_NT (Needleleaf trees), gpp_C3g (C3 grasses), gpp_SH (Shrubs), gpp_Cr (Croplands), and total gpp_gb.
- Plant functional types include BT, NT, C3g, SH, Cr.
- Temporal and spatial dimensions:
  - 1km x 1km grid cells across Great Britain.
  - Time period: 2001–2010.
  - 8-day timesteps (dayofyear and year accompany outputs).
- Files include inputs (parameters and grid information) and outputs (GPP components).

## Experimental design, data generation, and validation
- Data split:
  - Training_Data_standardised.csv: used to fit the emulator (sparse Gaussian processes) as described in the associated methodology.
  - Testing_Data_standardised.csv: used to validate the emulator.
- Data generation technique:
  - Inputs (parameters) and outputs are generated for different parameter combinations per grid cell.
  - Quality control: runs that failed or did not converge were discarded and not included.

## Data transformation, scaling, and unscaling
- Input scaling:
  - All input columns scaled to [0, 1].
  - Unscaling: Tr_max.csv and Tr_min.csv contain max/min values to revert scaling.
- Output scaling:
  - gpp_XX outputs (excluding gpp_gb) are scaled to have mean 0 and standard deviation 1.
  - Unscaling: mean_and_stddev.csv provides mean and std for each gpp_XX to revert standardisation.
- Purpose of scaling:
  - Facilitates stable emulator training and comparability across variables.

## Data structure and file descriptions
- Training_Data_standardised.csv
  - 91 columns: includes index, lon/lat, grid coordinates (X, Y), a wide set of input parameters (e.g., alpha_io, dqcrit_io_* per plant type, f0_io_*, g_grow_io_*, lai_max_io_*, nmass_io_*, rootd_ft_io_*, tleaf_of_io_*, tlow_io_*, tupp_io_*, vsl_io_*), and outputs gpp_BT, gpp_NT, gpp_C3g, gpp_SH, gpp_Cr, gpp_gb, dayofyear, year.
  - The 75+ input-related columns correspond to parameter settings and grid attributes; the remaining columns include the GPP outputs and timing fields.
- Testing_Data_standardised.csv
  - Same 91-column schema as training, containing the testing observations.
- Tr_max.csv
  - 75 columns: maximum values for the subset of input variables (row names align with Training/Testing files) to revert scaling.
- Tr_min.csv
  - 75 columns: minimum values for the subset of input variables to revert scaling.
- mean_and_stddev.csv
  - 10 columns: means and standard deviations used to standardise gpp_BT, gpp_NT, gpp_C3g, gpp_SH, gpp_Cr (the gpp_gb is not standardised here).
  - Columns include Tr_BT_mean, Tr_BT_std, Tr_NT_mean, Tr_NT_std, Tr_C3g_mean, Tr_C3g_std, Tr_SH_mean, Tr_SH_std, Tr_Cr_mean, Tr_Cr_std.
- References for the dataset and methodology:
  - Best et al. (2011) and Clark et al. (2011) for JULES model descriptions.
  - Emulation approach described in “Emulation of high-resolution land surface models with sparse Gaussian processes with application to JULES.”

## Metadata, data quality, and governance
- Metadata and documentation:
  - Detailed column descriptions for inputs and outputs are provided in Training_Data_standardised.csv and associated documentation.
  - “Guide for Data Providers” indicates emphasis on metadata, openness, and appropriate data governance.
- Data quality considerations:
  - Only converged, successful runs are included (failed runs discarded).
  - Data transformations, scaling, and unscaling procedures are documented to ensure reproducibility and transparency.
- Data access and sharing:
  - The dataset is organized with explicit files for raw/standardised data, scaling parameters, and unscaling references to support reuse in monitoring frameworks.
  - Public sharing of underlying data is facilitated by the provided metadata and unscale/unstandardise resources, though governance practices should still ensure appropriate data management and provenance.

## Relevance for monitoring frameworks
- How this dataset supports monitoring and decision-making:
  - Provides a transparent, reproducible basis for testing environmental health monitoring models via emulator-based approaches.
  - Enables evaluation of how parameter choices affect productivity proxies (GPP) across key land-cover types and grid cells.
  - Offers clearly documented data processing steps (scaling, standardisation, and convergence filtering) essential for auditability and comparability over time.
  - Facilitates communication of complex model outputs through standardized formats and accompanying unscaling guidance.
- Practical considerations for authors:
  - Ensure governance around data sharing and provenance aligns with organisational policies.
  - Leverage the provided metadata to avoid misinterpretation and to support integration into broader monitoring dashboards or decision-support tools.
  - Use the training/testing split to validate monitoring frameworks and document emulator performance and uncertainty.

## References
- Best, M. J., et al. The Joint UK Land Environment Simulator (JULES), model description-Part 1: energy and water fluxes. Geosci. Model Dev. 2011.
- Clark, D. B., et al. The Joint UK Land Environment Simulator (JULES), model description-Part 2: carbon fluxes and vegetation dynamics. Geosci. Model Dev. 2011.