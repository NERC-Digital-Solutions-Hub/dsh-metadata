# Supporting Information : Hydrogeochemical data for groundwater remediation systems in Bihar, India, 2018-2022

- Primary Data Contact: Dr Laura Richards (laura.richards@manchester.ac.uk) or Prof. David Polya (david.polya@manchester.ac.uk)

## Study area & sampling strategy
- Water samples collected in 2019 from 31 remediation systems in Bihar's Middle Gangetic Plain across multiple districts (Patna n=18; Buxar n=3; Gaya and Katihar n=2 each; Aurangabad, East Champaran, Nawada, Munger, Vaishali n=1 each).
- One remediation system in Ballia District (Uttar Pradesh) included due to proximity and co-existence in the Mid Ganga Plain.
- Sampling framed within a larger stratified random groundwater campaign (~300 tubewells across Bihar); remediation units identified during spot checks when access was granted.
- Patna district had a higher proportion of samples due to urban density and prevalence of household water treatment systems.
- “Remediation” encompasses various mitigation approaches, including point-of-use water treatment and potential switching to less-contaminated sources.

## Remediation system sampling & characterization
- For each system, collect paired samples: (i) inlet (untreated groundwater) and (ii) outlet (finished water). In some cases, sampled packaged water from local suppliers (inlet not available for these).
- Inlet samples obtained from handpumps or household taps connected to the untreated source; outlet samples from system outlets or nearest access point.
- Samples stored in rinsed plastic beakers; filtration (0.45 μm) upon collection; inlet/outlet water samples stored in glass bottles.
- For cation and trace metal analyses, samples were acidified with 2% trace-grade HNO3 after transport to laboratory.

## Chemical analysis (laboratory)
- Major and trace elements analyzed at Manchester Analytical Geochemistry Unit (MAGU).
- Methods:
  - ICP-MS (Agilent 7500cx) for As, U, Zn.
  - ICP-AES (Perkin-Elmer Optima 5300) for Fe, P, Ca, Mg, Mn, Na, Si.
- Quality assurance/quality control details provided in Richards et al., 2020.

## Nature and Units of recorded values
- Data file includes column headers with descriptive details; key variables include:
  - System_ID: ID number of remediation system.
  - As_Retention_%: Calculated arsenic retention = (1 - (C_outlet,As / C_inlet,As)) × 100.
  - Tech_Type_Code: 1 = reverse osmosis or other membrane system; 2 = non-membrane system.
  - Setting_User_Type_Code: 3 = household; 4 = non-household.
  - Inlet concentrations for Fe (ppm), P (ppm), As (ppb), Ca (ppm), Mg (ppm), Na (ppm), Si (ppm).
- Data structure summary: 31 remediation systems, 11 data columns, includes As retention, technology and setting categories, and inlet water composition.
- Handling of below-detection values: As < detection treated as 0.1 ppb; Fe and P < detection treated as 0.001 (units depend on parameter).

## Data structure and data availability
- The spreadsheet contains data for 31 remediation systems, including:
  - As retention, technology category, setting category, and inlet water composition for selected parameters (Fe, P, As, Ca, Mg, Na, Ni).
- 11 columns of data per remediation system.

## Quality control
- Detailed QA/QC procedures described in Richards et al. 2022.

## References
- Richards, L.A.; Kumar, A.; Shankar, P.; et al. (2020) Distribution and Geochemical Controls of Arsenic and Uranium in Groundwater-Derived Drinking Water in Bihar, India. International Journal of Environmental Research and Public Health, 17, 2500. https://doi.org/10.3390/ijerph17072500
- Richards, L.A.; Parashar, N.; Kumari, R.; et al. (2022) Household and community systems for groundwater remediation in Bihar, India: Arsenic and inorganic contaminant removal, controls and implications for remediation selection. Science of the Total Environment, 830, 154580. https://doi.org/10.1016/j.scitotenv.2022.154580