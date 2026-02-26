# Experimental design/Sampling regime

- Aims and scope
  - Study of environmental dissemination of antimicrobial resistant bacteria and genes by sampling water and sediment from five rivers influenced by sewage effluent in 2017.
  - Focus on a range of nutrients to assess wider environmental impact of sewage effluent on receiving environments.
  - Design includes upstream (10 m and 100 m), effluent (0 m), and downstream (10, 100, 250, 500, 1000 m) sampling to capture spatial gradients; three rounds to capture seasonal variation (Feb/Mar, Jun/Jul, Oct/Nov).

- Sampling design
  - Three sampling occasions in 2017 across five rivers receiving sewage effluent.
  - Location sequence: upstream (two points), outfall, downstream at multiple distances up to 1000 m.
  - Seasonal replication to identify temporal variation.

- Collection methods
  - Bulk water collected with a clean 2 L bottle on a sampling pole.
  - Subsamples taken into:
    - Two 500 mL bottles for suspended solids and chlorophyll.
    - An amber glass bottle for pH and alkalinity.
    - 60 mL bottles for total metals and total phosphorus.
  - Field filtration: additional subsamples filtered through a 0.45 μm membrane into 60 mL bottles for dissolved metals, nutrients, anions, and cations.
  - Bottles acid-washed; in-field water temperature measured.
  - Samples stored in the dark and returned to the lab within 6 hours.

- Calibration steps and quality control
  - Analyses (except some solids/chlorophyll/alkalinity) calibrated with Wallingford Nutrient Chemistry Laboratories standards; batch runs include Aquacheck QC standards.
  - QA/QC validated via blind testing against known Aquacheck values; performance assessed with z-scores (ISO/IEC 17043).
  - Some batches failed QC (>10% deviation) and were rerun; data omitted if instrument problems prevented timely analysis.
  - Post-analysis storage: samples kept in the dark at 4°C until data verification completed.

- Analytical methods
  - Total phosphorus (TP) and total dissolved phosphorus (TDP) determined by digestion with acidified potassium persulfate, followed by colorimetric measurement (molybdenum-blue) at 880 nm.
  - Soluble reactive phosphorus (SRP) measured on filtered samples via phosphomolybdenum-blue method (Murphy and Riley, modified by Neal et al.).
  - Ammonium determined by indophenol-blue colorimetric method.
  - Dissolved organic carbon (DOC) and total dissolved nitrogen measured with Elementar Vario Cube.
  - Major dissolved anions (fluoride, chloride, nitrite, nitrate, sulfate) measured by ion chromatography (Dionex AS50).

- Nature and units of recorded values
  - SampleID: unique sample identifier.
  - Date: day/month/year of sampling.
  - Location: closest urban area name.
  - Latitude / Longitude: geographic coordinates.
  - Site_distance: distance from sewage outfall in meters (negative upstream, positive downstream).
  - Day / Month / Year: date components.
  - Soluble_reactive_phosphorus: μg/L.
  - Total_dissolved_phosphorus: μg/L.
  - Total_phosphorus: μg/L.
  - Dissolved_ammonium: mg/L.
  - Dissolved_fluoride: mg/L.
  - Dissolved_chloride: mg/L.
  - Dissolved_nitrite: mg/L (as NO2).
  - Dissolved_nitrate: mg/L (as NO3).
  - Dissolved_sulphate: mg/L (as SO4).
  - Total_dissolved_nitrogen: mg/L.
  - Dissolved_organic_carbon: mg/L.

- Details of data structure
  - Data provided as a .csv file.
  - Rows represent samples; columns include site name, location, sampling date, sample name, and water chemistry parameters.

- Data accessibility and reuse considerations
  - Dataset supports analysis of nutrient dynamics and metal concentrations relative to sewage discharge location and across seasons.
  - Useful for exploring spatial (upstream vs downstream) and temporal patterns in phosphorus forms, nitrogen species, ammonium, DOC, and major anions.
  - Users should note QC outcomes and potential data omissions due to instrument issues; refer to QC notes and supplementary Table S1 for detection limits and uncertainty.
  - Standardized units and consistent naming (e.g., “sulphate”) facilitate cross-study comparability.

- References
  - Bowes et al. (2018) on weekly water quality monitoring data for the River Thames and major tributaries.
  - Neal et al. (2000) on phosphate measurement methodologies and interference considerations.
  - Neal et al. (2012) on lowland river water quality data resources for analysis.