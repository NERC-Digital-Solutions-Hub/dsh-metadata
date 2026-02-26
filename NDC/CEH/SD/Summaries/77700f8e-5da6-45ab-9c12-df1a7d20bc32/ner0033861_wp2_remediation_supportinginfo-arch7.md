# Supporting Information : Hydrogeochemical data for groundwater remediation systems in Bihar, India, 2018-2022

## Overview
- Provides hydrogeochemical data for 31 groundwater remediation systems in Bihar (Middle Gangetic Plain), with paired inlet (untreated) and outlet (finished) water samples.
- Includes remediation technology type, setting, and inlet water chemistry (selected major elements and Si).

## Study area and sampling strategy
- Study area: Bihar, India; districts include Patna (18), Buxar (3), Gaya (2), Katihar (2), and one each in Aurangabad, East Champaran, Nawada, Munger, Vaishali; one nearby system from Ballia District, Uttar Pradesh included due to proximity.
- Sampling approach: opportunistic sampling within a larger stratified random groundwater campaign (~300 tubewells). Samples collected under “spot check” conditions with no prior knowledge of sampling. More samples in Patna due to higher groundwater-sampling density and urban prevalence of household water treatment systems.

## Remediation system sampling & characterization
- For each system: collected subsamples of (i) inlet groundwater fed to the system and (ii) outlet water produced by the system. In some cases, packaged water from local suppliers was also sampled.
- Inlet samples obtained from handpumps or household taps connected to the untreated groundwater; outlet samples from system outlets or nearest accessible point.
- Sampling uses rinsed plastic containers; samples filtered (0.45 μm) for lab analysis and, for cations/trace metals, acidified (2% HNO3) after transport to the lab.

## Chemical analysis (laboratory)
- Analysis performed at Manchester Analytical Geochemistry Unit (MAGU).
- Methods:
  - ICP-MS for As, U, Zn.
  - ICP-AES for Fe, P, Ca, Mg, Mn, Na, K, Si.
- Additional method details and QA/QC information are provided in the associated publications.

## Nature and Units of Recorded Values
- Data stored in columns with headers detailing units and calculation methods.
- Key data items include:
  - System_ID: identification number of remediation system.
  - As_Retention_%: calculated arsenic retention = (1 − (C_outlet, As / C_inlet, As)) × 100.
  - Tech_Type_Code: 1 = reverse osmosis or other membrane system; 2 = non-membrane system.
  - Setting_User_Type_Code: 3 = household; 4 = non-household.
  - Inlet water concentrations (Fe, P, As, Ca, Mg, Na, Si) in the specified units (ppm or ppb as appropriate).
- Data labels indicate inlet and outlet concentrations where available; values below detection were set to 0.1 ppb for As and 0.001 for Fe and P.

## Details of data structure
- One spreadsheet containing data for 31 remediation systems.
- 11 columns cover: System_ID, As_Retention_%, Tech_Type_Code, Setting_User_Type_Code, and inlet concentrations for Fe, P, As, Ca, Mg, Na, Si.

## Quality control
- Quality control procedures described in Richards et al. (2022) accompanying the dataset.

## Data availability and usage (GIS relevance)
- Dataset enables spatial analysis of remediation system distribution, technology types, and performance (As retention) across Bihar.
- Can be integrated with GIS for mapping remediation coverage, comparing technology effectiveness by district or setting, and informing remediation planning or policy discussions.
- Useful for cross-referencing with broader groundwater datasets and public health data to assess remediation outcomes in different urban/rural and household vs. non-household contexts.

## References
- Richards, L.A.; Kumar, A.; Shankar, P.; Gaurav, A.; Ghosh, A.; Polya, D.A. (2020) Distribution and Geochemical Controls of Arsenic and Uranium in Groundwater-Derived Drinking Water in Bihar, India. Int. J. Environ. Res. Public Health 17, 2500. https://doi.org/10.3390/ijerph17072500
- Richards, L.A.; Parashar, N.; Kumari, R.; Kumar, A.; Mondal, D.; Ghosh, A.; Polya, D.A. (2022) Household and community systems for groundwater remediation in Bihar, India: Arsenic and inorganic contaminant removal, controls and implications for remediation selection, Science of the Total Environment, 830, 154580. https://doi.org/10.1016/j.scitotenv.2022.154580