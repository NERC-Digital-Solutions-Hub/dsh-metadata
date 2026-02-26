# Simulations of Emerald Ash Borer (EAB) spread in Great Britain with optimised surveillance

- Purpose and scope
  - Develop a GB-wide model of Emerald Ash Borer (EAB) lifecycle and spread to inform surveillance strategies.
  - Output maps and data to identify optimal locations for surveillance technologies (e.g., girdled trees, traps).
  - Model is implemented in C++ (compiled with Microsoft Visual Studio 2022) and uses NAG libraries for stochastic sampling and kernel integration.
  - Outputs enable optimization of surveillance under multiple entry-pathway scenarios.

- Model structure and scenarios
  - Time frame: annual time steps over 8 years.
  - Realizations: up to 10,000 realizations per scenario to capture incursion uncertainty.
  - Entry scenarios: 9 combinations of:
    - Pathway certainty for known entry points through wood imports (70%, 50%, 30%).
    - Probability of EAB escaping at port vs onwards depots (25%, 50%, 75%).
  - Output keys:
    - Maps identifying likely first incursion points on a 1 km x 1 km grid.
    - Data used to optimize surveillance across three trap types: girdled trees, sticky traps, under-bark sampling.

- Data inputs and GIS considerations
  - Input data managed under the TreeDensity workspace in Model_Input_Files.
  - Editable input: SampleEntry.txt (defines likely entry locations); other inputs define scenario parameters.
  - Core data sources include:
    - Forestry Commission-derived entry points and firewood-use data (for entry likelihoods).
    - Tree host density maps (treeDensity_GB.txt).
    - Ownership and other contextual maps (Owners_GB.txt, InclusionProbGB.txt, ADBInfection_GB.txt; some are placeholders or not used in this version).
  - Model outputs are structured to support GIS-based analysis and further optimization.

- Outputs and file organization
  - DataForOpt.txt: main simulation outputs per realization, including:
    - Simulation/realization number; initial incursion coordinates; weight; tree counts; observation coordinates; eight yearly larval averages; healthy trees after 8 years.
    - Used by an optimization algorithm (not included) for surveillance planning.
  - Results folder structure: \Results\[TRAP TYPE]\[XXXX]\Escape[YY] where:
    - TRAP TYPE ∈ {Girdled, Sticky_traps, Under_bark_sampling}
    - XXXX ∈ {3070, 5050, 7030} (scenario label)
    - YY ∈ {25, 50, 75} (escape pathway probability parameter)
  - Within each EscapeYY folder:
    - DataForOpt.txt
    - HighRisk.txt
    - SampleEntry.txt
    - XXXXEsYY.csv: final optimized surveillance results, including:
      - Number of sample locations (50, 100, 200, 400, 500)
      - Probability to detect infestation
      - Encoded trap locations (convertible to row/column via specified formulas)

- Spatial and temporal coverage
  - Spatial grid: 1 km x 1 km cells; grid indices Rows 0–1211, Columns 0–601.
  - Coordinate mapping: 0,0 corresponds to 54500 Eastings and 9500 Northings.
  - Temporal coverage: 8-year simulation horizon with annual resolution.
  - Initial ash-host density derived from 2020 data layers.

- Model development and usage
  - Core code components:
    - EAB_V1.cpp (main driver)
    - EAB_Model.cpp / EABModel.h (lifecycle and spread logic)
    - EABGrid.cpp / EABGrid.h (grid storage and access)
  - Input/Output organization:
    - Model_Input_Files in TreeDensity subdirectory
    - Outputs primarily DataForOpt.txt and per-scenario Results folders
  - Calibration and validation:
    - Parameterization described in Alonso Chavez et al. (2024).
    - Quality control acknowledges that GB validation is infeasible due to absence of EAB; input data are quality-checked against published sources and USA spread data for contextual alignment.

- Practical GIS implications
  - Facilitates GIS-based exploration of incursion risk and surveillance effectiveness across GB.
  - Enables comparison of surveillance strategies under different entry-pathway uncertainties.
  - Easy to update entry locations via SampleEntry.txt to test new scenarios and re-run analyses.
  - Outputs (DataForOpt.txt and XXXXEsYY.csv) can be imported into GIS workflows to visualize surveillance performance and inform decision-making.

- References
  - Alonso Chavez et al., 2024. Strategies for the early detection of Emerald Ash Borer (Agrilus planipennis) in Great Britain: targeted surveillance and stakeholder perspectives. Submitted to Applied Ecology.
  - Brown et al., 2023. Host map of Ash trees in Great Britain. 
  - Mercader et al., 2009. Dispersal of the emerald ash borer in newly-colonized sites. Agricultural and Forest Entomology.