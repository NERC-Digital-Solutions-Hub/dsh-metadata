# Data Overview

- Project context and aim
  - MERLIN project: upscale and transform freshwater ecosystem restoration across Europe using nature-based solutions; this dataset constitutes the first two years of water quality data from Hare Moss (peatland in the Forth catchment) as part of Case Study 17.
  - Objective: implement a control-intervention design to characterise baseline differences before restoration.

- Sampling locations and timeline
  - Fortnightly sampling at two sites from December 2021 to May 2022:
    - Hare Burn (downstream of planned restoration area) as initial monitoring site.
    - Black Burn near Auchencorth Research Facility as control site (closely positioned to restoration area; monitored since 2006; data published in prior datasets).
  - May 2022: two additional Hare Burn monitoring sites added (upstream and downstream) bringing total to four.
  - August 2022: Hare Burn site discontinued; three sites continued: Hare Burn Upstream, Hare Burn Downstream, Black Burn.
  - Spatial details:
    - Black Burn (AUCH): lat 55.794318, lon -3.248223
    - Hare Burn (HARE): lat 55.807011, lon -3.247759
    - Hare Burn Upstream (HARE US): lat 55.794768, lon -3.270693
    - Hare Burn Downstream (HARE DS): lat 55.801449, lon -3.259603
  - Map reference: Grid NT 21245 56644 (Figure 1 in the dataset).

- In-field collection and parameters
  - Water samples for total phosphorous (TP), soluble reactive phosphorous (SRP), dissolved organic carbon/total dissolved nitrogen (DOC/TdN) collected mid-stream; specific bottle types, filtration steps, and handling described.
  - Dissolved greenhouse gas samples collected in duplicates using headspace method.
  - Field physicochemical measurements: pH, electrical conductivity (EC), dissolved oxygen (DO), temperature; status of calibration and instrument checks noted.
  - Primary field team: several contributors including Alanna Grant, Toby Roberts, and Rebecca McKenzie.

- Sample storage and laboratory analyses
  - Storage:
    - TP, SRP, spare filtered samples: -18°C until batch analysis.
    - DOC and POC: 4°C; analyzed within a week.
    - Greenhouse gas samples: stored at room temperature until analysis.
  - Analyses:
    - DOC/TdN: Shimadzu TOC-LCPH with NPOC; standard and blank workflows; replicate handling; calibration checks.
    - UV/Vis SUVA: absorbance from 230–800 nm; SUVA254 calculated for aromaticity.
    - POC: pre-combusted filters, LOI-based conversion to mg/L with 0.58 factor.
    - TP and SRP: SEAL AQ2 with acid digestion and colorimetric molybdenum-blue method; calibration with standards; blanks used.
    - GHGs: dissolved CH4, CO2, N2O measured by GC (FID for CH4/CO2, μECD for N2O); concentrations calibrated against standards; results averaged per site.
  - Data organization: dataset records in columns A–V with site metadata, field measurements, and lab results.

- Data structure, variables, and units (Table 3 overview)
  - Site_Name, Site_Code, Date, Time
  - Field water quality: pH, pH_Temp, DO, DO_perc, DO_Temp, Cond, Cond_Temp, Temp_av
  - DOC, TdN, C_N, Abs_254, SUVA
  - TP, SRP, CH4, CO2, N2O, POC
  - Each variable includes specified decimals and units (e.g., DO mg/L, Cond µS/cm, TP mg/L, CH4 µg/L, etc.).

- Dataset completeness and data quality
  - Occasional missing or incorrect observations due to instrument or laboratory issues.
  - Table 4 lists data exclusions with date, site, determinant, and reason (e.g., below detection limit, not recorded, samples not collected, pH probe fault, sample contamination, instrument fault, sample unavailable, etc.).
  - Examples of excluded data span 2021–2023 and involve multiple determinants (e.g., N2O below LOD, TP, POC, Abs254/SUVA, pH, time issues).

- Dataset scope and use for GIS
  - Spatially explicit: four sites with precise coordinates and a grid reference; suitable for point-based GIS layers and time-enabled analyses.
  - Baseline data for a control-intervention restoration framework; supports map-based visualization of spatial patterns in water quality and changes across sites and over time.
  - Data can be exported to standard GIS formats (e.g., shapefiles, GeoJSON) with fields for site metadata, sampling dates, and lab/field measurements.
  - Limitations to consider in GIS: site changes over time (discontinuation of Hare Burn site), data exclusions and variability in measurement occasions.

- Acknowledgements, references, and funding
  - MERLIN is a Horizon 2020 research and innovation action (grant No 101036337).
  - References include Dinsmore et al. (2013), Weishaar et al. (2003), Dawson et al. (1995), and Pribyl (2010) for methodological context.