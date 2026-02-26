# Data Overview

## Project objectives
- MERLIN aims to upscale and transform freshwater ecosystem restoration across Europe by creating a framework for nature-based solutions ready for replication.
- This dataset covers the first two years of water quality data from Hare Moss (peatland in the Forth catchment), part of Case Study 17.
- Objective: implement a control-intervention approach to characterize baseline differences before restoration.

## Sampling Locations
- Fortnightly sampling Dec 2021–May 2022 at two sites: 
  - Hare Burn downstream of planned restoration area (monitoring site).
  - Black Burn near Auchencorth Research Facility (control site; monitored since 2006; previously published in other datasets).
- May 2022: two additional Hare Burn sites added (upstream and downstream), total four sites.
- August 2022: original Hare Burn site discontinued; monitoring continued at Hare Burn Upstream, Hare Burn Downstream, and Black Burn.
- Noted influence of upstream peat extraction on Hare Burn upstream area, including bank collapse and sand deposition over the two-year period.
- Sites and coordinates provided in Table 1 (AUCH, HARE, HARE US, HARE DS).

## In-field collection
- Analytes: total phosphorus (TP), soluble reactive phosphorus (SRP), dissolved organic carbon/total dissolved nitrogen (DOC/TdN); dissolved greenhouse gases collected in duplicates using headspace method.
- Water sampling: near mid-stream using a 60 ml syringe; TP syringed into sterile tubes; SRP and DOC filtered through 0.45 µm filters; POC collected via unfiltered samples.
- Sample containers: acid-washed bottles; careful labeling with project name, site code, sampling date.
- DGH sampling: duplicates for dissolved greenhouse gases (CH4, CO2, N2O) via headspace method with two syringes and Exetainer vials.
- Physicochemical parameters: pH, electrical conductivity, DO, and temperature measured in field using HACH HQ4300 with calibrated electrodes; calibration conducted before each use.

## Sample storage
- TP, SRP, and POC samples: frozen at -18°C until analysis (in batches).
- DOC and TdN samples: stored at 4°C and analyzed within a week.
- Greenhouse gas samples: stored at room temperature until batching for analysis.

## Sample analysis
- DOC/TdN: Shimadzu TOC-LCPH with TNM L, autosampler; method uses 680°C combustion to measure NPOC (DOC) and TdN; calibration, standards, blanks, and repeat measurements for quality control.
- UV/Vis SUVA: absorbance measured from 230–800 nm with 254 nm SUVA calculated to indicate DOC aromaticity.
- POC: pre-combusted GF/F filters; LOI method with conversion to carbon using a 0.58 factor; combustion at 375°C after drying.
- Total phosphorus: SEAL AQ2 Discrete analyzer with acid digestion and acid-molybdenum-blue colorimetric method; calibration with multiple standards; blanks used throughout.
- Soluble reactive phosphorus: SRP measured via the same colorimetric method as TP.
- Greenhouse gases: dissolved CH4, CO2, N2O analyzed with GC (μECD for N2O; FID for CH4/CO2); concentrations converted to µg L−1 using Henry’s law.

## Nature and units of recorded values
- Data recorded in columns covering site and sampling metadata (Site_name, Site_code, Date, Time).
- Field measurements: pH, pH_temp, DO, DO_percent, DO_temp, Conductivity, Conductivity_temp, Temp_av.
- DOC and TdN, C_N ratio, Abs_at_254, SUVA.
- TP, SRP, CH4_C, CO2_C, N2O_N, POC.
- Detailed column descriptions and units are specified in Table 3 of the dataset documentation.

## Dataset completeness
- Occasional data gaps due to instrument or analyzer failures, or sampling issues.
- Excluded data listed in Table 4 with dates, sites, determinants, and reasons, including:
  - Below detection limits (e.g., N2O-N).
  - Missing or unrecorded time or pH readings.
  - Missing samples (TP, SRP, POC) or samples unavailable.
  - Instrument faults or measurements performed in-lab rather than in situ.
  - Abnormally high/low results suggesting contamination or instrument faults.
  - Instances of pH measurement issues or not recorded times.
- Some exclusions relate to samples re-measured or rebooked after field issues; several August 2023 and October 2023 entries indicate instrument faults or abnormal results.

## Acknowledgements
- MERLIN is a research and innovation action funded under the European Commission Horizon 2020 programme (grant agreement No 101036337).

## References
- Dawson, J.J.C. et al. (1995). Downstream Changes in Free Carbon Dioxide in an Upland Catchment.
- Dinsmore, K.J. et al. (2013). Five year record of aquatic carbon and greenhouse gas concentrations from Auchencorth Moss.
- Pribyl, D.W. (2010). SOC to SOM conversion factors review.
- Weishaar, J.L. et al. (2003). Evaluation of SUVA as indicator of DOC composition and reactivity.