# Soil chemical properties from a field experiment in the Conwy Valley, North Wales, UK (20156) Metadata for Soil_properties.csv

## Overview
- Metadata accompanying the Soil_properties.csv dataset from a field experiment in Conwy Valley, North Wales (2015–2016).
- Documents experimental design, sampling regime, collection methods, analytical methods, data structure, quality control, and supporting files.
- Provides detailed descriptions of measured soil properties, units, and laboratory procedures to support data discovery, reuse, and governance.

## Experimental design and sampling regime
- Three transects, each 75 metres long and spaced 20 m apart, across the hillslope perpendicular to the river.
- Along each transect, intact soil cores were extracted at 2 m, 12 m, and 75 m distances in May 2016.
- Core length determined by soil depth or impermeable boundary identified by a geophysical survey; rows denote core lengths (row 1 = 1 m, row 2 = 2 m, row 3 = 3 m; n = 18 × 1 m cores).
- Cores: 4 cm diameter, wrapped in thin-walled polyethylene sleeves to preserve integrity, transported to the lab, and stored at 4°C prior to analysis.
- Field collection instrument: Cobra percussion hammer corer.

## Collection and laboratory methods
- Field and lab workflow documented and standardised to enable reproducibility.
- Analyses performed at Bangor University, School of Environment, Natural Resources and Geography.
- Key measurements (examples):
  - Soil water content (gravimetric, 105°C, 24 h)
  - Organic matter (LOI, 450°C, 16 h)
  - pH and electrical conductivity (1:2.5 soil-to-water extract)
  - Available nitrogen and phosphorus (NH4-N, NO3-N, PO4-P) via established extraction and colorimetric methods
  - Total carbon (TC) and total nitrogen (TN) via TruSpec elemental analyser
  - Dissolved organic carbon (DOC) and total dissolved nitrogen (TDN) via 1:5 soil-to-solution extracts and TOC analyzer
  - Microbial biomass C and N via chloroform fumigation (72 h, k_ec = 0.45; k_en = 0.54)
  - PLFA analysis for microbial community profiling (96-well high-throughput format)
  - Phosphorus sorption: 1.0 g soil with CaCl2 extractant and varying P concentrations, using 33P tracer and scintillation counting; adsorption estimated from solution-phase activity; Langmuir isotherm used to estimate P adsorption maxima
- Documentation of specific methods and equations cited (e.g., Mulvaney 1996; Miranda et al. 2001; Murphy & Riley 1962; Nair et al. 1984; Langmuir-based approaches).

## Nature and units of recorded values
- Values align with column names described in Detail of data structure.
- Units and data types reflect standard soil chemistry reporting (e.g., pH, EC in µS/cm, moisture %, LOI %, TOC mg/g, TDN mg/g, microbial C/N mg/g, PO4_P mg/kg, NH4_N mg/kg, NO3_N mg/kg, TC g/kg, TN g/kg, C:N ratio, Pmax mg/kg, NH4Adsorp mg/kg).
- Empty cells indicate missing data.

## Data structure and column descriptions
- Core structural fields:
  - Transect (numeric), Row (numeric), Depth (cm)
- Measured variables (examples):
  - pH, EC (µS/cm), MC (moisture content %), LOI (%), TOC (mg/g), TDN (mg/g)
  - Microbial_C (mg/g), Microbial_N (mg/g), PO4_P (mg/kg)
  - NH4_N (mg/kg), NO3_N (mg/kg), CtoN_ratio
  - TC (g/kg), TN (g/kg)
  - Pmax (mg/kg), NH4Adsorp (mg/kg)
- Data availability notes: some fields may be empty where data were not collected or not applicable.

## Quality control and provenance
- All samples analyzed in triplicate to support reproducibility and error estimation.
- Clear linkages to field plots (Plot_locations.csv) and accompanying metadata (Plot_locations_metadata.rtf) for locational context.
- Metadata and data structure are designed to support data discovery, reuse, and governance, including clear definitions of variables and units.

## Supporting documentation and data governance notes
- Plot_locations.csv: details of plot locations.
- Plot_locations_metadata.rtf: description of Plot_locations.csv.
- Emphasises the importance of metadata completeness for discoverability and interoperability.
- For data stewards: ensure ongoing availability, versioning, and traceability; maintain cross-references between Soil_properties.csv and its supporting location metadata; verify consistent units and column naming across datasets to facilitate reuse and interoperability.