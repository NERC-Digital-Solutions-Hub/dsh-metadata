# Data Overview

- Project context: MERLIN aims to upscale freshwater ecosystem restoration across Europe by developing a framework for immediate replication of nature-based solutions. This dataset covers the first two years of water quality data from Hare Moss (Forth catchment, Case Study 17) to implement a control–intervention approach and characterize baseline differences before restoration.

- Sampling locations and design:
  - Fortnightly sampling Dec 2021–May 2022 at two sites: Hare Burn downstream (initial monitoring site) and Black Burn near Auchencorth Research Facility (control site; monitored since 2006).
  - May 2022: two additional Hare Burn sites added (Upstream and Downstream), bringing total to four.
  - August 2022: Hare Burn original site discontinued; three sites continued (Hare Burn Upstream, Hare Burn Downstream, Black Burn).
  - Coordinates and site codes provided (AUCH, HARE, HARE US, HARE DS).

- In-field collection and measured parameters:
  - Analytes: total phosphorous (TP), soluble reactive phosphorous (SRP), dissolved organic carbon/total dissolved nitrogen (DOC/TdN), particulate organic carbon (POC); dissolved greenhouse gases (gas-phase sampling); physicochemical parameters (pH, electrical conductivity, dissolved oxygen, temperature).
  - Sampling approach: water collected near mid-channel with syringes, filters used for SRP/DOC, spare filtered sample collected for contingencies.
  - In-field measurements: pH, DO, conductivity, and temperatures measured with calibrated probes; field controls and calibration procedures described.

- Sample storage and laboratory analysis:
  - Storage: TP, SRP, and spare filtered samples frozen at -18°C; DOC and POC stored at 4°C and analyzed promptly; greenhouse gas samples stored at room temperature until analysis.
  - Analyses performed by named personnel:
    - DOC/TdN: Shimadzu TOC-LCPH with NPOC method; standard and blank protocol details provided.
    - UV/Vis: SUVA 254 nm via spectrophotometer; absorbance measured 230–800 nm.
    - POC: pre-combusted filters, LOI method, conversion to mg/L using 0.58 factor.
    - TP/SRP: SEAL AQ2 with acid digestion and colorimetric molybdenum-blue method; calibration standards outlined.
    - GHGs: dissolved CH4, CO2, N2O analyzed by GC (μECD for N2O; FID for CH4/CO2); results reported as ppmv converted to µg L−1 via Henry’s law.

- Dataset structure and metadata:
  - Data organized with columns covering site information, field physicochemical data, and lab results (A–V); detailed column definitions and units provided (Table 3), including site name/code, date/time, pH, DO, conductivity, temperatures, DOC, TdN, C:N, Abs_254, SUVA, TP, SRP, CH4, CO2, N2O, POC.

- Dataset completeness and quality controls:
  - Acknowledgement of occasional instrument or analyzer failures leading to missing or excluded data.
  - Exclusion log (Table 4) documents dates, sites, determinants, and reasons (e.g., below LOD, samples not collected, pH probe malfunction, sample contamination, instrument fault, unavailable samples, in-lab measurements due to field issues).

- Governance, provenance, and references:
  - MERLIN is a research and innovation action funded under the European Commission Horizon 2020 programme (grant agreement No 101036337).
  - Methods and calibration references included for TOC, SUVA, POC, TP/SRP, and GHG analyses.