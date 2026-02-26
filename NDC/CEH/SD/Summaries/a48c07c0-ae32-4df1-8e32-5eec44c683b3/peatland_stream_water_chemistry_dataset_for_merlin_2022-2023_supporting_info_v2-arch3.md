# Data Overview

- Project objectives
  - MERLIN aims to upscale and transform restoration of freshwater ecosystems in Europe by developing a framework for effective nature-based solutions.
  - This dataset covers the first two years of water quality data from Hare Moss (peatland in the Forth catchment) as part of Case Study 17.
  - Objective is a control-intervention approach to characterize baseline differences before restoration.

- Sampling locations and design
  - Fortnightly sampling Dec 2021–May 2022 at two sites: Hare Burn downstream (near restoration area) and Black Burn near Auchencorth Research Facility (control; monitored since 2006; data linked to previous datasets).
  - May 2022: two additional Hare Burn sites added (Upstream and Downstream), bringing total to four.
  - Aug 2022: original Hare Burn site discontinued; remaining sites are Hare Burn Upstream, Hare Burn Downstream, and Black Burn.
  - River context: Hare Burn influenced by intensive peat extraction upstream, contributing to bank erosion and deposition over the monitoring period.
  - Site coordinates and details are provided in Table 1 and Figure 1.

- In-field collection and sampling methods
  - Water quality indicators: total phosphorus (TP), soluble reactive phosphorus (SRP), dissolved organic carbon/total dissolved nitrogen (DOC/TdN), and dissolved greenhouse gases (GHG) measured in duplicate headspace samples.
  - Additional physicochemical measurements: pH, electrical conductivity, dissolved oxygen (DO), and temperature using a portable multimeter with calibrated electrodes.
  - Sample collection protocols: centralized middle-of-stream sampling using rinsed syringes and filters; specific bottles and volumes designated for each parameter; careful handling to minimize headspace and contamination.
  - Headspace gas sampling involved equilibration and transfer into Exetainer vials for CH4, CO2, and N2O analysis.

- Sample storage and handling
  - TP, SRP, and spare filtered samples stored at -18°C until batch analysis.
  - DOC and POC samples stored at 4°C and analyzed within a week or as soon as possible.
  - GHG samples stored at room temperature until analysis.

- Laboratory analyses and QA/QC
  - DOC/TdN: Shimadzu TOC-LCPH with NPOC method, using acidification and sparging; multiple standards and blanks; duplicate measurements with outlier exclusion.
  - UV/Vis and SUVA: Absorbance measured 230–800 nm; SUVA254 calculated to indicate DOC aromaticity.
  - Particulate Organic Carbon (POC): Pre-combusted filters, LOI method, conversion factor 0.58 to estimate C.
  - Total Phosphorous (TP) and Soluble Reactive Phosphorous (SRP): SEAL AQ2 discrete analyser with acid digestion and colorimetric detection; calibration and blanks included.
  - GHGs: Dissolved CH4, CO2, and N2O analyzed by GC (Agilent 7890B) with μECD and FID; concentrations converted from ppmv to µg L−1 using Henry’s law.
  - Data are structured to include a detailed description of methods, calibration, and quality control steps.

- Nature and units of recorded values
  - Data organized from field to lab results with clearly defined columns (Site_Name, Site_Code, Date, Time, pH, pH_Temp, DO, DO_perc, DO_Temp, Cond, Cond_Temp, Temp_av, DOC, TdN, C_N, Abs_254, SUVA, TP, SRP, CH4, CO2, N2O, POC; units specified per column).
  - Column-level metadata indicates measurement units, decimal places, and data types (e.g., pH, mg/L, µS/cm, °C, mg/L, µg/L).

- Dataset completeness and data exclusions
  - Documented occurrences of missing or excluded data due to instrument/lab issues, sampling gaps, or quality concerns.
  - Table 4 lists specific exclusions by date, site, determinant, and reason (e.g., below LOD, not recorded, samples not collected, instrument faults, sample contamination, sample unavailable, in situ measurement limitations).

- Acknowledgements and references
  - MERLIN is a research and innovation action funded by the European Commission’s Horizon 2020 programme (grant No 101036337).
  - Key references cited for methods and prior related datasets:
    - Dawson et al. (1995)
    - Dinsmore et al. (2013)
    - Pribyl (2010)
    - Weishaar et al. (2003)

- Relevance for monitoring frameworks
  - Demonstrates a structured, multi-site, control-intervention monitoring design with baseline characterization prior to restoration.
  - Provides comprehensive metadata, standardized sampling and analytical protocols, and transparent QA/QC processes.
  - Documents data provenance, site changes over time, and explicit reasons for data exclusion, enhancing data governance and reproducibility.
  - Reflects typical challenges highlighted for monitoring frameworks (data gaps, access to metadata, silos, data transformation, and the need for clear communication of complex findings).