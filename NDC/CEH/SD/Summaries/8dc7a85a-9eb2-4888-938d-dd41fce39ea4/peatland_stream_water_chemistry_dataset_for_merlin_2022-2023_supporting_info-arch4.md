# Data Overview

- Purpose and scope
  - MERLIN project aims to upscale and transform restoration of freshwater-related ecosystems in Europe by generating a framework for implementing nature-based solutions that can be replicated.
  - This dataset covers the first two years of water quality data from Hare Moss peatland (Forth catchment), part of Case Study 17, applying a control-intervention approach to characterize baseline conditions before restoration.

- Study design and sampling locations
  - Fortnightly sampling from December 2021 to May 2022 at two sites: Hare Burn (downstream of the planned restoration area) and Black Burn (near Auchencorth Research Facility, control site monitored since 2006).
  - May 2022: two additional Hare Burn sites added (upstream and downstream), expanding to four sites total.
  - August 2022: the original Hare Burn site discontinued; monitoring continued at Hare Burn Upstream, Hare Burn Downstream, and Black Burn (three sites).
  - Note: Hare Burn is affected by upstream peat extraction, contributing to bank erosion and sand deposition during the study period.
  - Exact site details and coordinates are provided in Table 1 and Figure 1.

- In-field collection and sampling methods
  - Analytes: total phosphorous (TP), soluble reactive phosphorous (SRP), dissolved organic carbon/total dissolved nitrogen (DOC/TdN), and dissolved greenhouse gases.
  - Sampling: close to mid-channel using a 60 mL syringe; TP into sterile 15 mL tubes; SRP and DOC filtered through 0.45 µm CA syringe filters; filtered samples collected into 15 mL tubes; POC sampled unfiltered into 250 mL HDPE bottles.
  - Filter handling: filter primed with stream water; same filter used for SRP and DOC unless clogged.
  - GHG sampling: duplicate headspace method with two 60 mL syringes, equilibrated, then transferred to Exetainer vials; ambient air sampled as a reference.
  - Physicochemical parameters: pH, electrical conductivity, dissolved oxygen (DO), and temperature measured with a portable HACH HQ4300 multimeter; calibrations performed before use (pH 4, 7, 10; 1413 µS/cm for conductivity).

- Sample storage and processing
  - Storage: TP, SRP, and spare filtered samples frozen at -18°C; DOC and POC stored at 4°C and analyzed within a week or sooner; GHG samples stored at room temperature until analysis.
  - Analyses conducted by project team members.

- Laboratory analysis methods
  - DOC and TdN (NPOC considered for DOC): Shimadzu TOC-LCPH with TNM L unit; 680°C combustion catalytic oxidation; acidification and sparging; NPOC used as DOC; quality control with standards and blanks; duplicate measurements with acceptance criterion CV ≤ 2%.
  - UV/Vis and SUVA: absorbance from 230 to 800 nm; SUVA254 calculated as absorbance at 254 nm normalized to DOC concentration (mg/L).
  - Particulate Organic Carbon (POC): filtration through pre-combusted GF/F filters, LOI-based determination, conversion to C using factor 0.58.
  - Total Phosphorous (TP) and Soluble Reactive Phosphorous (SRP): SEAL AQ2 Discrete analyser with acid digestion (K2S2O8) and acid molybdenum-blue colorimetric method; calibration with multiple standards; blanks used throughout.
  - Greenhouse Gases (GHG): dissolved CH4, CO2, and N2O analyzed by GC (Agilent 7890B) with μECD (N2O) and FID (CH4, CO2); concentrations calibrated against standards; results converted to µg/L using Henry’s law.

- Data structure and metadata
  - Dataset records are organized with fields for site information and sampling (columns A–C), field physicochemical data (D–K), and laboratory results (L–V).
  - Column descriptions and units include: Site_name, Site_code, Date, Time, pH, pH_temp, DO, DO_percent, DO_temp, Conductivity, Conductivity_temp, Temp_av, DOC, TdN, C_N, Abs_at_254, SUVA, TP, SRP, CH4_C, CO2_C, N2O_N, POC, among others.
  - Table 3 provides detailed description, decimals, and units for each parameter.

- Dataset completeness and data quality
  - Data gaps due to instrument or analyser issues, missing observations, or non-collection events.
  - Table 4 lists data exclusions by date, site, determinant, and reason (e.g., below detection limit, not recorded, samples not collected, pH probe malfunction, sample unavailable, instrument faults, anomalous results, contamination concerns, or in situ measurement limitations).

- Data governance and acknowledgments
  - MERLIN is a research and innovation action funded by the European Commission’s Horizon 2020 programme (grant agreement No 101036337).

- References
  - Cited methodological and background sources for TOC analysis, SUVA interpretation, SOC/SOM conversion factors, and related prior datasets.