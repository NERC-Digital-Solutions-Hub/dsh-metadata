# Experimental design/Sampling regime

- Objective: investigate the wider environmental impact of sewage effluent by measuring nutrients and related water chemistry; part of a larger study on the environmental dissemination of antimicrobial resistant bacteria and genes.
- Scope: water and sediment samples collected from five rivers receiving sewage effluent.
- Design: three sampling rounds in 2017 to capture seasonal variation (February/March, June/July, October/November).
- Sampling layout: for each site, collect upstream samples at 10 m and 100 m, the effluent at 0 m, and downstream at 10, 100, 250, 500, and 1000 m from the outfall.

## Collection methods

- Sample collection: clean 2 L bottle on a sampling pole; bulk samples subdivided into two 500 mL bottles for suspended solids and chlorophyll, an amber bottle for pH/alkalinity, and 60 mL bottles for total metals and total phosphorus (TP).
- In-field processing: additional subsamples filtered in the field through a 0.45 µm membrane into 60 mL bottles for dissolved metals, nutrients, anions and cations; store all bottles acid-washed.
- Measurements and storage: measure water temperature in the field; keep samples in the dark and return to the laboratory within 6 hours.

## Calibration steps and values and Quality control

- Standards and controls: analyses (except for suspended solids/chlorophyll/alkalinity) run with externally calibrated standards from Wallingford; include Aquacheck quality control standards (unknown concentration) in every batch.
- Validation: Aquacheck values checked with LGC Standards to verify z-scores (aiming for z ≤ 2); Aquacheck scheme accredited to ISO/IEC 17043.
- QC handling: any batch failing internal QC (>10% deviation from assigned value) rerun within 1–2 days; if instrument problems prevented timely analysis, data were omitted.
- Storage after analysis: samples stored in the dark at 4 °C until data verification completed.

## Analytical methods

- TP and TDP: digested unfiltered and 0.45 µm-filtered samples with acidified potassium persulfate in an autoclave (121 °C, 45 min), then react with acidified ammonium molybdate to form a blue complex quantified spectrophotometrically at 880 nm.
- SRP: determined on filtered samples (0.45 µm) using phosphomolybdenum-blue colorimetry (Murphy and Riley, modified by Neal et al., 2000).
- Ammonium: measured by indophenol-blue colorimetric method using a Seal AutoAnalyzer 3.
- DOC and TDN: analyzed with an Elementar Vario Cube.
- Major dissolved anions: fluoride, chloride, nitrite, nitrate and sulfate measured by ion chromatography (Dionex AS50).

## Nature and Units of recorded values

- SampleID: unique sample identifier.
- Date: date in day/month/year.
- Location: name of the closest urban area.
- Latitude/Longitude: geographic coordinates.
- Site_distance: distance from sewage outfall in metres (negative upstream, positive downstream).
- Day/Month/Year: components of sampling date.
- Soluble_reactive_phosphorus: SRP in μg/L.
- Total_dissolved_phosphorus: TDP in μg/L.
- Total_phosphorus: TP in μg/L.
- Dissolved_ammonium: NH4 in mg/L.
- Dissolved_fluoride: F in mg/L.
- Dissolved_chloride: Cl in mg/L.
- Dissolved_nitrite: NO2 in mg/L.
- Dissolved_nitrate: NO3 in mg/L.
- Dissolved_sulphate: SO4 in mg/L.
- Total_dissolved_nitrogen: TDN in mg/L.
- Dissolved_organic_carbon: DOC in mg/L.

## Details of data structure

- Data available as a .csv file with samples as rows.
- Columns include site name, location, sampling date, sample name, and a range of water chemistry parameters.

## References

- Bowes, M. et al. (2018). Weekly water quality monitoring data for the River Thames (UK) and its major tributaries (2009-2013): the Thames Initiative research platform. Earth System Science Data.
- Neal, C. et al. (2000). Phosphate measurement in natural waters: analytical issues with silica interference. Science of the Total Environment.
- Neal, C. et al. (2012). Lowland river water quality: UK data resource for process and environmental management analysis. Hydrological Processes.