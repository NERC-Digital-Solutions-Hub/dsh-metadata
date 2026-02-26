# Water quality monitoring data for rivers receiving sewage effluent (2017)

- Aim and scope
  - Describes nutrient measurements to assess the wider impact of sewage effluent on the receiving environment.
  - Sampling of water and sediment from five rivers that receive sewage effluent, conducted over three occasions in 2017 as part of a larger study on antimicrobial resistant bacteria and genes.
  - Design intended to capture seasonal variation (February/March, June/July, October/November).

- Experimental design and sampling regime
  - Upstream samples collected at 10 m and 100 m from the sewage outfall, an effluent sample at 0 m, and downstream samples at 10, 100, 250, 500 and 1000 m.
  - Three rounds to reflect seasonal changes.

- Collection methods
  - Bulk water collected with a clean 2 L bottle on a sampling pole.
  - Subsampling into: two 500 mL bottles (suspended solids and chlorophyll), an amber glass bottle for pH and alkalinity, and 60 mL bottles for total metals and total phosphorus (TP).
  - Field filtration through a 0.45 µm membrane into 60 mL bottles for dissolved metals, nutrients, anions and cations.
  - All bottles acid-washed prior to use; field temperature measured; samples stored in the dark and returned to the lab within 6 hours.

- Calibration steps, quality control and data validity
  - Analyses (except solids/chlorophyll/alkalinity) performed with calibration standards traceable to reference standards; included Aquacheck quality control standards (unknown concentration).
  - QC results checked against assigned values; z-scores (standard scores) used; QC protocol aligned with ISO/IEC 17043; accreditation by UKAS.
  - Individual batches rerun if QC deviated (>10% from the assigned value); if issues persisted due to instrument problems, affected data omitted.
  - Post-analysis, samples stored in the dark at 4°C until data verification completed.

- Analytical methods
  - Total phosphorus (TP) and total dissolved phosphorus (TDP) determined after digestion with acidified potassium persulfate; quantification via spectrophotometry at 880 nm.
  - Soluble reactive phosphorus (SRP) measured on filtered samples using phosphomolybdenum-blue colorimetry (Murphy and Riley, modified by Neal et al., 2000).
  - Ammonium determined by indophenol-blue colorimetric method.
  - Dissolved organic carbon (DOC) and total dissolved nitrogen (TDN) analyzed with a Vario Cube analyzer.
  - Major dissolved anions (fluoride, chloride, nitrite, nitrate, sulfate) determined by ion chromatography.

- Data structure and units
  - SampleID: unique identifier per sample.
  - Date: day, month, year (d/m/y).
  - Location: closest urban area.
  - Latitude/Longitude: geographic coordinates.
  - Site_distance: distance from sewage outfall (meters; upstream negative, downstream positive).
  - Day/Month/Year: sampling date components.
  - Soluble_reactive_phosphorus: μg/L.
  - Total_dissolved_phosphorus: μg/L.
  - Total_phosphorus: μg/L.
  - Dissolved_ammonium: mg/L.
  - Dissolved_fluoride: mg/L.
  - Dissolved_chloride: mg/L.
  - Dissolved_nitrite: mg/L.
  - Dissolved_nitrate: mg/L.
  - Dissolved_sulphate: mg/L.
  - Total_dissolved_nitrogen: mg/L.
  - Dissolved_organic_carbon: mg/L.

- Data structure and delivery
  - Data provided as a .csv file with samples as rows; columns for site name, location, sampling date, sample name, and water chemistry parameters.

- References and provenance
  - Bowes et al. (2018) for related methods and quality control context; supplementary materials (Table S1) include data accuracy and uncertainty details.
  - Foundational analytical references include Neal et al. (2000, 2012) and Eisenreich et al. (1975) for phosphorus methodologies.

- Data governance and stewardship implications
  - Emphasizes the importance of clear metadata (dates, locations, sample IDs, site distances, units) and traceable QA/QC processes for reuse.
  - Highlights need for consistent formatting, standard units, and documentation of any data omissions due to QC failures or instrument issues.
  - Supports data sharing and discoverability through well-defined data structure, documented methods, and references to methodological standards.