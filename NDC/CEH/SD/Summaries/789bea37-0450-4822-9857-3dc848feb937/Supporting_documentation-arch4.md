# This data is an ensemble of JULES (Best et al. 2011, Clark et al. 2011) simulations, ran for a select set of 1kmx1km grid cells in Great Britain, each with a different set of parameter values, from 2001 to 2010.

## Overview
- Ensemble of Joint UK Land Environment Simulator (JULES) simulations for GB grid cells, 2001–2010.
- Includes Gross Primary Productivity (GPP) outputs for five plant functional types (BT, NT, C3g, SH, Cr) and the combined total (gpp_gb).
- Data prepared for emulation: training and testing sets to fit/validate an emulator described in the associated publication.
- Inputs are scaled to [0,1]; outputs gpp_XX are scaled to zero mean and unit variance. Unscaling guidance is provided via Tr_max.csv, Tr_min.csv, and mean_and_stddev.csv.

## Data content and structure
- Five key data files:
  - Training_Data_standardised.csv: 91 columns including unique run ID, grid coordinates, and 75 input/parameter columns per grid cell, plus outputs.
  - Testing_Data_standardised.csv: identical structure for validation data.
  - Tr_max.csv: maximum values for a subset of input variables to restore original scales.
  - Tr_min.csv: minimum values for the same subset of inputs.
  - mean_and_stddev.csv: means and standard deviations for unstandardising GPP outputs (gpp_BT, gpp_NT, gpp_C3g, gpp_SH, gpp_Cr; gpp_gb excluded).
- Column details (high level):
  - Metadata: index, lon, lat, X, Y representing grid cell and location.
  - Plant functional type parameters: alpha_io, dqcrit_io_* (for BT, NT, C3g, SH, Cr), f0_io_*, g_grow_io_*, lai_max_io_*, nmass_io_*, rootd_ft_io_*, tleaf_of_io_*, tlow_io_*, tupp_io_*, vsl_io_*, and related variables per plant type.
  - Simulation outputs: gpp_gb and gpp_BT, gpp_NT, gpp_C3g, gpp_SH, gpp_Cr; time-related fields dayofyear and year.
  - Meteorological and state inputs: time, dtr, huss, precip, psurf, rlds, rsds, sfcWind, tas, plus fractional grid cover BT, NT, C3g, SH, Cr.
- Documentation included within the file set provides descriptions for all 91 columns.

## Experimental design / data generation
- Data split: randomly divided into training and testing datasets.
  - Training_Data_standardised.csv used to fit the emulator.
  - Testing_Data_standardised.csv used to validate emulator performance.
- Scaling:
  - Inputs scaled to [0,1].
  - Outputs gpp_XX (excluding gpp_gb) scaled to mean 0 and standard deviation 1.
- Quality control: runs that failed or did not converge were discarded and not included.

## Data processing and unscaling
- To revert input scaling: use Tr_max.csv and Tr_min.csv (matching rows/columns) to rescale inputs back to their original ranges.
- To revert output scaling: use mean_and_stddev.csv for the corresponding gpp_BT, gpp_NT, gpp_C3g, gpp_SH, gpp_Cr, excluding gpp_gb.

## Usage context and purpose
- Designed to support emulation of high-resolution land surface models with sparse Gaussian processes, specifically applying the emulator to JULES.
- Provides a ready-made paired dataset of parameter settings (inputs) and GPP outputs (targets) across a range of GB grid cells and years for robust emulator training and validation.
- References included for the JULES model descriptions and the emulator methodology.

## Data governance, provenance, and caveats
- Provenance: derived from established JULES model descriptions (Best et al. 2011; Clark et al. 2011).
- Documentation and metadata are embedded in the file descriptions to aid discoverability and reuse.
- Scope caveats:
  - Limited to select GB grid cells (1km x 1km) and 2001–2010 period.
  - Outputs assume grid-cell-level aggregation by plant type (e.g., gpp_BT represents BT in the entire cell).
  - Random split means training/validation sets are not temporally separated unless designed so in the original study.
  - Data quality controlled by discarding non-convergent or failed runs.

## Access and documentation
- Five CSV files constitute the dataset:
  - Training_Data_standardised.csv
  - Testing_Data_standardised.csv
  - Tr_max.csv
  - Tr_min.csv
  - mean_and_stddev.csv
- Row identifiers align across files to enable straightforward joining of inputs, outputs, and scaling parameters.
- Primary references:
  - Best et al. (2011) and Clark et al. (2011) on the JULES model
  - Emulation methodology paper: Emulation of high-resolution land surface models with sparse Gaussian processes with application to JULES