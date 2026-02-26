# Weekly water quality monitoring data for the River Thames (UK) and its major tributaries (2009-2013): the Thames Initiative research platform

- A data release accompanying a study of how sewage effluent affects receiving freshwater environments and, more broadly, the environmental dissemination of antimicrobial resistant bacteria and genes.
- Five rivers were sampled to examine nutrients and related water chemistry in relation to sewage outfalls, across multiple seasons.

## Experimental design and sampling regime

- Sampling locations and scale
  - River sites with sewage effluent influence; sampling conducted at multiple distances from the effluent source.
- Sampling points per site
  - Upstream: 10 m and 100 m
  - Effluent point: 0 m
  - Downstream: 10 m, 100 m, 250 m, 500 m, and 1000 m
- Temporal coverage
  - Three rounds of sampling to capture seasonal variation (February/March, June/July, October/November) in 2017 (part of a broader study on antimicrobial resistance dissemination).
- Objective
  - Measure a range of nutrients and related water chemistry to assess the wider impact of sewage effluent on receiving environments.

## Collection methods

- Sample collection
  - Bulk river water collected with a clean 2 L bottle on a sampling pole.
  - Subsamples taken into:
    - Two 500 mL bottles for suspended solids and chlorophyll
    - An amber glass bottle for pH and alkalinity
    - 60 mL bottles for total metals and total phosphorus (TP)
  - Field filtration
    - Some samples filtered in the field through a 0.45 µm membrane for dissolved metals, nutrients, anions, and cations analysis
- Handling and storage
  - Bottles acid-washed prior to use
  - In-field measurement of water temperature
  - Samples stored in the dark until lab return (within 6 hours)

## Calibration, quality control, and data integrity

- Calibration and standards
  - Most analyses calibrated against standards from Wallingford Nutrient Chemistry Laboratories.
  - Each batch run with an Aquacheck quality control standard (unknown concentration) to verify accuracy via z-scores.
- QC and re-analysis
  - Aquacheck results assessed against z-score targets (acceptable if z ≤ 2).
  - Batches failing internal QC (>10% off assigned value) re-run within 1–2 days.
  - If instrument problems prevented QC standards from meeting criteria, affected data were omitted.
- Data handling post-analysis
  - After analysis, samples stored in the dark at 4°C until all data were checked.

## Analytical methods

- Nutrient and water chemistry analyses (lab methods)
  - Total phosphorus (TP) and total dissolved phosphorus (TDP)
    - Digestion with acidified potassium persulfate; blue complex quantified spectrophotometrically at 880 nm.
  - Soluble reactive phosphorus (SRP)
    - Colorimetric phosphomolybdenum-blue method (Murphy and Riley, 1962; modified by Neal et al., 2000) on filtered samples.
  - Ammonium
    - Indophenol-blue colorimetric method (in AutoAnalyzer).
  - Dissolved organic carbon (DOC) and total dissolved nitrogen
    - Measured with an Elementar Vario Cube.
  - Major dissolved anions
    - Fluoride, chloride, nitrite, nitrate, sulfate via ion chromatography (Dionex AS50).
- Timing
  - SRP samples analyzed within 48 hours to minimize instability effects.

## Data structure and content

- File format
  - Data provided as a .csv file; samples as rows and variables as columns.
- Key fields and units
  - SampleID: unique sample identifier
  - Date: d/m/y
  - Location: name of the closest urban area
  - Latitude / Longitude: geographic coordinates
  - Site_distance: distance from sewage outfall in meters; negative = upstream, positive = downstream
  - Day / Month / Year: sampling date components
  - Soluble_reactive_phosphorus: μg/L
  - Total_dissolved_phosphorus: μg/L
  - Total_phosphorus: μg/L
  - Dissolved_ammonium: mg/L
  - Dissolved_fluoride: mg F/L
  - Dissolved_chloride: mg Cl/L
  - Dissolved_nitrite: mg NO2/L
  - Dissolved_nitrate: mg NO3/L
  - Dissolved_sulphate: mg SO4/L
  - Total_dissolved_nitrogen: mg N/L
  - Dissolved_organic_carbon: mg/L

## Data provenance and scope

- Context and sources
  - Data are part of a broader research platform (Thames Initiative) examining water quality and environmental processes in the River Thames and major tributaries (2009-2013 data used for the Thames Initiative; see Bowes et al., 2018).
  - Provides the nutrient-related measurements alongside metadata to support analyses of sewage influence and potential links to antimicrobial resistance dissemination.
- Documentation and references
  - Bowes et al. (2018): Weekly water quality monitoring data for the River Thames (UK) and its major tributaries (2009-2013)
  - Neal et al. (2000, 2012): Methodological references for phosphate measurement and UK data resources
- Data accessibility
  - Data are structured for straightforward ingestion into analysis pipelines; dataset includes metadata and QA notes to aid reproducibility and data discoverability.

## Practical notes for analysts

- Useful for correlating proximity to sewage outfalls with nutrient concentrations and potential downstream effects.
- The site_distance metric enables spatial analyses of nutrient gradients relative to the effluent source.
- Seasonal sampling rounds support examination of temporal variability in nutrient concentrations.
- QA procedures (Aquacheck, re-runs, omission criteria) inform data quality assessments and uncertainty considerations.
- Data provenance notes and references help frame methodological choices and enable cross-study comparisons.