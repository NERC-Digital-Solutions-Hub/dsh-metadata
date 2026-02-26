# Simulations of Emerald Ash Borer (EAB) spread in Great Britain with optimised surveillance

## Overview
- Purpose: Develop a model of Emerald Ash Borer (EAB) lifecycle and spread across Great Britain to inform optimal surveillance placement (e.g., girdled trees, traps).
- Implementation: Model written in C++, compiled with Microsoft Visual Studio 2022; stochastic sampling and dispersal kernel via NAG libraries (replaceable if no NAG license).
- Output intent: Generate maps of likely first incursion points on a 1 km × 1 km grid to guide surveillance, and provide data to optimise trap placement and detection strategies.
- Time horizon and scenarios: Annual time steps over 8 years; up to 10,000 realizations of entry points; 9 scenarios varying certainty of entry pathways (70%, 50%, 30%) and escape probability (25%, 50%, 75%).
- Data products: Model outputs used to optimise surveillance; results available for three trap types and nine scenario combinations.

## Purpose and end use
- Predicts where surveillance technologies should be located to detect EAB early.
- Outputs can be used to inform surveillance design choices and stakeholder discussions.

## Model inputs
- Location of inputs: Model_Input_Files directory; main code expects files in a subdirectory relative to the main code (..\TreeDensity).
- Editable input for scenario testing: SampleEntry.txt (describes tested entry locations). Other six input files are described in Table 1 (not all are intended to be edited for quick scenario testing).
- Input files (seven total) include data on infection, entry probabilities, ownership, and tree density (e.g., ADBInfection_GB.txt, InclusionProbGB.txt, Infection_GB.txt, Owners_GB.txt, SampleEntry.txt, treeDensity_GB.txt).

## Output data
- Primary model output: DataForOpt.txt, containing per-simulation results such as:
  - Simulation/realisation number
  - Initial incursion grid row and column
  - Weight
  - Ash tree number per cell
  - Observation grid row and column
  - Eight annual values of average larvae per tree in observation cells
  - Eight annual values of healthy ash trees accounting for EAB mortality
- Objective function: Omega, used by an external optimisation routine (not included) to evaluate surveillance effectiveness.
- Additional outputs per scenario: In the Results folder, for each trap type and scenario, there are:
  - DataForOpt.txt
  - HighRisk.txt
  - SampleEntry.txt
  - XXXXEsYY.csv (final optimised values and trap locations for that scenario and trap type)

## Model structure and data details
- Main model code and components:
  - EAB_V1.cpp (main calling code)
  - EAB_Model.cpp (lifecycle and spread)
  - EABModel.h, EABGrid.cpp, EABGrid.h (grid data storage and access)
- Input/output organization:
  - Model_Input_Files: seven input files (with SampleEntry.txt being the primary editable file for scenario testing)
  - Model output: Results/[TRAP TYPE]/[XXXX]/Escape[YY] containing DataForOpt.txt, HighRisk.txt, SampleEntry.txt, XXXXEsYY.csv
- File formats: Plain text (.txt) for inputs and outputs; some data also available as .csv

## Spatial coverage
- Grid specification: 1 km × 1 km cells
- Grid indexing: Rows 0–1211, Columns 0–601
- Spatial reference: 0,0 relates to 54500 Eastings and 9500 Northings

## Temporal coverage
- Time span: Simulations over 8 years
- Baseline year: Starting ash density informed by 2020 data layers

## Temporal resolution
- Annual time steps

## Model development and usage
- Governing references: Alonso Chavez et al., 2024 (model development and parameterisation)
- Core files (for use or modification):
  - EAB_V1.cpp; EAB_Model.cpp; EABModel.h; EABGrid.cpp; EABGrid.h
- Data and outputs are organized under TreeDensity subdirectory; DataForOpt.txt is the primary output for surveillance optimisation.

## Input data collection/generation/transformation
- Entry point scenarios: SampleEntry.txt can be edited to test different entry locations and scenarios
- Other input files provide the base data layers (infection, entry probabilities, ownership, density) and are described in detail within the documentation

## Calibration and validation
- Calibration: Parameterisation described in Alonso Chavez et al. (2024)
- Quality control: Direct validation is not feasible since EAB is not yet present in GB
  - Input data derived from published sources
  - Validation via summary statistics, spatial data plots, and comparison of modeled spread rates to USA data (Mercader et al., 2009)

## References
- Alonso Chavez, V. et al. 2024. Strategies for the early detection of Emerald Ash Borer (Agrilus planipennis) in Great Britain: targeted surveillance and stakeholder perspectives. Submitted to Applied Ecology.
- Brown, N. et al. 2023. Host map of Ash trees in Great Britain. https://doi.org/10.23637/rothamsted.98y37
- Mercader, R. J. et al. 2009. Dispersal of the emerald ash borer in newly-colonized sites. Agricultural and Forest Entomology.