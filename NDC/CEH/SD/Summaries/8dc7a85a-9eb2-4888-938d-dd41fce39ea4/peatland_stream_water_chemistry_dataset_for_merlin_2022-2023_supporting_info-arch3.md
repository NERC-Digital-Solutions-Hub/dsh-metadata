# Data Overview

- Project objectives
  - MERLIN aims to upscale and transform freshwater restoration across Europe by creating a framework for effective, replicable nature-based solutions.
  - The dataset presents the first two years of water quality data from Hare Moss (peatland in the Forth catchment) as part of Case Study 17.
  - Objective: implement a control-intervention approach to characterize baseline differences before restoration.

- Sampling locations and timeline
  - Fortnightly sampling Dec 2021–May 2022 at two sites: Hare Burn downstream of restoration area (initial monitoring site) and Black Burn near Auchencorth Research Facility (control site with monitoring since 2006).
  - May 2022: two additional Hare Burn sites added (upstream and downstream), total four sites.
  - August 2022: original Hare Burn site discontinued; monitoring continued at Hare Burn Upstream, Hare Burn Downstream, and Black Burn.
  - Upstream peat extraction upstream from the restoration area influenced Hare Burn monitoring (bank erosion and sand deposition observed).

- Site details
  - Four sampling locations (later reduced to three active sites after August 2022): Black Burn (AUCH), Hare Burn (HARE), Hare Burn Upstream (HARE US), Hare Burn Downstream (HARE DS).
  - Coordinates provided for each site; Hare Burn sites affected by local peat disturbance.

- In-field collection
  - Analytes: total phosphorus (TP), soluble reactive phosphorus (SRP), dissolved organic carbon/total dissolved nitrogen (DOC/TdN); dissolved greenhouse gases.
  - Sample collection: near-stream mid-channel using rinsed syringes; TP filtered into 15 mL tubes; SRP and DOC filtered through 0.45 µm filters; DOC sterilized containers for UV/Vis analysis; unfiltered water for particulate organic carbon (POC) analysis collected separately.
  - Gas sampling: dissolved greenhouse gases collected in duplicate using headspace method with syringes and Exetainer vials.
  - In-field measurements: pH, electrical conductivity, dissolved oxygen (DO), temperature using a multi-channel meter; pH and conductivity probes calibrated before use; multiple field personnel listed.

- Sample storage
  - TP, SRP, and spare filtered samples frozen at -18°C for batch analysis; DOC and POC stored at 4°C and analyzed within a week or sooner.
  - Greenhouse gas samples stored at room temperature until batch analysis.

- Sample analysis
  - DOC and TdN: Shimadzu TOC-LCPH with TNM L; method uses 680°C combustion with sparging; NPOC reported as DOC.
  - SUVA: UV/Vis absorbance (A at 254 nm) to calculate SUVA254 for DOC aromaticity.
  - POC: 45 mm GF/F filters pre-burned; LOI method with 0.58 conversion factor to estimate carbon content.
  - TP: SEAL AQ2 with persulfate digestion and acid molybdate colorimetric method; calibration and blanks included.
  - SRP: Same SEAL AQ2 method as TP after thawing.
  - Dissolved greenhouse gases (CH4, CO2, N2O): GC with μECD (N2O) and FID (CH4, CO2); concentrations converted to µg L using Henry’s law.
  - Quality controls: standards, blanks, and duplicate measurements; data processed by averaging duplicates and applying QC rules.

- Nature and units of recorded values
  - Data organized with sampling information (Site_name, Site_code, Date, Time) and field measurements (pH, pH_temp, DO, DO_percent, DO_temp, Conductivity, Conductivity_temp, Temp_av) and laboratory results (DOC, TdN, C_N, Abs_at_254, SUVA, TP, SRP, CH4_C, CO2_C, N2O_N, POC).
  - Units specified for each variable (e.g., pH, °C, mg/L, µS/cm, m, etc.).

- Dataset completeness
  - Occasional instrument or analyzer failures led to missing or excluded observations.
  - Exclusion rationale tabulated (e.g., below detection limits, samples not collected, time not recorded, pH probe malfunction, sample unavailable, instrument faults, abnormally high/low results due to contamination or instrument fault).

- Acknowledgements
  - MERLIN is a research and innovation action funded under the European Commission’s Horizon 2020 programme (grant agreement No 101036337).

- References
  - Cited methodological and previous data sources for context (Dawson et al. 1995; Dinsmore et al. 2013; Pribyl 2010; Weishaar et al. 2003).