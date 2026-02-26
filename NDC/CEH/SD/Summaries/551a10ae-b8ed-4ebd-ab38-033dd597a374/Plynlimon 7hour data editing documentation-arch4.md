# Metadata: Quality control and data editing

- Overview of the dataset
  - Plynlimon 7-hourly intensive hydrochemistry data set: rainfall and streamflow samples collected every 7 hours for nearly two years.
  - Released in two versions: Raw Data Archive (RDA) and edited data.
  - RDA preserves raw laboratory measurements with traceable, minimal corrections; edited data are the high-confidence, cleaned version intended for routine analyses.

- Raw Data Archive (RDA) vs edited data
  - RDA: unaltered except for traceable glitch corrections; allows return to original values if new information arises.
  - Edited data: removes unreliable values (flyers, outliers) and applies consistency checks; retains some controversial blocks if they plausibly reflect real patterns or mirror corrections in related analytes.

- Editing philosophy and criteria
  - Focus on data that pass a high confidence standard; problematic values are corrected or removed.
  - Expert judgment used to handle:
    - discrepancies between co-varying analytes
    - differences between 7-hourly and weekly sampling
    - abrupt, implausible shifts in variability across blocks
    - potential sample contamination, labeling errors, or carryover effects
  - Where feasible, consistency checks guide edits (e.g., SO4 with S, alkalinity with pH, charge balance, ANC vs Gran alkalinity, TDN with N species, ionic strength with conductivity).

- Data quality checks and consistency rules
  - Systematic cross-checks performed to identify and cull inconsistent data
  - Examples of correlations used to validate edits include: F with NH4, NO2 with nothing, Cl with Mg/Na/conductivity, Ca with Mg/Si/pH and with alkalinity
  - When a value conflicted with multiple co-varying analytes, it was prioritized as likely erroneous and culled
  - For derived or cross-checked quantities (e.g., SO4_by_ICP from edited S), edited values drive the derived series

- Sampling design and data structure
  - Sampling sites: rainfall at Carreg Wen (CR); streams at Lower Hafren (LHF) and Upper Hafren (UHF)
  - 7-hourly sampling versus long-term weekly sampling; autosamplers used for the 7-hourly data
  - Rainfall data from weekly samples can be averaged volume-weighted to compare with 7-hourly data
  - Annotations note occasional sample swaps or mislabeling between analytical blocks or trips; such issues are corrected in edited data (e.g., acidified vs un-acidified analyses swapped between trips)

- Data curation actions and notable examples
  - Large blocks of data culled where calibration problems or anomalous patterns were evident
  - Carryover from check standards (introduced every 10 samples) culled when evident (e.g., “picket fence” effects in low-level analytes)
  - Repeating “picket fence” spikes (e.g., Ca, Sc) addressed with ad hoc shifts or culling
  - Specific attention to alignment between ion chromatography data and ICP-OES/ICP-MS data (e.g., SO4 and SO4_by_ICP alignment after a suspected trip swap)
  - Several analytes had substantial culling in particular analytical blocks or entire time series (e.g., W omitted entirely; Cu culled across long periods; Sn largely removed from stream data)

- Per-analyte notes and data presentation
  - Analyses are organized in two groups: (1) IC/electrochemical/autoanalysis methods (in order of increasing atomic number), then (2) cations/metals (ICPOES/ICP-MS, in order of increasing atomic number)
  - Some measurements use unfiltered samples (conductivity, pH, Gran alkalinity, Gran acidity) while solute concentrations use filtered samples; historical tests suggested no significant differences for these analytes
  - Iodine (I) is not edited due to a short record
  - Tungsten (W) is omitted entirely from edited data due to pervasive low values and correction issues
  - Fluoride (F) is mostly culled due to early calibration issues
  - Don (dissolved organic nitrogen) is calculated from edited TDN, NO3, NO2, and NH4; negative DON values may occur due to uncertainties
  - Some low-concentration measurements (e.g., U) are retained but should be interpreted with caution; absolute values may be near detection limits
  - Lead (Pb) data culled in precipitation due to large disparities with weekly samples
  - Data integrity notes emphasize that certain blocks or samples may reflect process issues rather than true environmental signals

- Data provenance, accessibility, and usage cautions
  - The edited dataset is designed for routine analyses with documented editing decisions and a clear rationale
  - Raw data remain available for transparency and potential reanalysis if needed
  - Users should be aware of potential residual calibration issues, block-level shifts, carryover, and the caution required when interpreting very low concentrations
  - The two datasets differ in values where edits were applied; understanding the editing rationale is essential for valid interpretation

- Practical implications for data leaders
  - Emphasizes the importance of documenting data edits, provenance, and quality checks to enable trust and reuse
  - Demonstrates the role of expert judgment in data curation, especially when dealing with multi-method, multi-site time series
  - Highlights the necessity of consistency checks across related variables to distinguish real signals from artifacts
  - Underlines the value of clearly communicating data limitations, measurement protocols (filtered vs unfiltered), and any known anomalies or corrections to end users