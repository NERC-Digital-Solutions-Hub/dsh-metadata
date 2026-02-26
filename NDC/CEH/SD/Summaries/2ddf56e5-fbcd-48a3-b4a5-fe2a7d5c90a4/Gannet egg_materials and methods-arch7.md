# 2.1. Egg sampling and analysis

## Study design and spatial/temporal scope
- Fresh eggs collected from ten nests at each sampling year across two Scottish gannet colonies: Ailsa Craig and Bass Rock.
- For each colony/year, a sub-group of five eggs per year per colony selected randomly for PBDE analysis.
- Data are suitable for spatial-temporal mapping of PBDE concentrations across colonies and years.

## Sample collection and preparation
- Measured for each egg: weight, length, breadth; eggshells washed, air-dried, reweighed; contents homogenised and stored at -20 °C.
- Sub-sample (2 g) subjected to PBDE analysis with internal standard (13C12-labelled) added; soxhlet extraction in dichloromethane.
- Lipid content determined gravimetrically; extract cleaned with acidified silica, then gel permeation chromatography; final fraction prepared for GC-MS.

## PBDE analysis and QA/QC
- GC-MS analysis performed with a specified pesticide column and calibration against a 25-congener PBDE suite.
- Instrument detection limits (LoD) range by congener; concentrations reported on a wet weight basis and corrected for desiccation.
- QC procedures included: multiple blanks (all below LoD), five 13C12-labelled congener recoveries (typical 68–83%), and a QC standard run with each batch (concentrations within ±10% of expected).
- Not all congeners measured: nona-BDEs and BDE209 not determined due to poor recovery with this method.

## Data processing and measurements
- Concentrations corrected for extraction recovery; expressed as ng/g wet weight.
- Desiccation corrections applied using total egg weight/volume ratio.
- Egg volume estimated with V = 0.51 × L × B^2 (L = length, B = breadth).
- Shell index calculated as shell weight /(shell length × breadth); some samples lacked shell index data.
- For each egg, congeners below LoD treated as zero; ΣPBDE = sum of the 25 determined congeners.
- 3 eggs excluded from analyses due to volume/weight outliers (>3 SD from mean).

## Statistical analyses
- All PBDE concentrations log10-transformed to meet homogeneity of variance and normality assumptions.
- Temporal trends assessed with General Linear Model (GLM); colony/year interactions explored via Tukey post-hoc pairwise tests.
- Associations among PBDE congeners evaluated with Pearson correlations.
- Overall relationships between ΣPBDEs, congeners, and shell index or egg volume explored via multiple regression; shell index analyses limited to samples where calculation was possible (Bass Rock: n=46; Ailsa Craig: n=35).

## Limitations and data gaps
- Nona-BDEs and BDE209 not captured in this study due to poor recovery with the employed method.
- Some archived data (DecaBDE) exist but concentrations were below detection in current samples.
- Data quality hinges on sample integrity (damaged eggs excluded) and analyte recovery; some measurements unavailable for all eggs.

## GIS-ready data considerations
- Data components suitable for geospatial visualization: colony location (two sites), sampling year, nest-level sampling, and per-egg PBDE concentrations (25 congeners and ΣPBDE).
- Standardized units, desiccation-corrected values, and log-transformed concentrations facilitate consistent mapping and cross-site comparisons.
- Quality flags and methodological notes (e.g., congeners not measured, recovery rates) should accompany GIS datasets to aid interpretation.