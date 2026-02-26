# Simulations of Emerald Ash Borer (EAB) spread in Great Britain with optimised surveillance

- Purpose and scope
  - Develop a spatially explicit model of Emerald Ash Borer (EAB) lifecycle and spread across Great Britain to inform well-defined, optimized surveillance strategies for early detection.
  - Output supports identifying where to place surveillance technologies (e.g., girdled trees, traps) to maximise detection probability within an 8-year horizon.

- Project and provenance
  - Developed in 2023 by a multidisciplinary team as part of the NERC-funded Smarties project NE/T007729/1.
  - Collaborating institutions include Rothamsted Research, Forest Research, University of Warwick, and UC Davis (visiting scholar).

- Model structure and implementation
  - Core model written in C++, compiled with Microsoft Visual Studio 2022; uses stochastic sampling and a dispersal kernel (NAG libraries) to simulate EAB spread.
  - Outputs central to surveillance optimization: DataForOpt.txt (inputs for optimization) and surveillance results (three trap types × nine scenarios) stored under a structured Results directory.
  - Main model components documented in several files (EAB_V1.cpp, EAB_Model.cpp, EABGrid.cpp, etc.) with input and output data in plain text (.txt) and CSV formats.
  - Access to model code and data is provided via a Zenodo archive and associated project resources.

- Inputs and scenario design
  - Entry point and risk inputs reside in a subdirectory (Model_Input_Files) with seven key files; SampleEntry.txt is the primary file to modify for testing alternative entry locations.
  - Nine scenario configurations reflect varying certainties that EAB will enter via known pathways (70%, 50%, 30%) and probabilities of escape at ports vs depots (25%, 50%, 75%), with 10,000 realizations per scenario.
  - Spatial inputs include:
    - Ash host distribution map (treeDensity_GB.txt)
    - Gridded entry location likelihoods (SampleEntry.txt)
    - Additional supporting files (e.g., ADBInfection_GB.txt, InclusionProbGB.txt, Infection_GB.txt, Owners_GB.txt)
  - Baseline data sources: Forestry Commission inputs, Brown et al. 2023 host map, and Mercader et al. 2009 for comparative spread rates.

- Outputs and optimization
  - DataForOpt.txt contains per-simulation columns: simulation/realization, initial incursion location, weight, ash tree numbers, observation coordinates, and eight-year average larvae per tree.
  - Optimization objective Omega integrates detection probabilities across traps and years to identify surveillance strategies.
  - Optimized surveillance results are captured in per-scenario CSV files (XXXXEsYY.csv) that enumerate:
    - Number of sampling locations (e.g., 50, 100, 200, 400, 500)
    - Probability of detecting infestation
    - Mapped trap locations (encoded; convert to coordinates via a provided formula)
  - Surveillance types considered: girdled trees, sticky traps, and under-bark sampling.

- Spatial and temporal coverage
  - Spatial grid: 1 km x 1 km cells, indexed rows 0–1211 and columns 0–601; grid origin at 54500 Eastings and 9500 Northings.
  - Temporal horizon: 8 years with annual time steps.
  - Initial ash host density drawn from 2020 data layers; scenario-specific inputs determine entry points and early incursion dynamics.

- Model development, usage, and QA
  - Model development and parameterization described in Alonso Chavez et al., 2024; further context from Brown et al. 2023 and Mercader et al. 2009.
  - Calibration not performed via real GB EAB presence (validation not feasible in GB); parameterization derived from published data and cross-validation against US spread data where applicable.
  - Quality control measures include consistency checks on summary statistics and spatial plots; model parameterization and references documented for transparency.

- Data management, governance, and accessibility
  - Input data and outputs are organized with explicit directory structures and naming conventions to support reproducibility.
  - Users can modify SampleEntry.txt to explore alternative incursion scenarios; outputs are designed to be used by decision-makers to compare surveillance configurations.
  - Data sharing considerations noted (e.g., dataset metadata and provenance), with references to primary sources for inputs and model validation.

- References
  - Alonso Chavez et al. (2024) on strategies for early detection of Emerald Ash Borer in Great Britain.
  - Brown et al. (2023) Host map of Ash trees in Great Britain.
  - Mercader et al. (2009) Emerald Ash Borer dispersal dynamics in newly colonized sites.