# Simulations of Emerald Ash Borer (EAB) spread in Great Britain with optimised surveillance

## Overview
- Purpose: Model Emerald Ash Borer (EAB) lifecycle and spread across Great Britain to inform surveillance strategies for early detection (e.g., girdled trees, traps, under-bark sampling).
- Implementation: C++ model compiled with Visual Studio 2022; uses stochastic sampling and a dispersal kernel with NAG libraries; inputs include multiple scenario parameters and entry-point realizations.
- Outputs: Maps and data to predict optimal surveillance locations; supports optimization of detection approaches.

## Inputs and data sources
- Model structure and data are organized under a subdirectory system:
  - Main inputs located in Model_Input_Files (to be placed relative to the main code directory).
  - Key input files (described in the document): ADBInfection_GB.txt, InclusionProb.txt, Infection_GB.txt, Owners_GB.txt, SampleEntry.txt, treeDensity_GB.txt.
- Scenario testing:
  - SampleEntry.txt describes lists of entry locations; only this file needs modification to test new scenarios.
  - Nine scenarios tested by varying:
    - Entry certainty through known pathways: 70%, 50%, 30%.
    - Probability of EAB escaping at port vs onward depots: 25%, 50%, 75%.
  - For each scenario, 10,000 realizations of entry points are sampled to form model inputs (SampleEntry.txt).
- Spatial framework:
  - 1 km x 1 km grid covering Great Britain; grid indexing and input mappings align with specific data layers.

## Model outputs and how they are used
- Primary output: DataForOpt.txt, per simulation/realization, containing:
  - Initial incursion location (grid row/col), weight, ash-tree density per cell, observation location (row/col), and eight annual columns of average larvae per tree in the observation cell, plus eight columns of trees remaining after EAB mortality.
- Objective function: Omega, used in an optimization routine (not included) to maximize detection effectiveness across traps.
- Surveillance types and optimization:
  - Outputs prepared for three surveillance methods: girdled trees, sticky traps, under-bark sampling.
  - Results from optimizations are deposited as three trap-type folders × nine scenarios.

## File structure and naming conventions
- Outputs organized under: \Results\[TRAP TYPE]\[XXXX]\Escape[YY]
  - TRAP TYPE: Girdled, Sticky_traps, or Under_bark_sampling.
  - XXXX: scenario-specific labeling (e.g., 3070, 5050, 7030).
  - YY: probability of EAB escape (25, 50, 75).
- Contents in each Escape[YY] folder:
  - DataForOpt.txt
  - HighRisk.txt
  - SampleEntry.txt
  - XXXXEsYY.csv (final optimized locations and detectability metrics)
- Data formats: plain text (.txt) and comma-separated values (.csv).

## Spatial and temporal coverage
- Spatial:
  - Grid: 0 to 1211 rows, 0 to 601 columns (1 km x 1 km cells).
  - 0,0 corresponds to 54500 Eastings and 9500 Northings.
- Temporal:
  - Simulations span 8 years, with annual time steps.
  - Initial ash tree density derived from data layers around 2020.

## Model development and usage
- Development:
  - Described in Alonso Chavez et al., 2024.
  - Core code components:
    - EAB_V1.cpp: Main entry point and run control.
    - EAB_Model.cpp / EABModel.h: Lifecycle, spread, and model functions.
    - EABGrid.cpp / EABGrid.h: Grid data storage and access.
  - Input data reside in the TreeDensity subdirectory; outputs primarily DataForOpt.txt.
- Usage:
  - To test new entry scenarios, edit SampleEntry.txt in the appropriate Model_Input_Files subdirectory.
  - The model and associated code are made available with a DOI (Zenodo link provided in document).

## Calibration and quality control
- Parameterization:
  - Described in Alonso Chavez et al., 2024.
- Validation and data quality:
  - Direct field validation is not feasible since EAB is not yet established in GB.
  - Input data are drawn from published sources and quality-checked through summary statistics and spatial plots.
  - Spread-rate benchmarks compared to USA data (Mercader et al., 2009) for plausibility.

## Accessibility and citations
- Data usage requires citation, with full citation available on the data catalogue page.
- Key references informing model parameters and validation include Alonso Chavez et al. (2024) and Mercader et al. (2009).