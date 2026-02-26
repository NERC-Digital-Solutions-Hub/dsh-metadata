# Dataset: In situ field measurements of riverbed nitrogen transformations in the Hammer Stream

- Purpose and scope
  - In situ measurements of riverbed nitrogen transformations in the Hammer Stream, a sandy tributary of the River Rother, West Sussex, UK.
  - Measurements focus on nitrate reduction processes using 15N-labeled nitrate injections to quantify denitrification, anammox, and DNRA.
  - Baseline porewater chemistry (NO2, NO3, NH3, PO4, Cl, O2, pH, temperature, Fe(II), organic carbon, 15N2) collected prior to injections.
  - Data collected during four campaigns: November 2014, February 2015, April 2015, and July 2015, using the main piezometer network described in related publications.

- Data collection and methods
  - 15N-nitrate push-pull injections (300 μM, 98 atom% 15N) in de-oxygenated river water with KCl; samples collected over time with helium headspace.
  - Oxygen measurements in porewater using a microelectrode; calibration and correction for contamination (estimated 10 μM) subtracted from data.
  - pH and temperature recorded after assessing O2 concentration.
  - Nutrients and ions measured from filtered porewater samples (0.45 μm), frozen at -20°C until analysis.
  - Analytical methods:
    - NO2, NO3 via automated colorimetry (Griess method with inline Cd reduction for NOx).
    - NH3 via indophenol blue method.
    - SRP (PO4) via molybdenum blue method.
    - Chloride by ion-selective electrode.
    - CH4 and N2O via GC with appropriate headspace methods.
    - Fe(II) via phenanthroline complexation and UV/Vis detection.
    - Dissolved organic carbon via TOC analyzer.
  - Data are marked as 0 if below detection limits; ND indicates no data collected or sample lost.

- Data structure and column definitions
  - Spatial and site metadata
    - month: Nov, Feb, Apr, Jul (sampling season).
    - lat, long: coordinates of each piezometer.
    - peizo: piezometer numeric ID.
    - 1m of LOW: whether the piezometer is within 1 m of a large woody debris structure (y/n).
    - Depth and True depth: screened mid-point depth below the riverbed (cm).
    - head: vertical hydraulic gradient (m), measured with piezometers.
    - water depth: depth from river surface to screen depth (cm).
  - Baseline and in situ measurements
    - O2adj, O2adj%: dissolved oxygen concentration and percent saturation in porewater prior to injection.
    - pH, temp: porewater pH and temperature prior to injection.
    - NO2, NO3, NH3, PO4: concentrations in porewater prior to injection (μM).
    - Chloride (mM), CH4 (μM), N2O (nM), Fe II (μM), orgC (mg/L).
  - Isotope and nitrogen transformation metrics
    - p15N2: in situ rate of total 15N2 production (nM N L^-1 h^-1).
    - Denitrification, Anammox, DNRA: in situ rates (nM N L^-1 h^-1).
    - tot15n: sum of denitrification, anammox, and DNRA.
    - qN2, qN2O: proportion of 15N labeling in produced N2 and N2O.
    - %Anammox, %DNRA, %Denitrification: contribution percentages to N2 production.
  - Derived indicators
    - Percentages and ratios derived from isotope labeling to apportion N2 production among pathways.
  - Data quality notes
    - LODs and precision are provided for each measurement method.
    - Calculations rely on calibration factors and known solubility coefficients; specific equations and references are noted in the dataset documentation.

- Temporal and spatial coverage
  - Location: Hammer Stream, a sandy tributary of the River Rother, West Sussex, UK (coordinates provided for each piezometer).
  - Temporal span: four campaigns spanning late 2014 to mid-2015.

- Data quality, limitations, and handling
  - Values below detection limits annotated as 0; missing data marked as ND.
  - O2 contamination during sample transfer estimated and subtracted from O2 data (approximately 10 μM).
  - Detection limits and measurement uncertainties defined for each parameter.
  - Complex multi-method workflow requiring careful metadata management for discoverability and reproducibility.

- Context and references
  - Primary dataset references:
    - Shelley et al. 2017: Enhanced hyporheic exchange flow around woody debris and nitrate reduction in a sandy streambed.
    - Lansdown et al. 2014: Fine-Scale in Situ Measurement of Riverbed Nitrate Production and Consumption in an Armored Permeable Riverbed.
    - Methodological references for isotope and analytical techniques (e.g., Thamdrup & Dalsgaard; Risgaard-Petersen et al.; Trimmer et al.).
  - Data accompany the published studies and provide detailed methodological background for replication and secondary analyses.