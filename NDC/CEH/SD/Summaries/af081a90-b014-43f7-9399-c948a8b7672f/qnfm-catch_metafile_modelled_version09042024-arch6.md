# Metafile for the QNFM-CATCH dataset ' Simulated 15-min discharge time-series and baseline simulations for the River Kent following a Natural Flood Management intervention of 'Enhanced Hillslope Storage', Sedgewick, October 2015 to January 2016 '

## Overview
- Purpose: Provide simulated 15-minute discharge time-series to quantify flood peak reductions from Natural Flood Management (NFM) features, specifically Enhanced Hillslope Storage (EHS), in the River Kent catchment (209 sq km).
- Project context: Part of the NERC-funded Q-NFM research aiming to assess flood mitigation magnitudes across catchments; results discussed in Beven et al. (2022b).
- Data scope: 67 accepted baseline and 67 post-NFM simulations, covering 1 Oct 2015 to 17 Jan 2016 (including Storm Desmond) at Sedgwick gauging station.

## Data Description
- Observations modelled: Observed 15-minute discharge at Sedgwick (EA station) for 1 Oct 2015 to 17 Jan 2016.
- Modelling framework: Dynamic Topmodel (v0.2.1) with a rainfall field derived from direction-dependent, topographically controlled interpolation (Page et al., 2022).
- Parameter sampling: 100,000 Monte Carlo simulations using a wide range of model parameters; only 67 simulations passed acceptance criteria per scenario.
- Datasets provided:
  - QNFM-CATCH_baseline_datafile.csv
  - QNFM-CATCH_ehs_datafile.csv
- Data format: CSV; columns include:
  - Index: date and time (15-minute increments) from 00:00 01/10/2015 to 23:45 17/01/2016 (dd/mm/yyyy hh:mm).
  - Description: River discharge (units in cubic metres per second, m3/s).
  - 67 data columns: unique identifiers for each random parameter set (the numbers are unique IDs with no intrinsic meaning).

## Data Structure and Content
- Time index: 15-minute intervals spanning the 2015–2016 period.
- Parameter sets: 67 columns per dataset, each representing a different Monte Carlo parameter draw that produced a valid time-series.
- Column headers: unique IDs for parameter sets; the IDs carry no additional meaning beyond uniqueness.

## Modelling and Quality Control
- Modelling steps:
  - Model choice: Dynamic Topmodel.
  - Parameter ranges: prior distributions informed by Beven et al. (2022b) Table 1.
  - Initial sampling: 100,000 simulated datasets per scenario.
  - Limits of Acceptability (LoA): based on 2.5–97.5 percentile ranges of runoff coefficients from past events, with timing constraint of ±2 hours; applied to ranked hydrograph steps for 2015 events, including the largest flood on record.
  - Intermediate filters: after LoA, 3,249 datasets per scenario survived; evaluation against 2005 and 2009 events reduced to 118 per scenario.
  - Final filter: simulations with less than 10% of the area having surface storage >1 mm at any time step were kept; this yielded 67 surviving datasets per scenario.
- NFM scenario specifics:
  - EHS feature locations derived from the Working with Natural Processes (WwNP) dataset (Hankin et al., 2018).
  - Each bund feature modelled with a residence time of 10 hours.
- Objective of the final dataset: demonstrate the magnitude of flood peak reductions for a range of events, up to a 1-in-500-year event (0.2% exceedance).

## Data Access and Formats
- Files provided:
  - QNFM-CATCH_baseline_datafile.csv
  - QNFM-CATCH_ehs_datafile.csv
- Structure:
  - Time index column (dd/mm/yyyy hh:mm).
  - 67 parameter-set columns containing discharge time-series (m3/s) for baseline and post-NFM scenarios, respectively.
- Notes for data use:
  - The 67 column headers are unique IDs without intrinsic meaning; to link to specific parameter sets, refer to accompanying Beven et al. (2022b) documentation if available.
  - The datasets are designed for self-serve analysis of flood-peaking reductions under various plausible parameterisations.

## References and Interpretation
- Beven, K., Lane, S., Page, T., et al. 2022a. On (in)validating environmental models. Hydrological Processes.
- Beven, K., Page, T., Hankin, B., et al. 2022b. Deciding on fitness-for-purpose - of models and of natural flood management. Hydrological Processes.
- Hankin, B., Chappell, N.A., Page, T.J.C., et al. 2018. Mapping the potential for Working with Natural Processes - technical report SC150005/R6. Environment Agency.
- Page, T., Beven, K.J., Hankin, B., et al. 2022. Interpolation of rainfall observations during extreme rainfall events in complex mountainous terrain. Hydrological Processes.
- The interpreted findings and context for these datasets are detailed in Beven et al. (2022b).