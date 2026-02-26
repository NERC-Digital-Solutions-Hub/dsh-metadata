# Supporting Information : Hydrogeochemical data for groundwater remediation systems in Bihar, India, 2018-2022

## Study area & sampling strategy
- Samples collected in 2019 from remediation systems (n = 31) in Bihar, Middle Gangetic Plain, India.
- Districts involved: Patna (n = 18); Buxar (n = 3); Gaya and Katihar (n = 2 each); Aurangabad, East Champaran, Nawada, Munger and Vaishali (n = 1 each). One system from Ballia District, Uttar Pradesh included due to proximity and co-existence in the Mid Ganga Plain.
- Sampling framed within a larger stratified random groundwater campaign (~300 tubewells across Bihar); identified mitigation units reflect the frequency and types encountered.
- Sampling approach: spot checks at locations where remediation systems were present; owners/overseers often unaware sampling would occur; in some cases, known systems were sampled.
- “Remediation” encompasses various approaches to mitigate groundwater contaminants, including point-of-use (POU) water treatment and switching to less-contaminated sources.

## Remediation system sampling & characterization
- For each remediation system, collect paired samples: (i) untreated groundwater feed/inlet and (ii) finished product/outlet water.
- Some packaged water samples from local suppliers were included; inlet groundwater for these not always available.
- Inlet samples sourced from handpumps or household taps connected to the groundwater source; outlet samples from system outlets or nearest access point (e.g., storage vessel).
- Sample handling: plastic beakers, thoroughly rinsed between samples; filtration (0.45 μm) upon collection; acidification with 2% trace-grade HNO3 after transport to the laboratory.
- Further sampling details provided in Richards et al. (2020).

## Chemical analysis (laboratory)
- Analysis conducted at the Manchester Analytical Geochemistry Unit (MAGU).
- Major and trace elements analyzed via:
  - ICP-MS (Agilent 7500cx) for As, U, Zn.
  - ICP-AES (Perkin-Elmer Optima 5300) for Fe, P, Ca, Mg, Mn, Na, K, Si.
- Quality assurance/quality control details described in Richards et al. (2020).

## Nature and Units of Recorded Values
- Datafile columns include: System_ID (ID of remediation system); As_Retention_% (calculated retention of arsenic); Tech_Type_Code (remediation technology type); Setting_User_Type_Code (setting/user type); inlet concentrations for Fe, P, As, Ca, Mg, Na, Si; and related units.
- Arsenic retention calculated as: (1 - (C_outlet,As / C_inlet,As)) × 100; where C_outlet,As is outlet concentration, C_inlet,As is inlet concentration.
- Tech_Type_Code: 1 = reverse osmosis or other membrane systems; 2 = non-membrane systems.
- Setting_User_Type_Code: 3 = household; 4 = non-household.
- Inlet concentration fields provided in ppm or ppb as appropriate; values include Fe, P, As, Ca, Mg, Na, Si (units specified per parameter).
- Non-detects handled as: As = 0.1 ppb; Fe and P = 0.001 (for reporting purposes).
- Dataset pertains to remediation samples only where paired inlet–outlet data are available.
- Data structure includes 11 columns.

## Details of data structure
- Spreadsheet contains data for 31 remediation systems in Bihar, India.
- Includes: As retention, technology category, setting category, and water inlet composition (selected parameters Fe, P, As, Ca, Mg, Na, Ni).
- 11 data columns in total.

## Quality control
- Quality control procedures and details are described in Richards et al. (2022).

## Primary data contact
- Dr Laura L. Richards (laura.richards@manchester.ac.uk) or Prof. David A. Polya (david.polya@manchester.ac.uk)

## References
- Richards, L.A.; Kumar, A.; Shankar, P.; Gaurav, A.; Ghosh, A.; Polya, D.A. (2020) Distribution and Geochemical Controls of Arsenic and Uranium in Groundwater-Derived Drinking Water in Bihar, India. Int. J. Environ. Res. Public Health 17, 2500. https://doi.org/10.3390/ijerph17072500
- Richards, L.A.; Parashar, N.; Kumari, R.; Kumar, A.; Mondal, D.; Ghosh, A.; Polya, D.A. (2022) Household and community systems for groundwater remediation in Bihar, India: Arsenic and inorganic contaminant removal, controls and implications for remediation selection, Science of the Total Environment, 830, 154580. https://doi.org/10.1016/j.scitotenv.2022.154580