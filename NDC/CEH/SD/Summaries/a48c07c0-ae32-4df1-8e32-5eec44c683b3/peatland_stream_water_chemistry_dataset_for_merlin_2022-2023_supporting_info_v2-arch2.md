# Data Overview

- Objective: The MERLIN project aims to upscale and transform freshwater restoration across Europe by creating a framework for immediate replication of nature-based solutions. This dataset represents the first two years of water quality data from Hare Moss (peatland in the Forth catchment) to implement a control-intervention approach that characterises differences in the baseline period before restoration.

- Sampling locations and design:
  - Fortnightly sampling at two sites from December 2021 to May 2022.
  - Initial monitoring site: Hare Burn downstream of the planned restoration area.
  - Control site: Black Burn near Auchencorth Research Facility, monitored since 2006 and previously published data exist.
  - May 2022: two additional Hare Burn sites added (upstream and downstream), bringing total to four.
  - August 2022: original Hare Burn site discontinued; remaining sites are Hare Burn Upstream, Hare Burn Downstream, and Black Burn (3 sites).

- Data and variables collected:
  - In-field water chemistry: total phosphorus (TP), soluble reactive phosphorus (SRP), dissolved organic carbon/total dissolved nitrogen (DOC/TdN).
  - Dissolved greenhouse gases: CH4, CO2, N2O (headspace method; duplicates).
  - Physicochemical parameters: pH, electrical conductivity, dissolved oxygen (DO), temperature; DO and pH readings taken in situ with calibrated probes.
  - Sample storage and handling: TP, SRP, and spare filtered samples frozen at -18°C; DOC and POC stored at 4°C; greenhouse gas samples stored at room temperature for later analysis.

- Sample collection and analysis methods:
  - DOC/TdN: Shimadzu TOC-LCPH with TNM L unit; NPOC used as DOC proxy; calibration and blanks included; duplicate measurements with acceptance criteria.
  - SUVA: Absorbance (230–800 nm) with SUVA254 calculation to indicate aromaticity of DOC.
  - POC: Filter, pre-ignition at 450°C, LOI-based conversion (0.58) to estimate mg/L C.
  - TP and SRP: SEAL AQ2 discrete analyser; digestion with potassium persulfate; colorimetric orthophosphate determination (molybdate blue) with calibration standards; blanks and QA checks included.
  - GHG: Agilent 7890B GC with μECD for N2O and FID for CH4/CO2; concentrations reported as ppmv and converted to µg/L via Henry’s law.

- Data structure and units:
  - Data organized with sampling information (Site_Name, Site_Code, Date, Time) in columns A–C.
  - Field measurements (pH, pH_Temp, DO, DO_perc, DO_Temp, Cond, Cond_Temp, Temp_av) in columns D–K.
  - Laboratory analysis results (DOC, TdN, C_N, Abs_254, SUVA, TP, SRP, CH4, CO2, N2O, POC) in columns L–V.
  - Detailed column descriptions and units are provided in the dataset documentation (Table 3).

- Data quality and completeness:
  - Some observations were excluded due to instrument or analytical issues (e.g., below detection limits, missing time, unavailable samples, malfunctioning pH probes, abnormally low/high results, instrument faults).
  - Exclusion log (Table 4) lists dates, sites, determinants, and reasons for omission (e.g., N2O below LOD, pH unavailable, samples not collected, instrument faults).

- Outputs and data stewardship:
  - The project emphasizes standardised data collection and documentation to enable cross-site comparison and long-term monitoring.
  - Datasets are stored and uploaded to appropriate data portals to facilitate access and reuse by others, supporting broader environmental health and policy assessments.

- Acknowledgements and references:
  - MERLIN is funded under the European Commission Horizon 2020 programme (grant agreement No 101036337).
  - References cover methodological backgrounds and prior related datasets (e.g., Dinsmore et al. 2013; Weishaar et al. 2003).