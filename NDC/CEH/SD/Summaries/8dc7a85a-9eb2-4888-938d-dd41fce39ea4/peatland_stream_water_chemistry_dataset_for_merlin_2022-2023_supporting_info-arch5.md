# Data Overview

- Project objective: MERLIN aims to upscale and transform restoration of freshwater ecosystems in Europe by developing a framework for implementing nature-based solutions that can be replicated. This dataset covers the first two years of water quality data from Hare Moss peatland (Forth catchment), part of Case Study 17, to implement a control–intervention approach characterising baseline prior to restoration.

- Sampling locations and design:
  - Fortnightly sampling Dec 2021–May 2022 at two sites: Hare Burn downstream of planned restoration area (monitoring site) and Black Burn near Auchencorth Research Facility (control site, monitored since 2006).
  - May 2022: added two more Hare Burn sites (upstream and downstream), total of four sites.
  - August 2022: Hare Burn site discontinued; monitoring continued at Hare Burn Upstream, Hare Burn Downstream, and Black Burn (see Table 1 and Figure 1). Hare Burn is influenced by peat extraction upstream, affecting bank stability and sediment deposition.
  - Monitoring period spans Dec 2021–Oct 2023 with some interruptions due to field/lab issues (see completeness section).

- In-field collection (parameters and methods):
  - Water samples for total phosphorus (TP), soluble reactive phosphorus (SRP), and dissolved organic carbon/total dissolved nitrogen (DOC/TdN) collected near midstream using rinsed syringes; specific bottle types and volumes used for each parameter.
  - Filtration: SRP and DOC filtered through 0.45 µm syringe filter; priming steps described.
  - Particulate organic carbon (POC): unfiltered samples collected in a separate bottle; pre-rinsed bottles and filtration setup described.
  - Dissolved greenhouse gas samples collected in duplicate using headspace method with two 60 ml syringes and Exetainer vials.
  - Physicochemical parameters (pH, temperature, dissolved oxygen, conductivity) measured on-site with a HACH HQ4300 multimeter; regular calibration against standard solutions.

- Sample storage and handling:
  - TP, SRP, and spare filtered samples frozen at -18°C; DOC/POC kept at 4°C and analyzed within a week.
  - Greenhouse gas samples stored at room temperature until batch analysis.

- Sample analysis and QA/QC:
  - DOC and TdN: Shimadzu TOC-LCPH with NPOC method; Standards and blanks run at beginning/end of runs; calibration curves checked periodically; replicates averaged with outlier handling.
  - UV/Vis SUVA: Absorbance measured from 230–800 nm with SUVA at 254 nm; blank-corrected.
  - POC: Pre-combusted GF/F filters; LOI method with 0.58 conversion factor to estimate C content.
  - TP: SEAL AQ2 with acid digestion (potassium persulfate) and colorimetric phospho-molybdate method; multi-point calibration and blanks.
  - SRP: Same colorimetric method as TP on thawed samples.
  - GHG: Agilent 7890B GC with μECD for N2O and FID for CH4/CO2; concentrations calibrated against gas standards and converted to µg/L using Henry’s law.
  - Analyses conducted by named researchers; emphasis on calibration, blanks, and duplicate measurements where applicable.

- Nature and units of recorded values (dataset structure):
  - Data organized with Site_name, Site_code, Date, Time, and field measurements (pH, pH_temp, DO, DO_percent, DO_temp, Conductivity, Conductivity_temp, Temp_av, DOC, TdN, C_N, Abs_at_254, SUVA, TP, SRP, CH4_C, CO2_C, N2O_N, POC).
  - Units standardized (e.g., pH, °C, mg/L, µS/cm, µg/L, mg/L, ppmv converted to µg/L as needed).

- Dataset completeness and exclusions:
  - Some field/instrument/lab issues led to excluded data (e.g., below detection limits, missing times, samples not collected, pH probe failures, sample unavailability, abnormal DOC/TdN values, suspected contamination, in-lab pH measurements).
  - Exclusion details include dates, site codes, determinants, and reasons for removal (as documented in Table 4).

- Data governance and stewardship notes for Data Stewards:
  - Ensure complete, well-documented metadata aligned with the included column descriptions (Table 3) and units.
  - Capture data lineage: site changes, sampling period, and any exclusions with justifications (Table 4).
  - Maintain transparency about QA/QC procedures (calibration, blanks, duplicates) to support reproducibility.
  - Track updates and provide clear versioning, including rationale for any reprocessing or reanalysis.
  - Facilitate interoperability with other MERLIN datasets and related long-term monitoring records (e.g., prior Black Burn Hare Burn datasets cited).

- Acknowledgements and references:
  - MERLIN is funded as a Horizon 2020 research and innovation action (grant agreement No 101036337).
  - References include Dawson et al. (1995), Dinsmore et al. (2013), Pribyl (2010), and Weishaar et al. (2003).