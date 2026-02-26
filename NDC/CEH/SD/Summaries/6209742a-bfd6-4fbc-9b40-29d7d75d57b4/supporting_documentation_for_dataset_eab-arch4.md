# Simulations of Emerald Ash Borer (EAB) spread in Great Britain with optimised surveillance

## Overview
- Developed in 2023 by a team from Rothamsted Research, Forest Research, University of Warwick, and UC Davis as part of the Smarties project (NE/T007729/1).
- Purpose: model Emerald Ash Borer (EAB) lifecycle and spread across Great Britain to inform optimal surveillance strategies for early detection (e.g., girdled trees, traps).
- Implementation: C++ model compiled with Microsoft Visual Studio 2022; uses stochastic sampling and a dispersal kernel via NAG libraries (replacement possible if license unavailable).
- Outputs support optimization of surveillance locations and methods across multiple scenarios of entry pathways.

## Data and Inputs
- Input data reside in Model_Input_Files, with Testable scenarios configured via SampleEntry.txt (other seven files provide supporting data).
- Key input files (located under a TreeDensity subdirectory): ADBInfection_GB.txt, InclusionProb.txt, Infection_GB.txt, Owners_GB.txt, SampleEntry.txt, treeDensity_GB.txt. SampleEntry.txt is the primary file to modify to test different entry locations; others provide fixed data.
- Scenario design: nine scenarios varying the certainty of entry through known pathways (70%, 50%, 30%), with different probabilities of escape from ports vs depots; for each scenario, 10,000 realizations are sampled.
- Outputs:
  - DataForOpt.txt: simulation outputs (e.g., initial incursion point, larval density, tree health) used in a surveillance optimization routine (not included in this document).
  - Results per scenario/trap type: XXXXEsYY.csv files containing optimized surveillance results (locations and detection probabilities).
  - Directory structure: Results\[TRAP TYPE]\[XXXX]\Escape[YY], where TRAP TYPE is Girdled, Sticky_traps or Under_bark_sampling, XXXX corresponds to pathway certainty (e.g., 3070, 5050, 7030), and YY to escape probability (25, 50, 75).
- Data formats: inputs are plain text (.txt) and outputs include .txt and .csv files.

## Model Structure and Code
- Core model: EAB lifecycle and spread simulated on a 1 km x 1 km grid covering Great Britain; annual time steps over 8 years.
- Main code files:
  - EAB_V1.cpp (main calling code)
  - EAB_Model.cpp / EABModel.h (model lifecycle and spread)
  - EABGrid.cpp / EABGrid.h (grid data storage)
- Input and output data formats: .txt and .csv; model outputs DataForOpt.txt by default.
- Code accessibility: model and related inputs are provided with a DOI link; code can be compiled with alternative tools if desired.
- Parameterization and references: parameterization described in Alonso Chavez et al., 2024.

## Spatial and Temporal Coverage
- Spatial: GB-wide grid with 0 to 1211 rows and 0 to 601 columns; cells are 1 km x 1 km.
- Temporal: 8-year simulations with annual time steps; starting ash tree density informed by 2020 data layers.
- Spatial resolution and mapping: grid indexing and coordinate references provided; outputs include spatially explicit incidence and surveillance data.

## Model Development, Calibration, and Quality Control
- Model development described in Alonso Chavez et al., 2024; main references include:
  - Alonso Chavez et al., 2024 (Strategies for the early detection of Emerald Ash Borer in Great Britain)
  - Brown et al., 2023 (Host map of Ash trees in Great Britain)
  - Mercader et al., 2009 (EAB dispersal dynamics)
- Calibration and validation:
  - Parameterization documented in referenced works.
  - Quality control: direct validation is limited since EAB is not currently present in GB; inputs derived from published data and cross-checked with summary statistics and spatial data plots; spread rates compared with US data as a consistency check.

## Using the Model and Outputs
- Customization:
  - To test different incursion scenarios, edit SampleEntry.txt; other input files can remain fixed or adjusted per scenario.
- Running and outputs:
  - Compile and run via Visual Studio 2022; outputs include DataForOpt.txt (for surveillance optimization) and per-scenario trap-type result folders containing XXXXEsYY.csv files with optimized detection locations and probabilities.
  - DataForOpt.txt columns include simulation/realization number, initial incursion coordinates, weights, larval counts, observed cell coordinates, and eight-year averages/deaths.
  -XXXXEsYY.csv files describe number of sample locations, detection probability, and encoded location mappings for translating results to grid coordinates.
- Data governance:
  - Data usage requires citation per the data catalogue (Get data); dataset and model outputs are hosted with a DOI for reproducibility.
  - Documentation notes the presence of some dummy placeholder inputs in earlier files and emphasizes reliance on published data sources for quality control.

## Data Access and Compliance
- Access: data must be cited when used; full citation details available on the data catalogue page.
- Reproducibility: model code and input files are organized with explicit directory structures (TreeDensity, Model_Input_Files, Results); a Zenodo DOI provides access to the model and code.

## References
- Alonso Chavez, V., Brown, N., Milne, A. E., Parnell, S., et al. (2024). Strategies for the early detection of Emerald Ash Borer (Agrilus planipennis) in Great Britain: targeted surveillance and stakeholder perspectives. Submitted to Applied Ecology.
- Brown, N., Alonso Chavez, V., Milne, A. E., Parnell, S. (2023). Host map of Ash trees in Great Britain. https://doi.org/10.23637/rothamsted.98y37
- Mercader, R. J., Siegert, N. W., Liebhold, A. M., & McCullough, D. G. (2009). Dispersal of the emerald ash borer in newly-colonized sites. Agricultural and Forest Entomology, 11(4), 421-424.