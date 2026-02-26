# Metafile for the QNFM-CATCH dataset ' Simulated 15-min discharge time-series and baseline simulations for the River Kent following a Natural Flood Management intervention of 'Enhanced Hillslope Storage', Sedgewick, October 2015 to January 2016 '

## Overview
- This metafile accompanies the Q-NFM project outputs that quantify potential flood peak reductions from nature-based flood mitigation across large catchments.
- Focuses on a single NFM intervention, Enhanced Hillslope Storage (EHS), applied to the 209 sq km River Kent catchment in Cumbria.
- Presents 67 simulated discharge time-series (15-minute resolution) for baseline and post-NFM scenarios covering 1 Oct 2015 to 17 Jan 2016, including Storm Desmond.
- The study aims to illustrate flood peak reductions for events up to a 1-in-500-year return period; interpretations are reported in Beven et al. (2022b).

## Data Content and Structure
- Observed data: 15-minute discharge at the Environment Agency Sedgwick gauging station (period 01/10/2015–17/01/2016).
- Modelling: Dynamic Topmodel (latest version used at the time) with a rainfall field derived from a direction-dependent, topography-controlled interpolation based on observed rainfall in the Cumbrian Mountains.
- Parameter uncertainty: 10,000 Monte Carlo parameter sets; 67 simulations retained after applying acceptance criteria.
- Datasets included:
  - QNFM-CATCH_baseline_datafile.csv
  - QNFM-CATCH_ehs_datafile.csv
- Structure of each dataset:
  - Time index: 15-minute increments from 00:00:00 01/10/2015 to 23:45:00 17/01/2016.
  - Columns: 67 columns corresponding to unique identifiers for each random parameter set; headings are identifiers with no intrinsic meaning beyond uniqueness.
  - Descriptions: River discharge values; Units: cubic metres per second (m^3/s).

## Methods and Quality Control
- Modelling approach:
  - Baseline simulations using Dynamic Topmodel (v0.2.1) to represent pre-intervention conditions.
  - Post-NFM simulations updated with a DEM reflecting hillslope bunds for Enhanced Hillslope Storage.
- Parameter sampling and screening:
  - Initial Monte Carlo sampling of prior parameter distributions (independent uniform) to produce 100,000 simulated discharge datasets per scenario.
  - Limits of Acceptability (LoA) applied using 2.5–97.5 percentile ranges of runoff coefficients from past events with a timing constraint of ±2 hours.
  - This step reduced to 3,249 surviving datasets per scenario.
  - Further evaluation using hydrograph steps from 2005 and 2009 reduced to 118 per scenario.
  - Saturation-excess area criterion applied: simulations with less than 10% of the area exhibiting surface storage >1 mm at any step were rejected, leaving 67 surviving discharge datasets per scenario.
- NFM feature placement:
  - Bund locations based on the Working with Natural Processes (WwNP) dataset; each bund modeled with a 10-hour residence time.

## Provenance and References
- Beven, K., Lane, S., Page, T., Hankin, B., Smith, P., and Chappell, N.A. 2022a. On (in)validating environmental models. Hydrological Processes 36(10): e14703.
- Beven, K., Page, T., Hankin, B., Smith, P., Kretzschmar, A., Mindham, D., and Chappell, N. A. 2022b. Deciding on fitness-for-purpose - of models and of natural flood management. Hydrological Processes 36: e14752.
- Hankin, B., Chappell, N.A., Page, T.J.C., Kipling, K., Whitling, M., and Burgess-Gamble, L. 2018. Mapping the potential for Working with Natural Processes - technical report. SC150005/R6. Environment Agency, Bristol. 77p.
- Page, T., Beven, K.J., Hankin, B., and Chappell, N.A. 2022. Interpolation of rainfall observations during extreme rainfall events in complex mountainous terrain. Hydrological Processes 36: e14758.
- Dynamic Topmodel (v0.2.1) available at CRAN: https://cran.r-project.org/web//packages/dynatop/index.html

## Reuse and Data Governance (for Data Leaders)
- Clear documentation of data generation, parameterization, and quality gates supports reproducibility and auditability across data-sharing networks.
- Metadata conventions include time indexing, unit specification, and per-column identifiers to facilitate discoverability and interoperability.
- The dataset is designed to enable assessment of flood-peak reductions under a defined NFM intervention, supporting planning and policy discussions across catchments.
- For broader data-system integration, note the explicit linkage to methodological references (Beven et al. 2022a,b; Page et al. 2022) and the public availability of the modelling tool (Dynamic Topmodel) used in generation.
- Consider ongoing coordination with data custodians for future updates, validation, and potential extension to additional catchments or NFM scenarios.