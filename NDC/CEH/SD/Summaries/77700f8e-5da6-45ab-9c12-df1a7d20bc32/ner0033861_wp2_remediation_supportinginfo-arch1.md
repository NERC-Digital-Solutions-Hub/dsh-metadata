# Supporting Information : Hydrogeochemical data for groundwater remediation systems in Bihar, India, 2018-2022

## Overview
- Dataset contains hydrogeochemical data for 31 remediation systems in Bihar, India (Middle Gangetic Plain) collected in 2019.
- Includes inlet (untreated groundwater) and outlet (remediated water) samples where paired data are available, focusing on major and trace elements with a particular emphasis on arsenic retention.
- Some samples also include packaged water; inlet data for packaged water may be unavailable.
- The sampling is part of a larger stratified random groundwater campaign (~300 tubewells across Bihar) and reflects typical operating conditions during spot-check sampling.

## Study area and sampling strategy
- Remediation systems sampled across districts in Bihar: Patna (n=18), Buxar (n=3), Gaya (n=2), Katihar (n=2), and Aurangabad, East Champaran, Nawada, Munger, Vaishali (n=1 each); one additional system from Ballia District, Uttar Pradesh included due to proximity and co-existence.
- Sampling was opportunistic within the larger random groundwater study; access was granted by system owners, and sampling occurred under typical operating conditions without prior notification.
- The term "remediation" encompasses multiple approaches to reduce groundwater contaminants, including point-of-use water treatment and switching to less-contaminated sources.

## Remediation system sampling & characterization
- For each identified remediation system, collected:
  - Subsamples of inlet water (untreated groundwater) and outlet water (finished product).
  - In some cases, additional packaged water samples from local suppliers were collected (inlet not always available for packaged water).
- Inlet samples collected directly from handpumps or household taps connected to the untreated source; outlet samples from system outlets or nearest access point (e.g., storage vessel outlet).
- Samples stored in plastic Beakers; filtration (0.45 μm) prior to analysis; cation/trace metal samples acidified (2% HNO3) after transport to the lab.
- Sampling and handling followed published methods from Richards et al. (2020).

## Chemical analysis (laboratory)
- Analyses conducted at Manchester Analytical Geochemistry Unit (MAGU).
- Major and trace elements measured by:
  - ICP-MS (Agilent 7500cx) for arsenic (As), uranium (U), zinc (Zn).
  - ICP-AES (Perkin-Elmer Optima 5300) for iron (Fe), phosphorus (P), calcium (Ca), magnesium (Mg), manganese (Mn), sodium (Na), potassium (K), silicon (Si).
- Quality assurance/quality control procedures summarized in Richards et al. (2020) and details available in related publications.

## Nature and units of recorded values
- Data file includes columns with: System_ID, As_Retention_%, Tech_Type_Code, Setting_User_Type_Code, and inlet concentrations for Fe, P, As, Ca, Mg, Na, Si.
- As_Retention_% is calculated as: (1 - (C_outlet,As / C_inlet,As)) × 100.
- Tech_Type_Code: 1 = reverse osmosis or other membrane system; 2 = non-RO or other membrane system.
- Setting_User_Type_Code: 3 = household; 4 = non-household.
- Inlet concentration data are provided in units specified in the column headers (e.g., Fe_inlet in ppm, As_inlet in ppb, etc.).
- Non-detects/below-detection values are entered as 0.1 ppb for As and 0.001 for Fe and P.

## Data structure
- Spreadsheet contains data for 31 remediation systems, with 11 columns capturing system identifiers, retention, technology type, setting type, and inlet water composition (Fe, P, As, Ca, Mg, Na, Si).
- Inlet/outlet paired data are included where available.

## Quality control
- Quality control procedures are described in Richards et al. (2022); additional methodological details are provided in Richards et al. (2020).

## Practical uses for analysts
- Assess performance of different remediation technologies (Tech_Type_Code 1 vs 2) in reducing arsenic and other contaminants.
- Compare arsenic retention across setting types (household vs non-household) to inform remediation selection and deployment strategies.
- Explore relationships between inlet water chemistry (Fe, P, Ca, Mg, Na, Si) and removal efficiency (As_Retention%).
- Leverage paired inlet-outlet data to model treatment effectiveness under typical operating conditions and to identify factors influencing performance.
- Data supports cross-referencing with broader studies on arsenic and uranium in Bihar groundwater and on remediation controls and implications for remediation choice (Richards et al. 2020, 2022).

## Limitations and considerations
- Sampling is spot-check and reflects conditions at the time of collection; may not capture temporal variability.
- Only includes remediation systems with available paired inlet-outlet data; some units (e.g., packaged water) may have incomplete inlet data.
- Urban bias: higher sampling density in Patna due to urban groundwater dynamics and prevalence of household treatment systems.
- Data pertains to a specific time window (2019) within a broader 2018–2022 context.

## References
- Richards, L.A.; Kumar, A.; Shankar, P.; Gaurav, A.; Ghosh, A.; Polya, D.A. (2020) Distribution and Geochemical Controls of Arsenic and Uranium in Groundwater-Derived Drinking Water in Bihar, India. Int. J. Environ. Res. Public Health 17, 2500.
- Richards, L.A.; Parashar, N.; Kumari, R.; Kumar, A.; Mondal, D.; Ghosh, A.; Polya, D.A. (2022) Household and community systems for groundwater remediation in Bihar, India: Arsenic and inorganic contaminant removal, controls and implications for remediation selection, Science of the Total Environment, 830, 154580.