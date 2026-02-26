# A brief description/overview of the data being described

- Data collection and scope
  - The PULA water quality data folder contains 25 CSV files, each for one of 25 indicators, including Total Organic Carbon, major ions (e.g., Chloride, Fluoride, Bromine, Sulfate, Potassium, Aluminium, Calcium, Iron, Magnesium, Sodium), trace metals (e.g., Chromium, Manganese, Cobalt, Nickel, Copper, Zinc, Arsenic, Selenium, Molybdenum, Cadmium, Lead) and stable water isotopes (δD and δ18O).
  - Sampling period: February 2017 – May 2018.
  - Collaboration: Botswana Department of Water Affairs, Botswana International University of Science and Technology, and the University of Aberdeen.
  - Geography and purpose: groundwater and surface water from the Gaborone Reservoir catchment area in south-west Botswana; part of the NERC PULA project to assess impacts of extreme rainfall and flooding on water quality across varied geology and land use.

- Experimental design and sampling regime
  - 287 sampling occasions across 41 days, concentrated in ~15 sampling campaigns tied to flood-drought-flood cycles.
  - Spatial coverage aimed to capture regional variability; sites chosen for physiographical diversity and practical access.
  - Water types: surface water (grab samples) and groundwater (pumped grab samples after well flushing).
  - Field protocol: two bottles per analyte type (two for each analysis: one for measurement, one for re-runs if needed); samples labeled in the field; a data collection log captured local sampling conditions (provided separately).
  - Sample handling: samples refrigerated, shipped to University of Aberdeen in four batches; analyses performed promptly upon arrival.

- Analytical methods and instrumentation
  - Trace metals (P, Cr, Mn, Co, Ni, Cu, Zn, As, Se, Mo, Cd, Pb) analyzed by ICP-MS (Agilent 7900) at Aberdeen.
  - Major elements (Al, Ca, Fe, K, Mg, Na) analyzed by MP-AES at Aberdeen.
  - TOC analyzed with a LABTOC instrument.
  - Stable isotopes (δD, δ18O) analyzed with a TWIA-45-EP LGR instrument.
  - Calibration and QA: standard procedures applied; some results exceeded calibration range or fell below detection limits; Pb analyses were largely outside calibration ranges, leading to incomplete Pb data.

- Data structure, units, and metadata
  - Each of the 25 CSV files has a top row describing the columns.
  - Columns include: water type (SW or GW), sampling location name (Botswana DWA formal name), longitude, latitude, elevation (m), and sampling dates (dd/mm/yy).
  - Spatial coordinates: provided in UTM; latitude/longitude in decimal degrees; elevation in metres.
  - Data quality notes: some measurements recorded as below LO D (<LOD) in the CSVs; a minority of samples exceed calibration ranges (notably Pb); blank cells indicate missing values.
  - Data logging: a separate data collection log contains additional site- and sample-specific information.

- Data quality, limitations, and caveats
  - Several analytes show a substantial portion of samples below the detection limit (Cu, Zn, Cd, Pb, Al, Fe, Fl, Br).
  - Pb data are particularly incomplete due to calibration challenges.
  - Temporal and spatial coverage is uneven across campaigns and sites, which may affect trend analyses or spatial comparisons.
  - LODs and calibration ranges vary by time period (data before/after Nov 2017 have different LODs for certain parameters).

- Accessibility and governance considerations
  - Data are accompanied by a data collection log, enabling audit and context for each measurement.
  - Metadata detail supports data provenance, verification, and reuse, aligning with data quality and governance needs for monitoring frameworks.
  - Public sharing considerations exist (explicit metadata and logs aid transparency), though data completeness varies by analyte (notably Pb) and by detection limits across time.

- Relevance for monitoring frameworks
  - Provides a multi-parameter baseline across surface and groundwater within a defined catchment, suitable for evaluating policy-relevant water quality indicators.
  - Demonstrates comprehensive handling of sampling design, field logistics, laboratory workflows, and QA/QC practices.
  - Highlights challenges commonly faced in monitoring datasets: missing metadata, detection-limit issues, calibration-range limitations, and uneven data coverage, informing governance and standardization efforts for future monitoring programs.