# Simulations of Emerald Ash Borer (EAB) spread in Great Britain with optimised surveillance

- A 2023 developmental study by Milne, Alonso Chavez, Brown, Parnell, and van den Bosch, funded by NERC Smarties (NE/T007729/1), modeling EAB lifecycle and spread across Great Britain to inform optimal surveillance strategies.
- Purpose: predict where surveillance technologies (e.g., girdled trees, traps) should be placed to detect EAB early and mitigate impact on ash trees in GB.
- Access note: Data usage requires citation; full citation available on the data catalogue page.

## Overview and aims

- EAB is a non-native, destructive pest threatening ash trees globally; GB-specific surveillance planning is essential.
- Model outputs are designed to identify likely initial incursions and optimal surveillance locations on a 1 km x 1 km GB grid.
- The model is written in C++ and compiled with Microsoft Visual Studio 2022; stochastic sampling uses NAG libraries (replacable if needed).

## Model and scenarios

- Structure:
  - Time steps: annual, across 8 years.
  - Spatial grid: 1 km x 1 km cells; 0 <= row <= 1211, 0 <= col <= 601.
  - Outputs track larval density and tree health per infested cell; results feed into surveillance optimization.
- Entry point initialization:
  - Maps identify most likely first incursion points informed by Forestry Commission data and firewood-use data.
  - Nine scenarios model varying certainty that entry is via known pathways (70%, 50%, 30%) and probability of escape at port vs depots (25%, 50%, 75%).
  - For each scenario, 10,000 realizations are sampled and used as model inputs (SampleEntry.txt).
- Optimization:
  - An objective function (Omega) is used to evaluate surveillance effectiveness and guide optimization (not included in this release).
  - Three surveillance types considered: girdled trees, sticky straps, under-bark sampling.
  - Results from optimization are deposited separately for each trap type and scenario.

## Data inputs

- Location and inputs directory: Model_Input_Files (to be placed in a subdirectory of TreeDensity).
- Core input files (six or seven total; one is the primary scenario tester):
  - ADBInfection_GB.txt
  - InclusionProb.txt
  - Infection_GB.txt
  - Owners_GB.txt
  - SampleEntry.txt (modifiable to test different entry locations/scenarios)
  - treeDensity_GB.txt
- Notes:
  - SampleEntry.txt is the primary file to adjust when testing alternate scenarios.
  - Other files provide supporting data (entry probabilities, ownership, density, etc.) and are described in the accompanying documentation (Table 1 of the document).

## Outputs and data structure

- DataForOpt.txt: primary output used to optimize surveillance; columns include simulation/realization number, initial incursion location, weight, ash-tree density per cell, observation location, and eight-year averages of larvae per observation cell, plus ash-tree counts accounting for EAB deaths over 8 years.
- Optimization results (XXXXEsYY.csv): final optimized surveillance configurations for each trap type under each scenario.
- Directory structure for results:
  - Results/[TRAP TYPE]/[XXXX]/Escape[YY]/
  - TRAP TYPE: Girdled, Sticky_traps, Under_bark_sampling
  - XXXX: 3070, 5050, 7030
  - YY: 25, 50, 75
- Additional files in each Escape[YY] folder:
  - DataForOpt.txt
  - HighRisk.txt
  - SampleEntry.txt
  - XXXXEsYY.csv (with trap-type and scenario-specific optimizations)
- Data formats:
  - Model inputs: plain text (.txt)
  - Model outputs: DataForOpt.txt and CSV files in the Results folder

## Model components and code

- Main code and structure:
  - EAB_V1.cpp: Main calling code (initializes and runs model)
  - EAB_Model.cpp: Describes lifecycle and spread functions
  - EABModel.h: Header for the model
  - EABGrid.cpp / EABGrid.h: Grid storage and data access
- Input/output data organization:
  - Model_Input_Files: seven input files (description in Table 1)
  - Results: outputs per trap type and scenario as described above
- Model and input formats:
  - Model code and inputs are plain text and .csv
  - Model repository and solution: available at https://doi.org/10.5281/zenodo.10610811

## Spatial and temporal coverage

- Spatial:
  - Grid: 1 km x 1 km cells
  - Extent: 0 to 1211 (rows) and 0 to 601 (columns)
  - Spatial mapping: (0,0) corresponds to 54500 Eastings and 9500 Northings
- Temporal:
  - 8-year simulation horizon
  - Annual time-step
  - Initial ash-tree density sourced from 2020 data layers

## Model development, testing and usage

- Model development and references:
  - Alonso Chavez et al., 2024 (model development and underlying equations)
  - Related data and maps: Brown et al. 2023 (Ash host map for GB)
  - Mercader et al., 2009 (USA spread rates used for quality checks)
- Calibration and parameterization:
  - Described in Alonso Chavez et al., 2024
  - Input data quality checks include summary statistics and spatial plots; comparisons to USA spread rates for context
- Quality control:
  - Direct validation is not possible in GB since EAB is not present; data drawn from published sources and subjected to basic quality checks

## Model usage notes for analysts

- How to test different entry scenarios:
  - Edit SampleEntry.txt within the TreeDensity subdirectory to specify entry locations and scenario configurations.
- Reproducibility and accessibility:
  - Model code and solution set available via Zenodo link; code can be compiled with VS 2022
  - If NAG libraries are unavailable, stochastic sampling calls can be replaced with alternative libraries
- Output usage:
  - DataForOpt.txt serves as input to an optimization routine for surveillance placement
  - XXXXEsYY.csv files provide finalized surveillance configurations per scenario and trap type

## Licensing and citation

- Data use requires citation as stated at the top of the document; for full citation details, refer to the data catalogue page.
- References:
  - Alonso Chavez et al., 2024 (Strategies for the early detection of Emerald Ash Borer in Great Britain)
  - Brown et al., 2023 (Host map of Ash trees in Great Britain)
  - Mercader et al., 2009 (EAB dispersal in new sites)