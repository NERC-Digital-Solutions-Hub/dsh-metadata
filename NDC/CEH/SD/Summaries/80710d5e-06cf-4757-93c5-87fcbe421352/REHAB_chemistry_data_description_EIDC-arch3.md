# Weekly water quality monitoring data for the River Thames (UK) and its major tributaries (2009-2013): the Thames Initiative research platform

## Overview
- Describes experimental design and data collection for monitoring nutrients and related water quality parameters to assess the impact of sewage effluent and support environmental management.
- Part of a larger Thames Initiative framework, with methods and quality controls documented to ensure data usability for policy and decision-making.
- Information covers sampling design, collection, calibration, analytical methods, data structure, and references for the Thames dataset (2009–2013) and related methods.

## Experimental design / Sampling regime
- Water and sediment samples collected from five rivers receiving sewage effluent.
- Sampling occurred in three rounds (to capture seasonal variation): February/March, June/July, and October/November 2017.
- Design included: two upstream water samples (10 m and 100 m from outfall), a sample of effluent (0 m), and downstream water samples at 10, 100, 250, 500, and 1000 m.
- Aimed to assess the wider impact of sewage effluent on receiving environments.

## Collection methods
- Water collected with a clean 2 L plastic bottle on a sampling pole.
- Bulk samples subsampled into:
  - Two 500 mL bottles for suspended solids and chlorophyll analysis.
  - An amber glass bottle for pH and alkalinity.
  - 60 mL bottles for total metals and total phosphorus (TP) analysis.
- Additional subsamples filtered in the field through a 0.45 µm membrane for dissolved metals, nutrients, anions, and cations.
- Bottles acid-washed; field water temperature measured; samples stored in the dark and returned to the lab within 6 hours.

## Calibration steps and quality control
- Most chemical analyses run with externally calibrated standards traceable to reference standards; batch-wise Aquacheck QC standards used as blind controls.
- QC results checked against assigned values; z-scores (standard scores) assessed; Aquacheck scheme accredited to ISO/IEC 17043.
- Any QC batch >10% deviation retried within 1–2 days; instrument problems leading to degradation resulted in data omission.
- Post-analysis, samples stored in the dark at 4°C until data verification completed.

## Analytical methods
- Total phosphorus (TP) and total dissolved phosphorus (TDP) determined by digestion with acidified potassium persulfate and colorimetric detection (molybdenum-phosphorus complex) for unfiltered and 0.45 µm filtered samples, respectively.
- Soluble reactive phosphorus (SRP) measured by colorimetry (phosphomolybdenum-blue) on filtered samples.
- Ammonium determined by indophenol-blue colorimetric method.
- Dissolved organic carbon (DOC) and total dissolved nitrogen measured with an Elementar Vario Cube analyser.
- Major dissolved anions (fluoride, chloride, nitrite, nitrate, sulfate) measured by ion chromatography.

## Nature and units of recorded values
- SampleID: unique identifier for each sample.
- Date: day, month, year of sampling.
- Location: name of the closest urban area.
- Latitude/Longitude: geographic coordinates of sampling site.
- Site_distance: distance from sewage outfall (negative upstream, positive downstream) in meters.
- Day/Month/Year: individual components of the sampling date.
- Soluble_reactive_phosphorus: μg/L.
- Total_dissolved_phosphorus: μg/L.
- Total_phosphorus: μg/L.
- Dissolved_ammonium: mg/L.
- Dissolved_fluoride: mg F/L.
- Dissolved_chloride: mg Cl/L.
- Dissolved_nitrite: mg NO2/L.
- Dissolved_nitrate: mg NO3/L.
- Dissolved_sulphate: mg SO4/L.
- Total_dissolved_nitrogen: mg N/L.
- Dissolved_organic_carbon: mg/L.

## Details of data structure
- Data provided as a .csv file.
- Rows correspond to samples; columns include site name, location, sampling date, sample name, and water chemistry parameters.

## Data availability / provenance
- Ties to the Thames Initiative dataset documenting weekly water quality data for the River Thames and major tributaries (2009–2013) as described in Bowes et al. (2018) and related methodological references.
- Methods emphasize standardized protocols, quality assurance, and data governance to support open sharing and reproducibility.

## References
- Bowes, M., Armstrong, L., Harman, S., et al. (2018). Weekly water quality monitoring data for the River Thames (UK) and its major tributaries (2009-2013): the Thames Initiative research platform. Earth System Science Data, 10(3), 1637-1653.
- Neal, C., Neal, M., Wickham, H. (2000). Phosphate measurement in natural waters: analytical challenges with silica interference. Science of the Total Environment.
- Neal, C., Bowes, M., Jarvie, H., et al. (2012). Lowland river water quality: UK data resources for process and environmental management analysis. Hydrological Processes.