# UK estuary greenhouse gas and nutrients data set

## Purpose and scope
- Describes a standardized dataset of greenhouse gas and nutrient measurements across UK estuaries to support environmental monitoring and policy evaluation.
- Seven estuaries sampled as a subset from García-Martín et al. (2021): Clyde, Forth and Tay (central Scotland); Conwy and Clwyd (northern Wales); Dart and Tamar (southwest England).
- Four coordinated sampling campaigns in July and October 2017, and January and April 2018, designed to span salinity gradients.

## Sampling regime
- Estuary sites: Clyde, Forth, Tay, Conwy, Clwyd, Dart, Tamar.
- Sampling approach: axial surveys conducted from rigid inflatable boats or fixed points (bridges) due to logistics.
- Salinity targets: samples taken to span 1, 2, 5, 10, 15, and >25 ppt; exact point selection varied with salinity.
- Sampling points: location varied by survey to maintain coverage along the salinity gradient.
- Measurements at each sample location: physico-chemical parameters (temperature, salinity) in situ; water collected from surface for chemical analyses.

## Field measurements and sample handling
- In situ readings: temperature and salinity at ~10 cm below surface using a Hach HQ30D sensor.
- Water collection: bulk surface water at target salinities; subsamples allocated for various analyses.
- General handling: acid-washed containers; samples split for gas and chemical analyses as appropriate.

## Greenhouse gas sampling and analysis
- Clyde, Clywd, Conwy, Forth, Tay: headspace method with duplicate samples.
  - Sampling: exact volumes of water equilibrated with ambient headspace in a luer-lock syringe; 40 ml water equilibrated with 20 ml headspace; vigorous mixing underwater; samples injected into pre-evacuated 12 ml vials; ambient air collected.
- Tamar and Dart: 500 ml borosilicate bottles; overfilled to remove air; poisoned with mercuric chloride; GC analysis.
- Instrumentation and detection:
  - GC with FID for CH4 and CO2; μECD for N2O (Clyde, Clywd, Conwy, Forth, Tay) with LODs: CH4 40 ppb, CO2 5000 ppb, N2O 5 ppb.
  - Tamar/Dart: single-phase equilibration GC with FID (CH4) and ECD (N2O); calibrations traceable to NOAA WMO standards.
- Calculations and corrections:
  - Total dissolved gas derived from headspace and ambient air concentrations using Henry’s Law and temperature/salinity corrections (Bunsen solubility; Weiss & Price, 1980; Wiesenburg & Guinasso, 1979).

## Water chemistry analyses
- Dissolved organic carbon (DOC): measured at UKCEH Lancaster using a Shimadzu TOC-L after filtration (0.45 μm); LoD 0.6 mg/L C.
- Total dissolved carbon (TDC): freshwater samples include inorganic carbon removal step; LO D part of method; reflects both inorganic and organic carbon.
- Freshwater nutrients (Position 1; with Conwy exception): 
  - Nitrate + nitrite (NO3-N + NO2-N): ion chromatography; LoD 0.06 mg/L N.
  - Ammonium (NH4-N): indophenol blue colorimetry; LoD 0.033 mg/L N.
  - Total Nitrogen (TN): Shimadzu TOC-L with TNM-L; LO D 0.08 mg/L N.
  - Total Phosphorus (TP) and soluble phosphate (PO4-P): digestion and molybdenum blue colorimetry; LoD TP 0.008 mg/L; PO4-P LoD 0.005 mg/L.
- Saline nutrients (Positions 2–6; Plymouth Marine Laboratory):
  - Analysis by SEAL Analytical AAIII autoanalyser; methods per Brewer & Riley (nitrate + nitrite), Grasshoff (nitrite), Mantoura & Woodward (ammonium), Kirkwood (phosphate and silicate); LoDs vary by analyte (e.g., NO3-, PO4, SiO4: ~0.02 μM/L; NO2-: 0.01 μM/L; NH4+: 0.04 μM/L).
  - GO-SHIP protocols followed for sample handling and processing.

## Data structure, units, and quality control
- Units and columns described in Table 1 of the dataset (Estuary, Position 1–6, Lat, Long, Day, Month, Year, Salinity, Temperature, etc.).
- Data values reported to two decimal places.
- Missing values: flagged with an asterisk in the CSV; freshwater and saline datasets are analyzed at different laboratories, leading to gaps where data are not available in certain columns.
- Positioning:
  - Position 1: furthest upstream (freshwater)
  - Position 6: furthest downstream (saline)
- Recorded substances include: NO3-N, NO2-N, NH4-N, Silicate (SiO4), PO4-P, TP, TN, DOC, TDC, CH4, CO2, N2O, and corresponding saturation values (N2O sat, CH4 sat, CO2 sat).

## Data provenance and references
- Methods and dataset provenance draw on:
  - Becker et al. 2020 (GOSHIP nutrient manual)
  - García-Martín et al. 2021 (estuarine dissolved organic matter processing)
  - Standard methods for nitrite, nitrate, ammonium, phosphate, and GO-SHIP protocols
  - Foundational high-precision methane and nitrous oxide measurement techniques (Upstill-Goddard et al. 1996; related solubility references Weiss & Price, 1980; Wiesenburg & Guinasso, 1979)

## Relevance to environmental monitoring and data analysis
- Demonstrates a standardized, QA-driven approach to collecting and transforming environmental monitoring data.
- Outputs are presented in clear formats (tables, figures) and datasets are intended to be stored/uploaded to appropriate data portals.
- Highlights ongoing challenges and opportunities for analysts:
  - Increasing the utility of datasets by integrating with additional data sources (e.g., hydrology, land-use, climate data).
  - Ensuring broad access to underlying data to enable reproducibility and secondary analyses.