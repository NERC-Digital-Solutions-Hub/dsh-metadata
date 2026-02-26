# Data Overview

## Project and Dataset Scope
- MERLIN project aims to upscale and transform restoration of freshwater-related ecosystems in Europe by creating a framework for nature-based solutions that can be replicated.
- This dataset comprises the first two years of water quality data from Hare Moss, a peatland in the Forth catchment (Case Study 17), intended to support a control-intervention approach to characterize differences in the baseline period before restoration.

## Sampling Design and Sites
- Fortnightly sampling from December 2021 to May 2022 at two sites:
  - Hare Burn downstream of the planned restoration area (monitoring site)
  - Black Burn near the Auchencorth Research Facility (control site; monitored since 2006; data published in prior datasets)
- May 2022: two additional monitoring sites added along Hare Burn (upstream and downstream), total four sites.
- August 2022: original Hare Burn site discontinued; continued monitoring at Hare Burn Upstream (HARE US), Hare Burn Downstream (HARE DS), and Black Burn (AUCH).
- Anatomy of sites: Hare Burn is influenced by upstream peat extraction causing bank erosion and sediment deposition over the monitoring period.
- Location details provided in Table 1 and Figure 1 with exact coordinates for AUCH, HARE, HARE US, and HARE DS.

## In-Field Collection and Procedures
- Analytes collected: total phosphorus (TP), soluble reactive phosphorus (SRP), dissolved organic carbon/total dissolved nitrogen (DOC/TdN), and dissolved greenhouse gases.
- Water sampling:
  - Collected near the middle of the stream using a 60 mL syringe; TP into sterile 15 mL tubes (up to 13 mL), SRP and DOC filtered into sterile tubes using 0.45 µm filters; spare filtered sample collected.
  - Unfiltered water for particulate organic carbon (POC) collected directly into acid-washed 250 mL bottle.
  - Sample bottles labeled with project name, site code, sampling date.
- Dissolved greenhouse gas samples collected in duplicate using headspace method with two 60 mL syringes and Exetainer vials.
- Physicochemical parameters measured in-field: pH, electrical conductivity, dissolved oxygen, and temperature using a HACH HQ4300 multi-channel meter with calibrated probes.
- Field personnel: primarily Alanna Grant, Toby Roberts, and Rebecca McKenzie.

## Sample Storage and Handling
- TP, SRP, and spare filtered samples: stored at -18°C for later batch analysis.
- DOC and POC samples: stored at 4°C and analyzed within a week or as soon as possible.
- Greenhouse gas samples: stored at room temperature until batch analysis.

## Laboratory Analyses and QA/QC
- DOC and TdN:
  - Analyzed with Shimadzu TOC-LCPH (with TNM L unit and autosampler) using 680°C combustion, acidification, and sparging.
  - NPOC is used as DOC; calibration with standards; blanks and duplicate measurements; outlier handling when CV > 2%.
- UV/Vis SUVA:
  - Absorbance from 230 to 800 nm; SUVA254 calculated to indicate aromaticity of DOC.
- Particulate Organic Carbon (POC):
  - Filterable material captured on pre-combusted GF/F filters; LOI method with conversion factor 0.58 to estimate POC (mg/L).
- Total Phosphorus (TP) and Soluble Reactive Phosphorus (SRP):
  - TP: SEAL AQ2 discrete analyser with digestion (potassium persulfate) and acid molybdate–antimony colorimetric method; calibration with multiple standards; blanks included.
  - SRP: AQ2 discrete analyser using the same colorimetric method.
- Greenhouse Gases (GHG):
  - Analysis by GC with μECD for N2O and FID for CH4 and CO2; calibration with mixed standards; results in ppmv and converted to µg/L via Henry’s law; duplicates averaged.
- Data presentation:
  - Table 3 defines column headings, descriptions, and units for field and lab results (Site_Name, Site_Code, Date, Time, pH, pH_Temp, DO, DO_perc, DO_Temp, Cond, Cond_Temp, Temp_av, DOC, TdN, C_N, Abs_254, SUVA, TP, SRP, CH4, CO2, N2O, POC).

## Dataset Completeness and Exclusions
- Data completeness affected by occasional instrument or analyzer failures.
- Table 4 lists excluded data with date, site, determinants, and reasons (e.g., below detection limit, not recorded, samples not collected, pH probe malfunction, sample unavailable, instrument fault, contamination concerns).
- Examples of exclusions include:
  - 15/12/2021: N2O below LOD; time not recorded
  - 06/01/2022: samples not collected; time not recorded; pH issues
  - 29/04/2022: Abs 254/SUVA samples unavailable
  - 12/10/2023: Abnormally low DOC/TdN/C:N/SUVA due to instrument fault
- In total, a documented set of excluded observations ensures transparency about data gaps and data quality.

## Data Provenance, Documentation, and References
- Acknowledgement: MERLIN is a research and innovation action funded under the European Commission Horizon 2020 programme (grant No. 101036337).
- Data contributors include Alanna Grant, Rebecca McKenzie, Amy Pickard, Toby Roberts, and Bryan Spears.
- References provided for methods and previous related datasets (Dawson et al., Dinsmore et al., Pribyl, Weishaar et al.).

## Governance, Standards, and Sharing Considerations for Data Stewards
- Standards and consistency:
  - Use of established methods (TOC-LCPH, AQ2, GC with standard calibration protocols) ensures consistency and comparability with prior datasets.
  - Clear QA/QC protocols, including blanks, duplicates, acceptance criteria (e.g., CV thresholds), and routine instrument calibration.
- Metadata and discoverability:
  - Comprehensive metadata with explicit column definitions, units, and decimal places (Table 3) supports data discovery and reuse.
  - Site descriptions, codes, coordinates, dates, and times are documented to enable reproducibility and traceability.
- Data governance and integrity:
  - Documentation of data exclusions and reasons (Table 4) provides transparency about data quality and lifecycle.
  - Data are structured to support integration into data portals and catalogues; ongoing updates and dataset versioning are implied through the methodology of batch analyses and amended site configurations.
- Practical considerations for dissemination:
  - Data sharing aligned with project goals; emphasis on usability for researchers and practitioners evaluating baseline conditions before restoration interventions.
  - Acknowledgement of upstream disturbances (peat extraction) relevant for interpretation and metadata context.
- Potential challenges highlighted for governance:
  - Changes in sampling sites over time and occasional missing data require careful versioning and clear lineage in catalogs.
  - Handling of outlier/instrument-fault data through documented exclusions to maintain dataset integrity.

## Acknowledgements and References
- Acknowledgement of MERLIN funding and collaborators.
- References to methodology and related datasets supporting data interpretation and comparability.