# Coastal Biodiversity Ecosystem Service Sustainability (CBESS) the erosion rate of sediment cores from salt marsh sites at Morecambe Bay and Essex

- Purpose and scope
  - Dataset measures erosion rate of sediment cores from salt marsh sites, expressed as % mass loss per hour.
  - Experiment uses 16 cm diameter, 30 cm height cores placed in a flume tank flow to simulate three “waterfall” flows: Low, Medium, and High.
  - Erosion rate derived from mass loss over a 30-minute interval for each flow, with hourly conversion.

- Study locations and site characteristics
  - Essex sites: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM).
  - Morecambe Bay sites: Cartmel Sands (CS), Warton Sands (WS), West Plain (WP).
  - Site descriptions reflect two contrasting soil types: clay soils in Essex, sandy soils in Morecambe Bay.
  - Broad regional differences in inundation frequency, creek structure, and dominant grazing/vegetation.
  - Grazing regimes differ by site: Essex heavily grazed by geese and hares; Morecambe Bay heavily grazed by sheep with goose grazing; West Plain lightly grazed.

- Sampling timeframe and context
  - Field campaign conducted in Winter and Summer 2013.
  - Essex winter samples collected during an additional window: 2–6 March 2013.

- Variables and data structure
  - Core-level measurements: one large sediment core per 1 m x 1 m quadrat, with above-ground vegetation recorded.
  - For each core, erosion rate calculated from mass loss at times 0, 5, 10, 15, and 30 minutes during the 1.5-hour flume run.
  - Observed variables include two blocks (1 and 2) describing the same core procedure and measurements.
  - Key data fields (example): Season (Winter W / Summer S), Location (Essex E / Morecambe M), Site (AH, FW, TM, CS, WS, WP), Habitat (Mudflat MF / Saltmarsh SM), Quadrat Number, Scale (A-D with corresponding ranges), L_%massloss (low velocity), M_%massloss (medium velocity), H_%massloss (high velocity).

- Calibration and instrumentation
  - Stagnation pressures: Low 61 Pa, Medium 146 Pa, High 351 Pa.
  - All procedures followed field and/or laboratory methods as applicable.

- Data quality, treatment, and caveats
  - Statistical treatment of observations: none indicated.
  - Data checking procedures: none indicated.
  - Notable data issues: some cores destroyed at high flow; low-flow measurements can yield negative %mass loss due to initial water saturation.
  - Reliability guidance: results from medium flow are more reliable and should be preferentially used in overall modelling.

- Data format and accessibility
  - File format: Excel workbook.
  - Metadata and dataset field descriptions provided, including nominal row numbering and coded values for several fields.

- Practical implications for analysis
  - Enables cross-site comparisons of erosion rates under different hydrodynamic forces and soil types.
  - Supports modelling of erosion under varying grazing regimes and vegetation, by linking erosion metrics with site-specific context.
  - Medium-flow erosion rates recommended as the primary proxy for model calibration due to higher reliability.