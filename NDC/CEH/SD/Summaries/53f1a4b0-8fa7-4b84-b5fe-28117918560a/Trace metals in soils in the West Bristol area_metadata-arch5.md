# Outdoor and indoor cadmium distributions near an abandoned smelting works and their relations to human exposure.

## Purpose and scope
- Characterizes cadmium distributions in soils near an abandoned smelting works and examines relations to human exposure.
- Documents related metal concentrations (Al, Cr, Fe, Cu, Zn, Ni, As, Pb, Hg) and associated analytical methods.

## Data collection design
- Two soil sampling approaches: a nested grid-based survey within a broader grid.
- Sampling plan: 44 locations sampled in October 2007.
- Spatial design: 1 km grid within 5 km of the smelter; 5 km grid from 5 to 15 km (westerly sampling limited by Bristol Channel).
- At each site: five 15 cm deep × 4 cm diameter soil cores collected within a 10 m × 10 m area, then pooled to form a homogeneous sample.

## Laboratory methods and analytes
- Digestion: total metal concentrations determined after aqua regia digestion (0.5 g soil with 12 ml aqua regia) using microwave digestion at 200 °C.
- Instrumentation: inductively coupled plasma mass spectrometry (ICP-MS) with matrix-matched calibrants; internal standards Ga, In, Re to correct drift.
- Analytes: Cd and a suite of metals—Al, Cr, Cu, Zn, Ni, As, Pb, Hg.
- Detection limits: Cd detection limit = 0.02 μg g^-1.
- Quality control: inclusion of certified soil (ISE 921) with each batch; recoveries for Cd and other elements reported (Cd 96.3%; Al 42.3%; Cr 78.0%; Cu 89.5%; Zn 85.7%; Ni 85.6%; As 104%; Pb 93.4%; Hg 109%).

## Data processing and measurement metadata
- Soil processing: air-dried; removal of roots/stones; 2 mm sieve; coning and quartering; milling with non-metallic agate mill; thorough homogenization.
- Additional measurements: soil organic matter content and pH.
  - Organic matter: furnace combustion at 375 °C.
  - pH: electrode measurement on a soil:water mixture (1:2.5 by volume).

## Dataset structure and metadata (AVONMOUTH context)
- Columns include: Site number; Easting (Ordnance Survey Easting); Northing (Ordnance Survey Northing); Site description; Distance to smelter (km); Soil pH; Loss On Ignition; Metals (Al, Cr, Fe, Cu, Zn, Ni, As, Cd, Hg, Pb) with units (mg/kg) and methods (ICP-MS for most; specific techniques noted for each element).
- Explanation/Units and Method for each variable are specified to ensure consistent interpretation and interoperability.

## Data quality, provenance, and governance
- Provenance: explicit sampling design, site locations, and depth sampling; standardized preparation and analysis procedure; use of QA/QC materials.
- Quality indicators: instrument detection limits, recovery data from certified reference material, and internal standard corrections to address drift.
- Metadata considerations for data stewards:
  - Clearly document sampling dates, locations, depths, and pooling strategy.
  - Include detailed method metadata (digestion, instrumentation, internal standards, calibration approach).
  - Attach QA/QC results (recovery percentages, blanks, detection limits).
  - Note any spatial biases or limitations (westerly sampling constraint due to Bristol Channel).

## Data sharing and reuse considerations
- Temporal scope: data collected in October 2007; potential need to annotate temporal context and any subsequent re-analyses.
- Spatial scope: within 15 km of the smelter with defined grid schemes; consider geospatial metadata for reproducibility.
- Data should be accompanied by clear column definitions, units, and method descriptions to enable cross-study comparability (e.g., alignment with AVONMOUTH.csv metadata).

## Practical notes for data stewards
- Ensure consistent unit handling (mg/kg) and harmonize any historical data with current standards.
- Preserve sample-level metadata (location IDs, coordinates, depth, pooling notes) to support traceability.
- Link dataset to referenced material (Allen 1989; Jones 1991; Spurgeon et al. 2008) for methodological justification and context.

## References
- Allen, S. E. Chemical Analysis of Ecological Materials. 1989.
- Jones, D. T. Biological Monitoring of Metal Pollution in Terrestrial Ecosystems. 1991.
- Spurgeon, D. J. et al. Geographical and pedological drivers of distribution and risks to soil fauna of seven metals. Environmental Pollution, 2008.