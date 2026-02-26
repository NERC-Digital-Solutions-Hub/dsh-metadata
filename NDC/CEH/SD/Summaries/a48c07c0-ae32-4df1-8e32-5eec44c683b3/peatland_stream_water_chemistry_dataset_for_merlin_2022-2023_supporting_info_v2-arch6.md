# Data Overview

- Objectives and scope
  - MERLIN project aims to upscale restoration of freshwater ecosystems in Europe by developing a replicable framework for nature-based solutions.
  - This dataset covers the first two years of water quality data from Hare Moss peatland (Forth catchment) as part of Case Study 17.
  - Design uses a control-intervention approach to characterize baseline conditions before restoration.

- Sampling locations and design
  - Fortnightly sampling at two sites from Dec 2021 to May 2022: Hare Burn downstream of planned restoration (monitoring site) and Black Burn near Auchencorth (control site, long-term data).
  - May 2022: two additional Hare Burn sites added (upstream and downstream) for a total of four sites.
  - Aug 2022: original Hare Burn site discontinued; monitoring continued at Hare Burn Upstream, Hare Burn Downstream, and Black Burn.
  - Peat extraction upstream from Hare Burn influences site conditions (bank erosion and sand deposition observed).
  - Exact site coordinates and codes are documented (AUCH, HARE, HARE US, HARE DS).

- In-field collection methods
  - Analytes: total phosphorous (TP), soluble reactive phosphorous (SRP), dissolved organic carbon/total dissolved nitrogen (DOC/TdN), particulate organic carbon (POC), and dissolved greenhouse gases (GHG).
  - Water samples collected mid-channel using rinsed syringes; sample types and volumes specified to preserve integrity.
  - Filtration and bottles: SRP and DOC filtered with 0.45 µm filters into sterile tubes; POC collected on pre-combusted filters; headspace method used for dissolved GHGs.
  - Physicochemical measurements: pH, electrical conductivity, dissolved oxygen (DO), and temperature measured with a HACH HQ4300 multi-parameter meter; calibrations performed with standard solutions before use.
  - Field collection led by team members (notably Alanna Grant, Toby Roberts, Rebecca McKenzie).

- Sample storage and handling
  - TP, SRP, and spare filtered samples frozen at -18°C for batch analysis.
  - DOC and POC samples stored at 4°C and analyzed within a week or sooner.
  - Greenhouse gas samples stored at room temperature until analysis.

- Laboratory analysis and methods
  - DOC and TdN: measured with Shimadzu TOC-LCPH (NPOC method; includes TNM L and autosampler); quality control with standards, blanks, and calibration checks; duplicate measurements with a >2% CV re-measurement rule.
  - UV/Vis SUVA: absorbance measured from 230–800 nm; SUVA254 calculated to indicate dissolved organic carbon aromaticity.
  - POC: 45 mm GF/F filters pre-burned; LOI method used to convert to mg/L POC with a 0.58 carbon conversion factor.
  - TP and SRP: analyzed by SEAL AQ2 Discrete Analysers after digestion (K2S2O8) and colorimetric determination for orthophosphate; standards and blanks used for QC.
  - Greenhouse gases: dissolved CH4, CO2, and N2O analyzed by GC (μECD for N2O, FID for CH4/CO2); concentrations converted from ppmv to µg/L using Henry’s law; duplicates averaged.

- Data structure and units
  - Data are organized with sampling and results across columns: Site_Name, Site_Code, Date, Time, pH, pH_Temp, DO, DO_perc, DO_Temp, Cond, Cond_Temp, Temp_av, DOC, TdN, C_N, Abs_254, SUVA, TP, SRP, CH4, CO2, N2O, POC.
  - Column descriptions and units are specified in the dataset documentation (e.g., Date in dd/mm/yy, Time in hh:mm, pH (dimensionless), temperatures in °C, DO in mg/L, Cond in µS/cm, DOC/TdN in mg/L, CH4/CO2/N2O in relevant units per method).
  - Data quality controls include instrument calibrations, blanks, and duplicates; non-detections and problematic measurements may be flagged as exclusions.

- Dataset completeness and data exclusions
  - Some data were excluded due to instrument/lab issues or sample problems (see Table 4 in the document).
  - Exclusions include: measurements below detection limits, missing time or pH data, samples not collected, pH probes malfunctioning, sample unavailability, and suspected contamination or instrument faults.
  - Specific notable omissions span multiple dates/sites (e.g., 15/12/2021 N2O below LOD; 06/01/2022 TP/SRP/POC not collected; 29/04/2022 Abs 254/SUVA unavailable; various pH/probe issues).

- Acknowledgements and references
  - MERLIN is a research and innovation action funded by the European Commission under Horizon 2020 (grant agreement No 101036337).
  - References cited relate to methods and prior data on aquatic carbon, GHG measurements, SUVA interpretation, and SOC/SOM conversions.