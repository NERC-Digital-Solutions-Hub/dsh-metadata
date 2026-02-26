# LOCATE Part 2: ICP-MS Analyses of River Water Across Great Britain

- Objective and scope
  - LOCATE is a multidisciplinary NERC project involving the National Oceanography Centre, British Geological Survey, UK Centre for Ecology and Hydrology, Plymouth Marine Laboratory, and supporting universities and the Environment Agency.
  - Aim: improve understanding of carbon flow from land to the ocean.
  - Part 2 dataset contains ICP-MS analyses of cations from river water, collected alongside Part 1 datasets on river water parameters (temperature, SEC, salinity, nutrients, organic carbon, isotopes, etc.).
  - Sampling covers 41 rivers across England, Scotland, and Wales, monthly in 2017 (Jan–Dec) with additional sampling in Nov 2016; some sites not sampled in Nov 2016 as a trial.
  - Rivers and sampling sites are documented in locate_river_info.txt; coordination led by the British Geological Survey.

- Sampling design and site management
  - Sampling occurred at fixed sites on each river; most sites sampled in 2017 2–3 days per month (Dorset Stour (DSTO) excluded from some months or shifted).
  - In 2017, most sampling sites were moved to HMS sites to streamline data integration.
  - Photos were taken upstream and downstream at each site during sampling (not submitted to EIDC but available).

- Field sampling procedures (highlights)
  - Field workflow: in-field filtration and aliquoting into bottles; POC samples filtered in the lab later.
  - Samples kept dark and refrigerated or frozen during transit.
  - In-situ measurements: salinity, electrical conductivity (SEC), and temperature where possible.
  - Standard sampling depth and representativeness: ~0–30 cm mid-channel; samples from representative, moving water where necessary.
  - Protocols ensured clean collection (rinsed vessels, contamination precautions, glove use).
  - All samples returned to the laboratory, where acidification and storage steps were implemented to standardize handling.

- ICP-MS analyses: instrumentation, methods, and QA
  - Instrument: Agilent 8900 ICP-QQQ.
  - Analytical method: Ag_2.3.21 Determination of major and trace elements in aqueous samples using ICP-MS.
  - Analyte units: mg/L or μg/L, depending on element.
  - Sample preparation: water filtered to 0.45 μm, acidified to 1% HNO3; post-reception in the lab, 0.5% v/v HCl added to all filtered samples.
  - QA and accreditation: UKAS ISO/IEC 17025:2017 accredited laboratory (Lab number 1816).
  - QC regime: QC every ~20 samples; three calibration blocks per run; use of multi-element and single-element standards (LoQC1, LoQC2, HiQC3, and others) with defined concentrations.
  - Detection limits: two reported limits per element per column (Batch DL and Method DL); if a value is below DL, it should be reported as < DL.
  - Data handling: results stored in a CSV with 61 columns, including LIMS code, river, month, and concentrations for each element.

- Data format, contents, and interpretive notes
  - Data file: CSV with 61 columns; columns include river name, month, and concentrations for a wide suite of elements (Ca, Mg, Na, K, P, S, Si, SiO2, Ba, Sr, Mn, Fe, Li, Be, B, Al, Ti, Cr, Co, Ni, Cu, Zn, Ga, As, Se, Rb, Y, Zr, Nb, Mo, Ag, Cd, Sn, Sb, Cs, La, Pr, Nd, Sm, Eu, Gd, Tb, Dy, Ho, Er, Yb, Tm, Lu, Hf, Ta, W, Tl, Pb, Bi, Th, U, etc.).
  - Each element column includes two detection limit lines (Batch DL and Method DL) in lines 3 and 4 of each column.
  - Below-DL values should be reported as < DL, reflecting analytical noise and method detection limits.
  - Metadata and context files: locate_river_info.txt provides river sampling details; additional companion datasets exist for estuaries (part 1) and broader datasets via EIDC and BODC.

- Data provenance, access, and usage notes for data leaders
  - Sampling coordination and field procedures were standardized across teams; acidification and QA were centralized at the BGS Keyworth laboratory.
  - The dataset is part of an integrated data framework alongside Part 1 river water parameter data, enabling cross-parameter and cross-site analyses.
  - Access and documentation:
    - Part 2 data accompanied by river metadata file locate_river_info.txt.
    - Part 1 river water parameter data and estuary data are available via the EIDC and BODC, respectively.
    - The project reference and contact for sampling coordination: Andy Tye (BGS).
  - Practical considerations for use:
    - Be aware of site- and date-specific limitations (e.g., Dorset Stour sampling start times, November 2016 trial sampling).
    - Ensure proper handling of DL values when performing statistical analyses or data visualizations.
    - Use the QA/QC notes and calibration details to assess measurement uncertainty and comparability across runs.