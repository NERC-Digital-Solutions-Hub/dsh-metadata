# West Halladale wildfire burn severity and peat core sampling in Flow Country peatlands

- Location and context:
  - Wildfire in Flow Country peatlands, north of Scotland (Caithness and Sutherland).
  - Burnt roughly 60 km2 of wet heath and blanket bog within a 4000 km2 blanket bog area.
  - Fire originated near Melvich and Strathy, spreading toward West Halladale SSSI and Forsinard Flows National Nature Reserve.
  - Burn severity mapped by NatureScot; plots sampled across severity categories (low, medium, high) and drainage status (drained, undrained/near-natural).
  - High severity largely in drained peatlands; no high severity areas in near-natural southern sections.

- Sampling design and fieldwork (1.2, 1.3):
  - Sampling framework: sampling plots allocated by severity x drainage; each plot size equivalent to a quarter of a British National Grid cell.
  - Plot selection: 10–15 plots per severity x drainage combination; field viability limited by terrain, slope, peat depth, access.
  - Final core set: 34 cores collected across combinations; included two additional plots in drained high severity areas to reach 34.
  - Plot coding: cores named with severity letter (H, M, L) plus drainage status (N for near-natural) and a number (1–15).
  - Field logistics: five field visits in late Feb–Mar 2020; GPS located bottom-left corner of plots; coring with Russian sampler; cores placed in PVC half-pipes, labeled with codename, and logged with top/bottom identified.
  - Data and samples: field notes, photos, coordinates, depth, elevation, vegetation, and core metadata recorded; raw data transcribed to an Excel file; samples stored cold until analysis.

- Datasets and metadata (datasets described in 3.3):
  - Peat_core_coordinate.csv: core-level metadata
    - COREID: unique identifier (based on severity and number)
    - Depth of core: 40–50 cm
    - Lat_(Y)_OSGB, Long_(X)_OSGB: OSGB coordinates
    - Grid_Reference: British Grid coordinate
    - Alt_masl: altitude above sea level
    - Exposure: slope aspect/angle
    - Vegetation: surrounding vegetation description
  - Peat_core_data.csv: per 5 cm core sub-sections (lab measurements)
    - Core and sample identifiers (COREID, DEPTH)
    - Field-derived: SEVERITY, TYPE (DRAINED/UNDRAINED), etc.
    - Measurements: VOL (volume, cm3), WET_PEAT (g), DRY_PEAT (g), BD (bulk density, g cm-3), MOIST% (moisture %), vonPOST (humification index)
    - LOI-related: WET_PEAT10 (g for 10 g sample), DRY_PEAT10 (post-LOI), ASHg (ash), OM% (organic matter %), ASH% (ash %), OC% (organic carbon %), and related conversions
    - Notes: data range values and validity checks applied to ensure physical meaning

- Field and laboratory instruments (2.2, 3.2):
  - Field instruments:
    - GPS device; printed project maps
    - Russian corer; 0.5 m PVC half-pipes; saran wrap; measuring tape
    - Camera and field recording sheets
  - Laboratory instruments and procedures:
    - Measuring tape and knife for sub-sampling; foil; camera; recording sheets
    - Crucibles; precision balances (three- and five-decimal)
    - 100 mL cylinder for volume via water displacement
    - Oven (105°C) and muffle furnace (550°C) for LOI and ash
    - Desiccator; Milli-Q water system
  - Calibration and QA:
    - Balances calibrated per manufacturer instructions with standard weights
    - Data quality checks; removal of sub-samples with weighing errors (e.g., dry weight > wet weight)

- Analytical methods (4.2):
  - Bulk Density (BD) and Moisture Content (MC):
    - BD = dry weight / sample volume; volume from water displacement
    - MC% = ((wet weight - dry weight) / wet weight) × 100
  - Organic Matter (OM) and Ash Content:
    - LOI at 550°C for 4 hours to estimate OM
    - Ash % calculated from dry weights before/after ashing
    - OM% = LOI / dry weight at 105°C × 100
    - OC% = OM% / 2 (assuming 50% organic carbon in OM)
  - Von Post peat humification scale:
    - Rapid, qualitative assessment based on squeeze test and visual/color changes; values from H1 (least decomposed) to H9/H10 (varied end points)
  - Sub-sectioning and data capture:
    - Each core section (0–5 cm increments) analyzed in the laboratory
    - 10 g ± 0.05 g samples for LOI; measurements taken with pre-weighed crucibles
  - Quality control and data cleaning:
    - Sub-samples with measurement inconsistencies removed from analysis

- Timeframe and data handling:
  - Field sampling: 20–16 February to 16 March 2020 (five visits)
  - Covid-related delays: ten cores stored during July 2020; laboratory analyses completed when permitted
  - Data storage: field data transcribed to Excel; raw data organized in ERI folders
  - Data products intended for GIS mapping and spatial analysis of burn severity, drainage status, and peat properties

- End notes and references:
  - Methods referenced for peat density, LOI, and carbon content include Beilman et al. (2009), Chambers et al. (2011), Ekono (1981), Heiri et al. (2001), Melling et al. (2006), Ratcliffe et al. (2018a, 2018b)