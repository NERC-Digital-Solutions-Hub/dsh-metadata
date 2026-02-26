# Experimental Design and Laboratory Incubation Method

- Sediment collection: 0–10 cm depth from Wood Brook, Staffordshire, UK, June 2015; two locations (sandy mid-stream and gravel downstream); five pseudo-replicates per location; samples homogenised, sieved (2 mm), stored cold within 36 hours.
- Treatments and measurements: assays for microbial activity including FDA hydrolysis, extracellular phenol oxidase, and denitrification potential under different substrate conditions; also measured organic matter, moisture, and pH.
- Data product: dataset intended to support understanding of microbial processes and biogeochemistry in stream sediments.

## Data Collected and Variables

- Dataset: MicrobialActivityRates.csv with 11 columns:
  - Sediment_Type
  - Sample_Number
  - Fluorescein (mg fluorescein kg‑1 h‑1)
  - Dopachrome (μmol dopachrome g‑1 h‑1)
  - N2O_control (μg N2O-N g‑1 h‑1)
  - N2O_nitrate (μg N2O-N g‑1 h‑1)
  - N2O_carbon (μg N2O-N g‑1 h‑1)
  - N2O_mixed (μg N2O-N g‑1 h‑1)
  - OM_Content (%)
  - Moisture_Content (%)
  - pH
- Replicates: five pseudo-replicates per location; NAs where sampling was missed.
- Units: specified for each variable as above.

## Methods in Detail

- FDA hydrolysis: 1 g sediment in 125 ml flasks with THAM buffer and FDA substrate; incubated 37 °C for 3 hours; stop with acetone; measure absorbance at 490 nm.
- Extracellular phenol oxidase: 0.5 g dried sediment in 15 ml tubes with water; add L-DOPA; incubate 25 °C for 30 minutes; quantify dopachrome at 475 nm.
- Denitrification potential: 10 g field-moist sediment in serum bottles; incubate under anoxic conditions with specific substrates (water control, NO3, glucose, NO3+glucose); flush headspace with argon/acetylene to inhibit N2O reduction; sampling at 0, 3, 6 hours; replace gas to maintain conditions.
- Organic matter content: loss on ignition at 550 °C for at least 3 hours.
- Moisture content: drying at 105 °C overnight, then weighing.
- pH: sediment-water slurry (5 g sediment with 5 ml deionised water) shaken and equilibrated before pH measurement.

## Instrumentation and Calibration

- N2O analysis: Agilent 7890A GC with micro-electron capture detector; splitless injection, 60 °C oven, 350 °C ECD; 1 ml loop; argon/methane make-up gas; 9 min run; N2O elutes at 7 min.
- Fluorescein and dopachrome: Varian Cary UV-Vis spectrophotometer at 490 nm and 475 nm respectively.
- pH: HQ40d portable pH probe.
- Calibration:
  - GC-ECD: four-point calibration with 0, 2, 4, 6 ppm N2O against external standard; periodic nitrogen blank.
  - pH: standard buffers at pH 4.00 and 7.00.

## Data Structure and Metadata

- File: MicrobialActivityRates.csv with 11 columns as listed above.
- Recorded values include rates of fluorescein and dopachrome production, N2O production under various incubations, organic matter content, moisture, and pH.
- Notes: NAs result from missed sampling during the experiment.

## Data Quality and Governance Considerations

- Ensure complete documentation of sampling locations, replicate identifiers, and incubation conditions to enable reproducibility.
- Maintain consistent units and clear provenance from raw data to the CSV.
- Capture any deviations or anomalies in metadata to support data discovery and interoperability.
- Metadata should include instrument models, calibration dates, and exact reagent concentrations for future reuse.

## References

- Toberman, H., Evans, C. D., Freeman, C., Fenner, N., White, M., Emmett, B. A. and Artz, R. R. E. 2008. Summer drought effects upon soil and litter extracellular phenol oxidase activity and soluble carbon release in an upland Calluna heathland. Soil Biology and Biochemistry. 40, 1519-1532
- Sgouridis, F. and Ullah, S. 2014. Denitrification potential of organic, forest and grassland soils in the Ribble-Wyre and Conwy River catchments, UK. Environmental Science: Processes and Impacts, 16, 1551-1562