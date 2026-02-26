# Simulations of Emerald Ash Borer (EAB) spread in Great Britain with optimised surveillance

- Purpose and scope: A 2023-developed model of Emerald Ash Borer lifecycle and spread across Great Britain to support surveillance planning. Outputs inform where to locate surveillance technologies (girdled trees, traps, under-bark sampling) and are used to optimise detection strategies.
- Origin and accessibility: Developed by Milne, Chavez, Brown, Parnell, and van den Bosch as part of the NERC Smarties project. Model is in C++ (VS2022) with optional NAG libraries. Data usage requires citation per the dataset’s catalogue page.

## Data governance and provenance

-Authors and affiliations: British institutions (Rothamsted Research, Forest Research, University of Warwick) with visiting scholar from UC Davis.
-Data citation: “As a condition of using these data you must cite it.” Full citation available on the data catalogue page.
-Data structure and traceability: Clear separation between inputs, model code, and outputs, with descriptive file naming and directory structure to enable reproducibility.
-Version and sources: Parameterisation described in Alonso Chavez et al. (2024); inputs derived from published sources and cross-checked where possible.

## Input data

- Location of inputs: Model_Input_Files directory; main code resides in a subdirectory from which the model is run.
- Seven input files (editable one): ADBInfection_GB.txt, InclusionProb.txt, Infection_GB.txt, Owners_GB.txt, SampleEntry.txt, treeDensity_GB.txt (plus related data described in the accompanying tables).
- Modifiable parameter: SampleEntry.txt is the primary file to alter when testing different scenarios; other files provide fixed reference data.
- Model scope for inputs: Inputs define entry points, infection probabilities, ownership, and host density to initialize simulations.

## Output data

- Primary outputs: DataForOpt.txt (used for surveillance optimization), HighRisk.txt, SampleEntry.txt, and scenario-specific XXXXEsYY.csv files containing optimization results.
- DataForOpt.txt columns (example): Simulation/realisation number; Initial incursion Grid Row/Column; Weight; Ash tree number per cell; Observation Grid Row/Column; Average larvae per tree over 8 years (8 columns); Ash trees accounting for death from EAB over 8 years (8 columns).
- Optimization objective: Omega, a function that integrates detectability across traps and years.
- Output usage: Data used to optimise surveillance for early detection of EAB; results per trap type and scenario are stored under the Results folder structure.

## File structure and naming conventions

- Model input and code organization:
  - Model_Input_Files: seven input data files described above.
  - TreeDensity subdirectory: used for input data collection/generation; SampleEntry.txt editable to test scenarios.
- Outputs directory structure:
  - Results\[TRAP TYPE]\[XXXX]\Escape[YY] where TRAP TYPE is Girdled, Sticky_traps, or Under_bark_sampling; XXXX corresponds to scenario (e.g., 3070, 5050, 7030) and YY to probability/escape combinations (25, 50, 75).
  - Inside each Escape[YY] folder: DataForOpt.txt; HighRisk.txt; SampleEntry.txt; XXXXEsYY.csv (final optimized results for locations and detection probabilities).

## Model details

- Model purpose and scope: Simulates EAB lifecycle and spread with annual time steps over 8 years; identifies likely first incursion points and supports optimization of surveillance strategies.
- Implementation: Core model in C++ with files including EAB_V1.cpp (main), EAB_Model.cpp (life cycle/spread), EABGrid.cpp (grid data), and their headers. The code and inputs are available for compilation with various toolchains (VS2022 recommended). The model can be recompiled with alternate libraries if needed.
- Inputs/Outputs organization: Input files are in Model_Input_Files; outputs in DataForOpt and Results folders as described above.

## Spatial and temporal coverage

- Spatial grid: 1 km x 1 km cells; grid indexed Rows 0–1211 and Columns 0–601; 0,0 maps to 54500 Eastings and 9500 Northings.
- Temporal scope: 8-year simulations with annual time steps; baseline ash density derived from 2020 data layers.

## Model development, calibration and quality control

- Model development: Documented in Alonso Chavez et al., 2024; main code components listed (EAB_V1.cpp, EAB_Model.cpp, EABGrid.cpp, and headers).
- Calibration: Parameterisation described in Alonso et al. (2024); specific calibration steps and values referenced in the accompanying text.
- Data quality and validation: Direct ecological validation is not feasible since EAB is not currently present in GB; input data are from published sources and quality-checked via summary statistics and spatial plots. Spread rates compared to USA data (Mercader et al., 2009) as a validation reference.

## Reproducibility, access and usage notes

- Reproducibility: Scenario testing is enabled by editing SampleEntry.txt to alter entry locations; model code and input/output structure support replication of simulations and optimization.
- Software requirements: C++ compilation (Visual Studio 2022 suggested); optional NAG libraries used for certain computations.
- Data access and licensing: Data usage requires citation per the catalogue; data are shared with structured inputs/outputs to enable auditing and reuse.

## References

- Alonso Chavez, V., Brown, N., Milne, A. E., Parnell, S., et al. 2024. Strategies for the early detection of Emerald Ash Borer (Agrilus planipennis) in Great Britain: targeted surveillance and stakeholder perspectives. Submitted to Applied Ecology.
- Brown, N., Alonso Chavez, V., Milne, A. E., Parnell, S. 2023. Host map of Ash trees in Great Britain.
- Mercader, R. J., Siegert, N. W., Liebhold, A. M., & McCullough, D. G. 2009. Dispersal of the emerald ash borer in newly-colonized sites. Agricultural and Forest Entomology.