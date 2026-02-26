This data is an ensemble of JULES (Best et al. 2011, Clark et al. 2011) simulations, ran for a select set of 1kmx1km grid cells in Great Britain, each with a different set of parameter values, from 2001 to 2010.

# Overview and purpose
- Content: Simulated Gross Primary Productivity (GPP) for five plant functional types (gpp_BT, gpp_NT, gpp_C3g, gpp_SH, gpp_Cr) and the weighted total (gpp_gb) across grid cells.
- Use case: Data intended to fit an emulator described in a referenced study (Emulation of high-resolution land surface models with sparse Gaussian processes with application to JULES).
- Data split: Two files for experimental design and validation:
  - Training_Data_standardised.csv (for fitting the emulator)
  - Testing_Data_standardised.csv (for validating the emulator)

# Data content and structure
- File set (five files total):
  - Training_Data_standardised.csv
  - Testing_Data_standardised.csv
  - Tr_max.csv (maximum values for a subset of input variables to rescale back to original scale)
  - Tr_min.csv (minimum values for a subset of input variables)
  - mean_and_stddev.csv (mean and standard deviation for unstandardising the gpp_XX outputs; excludes gpp_gb)
- Training_Data_standardised.csv (91 columns)
  - Key identifiers: index (unique JULES run), lon, lat, X, Y (grid coordinates), year, time (8-day average timestep)
  - Input parameters (scaled 0–1) for each plant functional type and general model settings (examples: alpha_io, dqcrit_io_BT/NT/C3g/SH/Cr, f0_io_BT/NT/C3g/SH/Cr, g_grow_io_*, g_leaf_0_io, knl_io, lai_max_io_*, nmass_io_*, rootd_ft_io_*, tleaf_of_io_*, tlow_io_*, tupp_io_*, vsl_io_*, etc.)
  - Outputs (scaled): gpp_BT, gpp_NT, gpp_C3g, gpp_SH, gpp_Cr (and gpp_gb as the total)
  - Other descriptive fields: Description, time, dtr, huss, precip, psurf, rlds, rsds, sfcWind, tas, BT/NT/C3g/SH/Cr fractions, slope, soil conductivities and water contents, etc.
- Testing_Data_standardised.csv
  - Same structure as training data but used for validation.
- Tr_max.csv and Tr_min.csv
  - 75 columns each, containing the max/min values for the subset of input variables to rescale to original scales.
- mean_and_stddev.csv
  - Ten columns, giving Tr_BT_mean/Tr_BT_std, Tr_NT_mean/Tr_NT_std, Tr_C3g_mean/Tr_C3g_std, Tr_SH_mean/Tr_SH_std, Tr_Cr_mean/Tr_Cr_std (means and standard deviations used to standardise gpp outputs)
- Unscaling guidance:
  - Inputs scaled to [0,1] can be restored using Tr_max.csv and Tr_min.csv.
  - Outputs gpp_BT, gpp_NT, gpp_C3g, gpp_SH, gpp_Cr are scaled to mean 0 and stdev 1; unscale using mean_and_stddev.csv.

# Data provenance and quality control
- Generation and curation
  - Data are results from JULES simulations across UK grid cells with varied parameter settings.
  - Quality control: runs that failed or did not converge were discarded and not included in the dataset.
- Documentation and references
  - Data linked to the JULES model descriptions (Best et al. 2011; Clark et al. 2011) and to the emulator methodology described in related literature.

# Geospatial and temporal scope
- Geography: Great Britain, 1km x 1km grid cells.
- Time: 2001–2010, with an 8-day timestep representing a 8-day average (time field indicates which day in the 8-day window).

# Governance, accessibility, and usage considerations for Data Stewards
- Metadata and discoverability
  - Ensure clear metadata mapping for: unique run identifiers, grid coordinates, plant functional type definitions, and all input/output variables.
  - Include provenance links to the JULES model and emulator methodology references.
- Data standardization and interoperability
  - Maintain consistent column naming conventions and descriptions to support cross-dataset integration.
  - Preserve scaling/unscaling guidance with the corresponding max/min and mean/stddev files to enable reproducible use.
- Access, sharing, and licensing
  - Provide access to all five data files (train, test, and supporting scaling documents) through catalogues or portals with stable DOIs or persistent identifiers if available.
  - Document any usage restrictions or licensing terms (not specified in the data description; advisable to attach clear licensing).
- Data quality and lifecycle
  - Retain QC notes (e.g., which runs were discarded) to support data lineage.
  - Establish a versioning strategy for updates or reprocessing (e.g., re-running with new parameter sets or extended time periods) and reflect changes in Tr_max/Tr_min/mean_std files.
- Documentation and user support
  - Provide a data dictionary with explicit definitions for all 91 input columns and all 10 output-related statistics.
  - Offer guidance for unscaling steps (where to apply Tr_max/Tr_min and mean/stddev) and examples for emulator training/validation workflows.
- Data stewardship actions
  - Validate consistency between Training and Testing datasets and their accompanying scaling files.
  - Ensure that any future updates maintain backward compatibility or clearly version changes to prevent user confusion.
  - Document transformations applied (scaling, filtering of non-convergent runs) and preserve raw vs. processed states where feasible.

# Endnotes and references
- Data source and model background
  - The Joint UK Land Environment Simulator (JULES) model descriptions (Best et al. 2011; Clark et al. 2011) underpin the data content.
- Emulator methodology
  - The training data are intended to support emulation of high-resolution land surface models with sparse Gaussian processes (as described in the referenced emulator study).