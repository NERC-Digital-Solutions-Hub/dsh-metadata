# Water and sediment sampling from five rivers receiving sewage effluent: nutrient measurements and QA/QC (2017)

## Overview
- Part of a larger study on environmental dissemination of antimicrobial resistant bacteria and genes.
- Collected water and sediment samples from five rivers in 2017 to measure nutrients and related parameters.
- Sampling captured upstream, near-source, and downstream locations to assess sewage effluent impact.
- Three sampling rounds to capture seasonal variation: February/March, June/July, October/November.

## Experimental design and sampling regime
- Upstream samples at 10 m and 100 m from the sewage outfall.
- Effluent sample at 0 m.
- Downstream samples at 10, 100, 250, 500, and 1000 m from the outfall.
- Three rounds of sampling aligned with seasonal windows.

## Collection methods
- Water collected with a clean 2 L bottle on a sampling pole.
- Bulk samples sub-sampled into:
  - Two 500 mL bottles for suspended solids and chlorophyll.
  - An amber glass bottle for pH and alkalinity.
  - 60 mL bottles for total metals and total phosphorus (TP).
- Additional subsamples filtered in the field (0.45 µm) for dissolved metals and nutrients; collected in 60 mL bottles.
- All bottles acid-washed prior to use.
- In-field measurements included water temperature.
- Samples stored in the dark and returned to the laboratory within 6 hours.

## Calibration, quality control and data quality
- Most analyses run with externally calibrated standards traceable to reference standards.
- Included Aquacheck quality control standards (unknown concentration) as blind tests; z-scores checked against ISO/IEC 17043 accreditation.
- Occasional QC batch failures (>10% deviation) rerun within 1–2 days until QC met.
- If instrument problems prevented timely analysis, data for affected samples were omitted.
- Post-analysis, samples stored at 4 °C in the dark until QA checks completed.

## Analytical methods
- Total phosphorus (TP) and total dissolved phosphorus (TDP): digestion with acidified potassium persulfate, followed by colorimetric quantification.
- Soluble reactive phosphorus (SRP): colorimetric phosphomolybdenum-blue method after filtration.
- Ammonium: indophenol-blue colorimetric method.
- Dissolved organic carbon (DOC) and total dissolved nitrogen (TDN): Elementar Vario Cube.
- Major dissolved anions (fluoride, chloride, nitrite, nitrate, sulfate): ion chromatography (Dionex).
- SRP analyzed within 48 hours to minimize instability.

## Nature and units of recorded values
- SampleID: unique sample identifier.
- Date/Day/Month/Year: sampling date components.
- Location: closest urban area name.
- Latitude/Longitude: geographic coordinates.
- Site_distance: distance from sewage outfall in meters (negative upstream, positive downstream).
- Nutrient and chemistry columns include:
  - Soluble_reactive_phosphorus (µg/L)
  - Total_dissolved_phosphorus (µg/L)
  - Total_phosphorus (µg/L)
  - Dissolved_ammonium (mg/L)
  - Dissolved_fluoride (mg/L)
  - Dissolved_chloride (mg/L)
  - Dissolved_nitrite (mg/L)
  - Dissolved_nitrate (mg/L)
  - Dissolved_sulphate (mg/L)
  - Total_dissolved_nitrogen (mg/L)
  - Dissolved_organic_carbon (mg/L)

## Data structure and format
- Data provided as a CSV file.
- Rows represent samples; columns include site name, location, sampling date, sample name, and water chemistry parameters.

## References
- Bowes, M. et al. (2018). Weekly water quality monitoring data for the River Thames (UK) and its major tributaries (2009-2013): the Thames Initiative research platform. Earth System Science Data.
- Neal, C. et al. (2000). Phosphate measurement in natural waters: analytical challenges with silica interference.
- Neal, C. et al. (2012). Lowland river water quality: UK data resource for process and environmental management analysis. Hydrological Processes.