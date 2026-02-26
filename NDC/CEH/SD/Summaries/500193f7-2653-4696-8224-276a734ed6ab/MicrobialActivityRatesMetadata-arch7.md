# Experimental Design and Laboratory Incubation Method

## Context and Sampling
- Sediment collected from 0–10 cm depth within the Wood Brook streambed, Staffordshire, UK, in June 2015.
- Two locations: a sandy mid-stream reach and a gravel downstream reach.
- Five pseudo-replicates per location (total of 10 samples).
- Samples homogenised, sieved (2 mm), and stored cold within 36 hours of collection.

## Laboratory Measurements

- Fluorescein diacetate (FDA) hydrolysis
  - 1 g of airdried, homogenised sediment with 50 ml of 1 M THAM buffer and 0.5 ml FDA substrate.
  - Incubated at 37 °C for 3 hours; halted with acetone; absorbance measured at 490 nm.
  - Output: rate of fluorescein production (mg fluorescein kg−1 h−1).

- Extracellular phenol oxidase activity
  - 0.5 g dried sediment in 15 ml tubes with 3 ml deionised water; add 2 ml of 10 mM L-DOPA.
  - 30 min incubation at 25 °C, then centrifugation and filtration; dopachrome measured at 475 nm.
  - Output: phenol oxidase rate (μmol dopachrome g−1 h−1).

- Denitrification potential
  - 10 g field-moist sediment in 100 ml bottles; incubated under dark, anoxic conditions.
  - Substrate treatments: control (water), nitrate-spiked, carbon-spiked, and nitrate+carbon-spiked.
  - Bottles flushed with argon, headspace sampled (0, 3, 6 h); acetylene added to inhibit N2 to N2O conversion.
  - Gas analyses via GC with ECD; outputs as N2O production rates under each treatment (μg N2O-N g−1 h−1).

- Organic matter and moisture
  - Organic matter by loss on ignition at 550 °C; outputs in percent.
  - Moisture content by drying field-moist sediment at 105 °C; outputs in percent.

- pH
  - Sediment slurry (5 g in 5 ml deionised water); pH measured after settling.

## Instrumentation and Calibration

- Nitrous oxide: Agilent 7890A GC with micro-electron capture detector; 1 ml splitless loop; run time ~9 min; N2O elutes at ~7 min.
- Fluorescein and dopachrome: UV-Vis spectrophotometer (490 nm and 475 nm respectively).
- pH: portable pH probe.
- Calibrations:
  - GC-ECD calibrated daily with a four-point N2O standard (0, 2, 4, 6 ppm) plus periodic nitrogen blank.
  - pH probe calibrated with buffers of pH 4.00 and 7.00.

## Data Structure and Quality

- Dataset: single CSV file named MicrobialActivityRates.
- Columns (11 total):
  - Sediment_Type
  - Sample_Number
  - Fluorescein (mg kg−1 h−1)
  - Dopachrome (μmol g−1 h−1)
  - N2O_control (μg N2O-N g−1 h−1)
  - N2O_nitrate (μg N2O-N g−1 h−1)
  - N2O_carbon (μg N2O-N g−1 h−1)
  - N2O_mixed (μg N2O-N g−1 h−1)
  - OM_Content (%)
  - Moisture_Content (%)
  - pH
- Note: NAs result from missed sampling during the experiment.

## GIS-Relevant Considerations and Applications

- Potential map-based visualization of microbial activity indicators across sediment types and treatments (e.g., fluorescein and dopachrome proxy activities; denitrification potential under different substrate conditions).
- Relevant variables for spatial analysis: sediment type, organic matter, moisture, pH, and N2O production rates under various treatments.
- Data limitations for GIS: precise geographic coordinates are not provided; activity data are tied to two reaches and replicated samples, so spatial interpretation should incorporate site-level context and sampling dates.
- To support GIS workflows, ensure clear metadata on sampling locations, depth, and treatment conditions; consider integrating with broader watershed layers (sediment type maps, moisture regimes, pH soils) for visualization and modeling.

## References

- Toberman, H., Evans, C. D., Freeman, C., Fenner, N., White, M., Emmett, B. A. and Artz, R. R. E. 2008. Summer drought effects upon soil and litter extracellular phenol oxidase activity and soluble carbon release in an upland Calluna heathland. Soil Biology and Biochemistry. 40, 1519-1532
- Sgouridis, F. and Ullah, S. 2014. Denitrification potential of organic, forest and grassland soils in the Ribble-Wyre and Conwy River catchments, UK. Environmental Science: Processes and Impacts, 16, 1551-1562