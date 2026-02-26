# Outdoor and indoor cadmium distributions near an abandoned smelting works and their relations to human exposure

- Purpose and scope
  - Study of cadmium (Cd) and related metal distributions in soils near an abandoned smelting works and implications for human exposure.
  - Data generated include total metal concentrations (Cd and Al, Cr, Cu, Zn, Ni, As, Pb, Hg), soil organic matter, and pH.

- Data assets and schema
  - Data dictionary (AVONMOUTH.csv) defines:
    - Site identifiers and coordinates (site number, Easting, Northing) with units (Ordnance Survey).
    - Spatial and descriptive fields (site description, distance to smelter in kilometres).
    - Chemical measurements (soil pH, Loss On Ignition, and metal concentrations in mg/kg).
    - Methods for each measurement (e.g., ICPOES for Al, ICPMS for Cd, Cr, Cu, Zn, Ni, As, Pb, Hg).
    - Metadata notes clarifying units and acronyms (ICPMS, ICPOES).

- Study design and data collection
  - Two soil sampling sets: grid-based nested design.
  - Spatial layout:
    - 1 km grid within 5 km of the smelter.
    - 5 km grid extending to 15 km from the site (westerly sampling limited by Bristol Channel).
  - Sampling locations: 44 locations sampled in October 2007.
  - At each location: five separate soil cores (15 cm deep × 4 cm) collected within a 10 m × 10 m area and pooled to form a single sample.

- Laboratory processing and analysis
  - Sample preparation:
    - Soils air-dried, roots/stones removed, homogenized; sieved through 2 mm mesh.
    - Coning and quartering for sub-sampling; milled with non-metallic agate mill.
  - Digestion and measurement:
    - Aqua regia digestion: 0.5 g soil with 12 mL aqua regia, heated to 200 °C in a microwave digestion system (EPA 3051A-based protocol).
    - Elemental analysis by ICP-MS (Elan DRC II) using matrix-matched calibrants.
    - Internal standards: Ga, In, Re to correct instrument drift.
  - Detection limits and quality control:
    - Cd detection limit: 0.02 μg g^-1 (4× SD of blanks, adjusted for sample weight and digestion volume).
    - QA: certified reference soil (ISE 921) included with each batch; recoveries observed as Cd 96.3%, Al 42.3%, Cr 78.0%, Cu 89.5%, Zn 85.7%, Ni 85.6%, As 104%, Pb 93.4%, Hg 109%.
  - Additional measurements:
    - Soil organic matter by furnace combustion at 375 °C (LOI method).
    - Soil pH measured by electrode in a 1:2.5 soil:water suspension.

- Variables and data interpretation
  - Primary variables: total concentrations of Cd and a suite of metals (Al, Cr, Cu, Zn, Ni, As, Pb, Hg) in mg/kg.
  - Supporting soil properties: organic matter content (LOI) and pH, aiding interpretation of metal mobility and bioavailability.

- Data provenance and references
  - Methods aligned with established protocols:
    - Allen, 1989 for LOI and pH measurement references.
    - Jones, 1991 and Spurgeon et al., 2008 for previous soil monitoring approaches and regional context.
  - Spurgeon et al. (Environmental Pollution, 2011) as the primary source detailing the sampling design, processing, and analytic approach described here.

- Implications for data strategy (Data Leaders perspective)
  - Robust data dictionary with explicit units and measurement methods enhances discoverability and cross-study comparability.
  - Standardized sampling design (grid-based, nested) and QA procedures support reliable spatial analysis and exposure assessment.
  - Comprehensive metadata (methods, detection limits, recovery data) strengthens data quality assessment and governance.
  - Availability of spatial coordinates (Easting/Northing) enables GIS-based visualization and integration with other environmental datasets.
  - Documentation of limitations (variable recoveries by element, element-specific QA outcomes) informs interpretation and potential data gaps.